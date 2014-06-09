libname inlib '/strider/osbn/data/tracking/npa'; 
libname outlib '/home/snagan/temp_abhi/converted';

%macro SQUEEZE( DSNIN  /* name of input SAS dataset  */
              , DSNOUT /* name of output SAS dataset */
              ) ;
   /* PURPOSE: create SAS dataset &DSNOUT using LENGTH       */
   /*          statement for numeric vars that optimizes the */
   /*          variable to the fewest # of bytes needed      */
   /*          to maintain the accuracy of the values        */
   /*          contained in the variable                     */
   /*                                                        */
   /*          macro variable SQZLENTH is created which is   */
   /*          then invoked in a subsequent data step        */
   /*                                                        */
   /* NOTE:    only numeric variables are processed          */
   /*                                                        */
   /* EXAMPLE OF USE:                                        */
   /*          %SQUEEZE( DSNIN, DSNOUT )                     */
   %global SQUEEZE ;
   %local I ;
   %put *============================================* ;
   %put | Beginning to SQUEEZE.                      | ;
   %put | Please be patient because this process may | ;
   %put | require a lot of execution time.           | ;
   %put *============================================* ;
   %macro PUTNAME ;
      /* PURPOSE: put variable names into SAS source code */
      %do I = 1 %to &VAR_N ;
         &&VAR&I
      %end ;
   %mend PUTNAME ;
   %macro SQZLENTH ;
      /* PURPOSE: create variable name-variable length pairs */
      %do I = 1 %to &VAR_N ;
         &&VAR&I &&VLEN&I
      %end ;
   %mend SQZLENTH ;
   /***********************************************************/
   /* ensure that DSNIN not same as DSNOUT                    */
   /***********************************************************/
   %if "&DSNIN" = "&DSNOUT"
   %then %do ;
      %put *================================================* ;
      %put | ERROR from SQUEEZE:                            | ;
      %put | Input Dataset has same name as Output Dataset. | ;
      %put | Execution terminating forthwith.               | ;
      %put *================================================* ;
      %goto L9999 ;
   %end ;
   %let VAR_N = 0 ;
   /*##########################################################*/
   /* begin executable code                                    */
   /*##########################################################*/
   proc contents data=&DSNIN memtype=data noprint out=_cntnts_ ; run ;
   data _null_ ;
      set _cntnts_ ;
      if type = 1 ;
      var_no + 1 ;
      /* create macro var containing final # of macro vars */
      call symput( 'VAR_N', left( put( var_no, 4. ) ) ) ;
   run ;
   /* in case there are NO numeric vars in dataset,  */
   /* stop further processing                        */
   %if "&VAR_N" = "0" %then %do ;
      %put *==================================* ;
      %put | ERROR from SQUEEZE:              | ;
      %put | No numeric variables in dataset. | ;
      %put | Execution terminating forthwith. | ;
      %put *==================================* ;
      %goto L9999 ;
   %end ;
   /* put global macro names into environment for later retrieval */
   %do I = 1 %to &VAR_N ;
      %global VAR&I VLEN&I ;
   %end ;
   /* create macro vars containing variable name */
   /* process variables of numeric type only     */
   data _null_ ;
      set _cntnts_ ;
      if type = 1 ;
      var_no + 1 ;
      call symput( 'VAR' || left( put( var_no, 5. )), name ) ;
   run ;
   /* compute min # bytes (3 = min length, for  */
   /* portability over platforms)               */
   data _null_ ;
      set &DSNIN end=lastobs ;
      array _length_ ( &VAR_N ) 3 _temporary_ ;
      if _n_ = 1 then do i = 1 to &VAR_N ; _length_( i ) = 3 ; end ;
      %do I = 1 %to &VAR_N ;
         if &&VAR&I ne .
         then do ;
            if &&VAR&I ne trunc( &&VAR&I, 7 ) then _length_( &I )
            = max( _length_( &I ), 8 ) ; else
            if &&VAR&I ne trunc( &&VAR&I, 6 ) then _length_( &I )
            = max( _length_( &I ), 7 ) ; else
            if &&VAR&I ne trunc( &&VAR&I, 5 ) then _length_( &I )
            = max( _length_( &I ), 6 ) ; else
            if &&VAR&I ne trunc( &&VAR&I, 4 ) then _length_( &I )
            = max( _length_( &I ), 5 ) ; else
            if &&VAR&I ne trunc( &&VAR&I, 3 ) then _length_( &I )
            = max( _length_( &I ), 4 ) ;
         end ;
      %end ;
      if lastobs
      then do ;
         %do I = 1 %to &VAR_N ;
            call symput( "VLEN&I", put( _length_( &I ), 1. )) ;
         %end ;
      end ;
   run ;
   proc datasets nolist ; delete _cntnts_ ; run ;
   /* initialize SQZLENTH global macro var */
   %let SQZLENTH = LENGTH ;
   %do I = 1 %to &VAR_N ;
      %if "&&VLEN&I" ne ""
      %then %let SQZLENTH = &SQZLENTH %qtrim( &&VAR&I ) &&VLEN&I ;
   %end ;
   /* create global SQZLENTH variable containing  */
   /* var name-var length info                    */
   %let SQZLENTH = &SQZLENTH %str( ; ) ;
   /* apply SQZLENTH to incoming data, create output dataset */
   data &DSNOUT ;
      set &DSNIN ;
      &SQZLENTH
   run ;
%L9999:
%mend SQUEEZE ;

%macro convert_dt(ds=);

%SQUEEZE( inlib.&ds, &ds )

data outlib.&ds; 
  set &ds; 
  format BUSNA_ADD_DT BTIMA_BIN_LAST_DM_CNTCT_DT BCSAD_ADD_DT BTIMA_BUS_DT_RECENT_APPEARANCE BUSNA_UPD_DT BDUCC_DATE_LAST_FILING yymmddn8.; 
run;
 
proc datasets lib=work kill memtype=data;
run;
quit;
 
%mend;
 
%convert_dt(ds=osbn_npa_resp_merge_01201452_a); 
%convert_dt(ds=ds2); /* call for 2nd dataset */
%convert_dt(ds=ds3); /* cal for 3rd dataset */
%convert_dt(ds=ds4); /* call for 4th dataset */
%convert_dt(ds=ds5); /* call for 5th dataset */

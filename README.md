BUP
===
libname inlib '/strider/osbn/data/tracking/npa';
libname outlib '/home/snagan/temp_abhi/converted';
 
%macro convert_dt(ds=);
 
data outlib.&ds;
  set inlib.&ds (OBS=1000);
  format BUSNA_ADD_DT BTIMA_BIN_LAST_DM_CNTCT_DT BCSAD_ADD_DT BTIMA_BUS_DT_RECENT_APPEARANCE BUSNA_UPD_DT BDUCC_DATE_LAST_FILING date9.;
 
run;

%mend;
 
%convert_dt(ds=osbn_npa_resp_merge_01201452_a);
%convert_dt(ds=ds2); /* call for 2nd dataset */
%convert_dt(ds=ds3); /* cal for 3rd dataset */
%convert_dt(ds=ds4); /* call for 4th dataset */
%convert_dt(ds=ds5); /* call for 5th dataset */

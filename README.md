libname tmp "/strider/osbn/data/tracking/npa/";

%macro moe_auto_decryptor(ds=);

proc export data=tmp.&ds (obs=0) outfile="/home/snagan/temp_abhi/HEADER/&ds_header.tsv" dbms=tab replace; 
putnames=yes; 
run;
proc export data=tmp.&ds (firstobs=1) outfile="/home/snagan/temp_abhi/DATA/&ds..tsv" dbms=tab replace;
putnames=no;
run;

%mend;

%moe_auto_decryptor(ds=osbn_npa_resp_merge_12201348_a);

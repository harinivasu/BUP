BUP
===
libname tmp "/home/snagan/temp_abhi";
proc export data=tmp.osbn_npa_resp_merge_09201036_c (firstobs=1) outfile="data.tsv" dbms=tab replace;
putnames=no;
run;

/strider/osbn/data/tracking/npa/osbn_npa_resp_merge_12201348_a.sas7bdat 
/strider/osbn/data/tracking/npa/osbn_npa_resp_merge_12201344_a.sas7bdat
/strider/osbn/data/tracking/npa/osbn_npa_resp_merge_11201340_a.sas7bdat
/strider/osbn/data/tracking/npa/osbn_npa_resp_merge_10201336_a.sas7bdat
/strider/osbn/data/tracking/npa/osbn_npa_resp_merge_09201332_a.sas7bdat
/strider/osbn/data/tracking/npa/osbn_npa_resp_merge_08201328_a.sas7bdat
/strider/osbn/data/tracking/npa/osbn_npa_resp_merge_07201324_a.sas7bdat

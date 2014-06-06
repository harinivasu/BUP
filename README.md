libname inlib '/strider/osbn/data/tracking/npa';
libname outlib '/home/snagan/temp_abhi/converted';
data outlib.osbn_npa_resp_merge_01201452_a;
        set inlib.osbn_npa_resp_merge_01201452_a (OBS=1000);
        format BUSNA_ADD_DT BTIMA_BIN_LAST_DM_CNTCT_DT BCSAD_ADD_DT BTIMA_BUS_DT_RECENT_APPEARANCE BUSNA_UPD_DT BDUCC_DATE_LAST_FILING date9.;
run;

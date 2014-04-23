NOTE: Copyright (c) 2002-2010 by SAS Institute Inc., Cary, NC, USA.
NOTE: SAS (r) Proprietary Software 9.3 (TS1M1)
      Licensed to AMERICAN EXPRESS COMPANY, Site 70003184.
NOTE: This session is executing on the W32_7PRO  platform.



NOTE: Updated analytical products:

SAS/STAT 9.3_M1, SAS/ETS 9.3_M1, SAS/OR 9.3_M1

NOTE: SAS initialization used:
      real time           4.84 seconds
      cpu time            1.07 seconds

1    proc import datafile="C:\Share\sample.tsv" out=mydata dbms=tab replace;
2       getnames=yes;
3    run;

4     /**********************************************************************
5     *   PRODUCT:   SAS
6     *   VERSION:   9.3
7     *   CREATOR:   External File Interface
8     *   DATE:      23APR14
9     *   DESC:      Generated SAS Datastep Code
10    *   TEMPLATE SOURCE:  (None Specified.)
11    ***********************************************************************/
12       data WORK.MYDATA    ;
13       %let _EFIERR_ = 0; /* set the ERROR detection macro variable */
14       infile 'C:\Share\sample.tsv' delimiter='09'x MISSOVER DSD lrecl=32767 firstobs=2 ;
15          informat pin best32. ;
16          informat bin best32. ;
17          informat as_of_dt best32. ;
18          informat mail_drop_dt $4. ;
19          informat mail_ship_dt best32. ;
20          informat mail_date best32. ;
21          informat poid $9. ;
22          informat spid $3. ;
23          informat primary_source_code $10. ;
24          informat campaign_code $4. ;
25          informat cell_id $4. ;
26          informat cell_title $73. ;
27          informat offer_title $74. ;
28          informat bus_unit $2. ;
29          informat offer_type $2. ;
30          informat channel $2. ;
31          informat camp_type $1. ;
32          informat ia_code $3. ;
33          informat ia_description $30. ;
34          informat prod_group $17. ;
35          informat card_group $7. ;
36          informat emerg_premium $8. ;
37          informat model_validation best32. ;
38          informat first_year_free $3. ;
39          informat acquisition_pts best32. ;
40          informat acquisition_stmt_credit best32. ;
41          informat spend_threshold best32. ;
42          informat threshold_duration best32. ;
43          informat secondary_fpb_pts $1. ;
44          informat secondary_fpb_stmt_credit best32. ;
45          informat secondary_threshold_duration best32. ;
46          informat intro_apr $4. ;
47          informat bt_apr best32. ;
48          informat goto_apr best32. ;
49          informat step $1. ;
50          informat cell_waveid $10. ;
51          informat appdata $1. ;
52          format pin best12. ;
53          format bin best12. ;
54          format as_of_dt best12. ;
55          format mail_drop_dt $4. ;
56          format mail_ship_dt best12. ;
57          format mail_date best12. ;
58          format poid $9. ;
59          format spid $3. ;
60          format primary_source_code $10. ;
61          format campaign_code $4. ;
62          format cell_id $4. ;
63          format cell_title $73. ;
64          format offer_title $74. ;
65          format bus_unit $2. ;
66          format offer_type $2. ;
67          format channel $2. ;
68          format camp_type $1. ;
69          format ia_code $3. ;
70          format ia_description $30. ;
71          format prod_group $17. ;
72          format card_group $7. ;
73          format emerg_premium $8. ;
74          format model_validation best12. ;
75          format first_year_free $3. ;
76          format acquisition_pts best12. ;
77          format acquisition_stmt_credit best12. ;
78          format spend_threshold best12. ;
79          format threshold_duration best12. ;
80          format secondary_fpb_pts $1. ;
81          format secondary_fpb_stmt_credit best12. ;
82          format secondary_threshold_duration best12. ;
83          format intro_apr $4. ;
84          format bt_apr best12. ;
85          format goto_apr best12. ;
86          format step $1. ;
87          format cell_waveid $10. ;
88          format appdata $1. ;
89       input
90                   pin
91                   bin
92                   as_of_dt
93                   mail_drop_dt $
94                   mail_ship_dt
95                   mail_date
96                   poid $
97                   spid $
98                   primary_source_code $
99                   campaign_code $
100                  cell_id $
101                  cell_title $
102                  offer_title $
103                  bus_unit $
104                  offer_type $
105                  channel $
106                  camp_type $
107                  ia_code $
108                  ia_description $
109                  prod_group $
110                  card_group $
111                  emerg_premium $
112                  model_validation
113                  first_year_free $
114                  acquisition_pts
115                  acquisition_stmt_credit
116                  spend_threshold
117                  threshold_duration
118                  secondary_fpb_pts $
119                  secondary_fpb_stmt_credit
120                  secondary_threshold_duration
121                  intro_apr $
122                  bt_apr
123                  goto_apr
124                  step $
125                  cell_waveid $
126                  appdata $
127      ;
128      if _ERROR_ then call symputx('_EFIERR_',1);  /* set ERROR detection macro variable */
129      run;

NOTE: The infile 'C:\Share\sample.tsv' is:
      Filename=C:\Share\sample.tsv,
      RECFM=V,LRECL=32767,File Size (bytes)=28342,
      Last Modified=23Apr2014:15:27:59,
      Create Time=23Apr2014:15:29:02

NOTE: Invalid data for model_validation in line 26 275-276.
RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

26  CHAR  100001856.0.201303.NULL.02192013.20130301.AI80:0001.L7Z.A00000EF5W.AI80.G825.CHALLENGE
    ZONE  33333333303033333304544033333333033333333044333333304350433333443504433043330444444444
    NUMR  1000018569092013039E5CC90219201392013030191980A00019C7A9100000565791980978259381CC5E75

      87  R: MV EMERG GOLD FYF 25K/$1000/3M GIFTCARD REFRESHED PKG.AI80:0001/AMERICAN EXPRESS GO
    ZONE  53245244454244442454233422333323424445445425445454442544044333333324445444424555455244
    NUMR  2A0D605D52707FC40696025BF41000F3D079643124025625385400B791980A0001F1D52931E0580253307F



RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     173  LD/FYF/25000/$1000/3 MONTHS.CS.PS.DM.C.F2D.GOLD: PREFERRED REWARDS GOLD.CHARGE - GOLD.
    ZONE  44245423333322333323244454504505504404043404444325544455442545454524444044454422244440
    NUMR  C4F696F25000F41000F30DFE48393390394D93962497FC4A00256522540257124307FC493812750D07FC49

     259  CHARGE.EMERGING.MV.FYF.25000..1000.3....0.0.0..G825032013. 316
    ZONE  4445440444544440450454033333003333030000303030043333333330
    NUMR  38127595D5279E79D69696925000991000939999090909978250320139
pin=100001856 bin=0 as_of_dt=201303 mail_drop_dt=NULL mail_ship_dt=2192013 mail_date=20130301
poid=AI80:0001 spid=L7Z primary_source_code=A00000EF5W campaign_code=AI80 cell_id=G825
cell_title=CHALLENGER: MV EMERG GOLD FYF 25K/$1000/3M GIFTCARD REFRESHED PKG
offer_title=AI80:0001/AMERICAN EXPRESS GOLD/FYF/25000/$1000/3 MONTHS bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=F2D ia_description=GOLD: PREFERRED REWARDS GOLD
prod_group=CHARGE - GOLD card_group=CHARGE emerg_premium=EMERGING model_validation=.
first_year_free=FYF acquisition_pts=25000 acquisition_stmt_credit=. spend_threshold=1000
threshold_duration=3 secondary_fpb_pts=  secondary_fpb_stmt_credit=.
secondary_threshold_duration=. intro_apr=0 bt_apr=0 goto_apr=0 step=  cell_waveid=G825032013
appdata=  _ERROR_=1 _N_=25
NOTE: Invalid data for model_validation in line 38 250-251.

38  CHAR  100001980.0.201311.NULL.10212013.20131101.AS8J:0002.L7Z.A00000ETK3.AS8J.D463.MV EMERG
    ZONE  33333333303033333304544033333333033333333045343333304350433333454304534043330452444542
    NUMR  1000019809092013119E5CC9102120139201311019138AA00029C7A910000054B39138A944639D605D5270

      87  CTRL: DELTA GOLD FYF 35K/$1000/3MOS +$50SC/FPB/DELTA."AS8J:0002/DELTA GOLD/FYF/35,000/
    ZONE  45543244454244442454233422333323445222335424542444540245343333324445424444245423323332
    NUMR  342CA045C4107FC40696035BF41000F3DF30B45033F602F45C4192138AA0002F45C4107FC4F696F35C000F

     173  $1000/3MOS+$50SC/FPB".CS.PS.DM.C.NX6.DELTA GOLD: 9.99% BT.DELTA.SAC.EMERGING.MV.FYF.35
    ZONE  23333234452233542454204505504404045304445424444323233224504445405440444544440450454033
    NUMR  41000F3DF3B45033F602293390394D939E86945C4107FC4A09E995024945C41931395D5279E79D69696935

     259  000..1000.3..50..0.0.15.24..D463112013. 297
    ZONE  333003333030033003030332330043333333330
    NUMR  00099100093995099090915E249944631120139
pin=100001980 bin=0 as_of_dt=201311 mail_drop_dt=NULL mail_ship_dt=10212013 mail_date=20131101
poid=AS8J:0002 spid=L7Z primary_source_code=A00000ETK3 campaign_code=AS8J cell_id=D463
cell_title=MV EMERG CTRL: DELTA GOLD FYF 35K/$1000/3MOS +$50SC/FPB/DELTA
offer_title=AS8J:0002/DELTA GOLD/FYF/35,000/$1000/3MOS+$50SC/FPB bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=NX6 ia_description=DELTA GOLD: 9.99% BT prod_group=DELTA
card_group=SAC emerg_premium=EMERGING model_validation=. first_year_free=FYF
acquisition_pts=35000 acquisition_stmt_credit=. spend_threshold=1000 threshold_duration=3
secondary_fpb_pts=  secondary_fpb_stmt_credit=50 secondary_threshold_duration=. intro_apr=0
bt_apr=0 goto_apr=15.24 step=  cell_waveid=D463112013 appdata=  _ERROR_=1 _N_=37
NOTE: Invalid data for model_validation in line 52 272-273.

52  CHAR  10002057.0.201208.NULL.07202012.20120801.AD4B:0001.L7Z.A00000E64W.AD4B.S660.MV PREM BS
    ZONE  33333333030333333045440333333330333333330443433333043504333334335044340533304525544245
    NUMR  100020579092012089E5CC90720201292012080191442A00019C7A9100000564791442936609D60025D023

      87  KY - 30K/$500/3M - PASSPORT PKG (FF UPSELL).BLUE SKY - 0F15/P+13.99/P+13.99 - UPSELL T
    ZONE  45222334223332342225455545525442244255544420445425452223433252332332523323322255544425
    NUMR  B90D030BF4500F3D0D001330F2400B7086605035CC992C5503B90D00615F0B13E99F0B13E990D05035CC04

RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     173  O BLUE SKY PREF 0F15/P+13.99.CS.PS.DM.C.MWS.BLUE SKY: 4.99 LOB BT WITH FEE.BLUESKY.LEN
    ZONE  42445425452554423433252332330450550440404550445425453232332444245254542444044545450444
    NUMR  F02C5503B90025600615F0B13E9993390394D939D7392C5503B9A04E990CF202407948065592C553B99C5E

     259  DING.PREMIUM.MV.FYF.30000..500.3....0F15.0.17.24..S660082012. 319
    ZONE  4444055444540450454033333003330300003433030332330053333333330
    NUMR  49E79025D95D9D6969693000099500939999061590917E249936600820129
pin=10002057 bin=0 as_of_dt=201208 mail_drop_dt=NULL mail_ship_dt=7202012 mail_date=20120801
poid=AD4B:0001 spid=L7Z primary_source_code=A00000E64W campaign_code=AD4B cell_id=S660
cell_title=MV PREM BSKY - 30K/$500/3M - PASSPORT PKG (FF UPSELL)
offer_title=BLUE SKY - 0F15/P+13.99/P+13.99 - UPSELL TO BLUE SKY PREF 0F15/P+13.99 bus_unit=CS
offer_type=PS channel=DM camp_type=C ia_code=MWS ia_description=BLUE SKY: 4.99 LOB BT WITH FEE
prod_group=BLUESKY card_group=LENDING emerg_premium=PREMIUM model_validation=.
first_year_free=FYF acquisition_pts=30000 acquisition_stmt_credit=. spend_threshold=500
threshold_duration=3 secondary_fpb_pts=  secondary_fpb_stmt_credit=.
secondary_threshold_duration=. intro_apr=0F15 bt_apr=0 goto_apr=17.24 step=
cell_waveid=S660082012 appdata=  _ERROR_=1 _N_=51
NOTE: Invalid data for model_validation in line 71 163-164.

71  CHAR  10002057.0.201301.NULL.12102012.20130102.AGYX:0001.L7Z.A00000ED1G.AGYX.K605.MV CTRL CO
    ZONE  33333333030333333045440333333330333333330445533333043504333334434044550433304524554244
    NUMR  100020579092013019E5CC91210201292013010291798A00019C7A91000005417917989B6059D60342C03F

      87  STCO NO FEE EXEC PKG.AGYX:0001:COSTCO:FYF.CS.PS.DM.C.JVB.COSTCO.COSTCO.SAC..MV.FYF....
    ZONE  55442442444245442544044553333334455443454045055044040454044554404455440544004504540000
    NUMR  343F0EF06550585300B791798A0001A3F343FA69693390394D939A6293F343F93F343F931399D696969999

     173  ....0F6.0.15.24..K605012013. 200
    ZONE  0000343030332330043333333330
    NUMR  999906690915E2499B6050120139
pin=10002057 bin=0 as_of_dt=201301 mail_drop_dt=NULL mail_ship_dt=12102012 mail_date=20130102
poid=AGYX:0001 spid=L7Z primary_source_code=A00000ED1G campaign_code=AGYX cell_id=K605
cell_title=MV CTRL COSTCO NO FEE EXEC PKG offer_title=AGYX:0001:COSTCO:FYF bus_unit=CS
offer_type=PS channel=DM camp_type=C ia_code=JVB ia_description=COSTCO prod_group=COSTCO
card_group=SAC emerg_premium=  model_validation=. first_year_free=FYF acquisition_pts=.
acquisition_stmt_credit=. spend_threshold=. threshold_duration=. secondary_fpb_pts=
secondary_fpb_stmt_credit=. secondary_threshold_duration=. intro_apr=0F6 bt_apr=0 goto_apr=15.24
step=  cell_waveid=K605012013 appdata=  _ERROR_=1 _N_=70
NOTE: Invalid data for model_validation in line 80 235-236.

80  CHAR  100044280.0.201311.NULL.10212013.20131101.ASHC:0001.L7Z.A00000ETME.ASHC.U977.EMERGING
    ZONE  33333333303033333304544033333333033333333045443333304350433333454404544053330444544442
    NUMR  1000442809092013119E5CC91021201392013110191383A00019C7A910000054D5913839597795D5279E70

      87  MV BCE 150/500/3M SHORT FLAP INLINE.ASHC:0001/BLUE CASH EVERYDAY/FYF/$150 SC/$500/3MOS
    ZONE  45244423332333234254455244452444444045443333324454244542454554452454223332542233323445
    NUMR  D602350150F500F3D038F2406C1009EC9E591383A0001F2C5503138056529419F696F4150033F4500F3DF3

     173  ..CS.PS.DM.C.LPQ.BLUECASH EVERYDAY.BLUE CASH.LENDING.EMERGING.MV.FYF..150.500.3....0F1
    ZONE  20450550440404550445444542454554450445424454044444440444544440450454003330333030000343
    NUMR  E93390394D939C0192C55313805652941992C55031389C5E49E795D5279E79D69696991509500939999061


RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     259  5.0.12.99..U977112013. 280
    ZONE  3030332330053333333330
    NUMR  590912E999959771120139
pin=100044280 bin=0 as_of_dt=201311 mail_drop_dt=NULL mail_ship_dt=10212013 mail_date=20131101
poid=ASHC:0001 spid=L7Z primary_source_code=A00000ETME campaign_code=ASHC cell_id=U977
cell_title=EMERGING MV BCE 150/500/3M SHORT FLAP INLINE
offer_title=ASHC:0001/BLUE CASH EVERYDAY/FYF/$150 SC/$500/3MOS. bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=LPQ ia_description=BLUECASH EVERYDAY prod_group=BLUE CASH
card_group=LENDING emerg_premium=EMERGING model_validation=. first_year_free=FYF
acquisition_pts=. acquisition_stmt_credit=150 spend_threshold=500 threshold_duration=3
secondary_fpb_pts=  secondary_fpb_stmt_credit=. secondary_threshold_duration=. intro_apr=0F15
bt_apr=0 goto_apr=12.99 step=  cell_waveid=U977112013 appdata=  _ERROR_=1 _N_=79
NOTE: 100 records were read from the infile 'C:\Share\sample.tsv'.
      The minimum record length was 200.
      The maximum record length was 337.
NOTE: The data set WORK.MYDATA has 100 observations and 37 variables.
NOTE: DATA statement used (Total process time):
      real time           0.28 seconds
      cpu time            0.10 seconds


Errors detected in submitted DATA step. Examine log.
100 rows created in WORK.MYDATA from C:\Share\sample.tsv.



ERROR: Import unsuccessful.  See SAS Log for details.
NOTE: The SAS System stopped processing this step because of errors.
NOTE: PROCEDURE IMPORT used (Total process time):
      real time           1.55 seconds
      cpu time            0.29 seconds



130  libname outlib "C:\Share\";
NOTE: Libref OUTLIB was successfully assigned as follows:
      Engine:        V9
      Physical Name: C:\Share
131
132  FileName in_file "C:\Share\sample.tsv";
133
134  proc import datafile=in_file out=outlib.outsas
135  dbms=dlm
136  replace;
137  delimiter = '09'x;
138  run;

139   /**********************************************************************
140   *   PRODUCT:   SAS
141   *   VERSION:   9.3
142   *   CREATOR:   External File Interface
143   *   DATE:      23APR14
144   *   DESC:      Generated SAS Datastep Code
145   *   TEMPLATE SOURCE:  (None Specified.)
146   ***********************************************************************/
147      data OUTLIB.OUTSAS    ;
148      %let _EFIERR_ = 0; /* set the ERROR detection macro variable */
149      infile IN_FILE delimiter='09'x MISSOVER DSD lrecl=32767 firstobs=2 ;
150         informat pin best32. ;
151         informat bin best32. ;
152         informat as_of_dt best32. ;
153         informat mail_drop_dt $4. ;
154         informat mail_ship_dt best32. ;
155         informat mail_date best32. ;
156         informat poid $9. ;
157         informat spid $3. ;
158         informat primary_source_code $10. ;
159         informat campaign_code $4. ;
160         informat cell_id $4. ;
161         informat cell_title $73. ;
162         informat offer_title $74. ;
163         informat bus_unit $2. ;
164         informat offer_type $2. ;
165         informat channel $2. ;
166         informat camp_type $1. ;
167         informat ia_code $3. ;
168         informat ia_description $30. ;
169         informat prod_group $17. ;
170         informat card_group $7. ;
171         informat emerg_premium $8. ;
172         informat model_validation best32. ;
173         informat first_year_free $3. ;
174         informat acquisition_pts best32. ;
175         informat acquisition_stmt_credit best32. ;
176         informat spend_threshold best32. ;
177         informat threshold_duration best32. ;
178         informat secondary_fpb_pts $1. ;
179         informat secondary_fpb_stmt_credit best32. ;
180         informat secondary_threshold_duration best32. ;
181         informat intro_apr $4. ;
182         informat bt_apr best32. ;
183         informat goto_apr best32. ;
184         informat step $1. ;
185         informat cell_waveid $10. ;
186         informat appdata $1. ;
187         format pin best12. ;
188         format bin best12. ;
189         format as_of_dt best12. ;
190         format mail_drop_dt $4. ;
191         format mail_ship_dt best12. ;
192         format mail_date best12. ;
193         format poid $9. ;
194         format spid $3. ;
195         format primary_source_code $10. ;
196         format campaign_code $4. ;
197         format cell_id $4. ;
198         format cell_title $73. ;
199         format offer_title $74. ;
200         format bus_unit $2. ;
201         format offer_type $2. ;
202         format channel $2. ;
203         format camp_type $1. ;
204         format ia_code $3. ;
205         format ia_description $30. ;
206         format prod_group $17. ;
207         format card_group $7. ;
208         format emerg_premium $8. ;
209         format model_validation best12. ;
210         format first_year_free $3. ;
211         format acquisition_pts best12. ;
212         format acquisition_stmt_credit best12. ;
213         format spend_threshold best12. ;
214         format threshold_duration best12. ;
215         format secondary_fpb_pts $1. ;
216         format secondary_fpb_stmt_credit best12. ;
217         format secondary_threshold_duration best12. ;
218         format intro_apr $4. ;
219         format bt_apr best12. ;
220         format goto_apr best12. ;
221         format step $1. ;
222         format cell_waveid $10. ;
223         format appdata $1. ;
224      input
225                  pin
226                  bin
227                  as_of_dt
228                  mail_drop_dt $
229                  mail_ship_dt
230                  mail_date
231                  poid $
232                  spid $
233                  primary_source_code $
234                  campaign_code $
235                  cell_id $
236                  cell_title $
237                  offer_title $
238                  bus_unit $
239                  offer_type $
240                  channel $
241                  camp_type $
242                  ia_code $
243                  ia_description $
244                  prod_group $
245                  card_group $
246                  emerg_premium $
247                  model_validation
248                  first_year_free $
249                  acquisition_pts
250                  acquisition_stmt_credit
251                  spend_threshold
252                  threshold_duration
253                  secondary_fpb_pts $
254                  secondary_fpb_stmt_credit
255                  secondary_threshold_duration
256                  intro_apr $
257                  bt_apr
258                  goto_apr
259                  step $
260                  cell_waveid $
261                  appdata $
262      ;
263      if _ERROR_ then call symputx('_EFIERR_',1);  /* set ERROR detection macro variable */
264      run;

NOTE: The infile IN_FILE is:
      Filename=C:\Share\sample.tsv,
      RECFM=V,LRECL=32767,File Size (bytes)=28342,
      Last Modified=23Apr2014:15:27:59,
      Create Time=23Apr2014:15:29:02

NOTE: Invalid data for model_validation in line 26 275-276.
RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

26  CHAR  100001856.0.201303.NULL.02192013.20130301.AI80:0001.L7Z.A00000EF5W.AI80.G825.CHALLENGE
    ZONE  33333333303033333304544033333333033333333044333333304350433333443504433043330444444444
    NUMR  1000018569092013039E5CC90219201392013030191980A00019C7A9100000565791980978259381CC5E75

      87  R: MV EMERG GOLD FYF 25K/$1000/3M GIFTCARD REFRESHED PKG.AI80:0001/AMERICAN EXPRESS GO
    ZONE  53245244454244442454233422333323424445445425445454442544044333333324445444424555455244
    NUMR  2A0D605D52707FC40696025BF41000F3D079643124025625385400B791980A0001F1D52931E0580253307F

     173  LD/FYF/25000/$1000/3 MONTHS.CS.PS.DM.C.F2D.GOLD: PREFERRED REWARDS GOLD.CHARGE - GOLD.
    ZONE  44245423333322333323244454504505504404043404444325544455442545454524444044454422244440
    NUMR  C4F696F25000F41000F30DFE48393390394D93962497FC4A00256522540257124307FC493812750D07FC49

     259  CHARGE.EMERGING.MV.FYF.25000..1000.3....0.0.0..G825032013. 316
    ZONE  4445440444544440450454033333003333030000303030043333333330
    NUMR  38127595D5279E79D69696925000991000939999090909978250320139
pin=100001856 bin=0 as_of_dt=201303 mail_drop_dt=NULL mail_ship_dt=2192013 mail_date=20130301
poid=AI80:0001 spid=L7Z primary_source_code=A00000EF5W campaign_code=AI80 cell_id=G825
cell_title=CHALLENGER: MV EMERG GOLD FYF 25K/$1000/3M GIFTCARD REFRESHED PKG
offer_title=AI80:0001/AMERICAN EXPRESS GOLD/FYF/25000/$1000/3 MONTHS bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=F2D ia_description=GOLD: PREFERRED REWARDS GOLD
prod_group=CHARGE - GOLD card_group=CHARGE emerg_premium=EMERGING model_validation=.
first_year_free=FYF acquisition_pts=25000 acquisition_stmt_credit=. spend_threshold=1000
threshold_duration=3 secondary_fpb_pts=  secondary_fpb_stmt_credit=.
secondary_threshold_duration=. intro_apr=0 bt_apr=0 goto_apr=0 step=  cell_waveid=G825032013
appdata=  _ERROR_=1 _N_=25
NOTE: Invalid data for model_validation in line 38 250-251.

38  CHAR  100001980.0.201311.NULL.10212013.20131101.AS8J:0002.L7Z.A00000ETK3.AS8J.D463.MV EMERG
    ZONE  33333333303033333304544033333333033333333045343333304350433333454304534043330452444542
    NUMR  1000019809092013119E5CC9102120139201311019138AA00029C7A910000054B39138A944639D605D5270

      87  CTRL: DELTA GOLD FYF 35K/$1000/3MOS +$50SC/FPB/DELTA."AS8J:0002/DELTA GOLD/FYF/35,000/
    ZONE  45543244454244442454233422333323445222335424542444540245343333324445424444245423323332
    NUMR  342CA045C4107FC40696035BF41000F3DF30B45033F602F45C4192138AA0002F45C4107FC4F696F35C000F

RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     173  $1000/3MOS+$50SC/FPB".CS.PS.DM.C.NX6.DELTA GOLD: 9.99% BT.DELTA.SAC.EMERGING.MV.FYF.35
    ZONE  23333234452233542454204505504404045304445424444323233224504445405440444544440450454033
    NUMR  41000F3DF3B45033F602293390394D939E86945C4107FC4A09E995024945C41931395D5279E79D69696935

     259  000..1000.3..50..0.0.15.24..D463112013. 297
    ZONE  333003333030033003030332330043333333330
    NUMR  00099100093995099090915E249944631120139
pin=100001980 bin=0 as_of_dt=201311 mail_drop_dt=NULL mail_ship_dt=10212013 mail_date=20131101
poid=AS8J:0002 spid=L7Z primary_source_code=A00000ETK3 campaign_code=AS8J cell_id=D463
cell_title=MV EMERG CTRL: DELTA GOLD FYF 35K/$1000/3MOS +$50SC/FPB/DELTA
offer_title=AS8J:0002/DELTA GOLD/FYF/35,000/$1000/3MOS+$50SC/FPB bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=NX6 ia_description=DELTA GOLD: 9.99% BT prod_group=DELTA
card_group=SAC emerg_premium=EMERGING model_validation=. first_year_free=FYF
acquisition_pts=35000 acquisition_stmt_credit=. spend_threshold=1000 threshold_duration=3
secondary_fpb_pts=  secondary_fpb_stmt_credit=50 secondary_threshold_duration=. intro_apr=0
bt_apr=0 goto_apr=15.24 step=  cell_waveid=D463112013 appdata=  _ERROR_=1 _N_=37
NOTE: Invalid data for model_validation in line 52 272-273.

52  CHAR  10002057.0.201208.NULL.07202012.20120801.AD4B:0001.L7Z.A00000E64W.AD4B.S660.MV PREM BS
    ZONE  33333333030333333045440333333330333333330443433333043504333334335044340533304525544245
    NUMR  100020579092012089E5CC90720201292012080191442A00019C7A9100000564791442936609D60025D023

      87  KY - 30K/$500/3M - PASSPORT PKG (FF UPSELL).BLUE SKY - 0F15/P+13.99/P+13.99 - UPSELL T
    ZONE  45222334223332342225455545525442244255544420445425452223433252332332523323322255544425
    NUMR  B90D030BF4500F3D0D001330F2400B7086605035CC992C5503B90D00615F0B13E99F0B13E990D05035CC04

     173  O BLUE SKY PREF 0F15/P+13.99.CS.PS.DM.C.MWS.BLUE SKY: 4.99 LOB BT WITH FEE.BLUESKY.LEN
    ZONE  42445425452554423433252332330450550440404550445425453232332444245254542444044545450444
    NUMR  F02C5503B90025600615F0B13E9993390394D939D7392C5503B9A04E990CF202407948065592C553B99C5E

     259  DING.PREMIUM.MV.FYF.30000..500.3....0F15.0.17.24..S660082012. 319
    ZONE  4444055444540450454033333003330300003433030332330053333333330
    NUMR  49E79025D95D9D6969693000099500939999061590917E249936600820129
pin=10002057 bin=0 as_of_dt=201208 mail_drop_dt=NULL mail_ship_dt=7202012 mail_date=20120801
poid=AD4B:0001 spid=L7Z primary_source_code=A00000E64W campaign_code=AD4B cell_id=S660
cell_title=MV PREM BSKY - 30K/$500/3M - PASSPORT PKG (FF UPSELL)
offer_title=BLUE SKY - 0F15/P+13.99/P+13.99 - UPSELL TO BLUE SKY PREF 0F15/P+13.99 bus_unit=CS
offer_type=PS channel=DM camp_type=C ia_code=MWS ia_description=BLUE SKY: 4.99 LOB BT WITH FEE
prod_group=BLUESKY card_group=LENDING emerg_premium=PREMIUM model_validation=.
first_year_free=FYF acquisition_pts=30000 acquisition_stmt_credit=. spend_threshold=500
threshold_duration=3 secondary_fpb_pts=  secondary_fpb_stmt_credit=.
secondary_threshold_duration=. intro_apr=0F15 bt_apr=0 goto_apr=17.24 step=
cell_waveid=S660082012 appdata=  _ERROR_=1 _N_=51
NOTE: Invalid data for model_validation in line 71 163-164.

71  CHAR  10002057.0.201301.NULL.12102012.20130102.AGYX:0001.L7Z.A00000ED1G.AGYX.K605.MV CTRL CO
    ZONE  33333333030333333045440333333330333333330445533333043504333334434044550433304524554244
    NUMR  100020579092013019E5CC91210201292013010291798A00019C7A91000005417917989B6059D60342C03F

      87  STCO NO FEE EXEC PKG.AGYX:0001:COSTCO:FYF.CS.PS.DM.C.JVB.COSTCO.COSTCO.SAC..MV.FYF....
    ZONE  55442442444245442544044553333334455443454045055044040454044554404455440544004504540000
    NUMR  343F0EF06550585300B791798A0001A3F343FA69693390394D939A6293F343F93F343F931399D696969999

RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     173  ....0F6.0.15.24..K605012013. 200
    ZONE  0000343030332330043333333330
    NUMR  999906690915E2499B6050120139
pin=10002057 bin=0 as_of_dt=201301 mail_drop_dt=NULL mail_ship_dt=12102012 mail_date=20130102
poid=AGYX:0001 spid=L7Z primary_source_code=A00000ED1G campaign_code=AGYX cell_id=K605
cell_title=MV CTRL COSTCO NO FEE EXEC PKG offer_title=AGYX:0001:COSTCO:FYF bus_unit=CS
offer_type=PS channel=DM camp_type=C ia_code=JVB ia_description=COSTCO prod_group=COSTCO
card_group=SAC emerg_premium=  model_validation=. first_year_free=FYF acquisition_pts=.
acquisition_stmt_credit=. spend_threshold=. threshold_duration=. secondary_fpb_pts=
secondary_fpb_stmt_credit=. secondary_threshold_duration=. intro_apr=0F6 bt_apr=0 goto_apr=15.24
step=  cell_waveid=K605012013 appdata=  _ERROR_=1 _N_=70
NOTE: Invalid data for model_validation in line 80 235-236.

80  CHAR  100044280.0.201311.NULL.10212013.20131101.ASHC:0001.L7Z.A00000ETME.ASHC.U977.EMERGING
    ZONE  33333333303033333304544033333333033333333045443333304350433333454404544053330444544442
    NUMR  1000442809092013119E5CC91021201392013110191383A00019C7A910000054D5913839597795D5279E70

      87  MV BCE 150/500/3M SHORT FLAP INLINE.ASHC:0001/BLUE CASH EVERYDAY/FYF/$150 SC/$500/3MOS
    ZONE  45244423332333234254455244452444444045443333324454244542454554452454223332542233323445
    NUMR  D602350150F500F3D038F2406C1009EC9E591383A0001F2C5503138056529419F696F4150033F4500F3DF3

     173  ..CS.PS.DM.C.LPQ.BLUECASH EVERYDAY.BLUE CASH.LENDING.EMERGING.MV.FYF..150.500.3....0F1
    ZONE  20450550440404550445444542454554450445424454044444440444544440450454003330333030000343
    NUMR  E93390394D939C0192C55313805652941992C55031389C5E49E795D5279E79D69696991509500939999061

     259  5.0.12.99..U977112013. 280
    ZONE  3030332330053333333330
    NUMR  590912E999959771120139
pin=100044280 bin=0 as_of_dt=201311 mail_drop_dt=NULL mail_ship_dt=10212013 mail_date=20131101
poid=ASHC:0001 spid=L7Z primary_source_code=A00000ETME campaign_code=ASHC cell_id=U977
cell_title=EMERGING MV BCE 150/500/3M SHORT FLAP INLINE
offer_title=ASHC:0001/BLUE CASH EVERYDAY/FYF/$150 SC/$500/3MOS. bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=LPQ ia_description=BLUECASH EVERYDAY prod_group=BLUE CASH
card_group=LENDING emerg_premium=EMERGING model_validation=. first_year_free=FYF
acquisition_pts=. acquisition_stmt_credit=150 spend_threshold=500 threshold_duration=3
secondary_fpb_pts=  secondary_fpb_stmt_credit=. secondary_threshold_duration=. intro_apr=0F15
bt_apr=0 goto_apr=12.99 step=  cell_waveid=U977112013 appdata=  _ERROR_=1 _N_=79
NOTE: 100 records were read from the infile IN_FILE.
      The minimum record length was 200.
      The maximum record length was 337.
NOTE: The data set OUTLIB.OUTSAS has 100 observations and 37 variables.
NOTE: DATA statement used (Total process time):
      real time           0.06 seconds
      cpu time            0.06 seconds


Errors detected in submitted DATA step. Examine log.
100 rows created in OUTLIB.OUTSAS from IN_FILE.



ERROR: Import unsuccessful.  See SAS Log for details.
NOTE: The SAS System stopped processing this step because of errors.
NOTE: PROCEDURE IMPORT used (Total process time):
      real time           0.20 seconds
      cpu time            0.14 seconds



265  libname outlib "C:\Share\";
NOTE: Libref OUTLIB was successfully assigned as follows:
      Engine:        V9
      Physical Name: C:\Share
266
267  FileName in_file "C:\Share\sample.tsv";
268
269  proc import datafile=in_file out=outlib.outsas
270  dbms=dlm
271  replace;
272  delimiter = '09'x;
273  run;

274   /**********************************************************************
275   *   PRODUCT:   SAS
276   *   VERSION:   9.3
277   *   CREATOR:   External File Interface
278   *   DATE:      23APR14
279   *   DESC:      Generated SAS Datastep Code
280   *   TEMPLATE SOURCE:  (None Specified.)
281   ***********************************************************************/
282      data OUTLIB.OUTSAS    ;
283      %let _EFIERR_ = 0; /* set the ERROR detection macro variable */
284      infile IN_FILE delimiter='09'x MISSOVER DSD lrecl=32767 firstobs=2 ;
285         informat pin best32. ;
286         informat bin best32. ;
287         informat as_of_dt best32. ;
288         informat mail_drop_dt $4. ;
289         informat mail_ship_dt best32. ;
290         informat mail_date best32. ;
291         informat poid $9. ;
292         informat spid $3. ;
293         informat primary_source_code $10. ;
294         informat campaign_code $4. ;
295         informat cell_id $4. ;
296         informat cell_title $73. ;
297         informat offer_title $74. ;
298         informat bus_unit $2. ;
299         informat offer_type $2. ;
300         informat channel $2. ;
301         informat camp_type $1. ;
302         informat ia_code $3. ;
303         informat ia_description $30. ;
304         informat prod_group $17. ;
305         informat card_group $7. ;
306         informat emerg_premium $8. ;
307         informat model_validation best32. ;
308         informat first_year_free $3. ;
309         informat acquisition_pts best32. ;
310         informat acquisition_stmt_credit best32. ;
311         informat spend_threshold best32. ;
312         informat threshold_duration best32. ;
313         informat secondary_fpb_pts $1. ;
314         informat secondary_fpb_stmt_credit best32. ;
315         informat secondary_threshold_duration best32. ;
316         informat intro_apr $4. ;
317         informat bt_apr best32. ;
318         informat goto_apr best32. ;
319         informat step $1. ;
320         informat cell_waveid $10. ;
321         informat appdata $1. ;
322         format pin best12. ;
323         format bin best12. ;
324         format as_of_dt best12. ;
325         format mail_drop_dt $4. ;
326         format mail_ship_dt best12. ;
327         format mail_date best12. ;
328         format poid $9. ;
329         format spid $3. ;
330         format primary_source_code $10. ;
331         format campaign_code $4. ;
332         format cell_id $4. ;
333         format cell_title $73. ;
334         format offer_title $74. ;
335         format bus_unit $2. ;
336         format offer_type $2. ;
337         format channel $2. ;
338         format camp_type $1. ;
339         format ia_code $3. ;
340         format ia_description $30. ;
341         format prod_group $17. ;
342         format card_group $7. ;
343         format emerg_premium $8. ;
344         format model_validation best12. ;
345         format first_year_free $3. ;
346         format acquisition_pts best12. ;
347         format acquisition_stmt_credit best12. ;
348         format spend_threshold best12. ;
349         format threshold_duration best12. ;
350         format secondary_fpb_pts $1. ;
351         format secondary_fpb_stmt_credit best12. ;
352         format secondary_threshold_duration best12. ;
353         format intro_apr $4. ;
354         format bt_apr best12. ;
355         format goto_apr best12. ;
356         format step $1. ;
357         format cell_waveid $10. ;
358         format appdata $1. ;
359      input
360                  pin
361                  bin
362                  as_of_dt
363                  mail_drop_dt $
364                  mail_ship_dt
365                  mail_date
366                  poid $
367                  spid $
368                  primary_source_code $
369                  campaign_code $
370                  cell_id $
371                  cell_title $
372                  offer_title $
373                  bus_unit $
374                  offer_type $
375                  channel $
376                  camp_type $
377                  ia_code $
378                  ia_description $
379                  prod_group $
380                  card_group $
381                  emerg_premium $
382                  model_validation
383                  first_year_free $
384                  acquisition_pts
385                  acquisition_stmt_credit
386                  spend_threshold
387                  threshold_duration
388                  secondary_fpb_pts $
389                  secondary_fpb_stmt_credit
390                  secondary_threshold_duration
391                  intro_apr $
392                  bt_apr
393                  goto_apr
394                  step $
395                  cell_waveid $
396                  appdata $
397      ;
398      if _ERROR_ then call symputx('_EFIERR_',1);  /* set ERROR detection macro variable */
399      run;

NOTE: The infile IN_FILE is:
      Filename=C:\Share\sample.tsv,
      RECFM=V,LRECL=32767,File Size (bytes)=28342,
      Last Modified=23Apr2014:15:27:59,
      Create Time=23Apr2014:15:29:02

NOTE: Invalid data for model_validation in line 26 275-276.
RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

26  CHAR  100001856.0.201303.NULL.02192013.20130301.AI80:0001.L7Z.A00000EF5W.AI80.G825.CHALLENGE
    ZONE  33333333303033333304544033333333033333333044333333304350433333443504433043330444444444
    NUMR  1000018569092013039E5CC90219201392013030191980A00019C7A9100000565791980978259381CC5E75

      87  R: MV EMERG GOLD FYF 25K/$1000/3M GIFTCARD REFRESHED PKG.AI80:0001/AMERICAN EXPRESS GO
    ZONE  53245244454244442454233422333323424445445425445454442544044333333324445444424555455244
    NUMR  2A0D605D52707FC40696025BF41000F3D079643124025625385400B791980A0001F1D52931E0580253307F



RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     173  LD/FYF/25000/$1000/3 MONTHS.CS.PS.DM.C.F2D.GOLD: PREFERRED REWARDS GOLD.CHARGE - GOLD.
    ZONE  44245423333322333323244454504505504404043404444325544455442545454524444044454422244440
    NUMR  C4F696F25000F41000F30DFE48393390394D93962497FC4A00256522540257124307FC493812750D07FC49

     259  CHARGE.EMERGING.MV.FYF.25000..1000.3....0.0.0..G825032013. 316
    ZONE  4445440444544440450454033333003333030000303030043333333330
    NUMR  38127595D5279E79D69696925000991000939999090909978250320139
pin=100001856 bin=0 as_of_dt=201303 mail_drop_dt=NULL mail_ship_dt=2192013 mail_date=20130301
poid=AI80:0001 spid=L7Z primary_source_code=A00000EF5W campaign_code=AI80 cell_id=G825
cell_title=CHALLENGER: MV EMERG GOLD FYF 25K/$1000/3M GIFTCARD REFRESHED PKG
offer_title=AI80:0001/AMERICAN EXPRESS GOLD/FYF/25000/$1000/3 MONTHS bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=F2D ia_description=GOLD: PREFERRED REWARDS GOLD
prod_group=CHARGE - GOLD card_group=CHARGE emerg_premium=EMERGING model_validation=.
first_year_free=FYF acquisition_pts=25000 acquisition_stmt_credit=. spend_threshold=1000
threshold_duration=3 secondary_fpb_pts=  secondary_fpb_stmt_credit=.
secondary_threshold_duration=. intro_apr=0 bt_apr=0 goto_apr=0 step=  cell_waveid=G825032013
appdata=  _ERROR_=1 _N_=25
NOTE: Invalid data for model_validation in line 38 250-251.

38  CHAR  100001980.0.201311.NULL.10212013.20131101.AS8J:0002.L7Z.A00000ETK3.AS8J.D463.MV EMERG
    ZONE  33333333303033333304544033333333033333333045343333304350433333454304534043330452444542
    NUMR  1000019809092013119E5CC9102120139201311019138AA00029C7A910000054B39138A944639D605D5270

      87  CTRL: DELTA GOLD FYF 35K/$1000/3MOS +$50SC/FPB/DELTA."AS8J:0002/DELTA GOLD/FYF/35,000/
    ZONE  45543244454244442454233422333323445222335424542444540245343333324445424444245423323332
    NUMR  342CA045C4107FC40696035BF41000F3DF30B45033F602F45C4192138AA0002F45C4107FC4F696F35C000F

     173  $1000/3MOS+$50SC/FPB".CS.PS.DM.C.NX6.DELTA GOLD: 9.99% BT.DELTA.SAC.EMERGING.MV.FYF.35
    ZONE  23333234452233542454204505504404045304445424444323233224504445405440444544440450454033
    NUMR  41000F3DF3B45033F602293390394D939E86945C4107FC4A09E995024945C41931395D5279E79D69696935

     259  000..1000.3..50..0.0.15.24..D463112013. 297
    ZONE  333003333030033003030332330043333333330
    NUMR  00099100093995099090915E249944631120139
pin=100001980 bin=0 as_of_dt=201311 mail_drop_dt=NULL mail_ship_dt=10212013 mail_date=20131101
poid=AS8J:0002 spid=L7Z primary_source_code=A00000ETK3 campaign_code=AS8J cell_id=D463
cell_title=MV EMERG CTRL: DELTA GOLD FYF 35K/$1000/3MOS +$50SC/FPB/DELTA
offer_title=AS8J:0002/DELTA GOLD/FYF/35,000/$1000/3MOS+$50SC/FPB bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=NX6 ia_description=DELTA GOLD: 9.99% BT prod_group=DELTA
card_group=SAC emerg_premium=EMERGING model_validation=. first_year_free=FYF
acquisition_pts=35000 acquisition_stmt_credit=. spend_threshold=1000 threshold_duration=3
secondary_fpb_pts=  secondary_fpb_stmt_credit=50 secondary_threshold_duration=. intro_apr=0
bt_apr=0 goto_apr=15.24 step=  cell_waveid=D463112013 appdata=  _ERROR_=1 _N_=37
NOTE: Invalid data for model_validation in line 52 272-273.

52  CHAR  10002057.0.201208.NULL.07202012.20120801.AD4B:0001.L7Z.A00000E64W.AD4B.S660.MV PREM BS
    ZONE  33333333030333333045440333333330333333330443433333043504333334335044340533304525544245
    NUMR  100020579092012089E5CC90720201292012080191442A00019C7A9100000564791442936609D60025D023

      87  KY - 30K/$500/3M - PASSPORT PKG (FF UPSELL).BLUE SKY - 0F15/P+13.99/P+13.99 - UPSELL T
    ZONE  45222334223332342225455545525442244255544420445425452223433252332332523323322255544425
    NUMR  B90D030BF4500F3D0D001330F2400B7086605035CC992C5503B90D00615F0B13E99F0B13E990D05035CC04

RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     173  O BLUE SKY PREF 0F15/P+13.99.CS.PS.DM.C.MWS.BLUE SKY: 4.99 LOB BT WITH FEE.BLUESKY.LEN
    ZONE  42445425452554423433252332330450550440404550445425453232332444245254542444044545450444
    NUMR  F02C5503B90025600615F0B13E9993390394D939D7392C5503B9A04E990CF202407948065592C553B99C5E

     259  DING.PREMIUM.MV.FYF.30000..500.3....0F15.0.17.24..S660082012. 319
    ZONE  4444055444540450454033333003330300003433030332330053333333330
    NUMR  49E79025D95D9D6969693000099500939999061590917E249936600820129
pin=10002057 bin=0 as_of_dt=201208 mail_drop_dt=NULL mail_ship_dt=7202012 mail_date=20120801
poid=AD4B:0001 spid=L7Z primary_source_code=A00000E64W campaign_code=AD4B cell_id=S660
cell_title=MV PREM BSKY - 30K/$500/3M - PASSPORT PKG (FF UPSELL)
offer_title=BLUE SKY - 0F15/P+13.99/P+13.99 - UPSELL TO BLUE SKY PREF 0F15/P+13.99 bus_unit=CS
offer_type=PS channel=DM camp_type=C ia_code=MWS ia_description=BLUE SKY: 4.99 LOB BT WITH FEE
prod_group=BLUESKY card_group=LENDING emerg_premium=PREMIUM model_validation=.
first_year_free=FYF acquisition_pts=30000 acquisition_stmt_credit=. spend_threshold=500
threshold_duration=3 secondary_fpb_pts=  secondary_fpb_stmt_credit=.
secondary_threshold_duration=. intro_apr=0F15 bt_apr=0 goto_apr=17.24 step=
cell_waveid=S660082012 appdata=  _ERROR_=1 _N_=51
NOTE: Invalid data for model_validation in line 71 163-164.

71  CHAR  10002057.0.201301.NULL.12102012.20130102.AGYX:0001.L7Z.A00000ED1G.AGYX.K605.MV CTRL CO
    ZONE  33333333030333333045440333333330333333330445533333043504333334434044550433304524554244
    NUMR  100020579092013019E5CC91210201292013010291798A00019C7A91000005417917989B6059D60342C03F

      87  STCO NO FEE EXEC PKG.AGYX:0001:COSTCO:FYF.CS.PS.DM.C.JVB.COSTCO.COSTCO.SAC..MV.FYF....
    ZONE  55442442444245442544044553333334455443454045055044040454044554404455440544004504540000
    NUMR  343F0EF06550585300B791798A0001A3F343FA69693390394D939A6293F343F93F343F931399D696969999

     173  ....0F6.0.15.24..K605012013. 200
    ZONE  0000343030332330043333333330
    NUMR  999906690915E2499B6050120139
pin=10002057 bin=0 as_of_dt=201301 mail_drop_dt=NULL mail_ship_dt=12102012 mail_date=20130102
poid=AGYX:0001 spid=L7Z primary_source_code=A00000ED1G campaign_code=AGYX cell_id=K605
cell_title=MV CTRL COSTCO NO FEE EXEC PKG offer_title=AGYX:0001:COSTCO:FYF bus_unit=CS
offer_type=PS channel=DM camp_type=C ia_code=JVB ia_description=COSTCO prod_group=COSTCO
card_group=SAC emerg_premium=  model_validation=. first_year_free=FYF acquisition_pts=.
acquisition_stmt_credit=. spend_threshold=. threshold_duration=. secondary_fpb_pts=
secondary_fpb_stmt_credit=. secondary_threshold_duration=. intro_apr=0F6 bt_apr=0 goto_apr=15.24
step=  cell_waveid=K605012013 appdata=  _ERROR_=1 _N_=70
NOTE: Invalid data for model_validation in line 80 235-236.

80  CHAR  100044280.0.201311.NULL.10212013.20131101.ASHC:0001.L7Z.A00000ETME.ASHC.U977.EMERGING
    ZONE  33333333303033333304544033333333033333333045443333304350433333454404544053330444544442
    NUMR  1000442809092013119E5CC91021201392013110191383A00019C7A910000054D5913839597795D5279E70

      87  MV BCE 150/500/3M SHORT FLAP INLINE.ASHC:0001/BLUE CASH EVERYDAY/FYF/$150 SC/$500/3MOS
    ZONE  45244423332333234254455244452444444045443333324454244542454554452454223332542233323445
    NUMR  D602350150F500F3D038F2406C1009EC9E591383A0001F2C5503138056529419F696F4150033F4500F3DF3

     173  ..CS.PS.DM.C.LPQ.BLUECASH EVERYDAY.BLUE CASH.LENDING.EMERGING.MV.FYF..150.500.3....0F1
    ZONE  20450550440404550445444542454554450445424454044444440444544440450454003330333030000343
    NUMR  E93390394D939C0192C55313805652941992C55031389C5E49E795D5279E79D69696991509500939999061


RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     259  5.0.12.99..U977112013. 280
    ZONE  3030332330053333333330
    NUMR  590912E999959771120139
pin=100044280 bin=0 as_of_dt=201311 mail_drop_dt=NULL mail_ship_dt=10212013 mail_date=20131101
poid=ASHC:0001 spid=L7Z primary_source_code=A00000ETME campaign_code=ASHC cell_id=U977
cell_title=EMERGING MV BCE 150/500/3M SHORT FLAP INLINE
offer_title=ASHC:0001/BLUE CASH EVERYDAY/FYF/$150 SC/$500/3MOS. bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=LPQ ia_description=BLUECASH EVERYDAY prod_group=BLUE CASH
card_group=LENDING emerg_premium=EMERGING model_validation=. first_year_free=FYF
acquisition_pts=. acquisition_stmt_credit=150 spend_threshold=500 threshold_duration=3
secondary_fpb_pts=  secondary_fpb_stmt_credit=. secondary_threshold_duration=. intro_apr=0F15
bt_apr=0 goto_apr=12.99 step=  cell_waveid=U977112013 appdata=  _ERROR_=1 _N_=79
NOTE: 100 records were read from the infile IN_FILE.
      The minimum record length was 200.
      The maximum record length was 337.
NOTE: The data set OUTLIB.OUTSAS has 100 observations and 37 variables.
NOTE: DATA statement used (Total process time):
      real time           0.00 seconds
      cpu time            0.00 seconds


Errors detected in submitted DATA step. Examine log.
100 rows created in OUTLIB.OUTSAS from IN_FILE.



ERROR: Import unsuccessful.  See SAS Log for details.
NOTE: The SAS System stopped processing this step because of errors.
NOTE: PROCEDURE IMPORT used (Total process time):
      real time           0.09 seconds
      cpu time            0.07 seconds



400  libname outlib "C:\Share\";
NOTE: Libref OUTLIB was successfully assigned as follows:
      Engine:        V9
      Physical Name: C:\Share
401
402  FileName in_file "C:\Share\sample.tsv";
403
404  proc import datafile=in_file out=outlib.outsas
405  dbms=dlm
406  replace;
407  delimiter = '09'x;
408  run;

409   /**********************************************************************
410   *   PRODUCT:   SAS
411   *   VERSION:   9.3
412   *   CREATOR:   External File Interface
413   *   DATE:      23APR14
414   *   DESC:      Generated SAS Datastep Code
415   *   TEMPLATE SOURCE:  (None Specified.)
416   ***********************************************************************/
417      data OUTLIB.OUTSAS    ;
418      %let _EFIERR_ = 0; /* set the ERROR detection macro variable */
419      infile IN_FILE delimiter='09'x MISSOVER DSD lrecl=32767 firstobs=2 ;
420         informat pin best32. ;
421         informat bin best32. ;
422         informat as_of_dt best32. ;
423         informat mail_drop_dt $4. ;
424         informat mail_ship_dt best32. ;
425         informat mail_date best32. ;
426         informat poid $9. ;
427         informat spid $3. ;
428         informat primary_source_code $10. ;
429         informat campaign_code $4. ;
430         informat cell_id $4. ;
431         informat cell_title $73. ;
432         informat offer_title $74. ;
433         informat bus_unit $2. ;
434         informat offer_type $2. ;
435         informat channel $2. ;
436         informat camp_type $1. ;
437         informat ia_code $3. ;
438         informat ia_description $30. ;
439         informat prod_group $17. ;
440         informat card_group $7. ;
441         informat emerg_premium $8. ;
442         informat model_validation best32. ;
443         informat first_year_free $3. ;
444         informat acquisition_pts best32. ;
445         informat acquisition_stmt_credit best32. ;
446         informat spend_threshold best32. ;
447         informat threshold_duration best32. ;
448         informat secondary_fpb_pts $1. ;
449         informat secondary_fpb_stmt_credit best32. ;
450         informat secondary_threshold_duration best32. ;
451         informat intro_apr $4. ;
452         informat bt_apr best32. ;
453         informat goto_apr best32. ;
454         informat step $1. ;
455         informat cell_waveid $10. ;
456         informat appdata $1. ;
457         format pin best12. ;
458         format bin best12. ;
459         format as_of_dt best12. ;
460         format mail_drop_dt $4. ;
461         format mail_ship_dt best12. ;
462         format mail_date best12. ;
463         format poid $9. ;
464         format spid $3. ;
465         format primary_source_code $10. ;
466         format campaign_code $4. ;
467         format cell_id $4. ;
468         format cell_title $73. ;
469         format offer_title $74. ;
470         format bus_unit $2. ;
471         format offer_type $2. ;
472         format channel $2. ;
473         format camp_type $1. ;
474         format ia_code $3. ;
475         format ia_description $30. ;
476         format prod_group $17. ;
477         format card_group $7. ;
478         format emerg_premium $8. ;
479         format model_validation best12. ;
480         format first_year_free $3. ;
481         format acquisition_pts best12. ;
482         format acquisition_stmt_credit best12. ;
483         format spend_threshold best12. ;
484         format threshold_duration best12. ;
485         format secondary_fpb_pts $1. ;
486         format secondary_fpb_stmt_credit best12. ;
487         format secondary_threshold_duration best12. ;
488         format intro_apr $4. ;
489         format bt_apr best12. ;
490         format goto_apr best12. ;
491         format step $1. ;
492         format cell_waveid $10. ;
493         format appdata $1. ;
494      input
495                  pin
496                  bin
497                  as_of_dt
498                  mail_drop_dt $
499                  mail_ship_dt
500                  mail_date
501                  poid $
502                  spid $
503                  primary_source_code $
504                  campaign_code $
505                  cell_id $
506                  cell_title $
507                  offer_title $
508                  bus_unit $
509                  offer_type $
510                  channel $
511                  camp_type $
512                  ia_code $
513                  ia_description $
514                  prod_group $
515                  card_group $
516                  emerg_premium $
517                  model_validation
518                  first_year_free $
519                  acquisition_pts
520                  acquisition_stmt_credit
521                  spend_threshold
522                  threshold_duration
523                  secondary_fpb_pts $
524                  secondary_fpb_stmt_credit
525                  secondary_threshold_duration
526                  intro_apr $
527                  bt_apr
528                  goto_apr
529                  step $
530                  cell_waveid $
531                  appdata $
532      ;
533      if _ERROR_ then call symputx('_EFIERR_',1);  /* set ERROR detection macro variable */
534      run;

NOTE: The infile IN_FILE is:
      Filename=C:\Share\sample.tsv,
      RECFM=V,LRECL=32767,File Size (bytes)=28342,
      Last Modified=23Apr2014:15:27:59,
      Create Time=23Apr2014:15:29:02

NOTE: Invalid data for model_validation in line 26 275-276.
RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

26  CHAR  100001856.0.201303.NULL.02192013.20130301.AI80:0001.L7Z.A00000EF5W.AI80.G825.CHALLENGE
    ZONE  33333333303033333304544033333333033333333044333333304350433333443504433043330444444444
    NUMR  1000018569092013039E5CC90219201392013030191980A00019C7A9100000565791980978259381CC5E75

      87  R: MV EMERG GOLD FYF 25K/$1000/3M GIFTCARD REFRESHED PKG.AI80:0001/AMERICAN EXPRESS GO
    ZONE  53245244454244442454233422333323424445445425445454442544044333333324445444424555455244
    NUMR  2A0D605D52707FC40696025BF41000F3D079643124025625385400B791980A0001F1D52931E0580253307F

     173  LD/FYF/25000/$1000/3 MONTHS.CS.PS.DM.C.F2D.GOLD: PREFERRED REWARDS GOLD.CHARGE - GOLD.
    ZONE  44245423333322333323244454504505504404043404444325544455442545454524444044454422244440
    NUMR  C4F696F25000F41000F30DFE48393390394D93962497FC4A00256522540257124307FC493812750D07FC49

     259  CHARGE.EMERGING.MV.FYF.25000..1000.3....0.0.0..G825032013. 316
    ZONE  4445440444544440450454033333003333030000303030043333333330
    NUMR  38127595D5279E79D69696925000991000939999090909978250320139
pin=100001856 bin=0 as_of_dt=201303 mail_drop_dt=NULL mail_ship_dt=2192013 mail_date=20130301
poid=AI80:0001 spid=L7Z primary_source_code=A00000EF5W campaign_code=AI80 cell_id=G825
cell_title=CHALLENGER: MV EMERG GOLD FYF 25K/$1000/3M GIFTCARD REFRESHED PKG
offer_title=AI80:0001/AMERICAN EXPRESS GOLD/FYF/25000/$1000/3 MONTHS bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=F2D ia_description=GOLD: PREFERRED REWARDS GOLD
prod_group=CHARGE - GOLD card_group=CHARGE emerg_premium=EMERGING model_validation=.
first_year_free=FYF acquisition_pts=25000 acquisition_stmt_credit=. spend_threshold=1000
threshold_duration=3 secondary_fpb_pts=  secondary_fpb_stmt_credit=.
secondary_threshold_duration=. intro_apr=0 bt_apr=0 goto_apr=0 step=  cell_waveid=G825032013
appdata=  _ERROR_=1 _N_=25
NOTE: Invalid data for model_validation in line 38 250-251.

38  CHAR  100001980.0.201311.NULL.10212013.20131101.AS8J:0002.L7Z.A00000ETK3.AS8J.D463.MV EMERG
    ZONE  33333333303033333304544033333333033333333045343333304350433333454304534043330452444542
    NUMR  1000019809092013119E5CC9102120139201311019138AA00029C7A910000054B39138A944639D605D5270

      87  CTRL: DELTA GOLD FYF 35K/$1000/3MOS +$50SC/FPB/DELTA."AS8J:0002/DELTA GOLD/FYF/35,000/
    ZONE  45543244454244442454233422333323445222335424542444540245343333324445424444245423323332
    NUMR  342CA045C4107FC40696035BF41000F3DF30B45033F602F45C4192138AA0002F45C4107FC4F696F35C000F

RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     173  $1000/3MOS+$50SC/FPB".CS.PS.DM.C.NX6.DELTA GOLD: 9.99% BT.DELTA.SAC.EMERGING.MV.FYF.35
    ZONE  23333234452233542454204505504404045304445424444323233224504445405440444544440450454033
    NUMR  41000F3DF3B45033F602293390394D939E86945C4107FC4A09E995024945C41931395D5279E79D69696935

     259  000..1000.3..50..0.0.15.24..D463112013. 297
    ZONE  333003333030033003030332330043333333330
    NUMR  00099100093995099090915E249944631120139
pin=100001980 bin=0 as_of_dt=201311 mail_drop_dt=NULL mail_ship_dt=10212013 mail_date=20131101
poid=AS8J:0002 spid=L7Z primary_source_code=A00000ETK3 campaign_code=AS8J cell_id=D463
cell_title=MV EMERG CTRL: DELTA GOLD FYF 35K/$1000/3MOS +$50SC/FPB/DELTA
offer_title=AS8J:0002/DELTA GOLD/FYF/35,000/$1000/3MOS+$50SC/FPB bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=NX6 ia_description=DELTA GOLD: 9.99% BT prod_group=DELTA
card_group=SAC emerg_premium=EMERGING model_validation=. first_year_free=FYF
acquisition_pts=35000 acquisition_stmt_credit=. spend_threshold=1000 threshold_duration=3
secondary_fpb_pts=  secondary_fpb_stmt_credit=50 secondary_threshold_duration=. intro_apr=0
bt_apr=0 goto_apr=15.24 step=  cell_waveid=D463112013 appdata=  _ERROR_=1 _N_=37
NOTE: Invalid data for model_validation in line 52 272-273.

52  CHAR  10002057.0.201208.NULL.07202012.20120801.AD4B:0001.L7Z.A00000E64W.AD4B.S660.MV PREM BS
    ZONE  33333333030333333045440333333330333333330443433333043504333334335044340533304525544245
    NUMR  100020579092012089E5CC90720201292012080191442A00019C7A9100000564791442936609D60025D023

      87  KY - 30K/$500/3M - PASSPORT PKG (FF UPSELL).BLUE SKY - 0F15/P+13.99/P+13.99 - UPSELL T
    ZONE  45222334223332342225455545525442244255544420445425452223433252332332523323322255544425
    NUMR  B90D030BF4500F3D0D001330F2400B7086605035CC992C5503B90D00615F0B13E99F0B13E990D05035CC04

     173  O BLUE SKY PREF 0F15/P+13.99.CS.PS.DM.C.MWS.BLUE SKY: 4.99 LOB BT WITH FEE.BLUESKY.LEN
    ZONE  42445425452554423433252332330450550440404550445425453232332444245254542444044545450444
    NUMR  F02C5503B90025600615F0B13E9993390394D939D7392C5503B9A04E990CF202407948065592C553B99C5E

     259  DING.PREMIUM.MV.FYF.30000..500.3....0F15.0.17.24..S660082012. 319
    ZONE  4444055444540450454033333003330300003433030332330053333333330
    NUMR  49E79025D95D9D6969693000099500939999061590917E249936600820129
pin=10002057 bin=0 as_of_dt=201208 mail_drop_dt=NULL mail_ship_dt=7202012 mail_date=20120801
poid=AD4B:0001 spid=L7Z primary_source_code=A00000E64W campaign_code=AD4B cell_id=S660
cell_title=MV PREM BSKY - 30K/$500/3M - PASSPORT PKG (FF UPSELL)
offer_title=BLUE SKY - 0F15/P+13.99/P+13.99 - UPSELL TO BLUE SKY PREF 0F15/P+13.99 bus_unit=CS
offer_type=PS channel=DM camp_type=C ia_code=MWS ia_description=BLUE SKY: 4.99 LOB BT WITH FEE
prod_group=BLUESKY card_group=LENDING emerg_premium=PREMIUM model_validation=.
first_year_free=FYF acquisition_pts=30000 acquisition_stmt_credit=. spend_threshold=500
threshold_duration=3 secondary_fpb_pts=  secondary_fpb_stmt_credit=.
secondary_threshold_duration=. intro_apr=0F15 bt_apr=0 goto_apr=17.24 step=
cell_waveid=S660082012 appdata=  _ERROR_=1 _N_=51
NOTE: Invalid data for model_validation in line 71 163-164.

71  CHAR  10002057.0.201301.NULL.12102012.20130102.AGYX:0001.L7Z.A00000ED1G.AGYX.K605.MV CTRL CO
    ZONE  33333333030333333045440333333330333333330445533333043504333334434044550433304524554244
    NUMR  100020579092013019E5CC91210201292013010291798A00019C7A91000005417917989B6059D60342C03F

      87  STCO NO FEE EXEC PKG.AGYX:0001:COSTCO:FYF.CS.PS.DM.C.JVB.COSTCO.COSTCO.SAC..MV.FYF....
    ZONE  55442442444245442544044553333334455443454045055044040454044554404455440544004504540000
    NUMR  343F0EF06550585300B791798A0001A3F343FA69693390394D939A6293F343F93F343F931399D696969999

RULE:     ----+----1----+----2----+----3----+----4----+----5----+----6----+----7----+----8----+-

     173  ....0F6.0.15.24..K605012013. 200
    ZONE  0000343030332330043333333330
    NUMR  999906690915E2499B6050120139
pin=10002057 bin=0 as_of_dt=201301 mail_drop_dt=NULL mail_ship_dt=12102012 mail_date=20130102
poid=AGYX:0001 spid=L7Z primary_source_code=A00000ED1G campaign_code=AGYX cell_id=K605
cell_title=MV CTRL COSTCO NO FEE EXEC PKG offer_title=AGYX:0001:COSTCO:FYF bus_unit=CS
offer_type=PS channel=DM camp_type=C ia_code=JVB ia_description=COSTCO prod_group=COSTCO
card_group=SAC emerg_premium=  model_validation=. first_year_free=FYF acquisition_pts=.
acquisition_stmt_credit=. spend_threshold=. threshold_duration=. secondary_fpb_pts=
secondary_fpb_stmt_credit=. secondary_threshold_duration=. intro_apr=0F6 bt_apr=0 goto_apr=15.24
step=  cell_waveid=K605012013 appdata=  _ERROR_=1 _N_=70
NOTE: Invalid data for model_validation in line 80 235-236.

80  CHAR  100044280.0.201311.NULL.10212013.20131101.ASHC:0001.L7Z.A00000ETME.ASHC.U977.EMERGING
    ZONE  33333333303033333304544033333333033333333045443333304350433333454404544053330444544442
    NUMR  1000442809092013119E5CC91021201392013110191383A00019C7A910000054D5913839597795D5279E70

      87  MV BCE 150/500/3M SHORT FLAP INLINE.ASHC:0001/BLUE CASH EVERYDAY/FYF/$150 SC/$500/3MOS
    ZONE  45244423332333234254455244452444444045443333324454244542454554452454223332542233323445
    NUMR  D602350150F500F3D038F2406C1009EC9E591383A0001F2C5503138056529419F696F4150033F4500F3DF3

     173  ..CS.PS.DM.C.LPQ.BLUECASH EVERYDAY.BLUE CASH.LENDING.EMERGING.MV.FYF..150.500.3....0F1
    ZONE  20450550440404550445444542454554450445424454044444440444544440450454003330333030000343
    NUMR  E93390394D939C0192C55313805652941992C55031389C5E49E795D5279E79D69696991509500939999061

     259  5.0.12.99..U977112013. 280
    ZONE  3030332330053333333330
    NUMR  590912E999959771120139
pin=100044280 bin=0 as_of_dt=201311 mail_drop_dt=NULL mail_ship_dt=10212013 mail_date=20131101
poid=ASHC:0001 spid=L7Z primary_source_code=A00000ETME campaign_code=ASHC cell_id=U977
cell_title=EMERGING MV BCE 150/500/3M SHORT FLAP INLINE
offer_title=ASHC:0001/BLUE CASH EVERYDAY/FYF/$150 SC/$500/3MOS. bus_unit=CS offer_type=PS
channel=DM camp_type=C ia_code=LPQ ia_description=BLUECASH EVERYDAY prod_group=BLUE CASH
card_group=LENDING emerg_premium=EMERGING model_validation=. first_year_free=FYF
acquisition_pts=. acquisition_stmt_credit=150 spend_threshold=500 threshold_duration=3
secondary_fpb_pts=  secondary_fpb_stmt_credit=. secondary_threshold_duration=. intro_apr=0F15
bt_apr=0 goto_apr=12.99 step=  cell_waveid=U977112013 appdata=  _ERROR_=1 _N_=79
NOTE: 100 records were read from the infile IN_FILE.
      The minimum record length was 200.
      The maximum record length was 337.
NOTE: The data set OUTLIB.OUTSAS has 100 observations and 37 variables.
NOTE: DATA statement used (Total process time):
      real time           0.09 seconds
      cpu time            0.09 seconds


Errors detected in submitted DATA step. Examine log.
100 rows created in OUTLIB.OUTSAS from IN_FILE.



ERROR: Import unsuccessful.  See SAS Log for details.
NOTE: The SAS System stopped processing this step because of errors.
NOTE: PROCEDURE IMPORT used (Total process time):
      real time           0.20 seconds
      cpu time            0.20 seconds

535


536  proc print;
NOTE: Writing HTML Body file: sashtml.htm
537  run;

NOTE: There were 100 observations read from the data set OUTLIB.OUTSAS.
NOTE: PROCEDURE PRINT used (Total process time):
      real time           10.47 seconds
      cpu time            0.32 seconds



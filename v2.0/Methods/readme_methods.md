# CRC-AIM v2.0 Methods
## Natural History Methods
### Adenoma Generation and Location
![image](https://github.com/user-attachments/assets/3fd8eb5d-f8bc-4c9c-86df-bb5d4cd180b0)

**Parameters**

+ _r<sub>i</sub>(a)_: risk of developing an adenoma for individual i at age a

+ _I<sub>F</sub>(i)_: indicator function, which is equal to 1 when individual i is female and 0 otherwise

+ _I<sub>[a<sub>0</sub>,∞)</sub>(a)_: indicator function that is equal 1 if the individual’s age a ∈ [a<sub>0</sub>,∞)

+ _β<sub>j</sub>_: regression coefficients of the log-linear model

### Adenoma Growth

![image](https://github.com/user-attachments/assets/d4c2c1c7-787b-417c-9fe6-6efdaf5034d5)

**Parameters**

+ _d<sub>ij</sub>(t)_: diameter in millimeters (mm) of an adenoma _j_ at time _t_, measured after its initiation, in individual _i_ using the Richard's growth model

+ _p_: unknown parameter of the growth model

+ _λ<sub>ij</sub>_: growth rate of adenoma _j_ in individual _i_

+ _d<sub>max</sub>_: maximum diameter (50 mm)

+ _d<sub>min</sub>_: minimum diameter (1 mm)

The growth rate _λ<sub>ij</sub>_ is determined stochastically by first sampling the time to reach 10 mm in diameter (_t<sub>10mm</sub>_), which is assumed to follow the Fréchet distribution with scale parameter _s<sub>l</sub>_ and shape parameter _α<sub>l</sub> (l ∈{colon, rectum})_. The cumulative distribution function (CDF) at time _t_ after the initiation of an adenoma located at _l_ is given by:

![image](https://github.com/user-attachments/assets/148a0bb3-c6e7-4aed-b8b1-6324505628ed)

Once _t<sub>10mm</sub>_ is sampled from the CDF, the growth rate can be determined by solving the growth model using _d<sub>ij</sub>(t<sub>10mm</sub>)_ = 10.

![image](https://github.com/user-attachments/assets/dbea24b4-0168-43ef-b564-1befcea2f761)

### Transition from Adenoma to Preclinical CRC

![image](https://github.com/user-attachments/assets/805ea3f6-5053-4ba2-af1c-518769b3449f)

**Parameters**

+ _P<sub>ls</sub>(d,a)_: probability of transition to preclinical cancer at or before diameter _d_ at age _a_
+ _Φ(∙)_: standard normal CDF
+ _l_: location (colon or rectum)
+ _s_: sex (male or female)
+ _γ<sub>3</sub>_: set to be 0.5

### Transition from Preclinical CRC to Clinically Detectable CRC

**Colon Adenomas**

![image](https://github.com/user-attachments/assets/f03e1e7a-d881-4cb5-b809-437f6ebd446a)

**Parameters**

+ _S<sub>c</sub>(t)_: sojourn time for colon adenomas
+ _t_: year
+ _k_: shape parameter
+ _λ<sub>c</sub>_: location-specific scale parameter

**Rectal Adenomas**

![image](https://github.com/user-attachments/assets/8ac04330-509d-4228-bf25-a1ad4a997889)

**Parameters**

+ _S<sub>r</sub>(t)_: sojourn time for rectal adenomas
+ _t_: year
+ _k_: shape parameter
+ _λ<sub>c</sub>_: location-specific scale parameter
+ _exp(α)_: hazard ratio between rectal and colon adenomas 

### CRC Stage at Clinical Detection
* Multinominal distribution derived from SEER 1975-1979 data stratified by anatomic subsite location (proximal colon, distal colon, and rectum), age group at diagnosis, and sex

### CRC Size at Clinical Detection
* Assigned using SEER 2010-2015 data limited to cases diagnosed at ages 20-50 and assumed to follow a gamma distribution

### CRC Survival
* Based on parametric models with sex and age at diagnosis as covariates for each stage and location (colon vs rectum) fitted to SEER-reported cause-specific survival

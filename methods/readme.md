# CRC-AIM Methods

## Natural History Methods

### Adenoma Generation and Location
![Adenoma Generation Risk Function](../images/formula_adenoma_generation.PNG)

Instantaneous risk function of growing an adenoma

_Parameters_

* t - time in years
* α0 - baseline log risk parameter
* α0i - random baseline risk parameter assigned to individual i, ~ N(α0, σα)
* α1 - sex parameter
* α2 - age group parameter (four parameters total, one per age group)
  * k = 1: ages 20-49
  * k = 2: ages 50-59
  * k = 3: ages 60-69
  * k = 4: ages 70+

### Adenoma Growth
![Adenoma Growth CDF](../images/formula_adenoma_growth.PNG)

CDF of time to 10 mm adenoma size.

_Parameters_

* β1 - scale parameter
* β2 - location parameter

These parameters vary based on adenoma location (colon or rectum).

Time to 10 mm can be used to calculate a growth rate: λij for the j-th adenoma in the i-th individual:

![Adenoma Growth Rate](../images/formula_adenoma_growth_rate.PNG)

_Parameters_

* d - diameter of adenoma at given time (0: initiation, infinity: max)
* t_10mm - time for adenoma to grow to 10 mm as sampled from CDF above

The growth rate can be rewritten to evaluate the size of the adenoma at a given time t:

![Adenoma size at time t](../images/formula_adenoma_growth_diameter_at_time.PNG)

### Transition from Adenoma to Preclinical CRC
[formulas | parameters]: [description]

![Adenoma Transition Probability](../images/formula_adenoma_transition.PNG)

_Parameters_

* γ1
* γ2
  * c or r: colon or rectum
  * m or f: male or female
* γ3
* s - adenoma size in mm
* a - age of adenoma initiation in years

### Transition to Clinically Detectable CRC
[formulas | parameters]: [description]

![Transition to Clinically Detectable CRC](../images/formula_transition_crc_prob.PNG)

_Parameters_

* ξc - transition probability
* s_t+1 - size at time t+1
* s_t - size at time t

### CRC Growth
[formulas | parameters]: [description]
![CRC Growth Rate](../images/formula_crc_growth_rate.PNG)

_Parameters_

* sf - size final
* si - size initial
* tsf - time to final size

### CRC Size at Clinical Detection
[formulas | parameters]: [description]
![Adenoma Transition Probability](../images/formula_CRC_Size_Clinical_Detection.PNG)

_Parameters_

* s - CRC size in mm
* σ - scale parameter
* λ - shape parameter

### CRC Stage Upon Detection
[formulas | parameters]: [description]

Multinomial Logistic Regression Model

![Multinomial Logistic Regression Model](../images/formula_multinomial_categorical_regression.PNG)

Categorical Probability

![Categorical Probability](../images/formula_categorical_prob.PNG)

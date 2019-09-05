# Parameter Listing
## Natural History Model Parameters

From [Rand Corporation CISNET Paper](https://cisnet.flexkb.net/mp/pub/cisnet_colorectal_rand_profile.pdf#%5B%7B%22num%22%3A22%2C%22gen%22%3A0%7D%2C%7B%22name%22%3A%22XYZ%22%7D%2C0%2C753%2C0%5D)

### Adenoma Risk: 7 Parameters(Adenoma Risk Component)

CRC–SPIN uses a non–homogeneous Poisson process to simulate adenoma occurrence

* Expected baseline log–risk: alpha0
* Standard deviation of baseline log–risk: sigma alpha
* The effect of sex on risk: alpha1
* The effect of age on risk: alpha2k, k=1,2,3,4
  * CRC–SPIN simulates change in risk for 4 age groups:,,, and. 
  * Calibration results indicate that risk slows and may decline after age 70.
  
 ### Adenoma Growth: 4 Parameters
 
 CRC-Spin simulates the time to reach 10mm using a Frechet (Type 2 Extreme Value) distribution 
 
 * beta1c, beta1r: Shape parameters for colon and rectum respectively
 * beta2c, beta2r: Scale parameters for colon and rectum respectively
 
 ### Adenoma Size at Transition to Preclinical CRC: 7 estimated Parameters
 
 * Overall Intercept, log-size transition: gamma0
 * Sex Effect: gamma1
 * Location Effect (colon/rectum): gamma2
 * Interaction Sex/Location: gamma3
 * log linear effect of age at initiation: gamma4
 * log linear effect of age at initiation: gamma 5
 * standard deviation of log-size at transition: sigma_gamma
 
 
 ### Time to Clinical Cancer Component
 
 * Weibull scale parameter: mu1
 * Weibull shape parameter: mu2
 * log-proportional hazards, sojourn time for rectal cancers: mu3
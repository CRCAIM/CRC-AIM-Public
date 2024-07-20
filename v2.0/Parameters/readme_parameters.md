# CRC-AIM Parameter Listing
## Natural History Model Parameters

### Adenoma Generation: 7 Parameters
* β<sub>0</sub>: baseline log-risk
* σ<sub>0</sub>: standard deviation of baseline log-risk
* β<sub>1</sub>: sex effect
* β<sub>2</sub>: age effect (ages 20- <50)
* β<sub>3</sub>: age effect (ages 50- <60)
* β<sub>4</sub>: age effect (ages 60- <70)
* β<sub>5</sub>: age effect (ages ≥ 70)

### Adenoma Growth (Time to 10 mm): 4 Parameters
* s<sub>c</sub>: scale (colon)
* α<sub>c</sub>: shape (colon)
* s<sub>r</sub>: scale (rectum)
* α<sub>r</sub>: scale (rectum)

### Adenoma Growth (Richard's Growth Model): 1 Parameter
* p: shape parameter

### Transition from Adenoma to Cancer: 8 Parameters
* γ<sub>1cm</sub>: size (male, colon)
* γ<sub>2cm</sub>: age at initiation (male, colon)
* γ<sub>1rm</sub>: size (male, rectum)
* γ<sub>2rm</sub>: age at initiation (male, rectum)
* γ<sub>1cf</sub>: size (female, colon)
* γ<sub>2cf</sub>: age at initiation (female, colon)
* γ<sub>1rf</sub>: size (female, rectum)
* γ<sub>2rf</sub>: age at initiation (female, rectum)

### Sojourn Time: 3 Parameters
* λ<sub>c</sub>: scale (colon)
* k: shape (colon and rectum)
* α: Log-hazard ratio

#CATI model for Cholera epidemics

This repository contains the codes and data used for the following article:
 
__The impact of case-area targeted interventions in response to cholera outbreaks: A modeling study__

__Codes to be uploaded follow__


## To load the epidemic curve:

```
import numpy as np
epicurve=np.fromfile('epicurveNDjamena.binary',dtype=[('Date','datetime64[D]'),('NCases','int')])
```

# CATI model

This repository contains the data used in the following article:

__The potential impact of case-area targeted interventions in response to cholera outbreaks: A modeling study__

## Data

The folder `data` contains the following files:

- `data/casedata/locationOffset.csv` contains the xy-coordinates and dates of reported case households. The coordinates are in meters. A random offset has been added to each set of coordinates to make it impossible to identify household locations. The relative location of households, necessary to compute the tau-statistics, is preserved.

- `data/casedata/epicurve.csv` contains the number of reported cases per day.

- `data/population_distribution/populationDistrNdjamena.pickle` contains the population distribution derived from the remotely sensed built-up density and can be loaded in python using the following commands:

```python
library(pickle)
f=open('populationDistrNdjamena.pickle','r')
popMatrix=pickle.load(f)
gridProp=pickle.load(f)
f.close()
```

- `data/districts_ndjamena/tcd_polbnd_adm9_a_osm_170206.shp` contains the boundaries of the districts as used for the district-targeted mass campaigns. This data has been obtained from OpenStreetMap ([© OpenStreetMap contributors](https://www.openstreetmap.org/copyright)).

- The TRMM precipitation data used is by Huffman et al. (2010) and can been obtained from [IRIDL].

[IRIDL]: http://iridl.ldeo.columbia.edu/SOURCES/.NASA/.GES-DAAC/.TRMM_L3/.TRMM_3B42/.v7/.daily/.precipitation/X/15.0/15.25/RANGEEDGES/Y/12/12.25/RANGEEDGES/T/(01%20Apr%202011)(01%20May%202012)RANGEEDGES/

Huffman, G. J., Adler, R. F., Bolvin, D. T. & Nelkin, E. J. (2010), The TRMM
multi-satellite precipitation analysis (TMPA), in M. Gebremichael & F. Hossain,
eds, ‘Satellite Rainfall Applications for Surface Hydrology’, Springer Netherlands,
pp. 3–22.

[![DOI](https://zenodo.org/badge/98530259.svg)](https://zenodo.org/badge/latestdoi/98530259)

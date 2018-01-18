# CATI model

[![DOI](https://zenodo.org/badge/98530259.svg)](https://zenodo.org/badge/latestdoi/98530259)

This repository contains the data used in the following article:

__The potential impact of case-area targeted interventions in response to cholera outbreaks: A modeling study__

## Data

The folder `data` contains the following files:

- `data/casedata/locationOffset.csv` contains the xy-coordinates and dates of reported case households. The coordinates are in meters. A random offset has been added to each set of coordinates to make it impossible to identify household locations. The relative location of households, necessary to compute the tau-statistics, is preserved.

- `data/casedata/epicurve.csv` contains the number of reported cases per day.

- `data/population_distribution/populationDistrNdjamena.pickle` contains the population distribution derived from the remotely sensed built-up density (Global Urban Footprint, Esch et al. (2017) and Esch et al. (2011)) and can be loaded in python using the following commands:

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

## References

Azman, A., Luquero, F.J., Salje, H., Naibei, N., Adalbert, N., Ali, M., Bertuzzo, E., Finger, F., Toure, B., Massing, L.A., Ramazani, R., Cardon, A., Saga, B., Allan, M., Olson, D., Leglise, J., Porten, K., Lessler, J., 2018. Micro-hotspots of Risk in Urban Cholera Epidemics. bioRxiv 248476. https://doi.org/10.1101/248476

Esch, T., Heldens, W., Hirner, A., Keil, M., Marconcini, M., Roth, A., Zeidler, J., Dech, S., Strano, E. (2017): Breaking new ground in mapping human settlements from space – The Global Urban Footprint. ISPRS Journal of Photogrammetry and Remote Sensing 134 (2017) 30-42. https://doi.org/10.1016/j.isprsjprs.2017.10.012

Esch, T., Schenk, A., Ullmann, T., Thiel, M., Roth, A., Dech, S. (2011): Characterization of Land Cover Types in TerraSAR-X Images by Combined Analysis of Speckle Statistics and Intensity Information. IEEE Transactions on Geoscience and Remote Sensing, Volume 49, Issue 6, pp. 1911-1925. https://doi.org/10.1109/TGRS.2010.2091644.

Huffman, G. J., Adler, R. F., Bolvin, D. T. & Nelkin, E. J. (2010), The TRMM
multi-satellite precipitation analysis (TMPA), in M. Gebremichael & F. Hossain,
eds, ‘Satellite Rainfall Applications for Surface Hydrology’, Springer Netherlands,
pp. 3–22.

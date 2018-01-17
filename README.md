# CATI model for Cholera epidemics

This repository contains the data used in the following article:

__The potential impact of case-area targeted interventions in response to cholera outbreaks: A modeling study__

## Data

The folder `data` contains the following files:

- `data/casedata/locationOffset.csv` contains the xy-coordinates and dates of reported case households. The coordinates are in meters. A random offset has been added to each set of coordinates to make it impossible to identify household locations. The relative location of households, necessary to compute the tau-statistics, is preserved.
- `data/casedata/epicurve.csv` contains the number of reported cases per day.
- `data/districts_ndjamena/tcd_polbnd_adm9_a_osm_170206.shp` contains the boundaries of the districts as used for the district-targeted mass campaigns. This data has been obtained from OpenStreetMap ([© OpenStreetMap contributors](https://www.openstreetmap.org/copyright)).
- 

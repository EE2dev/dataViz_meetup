# Covid-19 in Bavaria
Data about the spread of the corona virus in Bavaria

## Data

### 1.1 Sources
The original data sources for the data are:

- https://www.stmgp.bayern.de/
- https://www.lgl.bayern.de/gesundheit/infektionsschutz/infektionskrankheiten_a_z/coronavirus/karte_coronavirus/index.htm
- http://opendatalab.de/projects/geojson-utilities/
- https://de.wikipedia.org/wiki/Liste_der_Landkreise_und_kreisfreien_St%C3%A4dte_in_Bayern
- https://de.wikipedia.org/wiki/COVID-19-F%C3%A4lle_in_Deutschland

### 1.2 Data description

#### corona_bavaria_daily_infected.csv
The data file has been manually created and collected from the Bayerisches Landesamt für Gesundheit und Lebensmittelsicherheit (LGL) which is the official source for reporting Covid-19 cases in the state of Bavaria. Each row corresponds to one day, each column represents a *Landkreis* or a *kreisfreie Stadt* in Bavaria. Each value depicts the published number of infected people in that *Landkreis*. 
The data does not reflect the ground truth and can just be used as an indication due to several fundamental properties:
- it just contains the subset of infected people which are tested and their test has been transmitted to the LGL.
- the number of infected people are counted from day 1. It does not represent the number of infected people on a particular day since the people recovering are (typically) not subtracted.
- this dataset is updated regularly (augmented by new cases)

#### landkreise_simplify200.geojson
This file contains the shapes of each *Landkreis* and *kreisfreie Stadt* in GeoJSON as well as some statistics from destatis from http://opendatalab.de/projects/geojson-utilities/. Additional statistics and regional information has been added from wikipedia. 


### Potential future data sources (not used yet)

- https://www.divi.de/register/kartenansicht


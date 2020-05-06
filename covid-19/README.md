# Covid-19 in Bavaria
Data about the spread of the corona virus in Bavaria.

Link to an observable notebook based on this data:
- https://observablehq.com/@ee2dev/coronavirus-in-bayern/2

## Data

### 1.1 Sources
The original data sources for the data are:

- https://www.stmgp.bayern.de/
- https://www.lgl.bayern.de/gesundheit/infektionsschutz/infektionskrankheiten_a_z/coronavirus/karte_coronavirus/index.htm
- http://opendatalab.de/projects/geojson-utilities/
- https://de.wikipedia.org/wiki/Liste_der_Landkreise_und_kreisfreien_St%C3%A4dte_in_Bayern
- https://de.wikipedia.org/wiki/COVID-19-F%C3%A4lle_in_Deutschland
- https://www.statistik.bayern.de/statistik/index.html

### 1.2 Data description

#### corona_bavaria_daily_infected.csv
The data file has been manually created and collected from the Bayerisches Landesamt für Gesundheit und Lebensmittelsicherheit (LGL) which is the official source for reporting Covid-19 cases in the state of Bavaria. Each row corresponds to one day starting with January 27th, 2020. The first column **Datum** is a date (string) in the format ("27.1.2020"). The second column **_gesamt** ist the total count of cases per day. The third column **_unbekannt** are cases which could not be assigned to a district by the LGL. Each column (from column 4 onwards) represents a district (*Landkreis* or a *kreisfreie Stadt*) in Bavaria. Each value depicts the published number of infected people in that *Landkreis*. The separator is a "," (comma).

Note:
- the data does not reflect the ground truth and can just be used as an indication
- it just contains the subset of infected people which are tested and their test has been transmitted to the LGL.
- the number of infected people are counted from day 1. It does not represent the number of infected people on a particular day since the people recovering are (typically) not subtracted.
- this dataset is updated regularly (augmented by new cases)

Sample view:

| Datum        | _gesamt          | _unbekannt  | Aichach-Friedberg	| Altötting  | ....|
| ------------- |:-------------:| -----:| ------------- |:-------------:| -----:|
| "27.1.2020"     | 1 | 0 |0 | 0 |... | 
| "28.1.2020"     | 4 | 0 |0 | 0 |... | 
| "29.1.2020"     | 4 | 0 |0 | 0 |... | 
| ...     | ... |... |... |... |... | 

#### corona_bavaria_daily_fatalities.csv
The data file has been manually collected from the Bayerisches Landesamt für Gesundheit und Lebensmittelsicherheit (LGL) which is the official source for reporting Covid-19 cases in the state of Bavaria. Each row corresponds to one day starting with March 25th, 2020 which is the first day, the LGL published corona related fatalities. The first column **Datum** is a date (string) in the format ("25.3.2020"). The second column **_gesamt** ist the total count of cases per day. The third column **_unbekannt** are cases which could not be assigned to a district by the LGL. Each column (from column 4 onwards) represents a district (*Landkreis* or a *kreisfreie Stadt*) in Bavaria. Each value depicts the published number of fatalities in that *Landkreis*. The separator is a "," (comma).

Note:
- limited testing and challenges in the attribution of the cause of death means that the number of confirmed deaths may not be an accurate count of the true number of deaths from COVID-19
- in few cases the number of deaths go down from one day to the other. Presumably, this happens mainly when a case has been assigned to the wrong *Landkreis* or *kreisfreie Stadt* before. Alternatively, a correction took place.
- this dataset is updated regularly (augmented by new cases)

Sample view:

| Datum        | _gesamt          | _unbekannt  | Aichach-Friedberg	| Altötting  | ....|
| ------------- |:-------------:| -----:| ------------- |:-------------:| -----:|
| "25.3.2020"     | 41 | 0 |0 | 0 |...| 
| "26.3.2020"     | 52 | 0 |0 | 0 |...| 
| "27.3.2020"     | 59 | 0 |0 | 0 |...| 
| ...     | ... |... |... |... |... | 

#### landkreise_simplify200.geojson
This file contains the shapes of each *Landkreis* and *kreisfreie Stadt* in GeoJSON as well as some statistics from destatis from http://opendatalab.de/projects/geojson-utilities/. 
<br><br>
Additional statistics and regional information has been added from wikipedia: For each object of the feature Array the following is added:

- properties.wiki.png
- properties.wiki.svg
- properties.wiki.link
- properties.wiki.Landkreis
- properties.wiki.Landkreis_wiki
- properties.wiki.Kreisstadt
- properties.wiki.groesste_Gemeinde
- properties.wiki.Regierungsbezirk
- properties.wiki.KFZ 
- properties.wiki.Einwohner
- properties.wiki.Flaeche
<br><br>
Also a centroid in [Lat, Long] format is added to each geometry object. For MultiPolygon the centroid is calculated from the first Polygon (irrespective of holes)

### Potential future data sources (not used yet)

- https://npgeo-corona-npgeo-de.hub.arcgis.com/
- https://www.divi.de/register/kartenansicht
- https://statistik.arbeitsagentur.de/Navigation/Statistik/Statistik-nach-Regionen/Politische-Gebietsstruktur/Bayern-Nav.html
- https://www.statistikportal.de/de/corona


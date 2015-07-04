# AAFB-CRB-Damage-Survey
# Notes

These notes describe mapping of the AAFB CRB survey data. All files associated with the mapping project are available on [GitHub](https://github.com/aubreymoore/AAFB-CRB-Damage-Survey).

## QGIS Map
The free, open-source Quantum GIS v2.8.1 was used to map damage levels for trees included in the survey:

* All survey data were downloaded from the Epicollect+ database as a CSV file.

* The CSV file was imported as a vector layer (Layer > Add layer > Add delimited text layer)

* Points outside of AAFB were excluded from analysis (Vector > Analysis tools > Points in polygon)

* Rules were developed to categorize points based on observations recorded in the attribute table. Colored placemark icons were used to visualize point categories.

* The resulting map was exported as a [PDF]( https://github.com/aubreymoore/AAFB-CRB-Damage-Survey/blob/master/AAFB-CRB-Damage-May2015.pdf ).

![map](https://github.com/aubreymoore/AAFB-CRB-Damage-Survey/blob/master/AAFB-CRB-Damage-May2015.pdf)

## Google Earth Map
Unfortunately, with the current version v2.8.1, all styling is lost when exporting point layers to KML or KMZ files. As a work around, an [IPython notebook]( https://github.com/aubreymoore/AAFB-CRB-Damage-Survey/blob/master/make-kml.ipynb ) was developed to do the job :

* In QGIS, the tree point layer was saved as an SQLite database.

* The Ipython notebook reads the database and writes a [KMZ file]( https://github.com/aubreymoore/AAFB-CRB-Damage-Survey/blob/master/aafb-crb-damage.kmz ) containing color-coded points for display using Google Earth .

## GIS Data Sources

GIS polygons are for from [DOD land in northern Guam](http://north.hydroguam.net/map-infrastructure-military-areas.php).
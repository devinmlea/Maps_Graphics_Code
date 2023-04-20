###########################################################
###########################################################

Flood Risk vs. Policies Bivariate Map Data README
Author: Devin Lea


I am providing this quick README to accompany the
"FloodRisk_VsPolcies_BivariateMapData.csv" file that was used
to produce my week 7 (Bivariate Map) 2023 Map Prompt Monday
map to help you understand what data are contained in
each column. I provide the data as is without any guarantees
to data quality beyond what I describe in my acompanying
"US_FloodRisk_VsCoverage_BivariateMap_ProjNotes.txt" file



###########################################################

Column names and quick description of the data they contain

FIPS: This is a unique five number code used for all US counties
and county equivalents.

NumBlds: This was the number of buildings footprints that had their
center point of the polygon within the county. This data was from
a 2018 version of the Microsoft US Building Footprints

BldsSFHA: The number of buildings per county that intersected the
Special Flood Hazard Area on National Flood Insurance Rate Maps.
This flood map data is from 2018.

BldsPctSFHA: The percentage calculated by dividing the number of
buildings in the SFHA by the number of buildings in the county and
then multiplying by 100.

Place: Provides the county name and state

Policies: The number of flood insurance policies in force in the
county as of November 30, 2022.

PctPolicies: The percentage calculated by dividing the number
of policies by the number of buildings in the county and multiplying
by 100

PctDiff: The difference between PctPolicies and BldsPctSFHA columns.
Positive numbers meant that PctPolicies > BldsPctSFHA
Negative numbers meant that PctPolicies < BldsPctSFHA

Var1Class
Determined by PctDiff column
Assigned "A" if pct diff where polcies > SFHA buildings exceeded 5%
Assigned "B" if pct diff between policies and SFHA buildings was between 5% and -5%
Assigned "C" if pct diff where SFHA buildings > policies exceeded 5% (i.e., was less than -5%)

Var2Class
Determined by BldsSFHA column
Assigned "1" if number of buildings in SFHA > 10,000
Assigned "2" if number of buildings was > 1,000 and < 10,000
Assigned "3" if number of buildings was < 1,000

VarClass
Concatination of Var1Class and Var2Class to create the unique 9 classes
used to create the Bivariate map
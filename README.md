# streetsofnyc
MADS Milestone 1 - Sheila/Moutaz/Stuart

Created a Data Processing Workflow for Streets of NYC
The output of the workflow will produce a database with the following tables inside:

1. tickets - 2020/2019 tickets data for those that can be matched to street seg
2. LION - Street details for NYC (exlcuding geometry)
3. cd_demographics - demographic data by community district
4. weather - from Moutaz pickle
5. collision - 2020/2019 collision data form Sheila csv
6. LION_dem - table joined for demographic data to streets by CD
7. ticketstreetdem - table that joins street codes/house number to lion_dem to get matching segment (for use in data analysis)
8. collisionstreetdem - table that joins each collision to lion_dem to get matching segment (for use in data analysis)

Run files as follows to reproduce:
1. Data Preprocessing - Tickets.ipynb
2. Data Cleaning - Tickets.ipynb
3. Data Cleaning - Other Datasets.ipynb (new)

Output: streetsofnyc.db

See: Ticket Data Analysis.ipynb(new) for examples of how to query to do analysis

Created geospatial database to run KNN analysis - see get_segment_latlong.ipynb for full details
of how we created a geospatial database in SQLITE and ran a KNN analysis on multiple points using the spatialite extension

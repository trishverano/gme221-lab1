# GmE 221 - Laboratory Exercise 1

## Overview
This laboratory sets up a spatial analysis environment using Python and PostGIS and performs a parcel-landuse overlay analysis.

## Environment Setup
-Python 3.14
-PostgreSQL with PostGIS
-GeoPandas, SQLAlchemy, psycopg2

## How to Run
1. Activate the virtual environment 
2. Run `main.py` to test the database connection 
3. Run `overlay.py` to compute landuse percentages 
## Outputs - PostGIS table: `parcel_landuse_percentage` - Visualization in QGIS 

## Reflection 1
In this lab, I started by setting up the PostGIS database and restoring the spatial data so it could be used for analysis. After that, I created a virtual environment in VS Code and installed the required Python libraries to make sure everything runs properly and consistently. I then connected Python to the database and tested if I could successfully load the parcel data.

For the main task, I performed an overlay analysis between parcels and land use using PostGIS functions. The database handled the spatial intersection and area calculation, while Python helped organize the workflow and compute the land-use percentages. After storing the results back into PostGIS, I opened them in QGIS to check if the outputs made sense visually and numerically.

Overall, this lab helped me understand that spatial analysis is a step-by-step process. It involves setting up the environment, connecting systems, running spatial operations, and interpreting the results — not just making maps.
 ## Reflection 2
In this part of the lab, I focused on performing the actual spatial overlay and computing the land-use percentages per parcel. I used a spatial query with ST_Intersection in PostGIS to determine where parcels and land-use polygons overlap. The database computed the intersection geometries and their areas, and then I used Python to calculate the percentage of each land-use type within every parcel.

After writing the results back to the database, I loaded the new table into QGIS to visually inspect the output. Seeing the percentages displayed on the map helped me check whether the results were reasonable based on the parcel shapes and land-use patterns.

This part made me realize that overlay analysis is more than just layering two maps. It involves clear computational steps — identifying intersections, calculating areas, and deriving percentages — before any visualization happens.
 
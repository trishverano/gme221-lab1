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

## Reflection
The successful database connection demonstrates that Python is functioning as an analytical controller rather than a standalone GIS tool. By connecting to a PostGIS-enabled PostgreSQL database, Python is able to issue spatial queries, retrieve geometry-aware results, and interact directly with spatial data stored in the database. In this workflow, PostGIS performs the core spatial computations using database-level GIS algorithms, while Python orchestrates the analysis, integrates results into GeoDataFrames, and manages the overall analytical process. This confirms that spatial computation is distributed across systems, with Python providing workflow logic and PostGIS providing robust, scalable spatial processing.
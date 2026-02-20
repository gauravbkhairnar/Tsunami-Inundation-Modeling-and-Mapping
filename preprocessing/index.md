# Merging of Bathymetry and Topography data 

The objective of this exercise is to interpolate Bathymetry and topography. The output of this will be input as **C grid** in ComMIT model.

Data inputs:
1. Bathymetry gridded raster or points data
2. Topography (Digital Elevation Model- DEM)

Here as a test case we are using GEBCO bathymetry and SRTM topography data

> **__Important Note:__**
> Both data should be in same coordinate system (WGS 84: EPSG:4326)

If data is not in WGS84:EPSG:4326 coordinate reference system then **Reprojection** is required

## Reprojection:
Go to ‘**Raster**’ tab → **Projections** → **Warp (reprojection)**
<br></br>
<img width="1079" height="772" alt="image" src="https://github.com/user-attachments/assets/671a2171-9cfe-4dcd-8619-e654a90d2c3b" />

Input layer → Select your raster layer
Taeget CRS → click on glob icon → drop down ‘No CRS (or unknown/ non-Earth projection) → select ‘Predefined CRS’ → in filter search ‘4326’ → Go to “Coordinate Reference System” tab and select ‘WGS84’ →<img width="35" height="37" alt="image" src="https://github.com/user-attachments/assets/a1102a5c-18f9-49e2-8e1f-28646ca28e31" />

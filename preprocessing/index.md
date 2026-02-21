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
<img width="100%" alt="image" src="https://github.com/user-attachments/assets/671a2171-9cfe-4dcd-8619-e654a90d2c3b" />

Input layer → Select your raster layer
Taeget CRS → click on glob icon <img width="35" height="37" alt="image" src="https://github.com/user-attachments/assets/a1102a5c-18f9-49e2-8e1f-28646ca28e31" />
 → drop down ‘No CRS (or unknown/ non-Earth projection) → select ‘Predefined CRS’ → in filter search ‘4326’ → Go to “Coordinate Reference System” tab and select ‘WGS84’ 


 click back by clicking <img width="37" height="35" alt="image" src="https://github.com/user-attachments/assets/a984728c-2655-4ff5-936b-10f70ede3a0c" /> this icon → scoll down and save the reprojected file by clicking ‘save to file tab’. → Click “Run”
 <img width="682" height="660" alt="image" src="https://github.com/user-attachments/assets/e8755035-78b1-4c87-90f5-ee238fa3743c" />
 <img width="676" height="648" alt="image" src="https://github.com/user-attachments/assets/cc33e32c-d71b-4231-9d9a-d7a5f9627105" />
 <img width="956" height="342" alt="image" src="https://github.com/user-attachments/assets/56586003-fa3e-40a5-bad5-9832ec5697a8" />
 <img width="959" height="928" alt="image" src="https://github.com/user-attachments/assets/36074c6d-143f-4a4b-910c-08292e46f466" />
 <img width="691" height="927" alt="image" src="https://github.com/user-attachments/assets/ba69ecd4-1f09-435a-9cd5-a3e1a81ad6bb" />




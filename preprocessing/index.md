<h1 style="text-align:center; margin-top:30px; margin-bottom:30px;">
            Merging of Bathymetry and Topography data 
</h1>

<div style="max-width:1400px; margin:0 auto; padding:0 10px;">
<h3>Objective</h3>
<p>          
The objective of this exercise is to interpolate bathymetry and topography datasets 
to generate a continuous elevation surface. The resulting raster will serve as the 
<strong>C-grid input</strong> for the ComMIT tsunami model.
</p>

<h3>Data Inputs</h3>

<ol>
<li>Bathymetry (gridded raster or point data)</li>
<li>Topography (Digital Elevation Model – DEM)</li>
</ol>


<p>
For demonstration purposes, this workflow utilizes 
<strong>GEBCO bathymetry</strong> and 
<strong>SRTM topography</strong> datasets.
</p>


<div style="background-color:#f57c00; 
            border-left:6px solid #fff8e1; 
            padding:14px 18px; 
            margin:25px 0;
            border-radius:6px;
            max-width:800px;">

<strong>Important:</strong><br>
If bathymetry and topography data are already available in point shapefile format, 
skip Steps 1 and 2.

</div>


 

## 1. Add Layer into QGIS
### If Bathymetry and Topography data is in raster format:
Layer --> Add Layer --> Add Raster Layer.. 
<img width="932" height="715" alt="image" src="https://github.com/user-attachments/assets/2990940a-e9aa-423f-80e3-2de9dfa7172b" style="border:1px solid #ccc; padding:4px;" />


<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:12px; 
            margin:15px 0;">
<strong>Important Note:</strong><br>
Both data should be in same coordinate system (WGS 84: EPSG:4326)
</div>

## 2. Reprojection:
If your Bathymetry and Topography layers are already in WGS 84: EPSG:4326, then ignore this step
Go to ‘**Raster**’ tab → **Projections** → **Warp (reprojection)**
<br> 
<img width="100%" alt="image" src="https://github.com/user-attachments/assets/671a2171-9cfe-4dcd-8619-e654a90d2c3b" style="border:1px solid #ccc; padding:4px;" />

Input layer → Select your raster layer
Taeget CRS → click on glob icon <img width="35" height="37" alt="image" src="https://github.com/user-attachments/assets/a1102a5c-18f9-49e2-8e1f-28646ca28e31" />
 → drop down ‘No CRS (or unknown/ non-Earth projection) → select ‘Predefined CRS’ → in filter search ‘4326’ → Go to “Coordinate Reference System” tab and select ‘WGS84’ 


 click back by clicking <img width="37" height="35" alt="image" src="https://github.com/user-attachments/assets/a984728c-2655-4ff5-936b-10f70ede3a0c" /> this icon → scoll down and save the reprojected file by clicking ‘save to file tab’. → Click “Run”
 <div style="text-align:center;">
 <img width="100%" alt="image" src="https://github.com/user-attachments/assets/e8755035-78b1-4c87-90f5-ee238fa3743c" style="border:1px solid #ccc; padding:4px;"/>
 </div>
 
 <br>

  <div style="text-align:center;">
 <img width="100%" alt="image" src="https://github.com/user-attachments/assets/cc33e32c-d71b-4231-9d9a-d7a5f9627105" style="border:1px solid #ccc; padding:4px;" />
  </div>
  
  <br>

 <div>
 <img width="100%" height="342" alt="image" src="https://github.com/user-attachments/assets/56586003-fa3e-40a5-bad5-9832ec5697a8" style="border:1px solid #ccc; padding:4px;" />
 </div>
 
 <br>
 
 <div>
  <img width="100%" height="928" alt="image" src="https://github.com/user-attachments/assets/36074c6d-143f-4a4b-910c-08292e46f466" style="border:1px solid #ccc; padding:4px;"/>
 </div>
 
  <br>

 <div>
 <img width="100%" height="927" alt="image" src="https://github.com/user-attachments/assets/ba69ecd4-1f09-435a-9cd5-a3e1a81ad6bb" style="border:1px solid #ccc; padding:4px;"/>
</div>


</div>
<br>

 


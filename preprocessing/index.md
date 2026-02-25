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
            color:white;
            border-radius:6px;
            max-width:800px;text-align:center;">

<strong>Important:</strong><br>
If bathymetry and topography data are already available in point shapefile format, 
skip Steps 1 and 2.
</div>


 

<h2>1. Add Layer into QGIS</h2>
If Bathymetry and Topography data is in raster format:<br>
Layer --> Add Layer --> Add Raster Layer.. <br>
<br>
<div style="text-align:center;">
<img width="932" height="715" alt="image" src="https://github.com/user-attachments/assets/2990940a-e9aa-423f-80e3-2de9dfa7172b" style="border:1px solid #ccc; padding:4px;" />
</div>
<br>


<div style="background-color:#f57c00; 
            border-left:6px solid #fff8e1; 
            padding:14px 18px; 
            color:white;
            margin:25px 0;
            border-radius:6px;
            max-width:800px;text-align:center;">

<strong>Important:</strong><br>
If bathymetry and topography data are already available in point shapefile format, 
skip Steps 1 and 2.
</div>


<br>

<h2>2. Reprojection:</h2>
<p>
If your Bathymetry and Topography layers are already in WGS 84: EPSG:4326, then ignore this step.<br>
Go to Raster tab → Projections→ Warp (reprojection)</p>
<br> 
<div style="text-align:center;">
<img  width="632" height="515"  alt="image" src="https://github.com/user-attachments/assets/671a2171-9cfe-4dcd-8619-e654a90d2c3b" style="border:1px solid #ccc; padding:4px;" />
</div>
<br>
Input layer → Select your raster layer
Taeget CRS → click on glob icon <img width="35" height="37" alt="image" src="https://github.com/user-attachments/assets/a1102a5c-18f9-49e2-8e1f-28646ca28e31" />
 → drop down ‘No CRS (or unknown/ non-Earth projection) → select ‘Predefined CRS’ → in filter search ‘4326’ → Go to “Coordinate Reference System” tab and select ‘WGS84’ 


 click back by clicking <img width="37" height="35" alt="image" src="https://github.com/user-attachments/assets/a984728c-2655-4ff5-936b-10f70ede3a0c" /> this icon → scoll down and save the reprojected file by clicking ‘save to file tab’. → Click “Run”
 <br>
 <div style="text-align:center;">
<img width="688" height="552" alt="Screenshot 2026-02-25 171040" src="https://github.com/user-attachments/assets/f5dfaf8d-f233-4b17-80c8-74f7ff94931b" style="border:1px solid #ccc; padding:4px;"/>
</div>
<br>

<div style="text-align:center;">
<img width="690" height="555" alt="Screenshot 2026-02-25 171715" src="https://github.com/user-attachments/assets/d2ad49d6-95a0-40fd-89d9-b7235818876d" style="border:1px solid #ccc; padding:4px;" />
 </div>
  
  <br>

 <div>
<img width="690" height="555" alt="Screenshot 2026-02-25 171911" src="https://github.com/user-attachments/assets/991d8001-e600-47c2-81d4-8ebc0e7968c3" style="border:1px solid #ccc; padding:4px;" />
 </div>
 
 <br>
 
 <div>
<img width="690" height="555" alt="Screenshot 2026-02-25 172129" src="https://github.com/user-attachments/assets/09762ba8-3235-4c41-acc6-05f45cd01e01" style="border:1px solid #ccc; padding:4px;"/>

 </div>
 
  <br>

 <div>
<img width="690" height="555" alt="Screenshot 2026-02-25 172541" src="https://github.com/user-attachments/assets/8d8df2a9-23f4-46e3-ac82-c7200f4a3a77" style="border:1px solid #ccc; padding:4px;"/>

</div>


</div>
<br>

 


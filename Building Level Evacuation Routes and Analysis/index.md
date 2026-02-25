<!DOCTYPE html>
<html>
<head>
<title>Building Level Evacuation Routes and Analysis</title>
</head>

<body style="font-family: Arial, sans-serif; line-height:1.6; margin:40px;">

<h1 style="text-align:center;">Building-Level Evacuation Routes and Analysis</h1>

<p>
This stage of the workflow focuses on preparing building footprint data and integrating it into QGIS 
for building-level evacuation route analysis.
</p>

<h2>Sections Covered</h2>
<ol>
<li>Downloading Building Footprints</li>
<li>Installing Required QGIS Plugin</li>
<li>Building-Level Evacuation Analysis</li>
</ol>

<hr>

<h2>1. Downloading Building Footprints (Open Buildings V3)</h2>

<p>
The Open Buildings V3 dataset contains <strong>1.8 billion building detections</strong> across an inference area of 
<strong>58 million km²</strong>, covering Africa, South Asia, South-East Asia, Latin America, and the Caribbean.
</p>

<p>
Building footprint data derived from the Google Open Buildings dataset (v3), © Google, licensed under CC BY 4.0.
</p>

<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:15px; 
            margin:20px 0; 
            border-radius:6px;">

<strong>Important Notes Regarding Open Buildings Dataset:</strong>
<ul>
<li>AI-derived dataset</li>
<li>May miss small or rural structures</li>
<li>Includes confidence scores</li>
<li>Should NOT be treated as cadastral or legal boundary data</li>
</ul>
</div>

<p>
Google Open Building Data is available at:
<br>
<a href="https://sites.research.google/gr/open-buildings/" target="_blank">
https://sites.research.google/gr/open-buildings/
</a>
</p>

<br>

<img src="https://github.com/user-attachments/assets/94822bf2-cd6d-429e-87ec-6e5819c4d68f" width="900">

<br><br>

<p>
Click on the <strong>"Download here"</strong> button.
You can search your Area of Interest (AOI) or zoom into your area and select the required tile.
</p>

<br>

<img src="https://github.com/user-attachments/assets/5703cc5d-42a1-480b-8c25-2fb562459964" width="900">

<br><br>

<p>
Download the file named: <strong>xxx_buildings.csv.gz</strong><br>
After downloading, extract the file to obtain the CSV file.
</p>

<hr>

<h2>2. Adding Building Data into QGIS</h2>

<h3>Step 1: Open QGIS</h3>
<p>Launch QGIS software.</p>

<h3>Step 2: Add Delimited Text Layer</h3>
<p>
Go to:<br>
<strong>Layer → Add Layer → Add Delimited Text Layer</strong>
</p>

<br>

<img src="https://github.com/user-attachments/assets/bcb68d61-d37c-48fc-8bce-acbf0136eae7" width="900">

<br><br>

<h3>Step 3: Configure Layer Settings</h3>

<ul>
<li>Select the extracted CSV file</li>
<li>Under <strong>Geometry Definition</strong>, choose <strong>Well Known Text (WKT)</strong></li>
<li>Select <strong>geometry</strong> in Geometry field</li>
<li>Set Geometry CRS to <strong>EPSG:4326 – WGS84</strong></li>
<li>Click <strong>Add</strong></li>
</ul>

<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:15px; 
            margin:20px 0; 
            border-radius:6px;">

<strong>Note:</strong><br><br>
This step may take considerable time as the dataset may contain more than 10 million building footprints.
</div>

<br>

<img src="https://github.com/user-attachments/assets/ea6ea5dd-b2f3-41e2-91d9-c4eb6a4a4b05" width="900">

<hr>

<h2>3. Selecting Area of Interest (AOI)</h2>

<p>
After the dataset is successfully loaded:
</p>

<ol>
<li>Activate the <strong>Select Features Tool</strong></li>
<li>Draw a polygon over your Area of Interest</li>
</ol>

<br>

<img src="https://github.com/user-attachments/assets/7c5b5324-db1b-42d7-89ea-b18a718b1889" width="900">

<hr>

<h2>4. Export Selected Buildings</h2>

<ol>
<li>Right-click the building layer in the Layer Panel</li>
<li>Select <strong>Export → Export Selected Features As</strong></li>
<li>Save the file as <strong>Shapefile (.shp)</strong></li>
</ol>

<br>

<img src="https://github.com/user-attachments/assets/7589ee86-00f8-496c-9e7d-66811d00fff2" width="900">

<br><br>

<img src="https://github.com/user-attachments/assets/d554e356-c16a-4606-81cc-a7a17719c05d" width="900">

<hr>

<h2>Reference</h2>

<p>
Sirko, W., Kashubin, S., Ritter, M., Annkah, A., Bouchareb, Y.S.E., Dauphin, Y., 
Keysers, D., Neumann, M., Cisse, M., & Quinn, J.A. (2021). 
<i>Continental-scale building detection from high resolution satellite imagery.</i> 
arXiv:2107.12283.
</p>

</body>
</html>

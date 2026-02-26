<div style="max-width:1400px; 
            margin:40px auto; 
            padding:0 30px; 
            font-family:Arial, sans-serif; 
            line-height:1.7;">

<h1 style="text-align:center; margin-bottom:30px;">
Building-Level Evacuation Routes and Analysis
</h1>

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

<hr style="margin:30px 0;">

<h2>1. Downloading Building Footprints (Open Buildings V3)</h2>

<p>
The Open Buildings V3 dataset contains <strong>1.8 billion building detections</strong> across 
an inference area of <strong>58 million km²</strong>, covering Africa, South Asia, 
South-East Asia, Latin America, and the Caribbean.
</p>

<p>
Building footprint data derived from the Google Open Buildings dataset (v3), © Google, 
licensed under CC BY 4.0.
</p>

<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:15px; 
            margin:25px 0; 
            border-radius:6px;">

<strong>Important Notes Regarding Open Buildings Dataset:</strong>
<ul style="margin-top:10px;">
<li>AI-derived dataset</li>
<li>May miss small or rural structures</li>
<li>Includes confidence scores</li>
<li>Should NOT be treated as cadastral or legal boundary data</li>
</ul>
</div>

<h2>1.1 Downloading </h2>
<p>
Google Open Building Data is available at:<br>
<a href="https://sites.research.google/gr/open-buildings/" target="_blank">
https://sites.research.google/gr/open-buildings/
</a>
</p>

<br>

<div style="text-align:center;">
<img src="https://github.com/user-attachments/assets/94822bf2-cd6d-429e-87ec-6e5819c4d68f" width="100%">
</div>

<br><br>

<p>
Click on the <strong>"Download here"</strong> button.  
You can search your Area of Interest (AOI) or zoom into your area and select the required tile.
</p>

<br>

<div style="text-align:center;">
<img src="https://github.com/user-attachments/assets/5703cc5d-42a1-480b-8c25-2fb562459964" width="100%">
</div>

<br><br>

<p>
Download the file named: <strong>xxx_buildings.csv.gz</strong><br>
After downloading, extract the file to obtain the CSV file.
</p>

<hr style="margin:30px 0;">

<h2>1.2 Adding Building Data into QGIS</h2>

<p><strong>(i)</strong> Open QGIS.</p>

<p><strong>(ii)</strong> Navigate to:</p>
<p><strong>Layer → Add Layer → Add Delimited Text Layer</strong></p>

<br>

<div style="text-align:center;">
<img src="https://github.com/user-attachments/assets/bcb68d61-d37c-48fc-8bce-acbf0136eae7" width="100%">
</div>

<br><br>

<p><strong>(iii)</strong> Configure Layer Settings:</p>

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
            margin:25px 0; 
            border-radius:6px;">

<strong>Note:</strong><br><br>
This step may take considerable time as the dataset may contain more than 10 million building footprints.
</div>

<br>

<div style="text-align:center;">
<img src="https://github.com/user-attachments/assets/ea6ea5dd-b2f3-41e2-91d9-c4eb6a4a4b05" width="100%">
</div>

<hr style="margin:30px 0;">

<h2>1.3 Selecting Area of Interest (AOI)</h2>

<ol>
<li>Activate the <strong>Select Features Tool</strong></li>
<li>Draw a polygon over your Area of Interest</li>
</ol>

<br>

<div style="text-align:center;">
<img src="https://github.com/user-attachments/assets/7c5b5324-db1b-42d7-89ea-b18a718b1889" width="100%">
</div>

<hr style="margin:30px 0;">

<h2>1.4 Export Selected Buildings</h2>

<ol>
<li>Right-click the building layer in the Layer Panel</li>
<li>Select <strong>Export → Export Selected Features As</strong></li>
<li>Save the file as <strong>Shapefile (.shp)</strong></li>
</ol>

<br>

<div style="text-align:center;">
<img src="https://github.com/user-attachments/assets/7589ee86-00f8-496c-9e7d-66811d00fff2" width="100%">
</div>

<br><br>

<div style="text-align:center;">
<img src="https://github.com/user-attachments/assets/d554e356-c16a-4606-81cc-a7a17719c05d" width="100%">
</div>

<h2>2. Installing Required QGIS Plugin</h2>

<p>
We will install <strong>Build_Short_Evac_Time</strong>, a QGIS plugin designed to automatically 
identify buildings requiring evacuation within a tsunami-affected area and generate 
the shortest evacuation routes to designated safe shelters using minimal user input.
</p>

<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:15px; 
            margin:25px 0; 
            border-radius:6px;">
<strong>This plugin requires prerequisites. Please complete the following steps before installing the plugin.</strong>
</div>

<h3>2.1 Installing Prerequisites</h3>

<p><strong>(i)</strong> Download the <strong><a href="https://indiannational-my.sharepoint.com/:t:/g/personal/gb_khairnar-p_incois_gov_in/IQAjMkcNdlQUT6O7jB9G4z1FAdqugvRDl9Xh44rVVSDPzgY?e=o2PuOq" target="_blank">
requirements.txt</a></strong> file.</p>


<p><strong>(ii) </strong>Installation:</p>

<p><strong>For Windows:</strong></p>
<ul>
<li>Copy the <strong>requirements.txt</strong> file path</li>
<li>Open <strong>Start → OSGeo4W Shell</strong></li>
<li>Navigate to the file location using:<br>
<code>cd &lt;paste file path&gt;</code></li>
<li>Run the following command:</li>
</ul>

<pre style="background:#f4f4f4; padding:10px; border-radius:5px;">
pip install -r requirements.txt
</pre>

<p><strong>For Linux:</strong></p>
<ul>
<li>Open Terminal</li>
<li>Navigate to the file location:<br>
<code>cd &lt;requirements file path&gt;</code></li>
<li>Run:</li>
</ul>

<pre style="background:#f4f4f4; padding:10px; border-radius:5px;">
python3 -m pip install --user -r requirements.txt
</pre>

<p><strong>(iii)</strong> Restart QGIS after installation.</p>

<hr style="margin:30px 0;">

<h3>2.2 Installing the Plugin</h3>

<p>
Open QGIS → <strong>Plugins → Manage and Install Plugins</strong> → 
Select the <strong>"All"</strong> tab → Search for 
<strong>Build_Short_Evac_Time</strong> → Install the plugin.
</p>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/b6752b5c-9409-470f-b87d-6001830c2f62" width="70%">
</div>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/1e94340f-7866-44f9-b0d9-c6acdbd32538" width="90%">
</div>

<h4>Input Requirements</h4>

<p>The first three datasets must be vector layers in one of the following supported formats:</p>

<ul>
<li>Shapefile (.shp)</li>
<li>GeoJSON (.geojson)</li>
</ul>

<p>The optional Digital Elevation Model (DEM) must be in <strong>.tif</strong> format.</p>

<p><strong>Required Layers:</strong></p>

<ol>
<li><strong>Building Layer</strong> (Geometry: Polygon)</li>
<li><strong>Evacuation Shelters Layer</strong> (Geometry: Point)</li>
<li><strong>Flood Inundation Layer</strong> (Geometry: Polygon)</li>
<li><strong>(Optional)</strong> Digital Elevation Model (Raster: TIFF)</li>
</ol>

<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:15px; 
            margin:25px 0; 
            border-radius:6px;">
<strong>Important Note:</strong>
All input layers must be projected in <strong>EPSG:4326 (WGS 84)</strong> 
to ensure correct spatial analysis and routing.
</div>

<hr style="margin:30px 0;">

<h2>3. Building-Level Evacuation Analysis</h2>

<p>
After successful installation, navigate to:
<strong>QGIS → Plugins → Build_Short_Evac_Time → Build Shortest Evacuation Time</strong>.
</p>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/c3c645a9-41c0-4c68-b608-c3ed63877e4a" width="90%">
</div>

<h3>(i) Select Input Layers</h3>

<ul>
<li>If the Building, Evacuation Shelter, and Flood Inundation layers are already loaded in the QGIS Layers Panel, select them using the dropdown menus.</li>
<li>Alternatively, use the <strong>Browse</strong> buttons to select input layers directly from disk.</li>
<li>Uploading DEM is optional. If provided, terrain slope will be incorporated into walking time calculation for more realistic results. If not provided, terrain is assumed to be flat.</li>
</ul>

<h3>(ii) Select Output Folder (Optional)</h3>

<ul>
<li>Specify an output folder to save results.</li>
<li>If no folder is provided, temporary memory layers will be created automatically.</li>
</ul>

<h3>(iii) Run the Model</h3>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/5c869117-b20d-420a-b00a-cac3d6ed3f53" width="95%">
</div>

<h3>Output</h3>

<p>After successful execution, the following layers will be added to the QGIS Layers Panel:</p>

<p><strong>1. buildings_with_clusters</strong></p>
<ul>
<li>Contains buildings identified as requiring evacuation</li>
<li>Includes building-level evacuation attributes</li>
</ul>

<p><strong>2. Evacuation_Routes</strong></p>
<ul>
<li>Represents the shortest walking routes from each building to its assigned evacuation shelter</li>
</ul>

<h3>Output Attributes</h3>

<ul>
<li>Each building is assigned to the nearest evacuation shelter and that shelter’s ID and the shortest route is computed between each building and its assigned shelter.</li>
<li>Walking time is calculated and stored in the <strong>Time</strong> field from the building to the shelter.</li>
</ul>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/cc3bfdcd-8c0b-4713-92fb-0adb4e8597ea" width="45%">
<img src="https://github.com/user-attachments/assets/8365c3e8-be6f-4afa-99f8-d0e549d65a85" width="40%">
</div>

<h3>Assumptions</h3>

<ul>
<li>Evacuation is assumed to occur by walking to avoid traffic congestion</li>
<li>All evacuees are assumed to be physically fit adults and walking speed is considered as 5 m/s</li>
<li>Road network derived from OpenStreetMap is assumed to be fully passable. Off-road evacuation is not considered</li>
<li>All evacuees are assumed to start from the nearest accessible node/junction on the road network. The distance from each building to the nearest junction and the walking time within the building (in case of a big building/multi-story) are not considered.</li>

</ul>

<h3>Exceptions and Special Conditions</h3>

<ul>
<li><strong>No Buildings in Flood Zone:</strong> If no buildings intersect with the flood inundation zone, the process terminates automatically and a message is displayed:
“No Buildings in the Flood Zone”</li>
<li><strong>All Shelters Within Flood Zone:</strong> If all evacuation shelters fall within the flooding/inundation area, the process terminates and the following message is shown:
“All evacuation shelters are in the flood zone”.</li>
<li><strong>If no OpenStreetMap (OSM) pedestrian road network is found in the vicinity of the buildings, the process stops and a warning message is displayed:
“Road Network Not Found”.</li>
</ul>

<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:15px; 
            margin:25px 0; 
            border-radius:6px;">

<strong>Important Notes:</strong>
<ul style="margin-top:10px;">
<li>The model executes using sequential processing; parallel processing is not implemented.</li>
<li>Sample datasets are available in the 
<a href="https://github.com/gauravbkhairnar/Build_Short_Evac_Time_QGIS_Plugin/tree/main/sample_data" target="_blank" style="color:white; text-decoration:underline;">
sample data folder
</a> for testing and demonstration.
</li>
</ul>
</div>






















<hr style="margin:30px 0;">

<h2>Reference</h2>

<p>
Sirko, W., Kashubin, S., Ritter, M., Annkah, A., Bouchareb, Y.S.E., Dauphin, Y., 
Keysers, D., Neumann, M., Cisse, M., & Quinn, J.A. (2021). 
<i>Continental-scale building detection from high resolution satellite imagery.</i> 
arXiv:2107.12283.
<br>
Putra, H., Kemal, B. M., & Mas, E. (2020, February). Identification of factors influencing the evacuation walking speed in Padang, Indonesia. In 2nd International Symposium on Transportation Studies in Developing Countries (ISTSDC 2019) (pp. 125-130). Atlantis Press.
<br>
Srinivasa Kumar, T., & Manneela, S. (2021). A review of the progress, challenges and future trends in tsunami early warning systems. Journal of the Geological Society of India, 97(12), 1533-1544
<br>
Universal Transverse Mercator coordinate system – Wikipedia
https://en.wikipedia.org/wiki/Universal_Transverse_Mercator_coordinate_system

</p>












</div>

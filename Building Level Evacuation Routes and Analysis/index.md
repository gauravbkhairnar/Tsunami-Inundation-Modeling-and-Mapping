# This step contains 3 sections:
1. Downloading Building footprints
2. Installing QGIS Plugin
3. Building level evacuation analysis

# 1. Downloading Building footprints (Open Buildings V3)
The dataset contains 1.8 billion building detections, across an inference area of 58M km2 covering Africa, South Asia, South-East Asia, Latin America and the Caribbean. The current dataset is in its 3rd version. Building footprint data derived from the Google Open Buildings dataset (v3), © Google, licensed under CC BY 4.0.


<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:12px; 
            margin:15px 0;">

<strong>Important Notes regarding open building dataset:</strong><br>
•	AI-derived<br>
•	May miss small or rural structures<br>
•	Has confidence scores<br>
•	Should not be treated as cadastral truth<br>
</div>

Google Open Building Data is available on the link below: <br>
https://sites.research.google/gr/open-buildings/

<img width="940" height="505" alt="image" src="https://github.com/user-attachments/assets/94822bf2-cd6d-429e-87ec-6e5819c4d68f" />

<br>
Click on "Download here" Button
You can search your are of interest location or you can zoom on your area of interest and select the tile to download. 
<br>
<img width="940" height="505" alt="image" src="https://github.com/user-attachments/assets/5703cc5d-42a1-480b-8c25-2fb562459964" />
<br>
Click on xxx_buildings.csv.gz file for downloading.
After downloading unzip xxx_buildings.csv.gz.

## To add the buildings data into QGIS:
Open QGIS.
Add layer --> Add Delimited text layer
<br>
<img width="940" height="505" alt="image" src="https://github.com/user-attachments/assets/bcb68d61-d37c-48fc-8bce-acbf0136eae7" />
<br>
select file path and select csv file

Click on **Geometry Definition** section --> **Well known text (WKT)** --> select geometry in **Geometry field** and **geometry CRS** : EPSG 4326-WGS84
Click Add (**This step will take more time.. As you are adding more than 10 million buildings in QGIS**)
<br>
<img width="940" height="592" alt="image" src="https://github.com/user-attachments/assets/ea6ea5dd-b2f3-41e2-91d9-c4eb6a4a4b05" />
<br>
Once data successfully added in QGIS --> click on Select layer icon and draw polygon which is of your area of interest. 
<br>
<img width="940" height="505" alt="image" src="https://github.com/user-attachments/assets/7c5b5324-db1b-42d7-89ea-b18a718b1889" />
<br>
After selection, Export it into .shp file by right clicking on layer in layer pannel --> Export --> Export Selected features.
<img width="940" height="1070" alt="image" src="https://github.com/user-attachments/assets/7589ee86-00f8-496c-9e7d-66811d00fff2" />
<br>
<img width="928" height="1039" alt="image" src="https://github.com/user-attachments/assets/d554e356-c16a-4606-81cc-a7a17719c05d" />
<br>



# Reference
W. Sirko, S. Kashubin, M. Ritter, A. Annkah, Y.S.E. Bouchareb, Y. Dauphin, D. Keysers, M. Neumann, M. Cisse, J.A. Quinn. Continental-scale building detection from high resolution satellite imagery. arXiv:2107.12283, 2021.

# This step contains 3 sections:
1. Downloading Building footprints
2. Installing QGIS Plugin
3. Building level evacuation analysis

# 1. Downloading Building footprints
## Open Buildings V3
The dataset contains 1.8 billion building detections, across an inference area of 58M km2 covering Africa, South Asia, South-East Asia, Latin America and the Caribbean. The current dataset is in its 3rd version. Building footprint data derived from the Google Open Buildings dataset (v3), © Google, licensed under CC BY 4.0.


<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:12px; 
            margin:15px 0;">

<strong>Important Notes regarding open building dataset:</strong><br>
•	AI-derived
•	May miss small or rural structures
•	Has confidence scores
•	Should not be treated as cadastral truth
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









# Reference
W. Sirko, S. Kashubin, M. Ritter, A. Annkah, Y.S.E. Bouchareb, Y. Dauphin, D. Keysers, M. Neumann, M. Cisse, J.A. Quinn. Continental-scale building detection from high resolution satellite imagery. arXiv:2107.12283, 2021.

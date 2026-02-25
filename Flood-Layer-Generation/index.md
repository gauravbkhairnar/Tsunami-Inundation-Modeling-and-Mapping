<h1 style="text-align:center; margin-top:30px; margin-bottom:30px;">
            Flood Layer Generation
</h1>

<div style="max-width:1400px; margin:0 auto; padding:0 10px;">

<h3>Objective</h3>

The objective of this exercise is to generate a flood zone using output from the ComMIT model.

Data inputs:
<ul><li>Raster Layer in .TIFF format (Generated from ComMIT)</li></ul>

1. Download the <strong>'Flood_Layer_Generation.model3'</strong> file from <a href="https://indiannational-my.sharepoint.com/:u:/g/personal/gb_khairnar-p_incois_gov_in/IQBGrV2RltbzQIKHZYlADkx3AeDDSrvKzrMrfnETn_mIsfk?e=Io2Yvv">here</a> <br>
<br>
2. Open QGIS --> <strong>Open Processing Toolbox</strong> <br>
3. Click on this icon <img width="32" height="31" alt="image" src="https://github.com/user-attachments/assets/5c3fd9b0-5de8-4957-bebb-6eb9dc093ead" /><br>
<img align="center" width="100%" alt="processingtoobox" src="https://github.com/user-attachments/assets/152c6524-5b27-4b80-8ef0-7ae67a495da3" style="border:1px solid #ccc; padding:4px;"  />
<br>
<br>
Click on <strong>Add Model</strong> to Toolbox
<br>
<br>
<img align="center" width="331" height="282" alt="processingtoobox2" src="https://github.com/user-attachments/assets/f6a3437b-b3be-4ee1-9f37-79b3e1ee359e" style="border:1px solid #ccc; padding:4px;"  />

<br>

Select the directory and select the downloaded <strong>Flood_Layer_Generation.model3</strong> model --> Open.
<br>

4. Add ComMIT output to QGIS:
   <strong>Layers --> Add Layer --> Add Raster Layer..</strong>
   <img align="center" width="100%" alt="image" src="https://github.com/user-attachments/assets/2990940a-e9aa-423f-80e3-2de9dfa7172b" style="border:1px solid #ccc; padding:4px;" />

5. Flood Layer Generation:
   Scroll down in processing toolbox --> Double Click on <strong>Models</strong> --> Click on <strong>Flood_Layer_Generation</strong>
   <br>
   <img align="center" width="1920" height="1031" alt="model" src="https://github.com/user-attachments/assets/fa8d1365-9f60-4675-8df0-5b200ff95ecd" style="border:1px solid #ccc; padding:4px;"/>
<br>

Select the Raster layer by dropping down <strong>Input Inundation Raster Layer</strong> --> Give the area in square meters for removing holes --> if you want to save output flood layers then pls ckick on <img width="32" height="31" alt="image" src="https://github.com/user-attachments/assets/af293a4d-9f30-41d9-bced-d9d2d5453710" /> and click on <strong>Save to File..</strong> and locate directory and click save. --> Click <strong>Run</strong>
<br>
<img align="center" width="942" height="861" alt="model2" src="https://github.com/user-attachments/assets/04ec025a-8c3a-487f-977d-5ad4bc1e248b" style="border:1px solid #ccc; padding:4px;" />
<br>
After a successful run, 2 Layers will be added in the Layer Panel. 



</div>






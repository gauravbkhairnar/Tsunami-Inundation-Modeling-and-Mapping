<h1 style="text-align:center; margin-top:30px; margin-bottom:30px;">
            Flood Layer Generation
</h1>

<div style="max-width:1400px; margin:0 auto; padding:0 10px;">

<h3>Objective</h3>
<p>
The objective of this exercise is to generate a flood zone using output from the ComMIT model.

Data inputs:
* Output of the Raster Layer in .TIFF format
 
<div style="background-color:#f57c00; 
            border-left:5px solid #fff8e1; 
            color:white; 
            padding:12px; 
            margin:15px 0;">

<strong>Important Note:</strong><br>
</p>
</div>

1. Download the 'Flood_Layer_Generation.model3' file from [here](https://indiannational-my.sharepoint.com/:u:/g/personal/gb_khairnar-p_incois_gov_in/IQBGrV2RltbzQIKHZYlADkx3AeDDSrvKzrMrfnETn_mIsfk?e=Io2Yvv) <br>
2. Open QGIS --> Open Processing Toolbox <br>
3. Click on this icon <img width="32" height="31" alt="image" src="https://github.com/user-attachments/assets/5c3fd9b0-5de8-4957-bebb-6eb9dc093ead" /><br>
<img width="100%" alt="processingtoobox" src="https://github.com/user-attachments/assets/152c6524-5b27-4b80-8ef0-7ae67a495da3" style="border:1px solid #ccc; padding:4px;"  />
<br>
Click on Add Model to Toolbox <br>
<img width="100%" alt="image" src="https://github.com/user-attachments/assets/8c26e05c-b0b7-4e70-8cc6-7bf6851b1273" style="border:1px solid #ccc; padding:4px;"  /><br>

Select the directory and select the downloaded Flood_Layer_Generation.model3 model --> Open.<br>

4. Add ComMIT output to QGIS:
   Layers --> Add Layer --> Add Raster Layer..
   <img width="100%" alt="image" src="https://github.com/user-attachments/assets/2990940a-e9aa-423f-80e3-2de9dfa7172b" style="border:1px solid #ccc; padding:4px;" />

5. Flood Layer Generation:
   Scroll down in processing toolbox --> Double Click on **Models** --> Click on **Flood_Layer_Generation**
   <img width="100%" alt="model" src="https://github.com/user-attachments/assets/d02b8a99-8d15-4f86-a5a7-672a6bee69df" style="border:1px solid #ccc; padding:4px;"/>

Select the Raster layer by dropping down **Input Inundation Raster Layer** --> Give the area in square meters for removing holes --> if you want to save output flood layers then pls ckick on <img width="32" height="31" alt="image" src="https://github.com/user-attachments/assets/af293a4d-9f30-41d9-bced-d9d2d5453710" /> and click on **Save to File..** and locate directory and click save. --> Click **Run**

<img width="100%" alt="model2" src="https://github.com/user-attachments/assets/09e3795e-4261-4b1a-b0c2-09e638ad3fbb" style="border:1px solid #ccc; padding:4px;" />

After a successful run, 2 Layers will be added in the Layer Panel. 



</div>






<h1 style="text-align:center; margin:40px 0;">
Flood Layer Generation
</h1>

<div style="max-width:1400px; margin:0 auto; padding:0 30px; line-height:1.7;">

<h2>Objective</h2>

<p>
The objective of this exercise is to generate a flood zone using the inundation 
output produced by the <strong>ComMIT tsunami model</strong>.
</p>

<h2>Data Input</h2>

<ul>
<li>Raster layer in <strong>.TIFF</strong> format (generated from ComMIT)</li>
</ul>

<hr style="margin:30px 0;">

<h2>Procedure</h2>

<h3>Step 1: Download the Model File</h3>

<p>
Download the <strong>Flood_Layer_Generation.model3</strong> file from 
<a href="https://indiannational-my.sharepoint.com/:u:/g/personal/gb_khairnar-p_incois_gov_in/IQBGrV2RltbzQIKHZYlADkx3AeDDSrvKzrMrfnETn_mIsfk?e=Io2Yvv" target="_blank">
here
</a>.
</p>

<h3>Step 2: Open Processing Toolbox in QGIS</h3>

<p>
Open <strong>QGIS</strong> → Navigate to <strong>Processing Toolbox</strong>.
</p>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/152c6524-5b27-4b80-8ef0-7ae67a495da3" 
style="max-width:100%; border:1px solid #ccc; padding:6px;">
</div>

<p>
Click on <strong>Add Model</strong> to add the downloaded model to the toolbox.
</p>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/f6a3437b-b3be-4ee1-9f37-79b3e1ee359e" 
style="max-width:60%; border:1px solid #ccc; padding:6px;">
</div>

<p>
Select the downloaded <strong>Flood_Layer_Generation.model3</strong> file and click <strong>Open</strong>.
</p>

<h3>Step 3: Add ComMIT Output Raster</h3>

<p>
Go to:
<strong>Layers → Add Layer → Add Raster Layer</strong>
and load the ComMIT inundation output.
</p>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/2990940a-e9aa-423f-80e3-2de9dfa7172b" 
style="max-width:100%; border:1px solid #ccc; padding:6px;">
</div>

<h3>Step 4: Run Flood Layer Generation Model</h3>

<p>
In the Processing Toolbox:
Scroll down → Double-click <strong>Models</strong> → Select 
<strong>Flood_Layer_Generation</strong>.
</p>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/fa8d1365-9f60-4675-8df0-5b200ff95ecd" 
style="max-width:100%; border:1px solid #ccc; padding:6px;">
</div>

<p>
Configure the model parameters:
</p>

<ul>
<li>Select the inundation raster under <strong>Input Inundation Raster Layer</strong>.</li>
<li>Specify the minimum hole area (in square meters) for removal.</li>
<li>If required, click <strong>Save to File…</strong> to export the output flood layer.</li>
<li>Click <strong>Run</strong>.</li>
</ul>

<div style="text-align:center; margin:20px 0;">
<img src="https://github.com/user-attachments/assets/04ec025a-8c3a-487f-977d-5ad4bc1e248b" 
style="max-width:80%; border:1px solid #ccc; padding:6px;">
</div>

<h3>Output</h3>

<p>
After successful execution, two new layers will be added to the 
<strong>Layers Panel</strong>, representing the generated flood zone outputs.
</p>

</div>

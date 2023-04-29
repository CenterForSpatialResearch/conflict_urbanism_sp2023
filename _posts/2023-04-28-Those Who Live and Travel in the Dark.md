---
layout: post
date:   2023-04-28
image: "/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/cover image-01.jpg"
title:  "Those Who Live and Travel in the Dark"
author: "Kelly Shining Hong, Candice Siyun Ji, Alan Ren, Wei Xiao"
---

### INTRODUCTION  

Nighttime satellite imagery has been commonly used to estimate population density and economic activity indicators (Liu et al., 2021; Elvidge et al., 2007; Elvidge et al., 2012; Zhao et al., 2019). However, this approach has limitations, as it may often fail to capture areas that are inhabited but lack adequate infrastructure. In response, the In Plain Sight project, a collaboration between Diller Scofidio + Renfro and the Center for Spatial Research, has pioneered an innovative approach to night light imagery by revealing the gaps in the network and highlighting individual lights and zones where lights are missing.

Building on this novel approach, this project seeks to challenge the conventional use of night light imagery by integrating other sources of datasets to provide a more comprehensive understanding of the lives and infrastructure behind nighttime activities. Specifically, the project aims to compare nighttime light satellite imagery with informal mobility network datasets, census grid counts, and building footprint datasets produced by governments and researchers worldwide. By examining the relationship between the built environment, infrastructure, and human settlement at the scale of satellite imagery, the project aims to challenge existing assumptions about the geographies of belonging and infrastructure exclusion

This comparative analysis across different datasets will enable the project to identify global patterns and reveal untold stories of places where people live but lack adequate infrastructure at night. The project zoomed in on five case study cities in Africa, examining the intersection of nighttime activity and the built environment to reveal new insights into the spatial and social dimensions of urban life in these contexts. Overall, this project seeks to contribute to a more nuanced and comprehensive understanding of urban infrastructures or the lack thereof and the lives they shape.


**Dominant Narrative of Night-time Light Satellite Imagery**

- “(N)ightlight intensities as a proxy of **economic activity** degrees to estimate **county-level GDP**” - Liu et al., 2021
- “Remotely-sensed anthropogenic lighting signals and their spatial variations at night provide us with an efficient proxy **measure of the demographic** and **economic related activities** during urbanization and regional development” - Zhao et al., 2019
- “This data can reveal **local context** and quantify **relative economic performance** - especially in places where official information is unavailable, unreliable, or out-of-date.” - Foster and Lechler 2022
- “Multi-spectral low-light imaging data would be … potentially a stronger predictor of variables such as ambient **population density** and **economic activity**.” - Elvidge et al., 2007



#### Areas of Focus  
![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Continent Map-01.png)
The five African case-study cities are Accra, Ghana; Addis Ababa, Ethiopia; Cairo, Egypt; Harare, Zimbabwe; Nairobi, Kenya. 



#### Research Questions  
1. Are there areas where urban clusters exist, but lacking access to infrastructural light and not considered as urban zones? Which of these areas are serviced by informal buses?
2. What are the transportation options and conditions in these areas?
3. How does the built environment pattern in these areas compare to their respective city centers?





### Methodology  

![methodology chart overview](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology_Overview.PNG)
The above diagram illustrates a detailed step-by-step methodology breakdown of the research project. In summary, the overall processing can be divided into four main sections.



1. **Raw data collection**: In this step, five primary datasets are collected from each source’s website, including V.2 VIIRS Nighttime Lights, UN WPP-Adjusted Population Density, Building Footprints, Informal Bus Routes, and City Administrative Boundaries. Besides nighttime and population data at the global scale, other datasets should be collected locally depending on each study city.
![Methodology diagram](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology_Diagram.PNG)

- *Layer 1: Night-time Light Satellite Imagery*
![Nighttime Light Satellite Imagery](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Nighttime Data_Recolored.PNG)

- *Layer 2: Gridded Population Density*
![World Population](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/WorldPopulation.PNG)

- *Layer 3: Informal Bus Transit System*
![Informal bus routes](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Digital Matatus.PNG)

- *Layer 4: Building Footprints*
![Building Footprint](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Building Footprint.PNG)

- *Layer 5: City Administrative Boundries*
Varies based on each city. 


2. **Data Processing**: This step requires raster (image) and vector manipulation with geoprocessing software, including QGIS and ArcGIS. The datasets that require raster processing are V.2 VIIRS Nighttime Lights and UN WPP-Adjusted Population Density, which come in tif format with geo-referencing systems. For the nighttime light data, a threshold of 13DN (Columbia Climate School) is used as the light intensity indicator for urban zones. For the gridded population, a threshold of 300 people per square kilometer (European Union) is taken as the population density indicator for urban clusters. For identified urban clusters, a classification system was applied to all studied cities to visualize population density. The rest of the vector dataset generally requires less processing, as shown in the methodology breakdown diagram. 
![image processing nairobi demo](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology 1.gif)



3. **Data Visualization**: After all datasets are processed into the ideal formats, they are overlaid to identify areas of research interests based on the following criteria - places where urban clusters are presented but without nighttime light, while informal bus routes reach to the spots.
![layering Datasets nairobi demo](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology 2.gif)


4. **Machine Learning**: Further research is then done to explore the urban fabrics and materiality of the built environment. Two machine learning classification models are employed in this step, both at the satellite scale in the unit of two kilometers by two kilometers square from the central coordinate of each city and selected towns. The first model reclassified the urban patterns into built, vegetation, and water coverage using Landsat 8 images, from which we can investigate the degree of urbanization. The second model extracts materials from satellite images with a pre-determined color range to recognize earth as a material in the urban context, as an indicator of potential under/undeveloped areas or road and buildings constructed out of raw earth. 





### Case Study Site Selection Results  


#### Accra, Ghana  
![Accra map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Accra_final.gif)

As a coastal city, Accra's population is mainly concentrated in the southern part of the city, and the informal bus routes are predominantly distributed along the coastline. The uncovered areas are three newly emerging, fast-growing new towns located near the NASA nighttime light image boundary, with a relatively low building footprint density. 



#### Addis Ababa, Ethiopia  
![Addis Ababa map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Addis_final.gif)

Addis Ababa's city center exhibits a smaller population compared to other regions. Informal bus stops can be found along both sides of the city's primary roads, mainly in suburban areas that fall short of the urban density standard of 300 people per square kilometer. Notably, the two adjacent satellite towns lack informal bus stop points. The NASA nighttime light image is considerably smaller than the areas with the lowest population density boundary, suggesting that many self-built houses are without nighttime electricity supply.
<sub>Data limitations allowed us to obtain only stop points rather than complete stop trips.</sub>



#### Cairo, Egypt  
![Cairo map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Cairo_final.gif)

Among the analyzed urbanizing cities, Cairo appears to be the most developed. With the exception of the 10th Ramadan City, all informal bus areas fall within the urban region and the NASA nighttime light image boundaries.
While the horizontal connection of informal bus trips is well-developed, the city lacks vertical connections. This limitation may result from the agricultural land situated to the north and south of the city.




#### Harare, Zimbabwe  
![Harare map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Harare_final.gif)

Harare's urban morphology resembles Addis Ababa's, featuring a central radial pattern connecting surrounding satellite towns. However, areas containing informal bus stops almost entirely overlap with the regions with the lowest urban population density. 
The NASA nighttime light image in Harare is significantly smaller than the areas with the lowest population density boundary. Interestingly, the city's most populated areas in the southern and eastern parts are not included by the NASA nighttime light image boundary.



#### Nairobi, Kenya  
![Nairobi map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Nairobi_final.gif)

When considering city areas with a population density of 300 people per square kilometer, Nairobi's urban extent actually surpasses its planned administrative area, so it’s blurring the concept of suburbs. 
But if we just look the official Nairobi administrative area, the NASA nighttime light image and urban extent nearly coincide within the Nairobi administrative area.
The informal bus system connects numerous surrounding villages and new towns, though it does not overlap with the NASA nighttime light image boundary in the city's western part. This observation indicates an imbalanced development between Nairobi's eastern and western regions.








### Findings  

By analyzing the layers of datasets, a few key themes emerged highlighting the urban fabric patterns, the percentage of earth, the availability of transportation options, and the informal mobility conditions experienced by residents living in areas with low levels of night light.


![transportation options comparison](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/forms of transportation comparison.jpg)


![Epworth transportation](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/transportation comparison examples_Epworth.jpg)

![Alem Gena transportation](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/transportation comparison examples_Alem Gena.jpg)


![informal transportation images](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/informal transportation example.jpg)






Write **words in bold** like this.  

Italics are *similar* and are formatted like this.  

To make a paragraph break you need to add two spaces at the end of your line before going to the next line.  

See this is now a new paragraph.  

Lists are easy:
1. they can be ordered
1. like this
1. notice that the numbers are automatically ordered
  1. use two spaces in front to indent

Or they can just be bullet points:
- like this
* or like this
  - use two spaces
  - to have nested lists

Use Author-Date parenthetical citations following Chicago Manual of Style conventions throughout your document, and add a works cited at the bottom of your post. See Author-Date quick guide [here](https://www-chicagomanualofstyle-org.ezproxy.cul.columbia.edu/tools_citationguide/citation-guide-2.html) for citation conventions.  

To include hyperlinks format them like this [text of link](http://c4sr.columbia.edu/).  

To embed images first ensure that the file is at least 740px wide. Then place the image file in a folder named for your group in the images folder. Then link to that image using the format here, but replace the file path with the name of your group's folder and appropriate image file name:  

![description of image](/template_site/images/sample_image.png)

If you want to include html files (i.e. an interactive map) host these via your personal github page, and then you can embed them in your document with a iframe. The format looks like this:  

<div class="iframe-column"><iframe src="https://player.vimeo.com/video/290575503?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0"></iframe></div>  


All you need to do to use one is replace the url that is between the two " ". Here is an iframe of mapbox tiles:  

<div class="iframe-column"><iframe src="https://api.mapbox.com/styles/v1/mapbox/satellite-v9.html?title=true&access_token=pk.eyJ1IjoibWFwYm94IiwiYSI6ImNpejY4NDg1bDA1cjYzM280NHJ5NzlvNDMifQ.d6e-nNyBDtmQCVwVNivz7A#2/0/0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0"></iframe></div>
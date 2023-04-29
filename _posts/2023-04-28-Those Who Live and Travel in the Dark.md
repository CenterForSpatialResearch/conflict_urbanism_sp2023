---
layout: post
date:   2023-04-28
image: "/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/cover image-01.jpg"
title:  "Those Who Live and Travel in the Dark"
author: "Kelly Shining Hong, Candice Siyun Ji, Alan Ren, Wei Xiao"
---

#### INTRODUCTION  

Previous studies have commonly correlated night light as a proxy of population density and economic activity indicators (Liu et al., 2021, Elvidge et al., 2007, Elvidge et al., 2012, Zhao et al., 2019). However, relying on nighttime satellite imagery to analyze human activities can overlook areas that are populated but lack infrastructure. Our project seeks to counter this approach by examining the "dark" spots on the nighttime light map and identifying anomalies in population distribution. Specifically, we will compare nighttime light satellite imagery with building footprint datasets, informal mobility network datasets, and census grid counts produced by governments and researchers worldwide. This comparison will enable us to reveal global patterns and stories of places with people but a lack of infrastructural lights at night, with a focus on cities in Africa.


**Nighttime Light Satellite Imagery**

![Nighttime Light Satellite Imagery](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Nighttime Data_Recolored.PNG)

Remote sensing of nighttime light emissions offers a unique perspective for investigations into human behaviors.


**Dominant Narrative of Night-time Light Satellite Imagery**

Previous studies have commonly correlated night light as a proxy of population density and economic activity indicators.

- “(N)ightlight intensities as a proxy of **economic activity** degrees to estimate **county-level GDP**” -Liu et al., 2021
- “Remotely-sensed anthropogenic lighting signals and their spatial variations at night provide us with an efficient proxy **measure of the demographic** and **economic related activities** during urbanization and regional development” -Zhao et al., 2019
- “This data can reveal **local context** and quantify **relative economic performance** - especially in places where official information is unavailable, unreliable, or out-of-date.” -Foster and Lechler 2022
- “Multi-spectral low-light imaging data would be … potentially a stronger predictor of variables such as ambient **population density** and **economic activity**.” -Elvidge et al., 2007


**Countering the Dominant Narrative by Layering Datasets**

![Methodology diagram](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology_Diagram.PNG)

This project layers sources of datasets other than the Night-time Lights to tell a new story of the lives behind the night-time infrastructure. 

*Layer 1: Night-time Light Satellite Imagery* as mentioned above

*Layer 2: Gridded Population Density*
![World Population](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/WorldPopulation.PNG)

*Layer 3: Informal Bus Transit System*
![Informal bus routes](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Digital Matatus.PNG)

*Layer 4: Building Footprints*
![Building Footprint](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Building Footprint.PNG)

**Areas of Focus**
![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Continent Map-01.png)



#### Methodology  

![methodology chart overview](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology_Overview.PNG)

As mentioned earlier in the first section, four main datasets, with the addition of city/town administrative boundaries used to locate the study area, are utilized in this study. The datasets that require image processing are night-time light and gridded population data, which come as in tif format with geo-referencing system. For the nighttime light data, we utilized the threshold of 13 digital number as the indicator of urban zone, as suggested by Columbia Climate School. For the gridded population, a threshold of 300 people per square kilometer is taken as the indicator of urban cluster, following the suggestions by European Union. For urban clusters that are identified, a further classification system was applied to all studied cities to visualize population density, which will be shown later in the mapping. The rest of the datasets in general requires less pre-processing, as shown in this diagram. The purpose of this diagram is to also show that with datasets available, this study can be re-produced for any cities across the globe as an universal methodology.


**Nairobi Demo: Image Processing**
![image processing nairobi demo](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology 1.gif)
Here is a quick demo of Nairobi showing how nighttime light data, comes in as a raster image, were reclassified based on the threshold and vectorized through QGIS to generate urban zone footprint shapefile. Similar actions is applied to the gridded population data, with an additional step of clipping which enabled the dataset to remain in raster format while maintaining its cell values for density mapping.


**Nairobi Demo: Layering Datasets**
![layering Datasets nairobi demo](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology 2.gif)
After all datasets are pre-processed into the ideal format, they can be layered together in helping us identify the area where human habitation is presented but lacking infrastructure light, while informal bus routes reach those areas, indicating human and potential capital flows. As shown here, areas in nairobi such as misiri village and kiserian fulfill the conditions mentioned earlier. 



#### Case Study Site Selection Results  






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
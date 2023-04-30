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

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


#### Areas of Focus  
![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Continent Map-01.png)
The five African case-study cities are Accra, Ghana; Addis Ababa, Ethiopia; Cairo, Egypt; Harare, Zimbabwe; Nairobi, Kenya. 


![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)

#### Research Questions  
1. Are there areas where urban clusters exist, but lacking access to infrastructural light and not considered as urban zones? Which of these areas are serviced by informal buses?
2. What are the transportation options and conditions in these areas?
3. How does the built environment pattern in these areas compare to their respective city centers?


![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 2-01.png)



### Methodology  

![methodology chart overview](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology_Overview.PNG)
The above diagram illustrates a detailed step-by-step methodology breakdown of the research project. In summary, the overall processing can be divided into four main sections.

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


1. **Raw data collection**: In this step, five primary datasets are collected from each source’s website, including V.2 VIIRS Nighttime Lights, UN WPP-Adjusted Population Density, Building Footprints, Informal Bus Routes, and City Administrative Boundaries. Besides nighttime and population data at the global scale, other datasets should be collected locally depending on each study city.
  ![Methodology diagram](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology_Diagram.PNG)

 ![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


 - *Layer 1: Night-time Light Satellite Imagery*
 ![Nighttime Light Satellite Imagery](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Nighttime Data_Recolored.PNG)

   <sub>Data Source: NASA VIIRS Night-time Lights (C. D. Elvidge et al., 2017)</sub>

 ![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


 - *Layer 2: Gridded Population Density*
 ![World Population](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/WorldPopulation.PNG)

   <sub>Data Source: UN WPP-Adjusted Population Density (Center for International Earth Science Information Network, Columbia University, 2018)</sub>

 ![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


 - *Layer 3: Informal Bus Transit System*
 ![Informal bus routes](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Digital Matatus.PNG)

   <sub>Data Source: DATUM. Image Source: digitalmatatus, Civic Data Design Lab MIT, 2014</sub>

 ![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)

 - *Layer 4: Building Footprints*
 ![Building Footprint](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Building Footprint.PNG)

   <sub>Data Sources: Microsoft Building Footprint, Microsoft Maps & Geospatial; Open Buildings, Google</sub>
 
 ![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)

 - *Layer 5: City Administrative Boundries*
   Varies based on each city. 

 ![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


2. **Data Processing**: This step requires raster (image) and vector manipulation with geoprocessing software, including QGIS and ArcGIS. The datasets that require raster processing are V.2 VIIRS Nighttime Lights and UN WPP-Adjusted Population Density, which come in tif format with geo-referencing systems. For the nighttime light data, a threshold of 13DN (Columbia Climate School) is used as the light intensity indicator for urban zones. For the gridded population, a threshold of 300 people per square kilometer (European Union) is taken as the population density indicator for urban clusters. For identified urban clusters, a classification system was applied to all studied cities to visualize population density. The rest of the vector dataset generally requires less processing, as shown in the methodology breakdown diagram. 
  ![image processing nairobi demo](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology 1.gif)

  ![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


3. **Data Visualization**: After all datasets are processed into the ideal formats, they are overlaid to identify areas of research interests based on the following criteria - places where urban clusters are presented but without nighttime light, while informal bus routes reach to the spots.
  ![layering Datasets nairobi demo](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Methodology 2.gif)

  ![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


4. **Machine Learning**: Further research is then done to explore the urban fabrics and materiality of the built environment. Two machine learning classification models are employed in this step, both at the satellite scale in the unit of two kilometers by two kilometers square from the central coordinate of each city and selected towns. The first model reclassified the urban patterns into built, vegetation, and water coverage using Landsat 8 images, from which we can investigate the degree of urbanization. The second model extracts materials from satellite images with a pre-determined color range to recognize earth as a material in the urban context, as an indicator of potential under/undeveloped areas or road and buildings constructed out of raw earth. 


![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 2-01.png)



### Case Study Site Selection Results  


#### Accra, Ghana  
![Accra map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Accra_final.gif)

As a coastal city, Accra's population is mainly concentrated in the southern part of the city, and the informal bus routes are predominantly distributed along the coastline. The uncovered areas are three newly emerging, fast-growing new towns located near the NASA nighttime light image boundary, with a relatively low building footprint density. 

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


#### Addis Ababa, Ethiopia  
![Addis Ababa map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Addis_final.gif)

Addis Ababa's city center exhibits a smaller population compared to other regions. Informal bus stops can be found along both sides of the city's primary roads, mainly in suburban areas that fall short of the urban density standard of 300 people per square kilometer. Notably, the two adjacent satellite towns lack informal bus stop points. The NASA nighttime light image is considerably smaller than the areas with the lowest population density boundary, suggesting that many self-built houses are without nighttime electricity supply.

<sub>Data limitations allowed us to obtain only stop points rather than complete stop trips.</sub>

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


#### Cairo, Egypt  
![Cairo map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Cairo_final.gif)

Among the analyzed urbanizing cities, Cairo appears to be the most developed. With the exception of the 10th Ramadan City, all informal bus areas fall within the urban region and the NASA nighttime light image boundaries.
While the horizontal connection of informal bus trips is well-developed, the city lacks vertical connections. This limitation may result from the agricultural land situated to the north and south of the city.


![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


#### Harare, Zimbabwe  
![Harare map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Harare_final.gif)

Harare's urban morphology resembles Addis Ababa's, featuring a central radial pattern connecting surrounding satellite towns. However, areas containing informal bus stops almost entirely overlap with the regions with the lowest urban population density. 
The NASA nighttime light image in Harare is significantly smaller than the areas with the lowest population density boundary. Interestingly, the city's most populated areas in the southern and eastern parts are not included by the NASA nighttime light image boundary.

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


#### Nairobi, Kenya  
![Nairobi map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/Nairobi_final.gif)

When considering city areas with a population density of 300 people per square kilometer, Nairobi's urban extent actually surpasses its planned administrative area, so it’s blurring the concept of suburbs. 
But if we just look the official Nairobi administrative area, the NASA nighttime light image and urban extent nearly coincide within the Nairobi administrative area.
The informal bus system connects numerous surrounding villages and new towns, though it does not overlap with the NASA nighttime light image boundary in the city's western part. This observation indicates an imbalanced development between Nairobi's eastern and western regions.


![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 2-01.png)


### Findings  

By analyzing the layers of datasets, a few key themes emerged highlighting the urban fabric patterns, the percentage of earth, the availability of transportation options, and the informal mobility conditions experienced by residents living in areas with low levels of night light.

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


#### *Built Environment Findings on the Satellite Scale*  


#### Urban Fabric   

*How does the urban fabric manifest in areas lacking formal transportation infrastructure and reliant on informal modes of transportation, and how does it compare to the urban fabric in their respective city centers?*



![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/IMAGE COLLECTION.jpg)

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/ML IMAGE COLLECTIN.jpg)

<sub>Green is non-built features vs. Orange is built features</sub>


The findings from the machine learning classification models reveal that towns located at the end of informal bus routes generally have lower levels of built features compared to their respective city centers. For example, in Nairobi, the four towns of Githunguri, Karen Hardy, Kiserian, and Misiri Village at the end of the informal bus route exhibit an average of only 7.9% of built features, while the central coordinate of Nairobi has an 83.2% built area. Similarly, in Addis Ababa, the four towns of Akaki, Alem Gena, Menagesha, and VFAC at the end of the informal bus route exhibit an average of 62.0% of built features compared to the central coordinates’ 89.3% built area. These results indicate a possible relationship between the absence of formal transportation infrastructure and the built environment and urban fabric in these regions.

However, an outlier to this trend was observed in Harare, Zimbabwe, where the towns at the periphery of the city exhibited a higher level of built features (66.9% built area) compared to the city center (34.3%). This anomaly could be attributed to the "infrastructural degeneration" of Harare in recent decades, as the city's infrastructure and services have failed to keep pace with population growth, resulting in physical infrastructure decline (Atwood 2016; Ndlovu and Narayanan 2023). The machine learning of the satellite images further support this claim, as the towns located at the end of informal transit routes have a higher level of built features compared to the geographic center of Harare.

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)

#### Recognition of Earth  

*How much percent of earth is exhibited in areas lacking formal transportation infrastructure and reliant on informal modes of transportation, and how does it compare to the urban fabric in their respective city centers?*

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)

#### *Transportation Findings on the Town Scale*  

*What are the available transportation options for people living and working in these areas?*
The residents of the sites selected near the capital cities often lack access to affordable and convenient methods of transportation. Owning a car might be a far dream, calling a taxi costs more than a day’s wage, and buses are time consuming. When the need to travel persists, informal transportation usually becomes the best option.  

#### Transportation Options  

![transportation options comparison](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/forms of transportation comparison.jpg)

For this catalog, options of transportation from the neighboring towns to their capital cities are shown, and for reference, the median monthly income for each capital city is provided. We can see that taking buses is time consuming, driving is not feasible, and taxis are very expensive. No matter how the residents of the neighboring towns travel, there are always limitations.

<sub>Gas means the amount of gas money required to make such a trip. Buses and Taxis are either formal or informal. All info is extracted from the Rome2Rio website.</sub>

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


![Epworth transportation](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/transportation comparison examples_Epworth.jpg)

For traveling from Epworth to Harare, the informal bus (shown as taxi here) only costs 1 dollar, but the official taxi (shown as taxi via Epworth) costs 25-30 dollars. In addition, the informal bus stops on the edge of the town, requiring people to walk a significant distance before they can get to the minibus stop, whereas the official taxi goes directly into the town. This is common across many towns. 

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


![Alem Gena transportation](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/transportation comparison examples_Alem Gena.jpg)
For traveling from Alem Gena to Addis Ababa, driving with a car only takes 19 minutes, while taking the bus requires 5 hours, an astonishingly long trip.

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)


#### Informal Transit Conditions  

![informal transportation images](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/informal transportation example.jpg)

Informal buses constitute a significant part of the transportation systems in and around these capital cities, and all of them are being referred to differently. 

- Accra, Ghana: Trotro <sub>(lucianf, "lfip_090828_0461," Photograph, August 28, 2009, Flickr, https://www.flickr.com/photos/lucianf/4669380925/in/photostream/)</sub>
- Addis Ababa, Ethiopia: Minibus Taxi <sub>(Ryan Kilpatrick, "Minibus taxi in Addis," Photograph, December 18, 2011, Flickr, https://www.flickr.com/photos/rkilpatrick21/6530701729)</sub>
- Cairo, Egypt: Microbus <sub>(Robert Johnson, "Getting off the micro bus," Photograph, April 4, 2013, Business Insider, https://www.businessinsider.com/the-cairo-micro-bus-hand-signals-2013-4)</sub>
- Harare, Zimbabwe: Mushikashika (Pirate Taxis) <sub>(Sharon Buwerimwe, "Pirate taxis in the CBD also known as Mushikashika," Photograph, March 28, 2023, NewsDay Zimbabwe, https://www.newsday.co.zw/local-news/article/200009401/police-intensify-crackdown-on-pirate-taxis)</sub>
- Nairobi, Keyna: Matatus <sub>(ack Kavanagh, "Catching a matatu in Nairobi, Kenya," Photograph, December 19, 2018, UN environment programme, https://www.unep.org/news-and-stories/story/nairobi-matatus-odd-engine-idling-culture-pollutes-harms-health)</sub>


![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 2-01.png)

### Project Limitations & Call for Further Research  

This study offers a glimpse into the built environment and transportation conditions in areas with urban clusters lacking infrastructural light and reliant on informal buses. While the methodology and findings provide an initial basis for further research, the limitations of this project suggest several directions for future investigation.

#### Distanced Perspective  

One significant limitation of this study is the distanced perspective adopted in examining cities and their urban patterns. While this approach enables research on a larger scale, it may overlook essential details only visible through close examination. For instance, this project uses identical filtering thresholds for nighttime light and population data for all selected case study areas, which has advantages and limitations. While the consistent thresholds enable the identification of urban clusters and comparison of different cities at a continental level, they may lead to the loss of granularity of city characteristics. For example, Kibera, an area in Nairobi, was classified as "well-lighted" in this study, despite lacking fundamental infrastructure. Future research could consider varying filtering thresholds to reflect cities' unique demographics and conditions, enabling a more accurate depiction of urban patterns and findings.This limitation also highlights the need for qualitative research and firsthand experience in overlooked areas to obtain a more comprehensive understanding of these regions' population characteristics and infrastructure.




#### Data Availability

The availability of data also impacted this project's case study selection. Some countries lack existing datasets for certain variables, such as informal bus routes maps and population data, which limits the project's scope and case study selections. Moreover, the limited availability of qualitative data for selected towns and cities in Africa suggests the need to gather more qualitative data in under-studied areas to provide a more robust evidence base for future research. Overall, this study calls for more data and research to deepen our understanding of complex urban environments that remain under-researched.


![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 2-01.png)

### Conclusion  

This project is a tapestry woven with threads of discovery, striving to reveal the hidden stories that lay beyond the surface of existing datasets. While the nightlight satellite imagery taken at 1am may typically reflect population density and economic activity, it often overshadows the realities of those who are excluded from basic amenities–those who live and travel in the dark. By layering this imagery with global gridded population density, informal bus routes, and building footprints in five African cities and their surroundings, we witness the tenacious, mobile, and adaptive spirit of humanity, and shed light on the stories of lives and the inequitable access to fundamental resources in these areas. Our aim is to empower new voices, provoke new research, and catalyze action towards designing and developing cities that provide equitable access to infrastructure for all.

![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 2-01.png)


### Bibliography

#### Literature  
Atwood, Atwood. 2016. “Zimbabwe’s Unstable Infrastructure.” Sphere Journal for Digital Cultures #3 Unstable Infrastructures (June). https://spheres-journal.org/contribution/zimbabwes-unstable-infrastructure/.


Diller Scofidio + Renfro, Laura Kurgan, Robert Gerard Pietrusko. 2018. Center for Spatial Research. In Plain Sight. Video, 12:24. https://vimeo.com/290575503. 


Elvidge, Christopher D., Jeffrey Safran, Benjamin Tuttle, Paul Sutton, Pierantonio Cinzano, Donald Pettit, John Arvesen, and Christopher Small. 2007. “Potential for Global Mapping of Development via a Nightsat Mission.” GeoJournal 69 (1/2): 45–53.


Foster, Hugo, and Lechler Marie. 2022. “How Nighttime Lights Illuminate Economic Activity.” S&P Global (blog). November 7, 2022. https://www.spglobal.com/marketintelligence/en/mi/research-analysis/how-nighttime-lights-illuminate-economic-activity.html. 


Liu, Haoyu, Xianwen He, Yanbing Bai, Xing Liu, Yilin Wu, Yanyun Zhao, and Hanfang Yang. 2021. “Nightlight as a Proxy of Economic Indicators: Fine-Grained GDP Inference around Chinese Mainland via Attention-Augmented CNN from Daytime Satellite Imagery.” Remote Sensing 13 (11): 2067. https://doi.org/10.3390/rs13112067. 


Ndlovu, Ray, and Archana Narayanan. 2023. “Zimbabwe Plans a New City for the Rich.” Bloomberg.Com, January 26, 2023. https://www.bloomberg.com/news/features/2023-01-26/zimbabwe-plans-a-new-city-for-the-rich-as-harare-decays.


Zhao, Min, Yuyu Zhou, Xuecao Li, Wenting Cao, Chunyang He, Bailang Yu, Xi Li, Christopher D. Elvidge, Weiming Cheng, and Chenghu Zhou. 2019. “Applications of Satellite Remote Sensing of Nighttime Light Observations: Advances, Challenges, and Perspectives.” Remote Sensing 11 (17): 1971. https://doi.org/10.3390/rs11171971. 


![continent map](/conflict_urbanism_sp2023/images/Those Who Live and Travel in the Dark Images/break 1-01.png)

#### Datasets
**Worldwide Datasets**

C. D. Elvidge, M. Zhizhin, T. Ghosh, F-C. Hsu, "Annual time series of global VIIRS nighttime lights derived from monthly averages: 2012 to 2019", Remote Sensing (In press). Accessed April 29, 2023. Retrieved from https://eogdata.mines.edu/products/vnl/ 


Center for International Earth Science Information Network - CIESIN - Columbia University. 2020. Gridded Population of the World, Version 4 (GPWv4): Population Density Adjusted to Match 2015 Revision UN WPP Country Totals, Revision 11. Palisades, New York: NASA Socioeconomic Data and Applications Center (SEDAC). Retrieved from https://doi.org/10.7927/H4F47M65. https://sedac.ciesin.columbia.edu/data/collection/gpw-v4 


Microsoft. “GlobalMLBuildingFootprints.” GitHub. Accessed April 29, 2023. Retrieved from https://github.com/microsoft/GlobalMLBuildingFootprints/ 


Google. "Open Buildings." Accessed April 29, 2023. Retrieved from https://sites.research.google/open-buildings/#download.  


Datum. "Mapeo Digital de Transporte Publico: Casos de Estudio." Accessed April 29, 2023. Retrieved from https://datum.la/mapeo-digital-de-transporte-publico-casos-de-estudio. 


U.S. Geological Survey, “Landsat-8 Image”. Accessed April 29, 2023. Retrieved from https://www.usgs.gov/landsat-missions/landsat-data-access 


**City/Town Specific Datasets**

*Accra:*
Angel, Shlomo. Parent, Jason. Civco, Daniel L.. Blei, Alejandro M. (2012). Administrative Boundaries, Accra, Ghana, 1990. [Shapefile]. Lincoln Institute of Land Policy. Retrieved from https://earthworks.stanford.edu/catalog/stanford-sh681sw5018 


The Humanitarian Data Exchange, OCHA Regional Office for West and Central Africa (ROWCA), “Ghana - Subnational Administrative Boundaries.” Accessed April 29, 2023. Retrieved from https://data.humdata.org/dataset/cod-ab-gha 


*Addis Ababa:*
The Humanitarian Data Exchange, OCHA Regional Office for West and Central Africa (ROWCA), “Ethiopia - Subnational Administrative Boundaries.” Accessed April 29, 2023. Retrieved from https://data.humdata.org/dataset/cod-ab-eth 


*Cairo:*
The Humanitarian Data Exchange, OCHA Regional Office for West and Central Africa (ROWCA), “Egypt - Subnational Administrative Boundaries.” Accessed April 29, 2023. Retrieved from https://data.humdata.org/dataset/cod-ab-egy 


*Harare:*
The Humanitarian Data Exchange, OCHA Regional Office for West and Central Africa (ROWCA), “Zimbabwe - Subnational Administrative Boundaries.” Accessed April 29, 2023. Retrieved from https://data.humdata.org/dataset/cod-ab-zwe


*Nairobi:*
Code for Kenya, "Kenya Counties Shapefile." Created October 21, 2015. Accessed April 29, 2023. https://africaopendata.org/dataset/kenya-counties-shapefile. 
UN Humanitarian Data Exchange, “Kenya Sub Counties.” Created October 21, 2015. Accessed April 29, 2023. Retrieved from https://data.amerigeoss.org/dataset/kenya-sub-counties 





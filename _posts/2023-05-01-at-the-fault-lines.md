---
layout: post
date:   2020-05-01
image: "/conflict_urbanism_sp2023/images/At the Fault Lines/atfl_logo.png"
title:  "At the Fault Lines: Developing an Alternative Earthquake Risk Assessment Method for Istanbul's Building Stock"
author: "Taha Erdem Ozturk"
---
#### **INTRODUCTION**  

On February 6, 2023, two consecutive earthquakes of Magnitudes 7.8 and 7.7 struck Southern Turkey and Northern Syria, killing more than 52,000 people. Namely the Kahramanmaras Earthquake is the largest since the 1939 Erzincan Earthquake with the same magnitude, and the second largest that’s ever recorded in the region. Affecting 14 million people and leaving 1.5 million people homeless across 21 provinces, it is now accepted as the deadliest natural disaster in the history of the country.

![Turkey Fault Lines](/conflict_urbanism_sp2023/images/At the Fault Lines/faultLine.png)
*Turkey Sits on Top of Two Major Fault Lines, One of The Most Seismically Active Countries in the World*  

Yet, Turkey is no stranger to such catastrophic earthquakes, as the country geographically sits on top two major fault zones - the North Anatolian fault zone being one of the most seismically active in the World. 20 years ago when a similarly destructive earthquake struck near Istanbul, the country’s economic and population center, it was a wake up call for the country: The government changed shortly after being deemed “incompetent,” much stricter building codes and regulations were put in place, nation-wide first response organizations were founded, and a new “earthquake tax” was introduced to help fund urban renewal and recovery efforts.

However, the recent earthquakes exposed that many of these efforts have been immensely inadequate, mostly due to large-scale corrupt political, regulatory, and construction practices throughout the 20-year AKP rule. Moreover, the country’s most prominent scientists have been incessantly alarming against a long-awaited “Istanbul Earthquake” to strike in the next decade, with consequences exponentially graver. This study aims to dissect these corrupt practices, identify their traces in the architectural level across an urban scale, and develop an alternative risk assessment mapping method that may offer critical insight for local authorities, municipalities, as well as individuals.


#### **PROJECT SCOPE**

This project aims to create a crowdsourced building-scaled earthquake risk map to alleviate some of these issues and offer an informative platform for the public and the authorities. By using an interactive online map, users and data collectors can survey some certain building characteristics that, when combined, may offer valuable information regarding the structural quality of the building stock. Although it may not be as accurate as a structural analysis, this method offers a fast and highly scalable alternative to map and visualize the earthquake-prone buildings in the city.

#### **RESEARCH QUESTION**

The February 6 earthquakes have shown us that a particular building type (or building characteristics due to common construction malpractices) are known to be particularly more under risk during an earthquake. Given some of these characteristics could be visually identified without requiring a structural assessment, could we identify these in a pilot neighborhood using crowd-sourcing data collection methods, and then train a machine learning model that could automatically identify these on Google StreetView images?

#### METHODOLOGY

![Methodology Diagram](/conflict_urbanism_sp2023/images/At the Fault Lines/atfl_methodology.png)  

The above diagram illustrates the main framework of the methodology behind the alternative risk assessment mapping technique in five steps. 

1. ******************************Geospatial Data******************************
    1. This step sets a common base for all following steps by cleaning up and bringing together all required geospatial (building footprints, administrative borders, roads, highways, sidewalks, parks, and transportation infrastructure) in GIS. Building footprints are mainly obtained through Istanbul Technical University’s UYGAR 2D AutoCAD DWG maps. Although these maps are highly accurate, they also include unnecessary amounts of information (unnecessary text layers, urban furniture and items such as streetlight and manhole locations) — hence it is critical for DWG files to be cleaned up before importing into GIS. 
    
    Additionally, these maps may need to be supported with Microsoft Planetary Computer Building Footprint dataset for unregistered buildings that are not present on the 2D map drawings. Two datasets combined and georeferenced correctly on the GIS workspace, this first step is critical to create a base dataset that will allow collaborators to add their on-site observations. 
2. **********************Building Data**********************
    1. The aforementioned 2D map drawings also include building and location information like post codes, location and address identifiers, building numbers, and number of floors. However, these exist as text objects nested within the polylines that represent each building’s footprint. Although QGIS does not have a tool for linking these text objects with the geometry they are nested inside, there may be 3rd-party plug-ins to automatically combine building data with the geometry.
    
    The below data entries are essential to identify each building:
        1. Pafta/Ada numbers (location and neighborhood administrative border identifiers)
        2. Building number (local street identifier),
        3. Number of floors/building height,
        4. Year of construction (if available, this is very useful to determine the specific Building Code under which the building was constructed — as buildings constructed before 1999 Earthquake are considered to constitute “high risk of failure during an earthquake”)
3. ************************************************************************************************Crowdsourced Pilot Building Risk Assessment Data and Labeling************************************************************************************************
    1. Once the building stock is digitized, the project relies on data collectors for creating the pilot building risk assessment dataset. This step utilizes an online data-collection service such as Kobo Toolbox, to allow multiple users to simultaneously add additional data entries to the geospatial building data. 
    
    Data collectors are expected to photograph the front-facing facade of every building, and fill in four questions for each building:
    
    1. Are there any visible cracks on the building?
    2. Are there any removed vertical supporting elements on the ground floor?
    3. Does the building have a soft floor?
    4. Are there any visible signs of sea-sand based cement usage?
    
    These questions are based on the most common construction malpractices that is known to contribute to a structural failure during an earthquake, and are usually easy to detect with naked eye without a structural assessment. 
    
4. ********Pilot Neighborhood Dataset********
    1. Once all the buildings in the selected pilot neighborhood is digitized and labeled as mentioned in Step 3, the merged data is used to visualize an interactive risk analysis map as well as used to train the Risk Assessment Model. The ML model is trained through comparing the building images with crowdsourced binary labels. 
5. **********************************************City-wide ML Risk Assessment Model**********************************************
    1. Once the ML model is able to accurately detect the aforementioned building features that may constitute structural failure risk, it may be further trained on Google StreetView images, and later be used to generate a city-wide risk assessment map. 

---

**DATA SOURCES**

1. This project heavily relies on online data collection tools like Kobo Toolbox, and crowdsourced data collection methods. Creating an online data collection tool on an up-to-date city map, where collectors can access each building’s location, image, address, and door number.
    - **Istanbul Technical University’s UYGAR Maps** are high-detail 2D maps in AutoCAD DWG format. This dataset includes building numbers, floor and height data, as well as zoning data. This dataset is by far the most reliable despite requiring DWG-GIS conversion processes.
    - **Istanbul Metropolitan Municipality’s BIMTAS Building Stock dataset** is the most up-to-date, detailed GIS/ShapeFile building stock dataset, however this is not open for public/academic use.
    - **OpenStreetMaps** has a fairly detailed GIS/ShapeFile dataset that covers a wide landmass across the city, however these are not consistent and far from complete.
    - **Garmin Maps** has a detailed GIS/ShapeFile dataset, however there are some ShapeFile geometry issues - some buildings/areas are corrupt, hence cannot be used.
    - **Microsoft Planetary Computer** **Building Footprint Dataset** is another alternative dataset that uses specialized ML models to generate building footprints from satellite imagery. This could be a valuable tool to obtain building shape data in certain neighborhoods where many buildings are purposefully not registered to the municipality’s system to avoid regulations.
2. Each building should be labeled with certain “risk assessment identifiers”, such as whether the building has visible cracks, protruding elements, or removed columns. These images and labels will later be used to train a machine learning model. 
    - **Creating synthetic data (computationally generated synthetic building dataset based on the crowdsourced and labeled building data)** to further train the risk assessment model. This method is quite common in training machine learning models with limited datasets, and increases accuracy of the model.
3. The machine learning model could further be trained on Google StreetView imagery after the initial training on crowd-sourced labeled dataset. 
    1. **Google StreetView** has a very up-to-date street imagery of Istanbul, which can later be used with the ML-based model to generate an risk assessment map without the need of a crowdsourcing method.
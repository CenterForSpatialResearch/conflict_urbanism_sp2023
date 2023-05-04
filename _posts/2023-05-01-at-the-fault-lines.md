---
layout: post
date:   2020-05-01
image: "/conflict_urbanism_sp2023/images/At the Fault Lines/atfl_logo.png"
title:  "At the Fault Lines: Developing an Alternative Earthquake Risk Assessment Method for Istanbul's Building Stock"
author: "Taha Erdem Ozturk"
---
![At the Fault Lines](/conflict_urbanism_sp2023/images/At the Fault Lines/atfl_logo.png)

#### **INTRODUCTION**  

On February 6, 2023, two consecutive earthquakes of Magnitudes 7.8 and 7.7 struck Southern Turkey and Northern Syria, killing more than 52,000 people. Namely the Kahramanmaras Earthquake is the largest since the 1939 Erzincan Earthquake with the same magnitude, and the second largest that’s ever recorded in the region. Affecting 14 million people and leaving 1.5 million people homeless across 21 provinces, it is now accepted as the deadliest natural disaster in the history of the country.

![Turkey Fault Lines](/conflict_urbanism_sp2023/images/At the Fault Lines/faultLines.png)
*Turkey Sits on Top of Two Major Fault Lines, One of The Most Seismically Active Countries in the World*  

Yet, Turkey is no stranger to such catastrophic earthquakes, as the country geographically sits on top two major fault zones - the North Anatolian fault zone being one of the most seismically active in the World. 20 years ago when a similarly destructive earthquake struck near Istanbul, the country’s economic and population center, it was a wake up call for the country: The government changed shortly after being deemed “incompetent,” much stricter building codes and regulations were put in place, nation-wide first response organizations were founded, and a new “earthquake tax” was introduced to help fund urban renewal and recovery efforts.

However, the recent earthquakes exposed that many of these efforts have been immensely inadequate, mostly due to large-scale corrupt political, regulatory, and construction practices throughout the 20-year AKP rule. Moreover, the country’s most prominent scientists have been incessantly alarming against a long-awaited “Istanbul Earthquake” to strike in the next decade, with consequences exponentially graver. This study aims to dissect these corrupt practices, identify their traces in the architectural level across an urban scale, and develop an alternative risk assessment mapping method that may offer critical insight for local authorities, municipalities, as well as individuals.


#### **PROJECT SCOPE**

This project aims to create a crowdsourced building-scaled earthquake risk map to alleviate some of these issues and offer an informative platform for the public and the authorities. By using an interactive online map, users and data collectors can survey some certain building characteristics that, when combined, may offer valuable information regarding the structural quality of the building stock. Although it may not be as accurate as a structural analysis, this method offers a fast and highly scalable alternative to map and visualize the earthquake-prone buildings in the city.


#### **RESEARCH QUESTION**

The February 6 earthquakes have shown us that a particular building type (or building characteristics due to common construction malpractices) are known to be particularly more under risk during an earthquake. Given some of these characteristics could be visually identified without requiring a structural assessment, could we identify these in a pilot neighborhood using crowd-sourcing data collection methods, and then train a machine learning model that could automatically identify these on Google StreetView images?


#### **UNDERSTANDING THE COLLAPSE**

<iframe src="https://player.vimeo.com/video/823901043?h=38b5dd5dee" width="640" height="1128" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

Many videos and photos like the one above from the moment of collapse all hint at a common type of structural failure: First, the ground floor suddenly collapses, followed by all the floors above shortly after, pancaking on top of each other layer by layer in just a matter of seconds.

![Dissecting a Pancake Collapse](/conflict_urbanism_sp2023/images/At the Fault Lines/pancake-collapse.png)

These "pancake collapses" are recognized as the primary cause of devastating consequences resulting from earthquakes in the region, such as the 1999 Golcuk earthquake, as reported by the infrastructure assessment team sent to the area. The factors leading to this phenomenon have been researched extensively and can be narrowed down to four primary construction/design shortcomings.

1. **Soft Story Buildings**
    
    Soft story buildings are multiple story buildings that has a ground floor that has large windows, wide openings, and large open commercial shopfronts where a shear wall or vertical support element would typically be needed to ensure that the structural stability. Especially in earthquake-prone areas such as Turkey, at least 30% of the ground floor area must be dedicated to structural elements to ensure that the structural system could withstand the stress of the above floors. Soft story buildings are highly common in the region, with many multi-story apartment buildings accommodate commercial floor space on the ground floor, which is allowed by mixed-used zoning practices. The 1999 quake has led to an updated building code that prohibited such structures, many developers did not feel pressed to follow the regulations due to the lack of a strictly enforced control mechanism. 
    
2. **Excessive Cantilevering Above the Ground Floor**
    
    Another common practice is excessive cantilevering above the ground floor, as this allows developers to go beyond the site land usage limitations to maximize profits over extra square footage. Although cantilevering structures are a common practice in architectural design, combined with other malpractices such as soft story building designs, or using lower-quality building materials significantly increases the structural stress on the ground-level structural system. This may lead to a structural failure in the moment of an earthquake, even when the building may be able to withstand this load under normal conditions.
    
3. **Structural Alterations**
    
    Structural alterations such as removing vertical supporting elements on the ground floor to open up space for commercial activities is another common practice many building owners employ to maximize profitability. Although there are multiple laws and regulations strictly prohibiting this, many buildings that has such alterations go unnoticed as it’s mostly done in the inside of the buildings. 
    
4. **Subpar/Prohibited Construction Materials** 
    
    > I am ‘coming from the kitchen’ in this business, as we say, meaning all my family, under my father, were also a part of this sector, the construction sector. I grew up working with him, witnessing all of the development at that time. I’m not in a position to regret what I’ve said. The fact is that 70 percent of all the settlements in Istanbul, I would say, are vulnerable to a major earthquake. This is a diagnosis. Without the proper diagnosis treating a patient is not possible. The construction materials used for various settlements in different parts of Istanbul used to be of poor quality. *-Ali Agaoglu, Turkish Real Estate Mogul*

    The 1999 Earthquake has shown that the usage of certain construction materials, such as “sea-sand mixed cement” or rebars with no ribs, can be a significant risk factor during a earthquake. Although most of these materials cannot be identified without a structural test, some easy-to-spot visual hints can offer useful information. Many locals are advised to look for sea shells on the surface of the concrete to identify whether the cement is mixed with sea-sand.


#### METHODOLOGY

![Methodology Diagram](/conflict_urbanism_sp2023/images/At the Fault Lines/atfl_methodology.png)  

The above diagram illustrates the main framework of the methodology behind the alternative risk assessment mapping technique in five steps. 

1. **Geospatial Data**
    This step sets a common base for all following steps by cleaning up and bringing together all required geospatial (building footprints, administrative borders, roads, highways, sidewalks, parks, and transportation infrastructure) in GIS. Building footprints are mainly obtained through Istanbul Technical University’s UYGAR 2D AutoCAD DWG maps. Although these maps are highly accurate, they also include unnecessary amounts of information (unnecessary text layers, urban furniture and items such as streetlight and manhole locations) — hence it is critical for DWG files to be cleaned up before importing into GIS. 
    
    Additionally, these maps may need to be supported with Microsoft Planetary Computer Building Footprint dataset for unregistered buildings that are not present on the 2D map drawings. Two datasets combined and georeferenced correctly on the GIS workspace, this first step is critical to create a base dataset that will allow collaborators to add their on-site observations.

2. **Building Data**
    The aforementioned 2D map drawings also include building and location information like post codes, location and address identifiers, building numbers, and number of floors. However, these exist as text objects nested within the polylines that represent each building’s footprint. Although QGIS does not have a tool for linking these text objects with the geometry they are nested inside, there may be 3rd-party plug-ins to automatically combine building data with the geometry.
    
    The below data entries are essential to identify each building:
        1. Pafta/Ada numbers (location and neighborhood administrative border identifiers)
        2. Building number (local street identifier),
        3. Number of floors/building height,
        4. Year of construction (if available, this is very useful to determine the specific Building Code under which the building was constructed — as buildings constructed before 1999 Earthquake are considered to constitute “high risk of failure during an earthquake”)

3. **Crowdsourced Pilot Building Risk Assessment Data and Labeling**
    Once the building stock is digitized, the project relies on data collectors for creating the pilot building risk assessment dataset. This step utilizes an online data-collection service such as Kobo Toolbox, to allow multiple users to simultaneously add additional data entries to the geospatial building data. 
    
    Data collectors are expected to photograph the front-facing facade of every building, and fill in four questions for each building:
    
    1. Are there any visible cracks on the building?
    2. Are there any removed vertical supporting elements on the ground floor?
    3. Does the building have a soft floor?
    4. Are there any visible signs of sea-sand based cement usage - such as visible sea shells on the surface?

4. **Pilot Neighborhood Dataset**
    Once all the buildings in the selected pilot neighborhood is digitized and labeled as mentioned in Step 3, the merged data is used to visualize an interactive risk analysis map as well as used to train the Risk Assessment Model. The ML model is trained through comparing the building images with crowdsourced binary labels.

5. **City-wide ML Risk Assessment Model**
    Once the ML model is able to accurately detect the aforementioned building features that may constitute structural failure risk, it may be further trained on Google StreetView images, and later be used to generate a city-wide risk assessment map. 


![KoboToolbox-powered Online Survey System](/conflict_urbanism_sp2023/images/At the Fault Lines/kobotoolbox-survey.gif)  

**DATA SOURCES**

![Various different maps merged and cleaned up into one single GIS basemap](/conflict_urbanism_sp2023/images/At the Fault Lines/istanbul-maps.png)  

1. This project heavily relies on online data collection tools like Kobo Toolbox, and crowdsourced data collection methods. Creating an online data collection tool on an up-to-date city map, where collectors can access each building’s location, image, address, and door number.
    - **Istanbul Technical University UYGAR Maps** are high-detail 2D maps in AutoCAD DWG format. This dataset includes building numbers, floor and height data, as well as zoning data. This dataset is by far the most reliable despite requiring DWG-GIS conversion processes.
    - **Istanbul Metropolitan Municipality’s BIMTAS Building Stock dataset** is the most up-to-date, detailed GIS/ShapeFile building stock dataset, however this is not open for public/academic use.
    - **OpenStreetMaps** has a fairly detailed GIS/ShapeFile dataset that covers a wide landmass across the city, however these are not consistent and far from complete.
    - **Garmin Maps** has a detailed GIS/ShapeFile dataset, however there are some ShapeFile geometry issues - some buildings/areas are corrupt, hence cannot be used.
    - **Microsoft Planetary Computer** **Building Footprint Dataset** is another alternative dataset that uses specialized ML models to generate building footprints from satellite imagery. This could be a valuable tool to obtain building shape data in certain neighborhoods where many buildings are purposefully not registered to the municipality’s system to avoid regulations.
2. Each building should be labeled with certain “risk assessment identifiers”, such as whether the building has visible cracks, protruding elements, or removed columns. These images and labels will later be used to train a machine learning model. 
    - **Creating synthetic data (computationally generated synthetic building dataset based on the crowdsourced and labeled building data)** to further train the risk assessment model. This method is quite common in training machine learning models with limited datasets, and increases accuracy of the model.
3. The machine learning model could further be trained on Google StreetView imagery after the initial training on crowd-sourced labeled dataset. 
    1. **Google StreetView** has a very up-to-date street imagery of Istanbul, which can later be used with the ML-based model to generate an risk assessment map without the need of a crowdsourcing method.
---
title: "SR 542 Deming Community Survey: Data Collection and O-D Routing Pilot"
date: 2022-09-13
layout: post
---

In July and August 2022, I piloted the first public ArcGIS Survey 123 survey at WSDOT. Generally speaking, planning studies in the Northwest Region tend to utilize SurveyMonkey or other similar web platforms without the ability to collect spatial data - unless consultants or partners provide access to more sophisticated tools. 

Using Survey123 allowed our planning team to collect GIS point data from survey respondents on specifically where their trips originate and end. Survey respondents could choose a specific location such as their home building footprint, or a more general area. Creating repeats in Survey 123 Connect allowed us to collect multiple data points in one survey. 

After the survey closed in September 2022, three point data feature classes had been generated from Survey 123: A trip origin feature class, trip destination feature class, and general "transportation challenge" feature class where survey respondents had marked their most pressing issue along the corridor and chosen descriptive categories to identify why the location was a challenge. These feature classes were linked to the rest of the survey questions by a common GlobalID key. 

The trip origin and destination feature classes were uploaded into ArcGIS Online and analyzed using the "Connect Origins to Destinations" tool: 

<img src="https://raw.githubusercontent.com/katiebunge/gisportfolio/main/RouteTool.PNG">

Routes were generated using the ESRI street network using the "rural drive time" criteria and matched via the common GlobalID key. Some trips were not generated as points inputted by users could not be routed to the street network. 

I then filtered the route data for various criteria including trips traveling directly to the study area of Deming, WA, trips originating in or east of Deming along SR 542 (Mount Baker Highway), and trips originating outside the community. By applying a very low transparency to each route line, a "heat map" effect was approximated: 

<img src="https://raw.githubusercontent.com/katiebunge/gisportfolio/main/assets/images/EWhatcomTrips.png">
A heat map of survey respondent estimated trips originating in eastern Whatcom County, WA

<img src="https://raw.githubusercontent.com/katiebunge/gisportfolio/main/assets/images/TripsToDeming.png">
A heat map of survey respondent estimated trips traveling to Deming, WA

This work is still underway. My hope is that we can develop an interactive data explorer to communicate survey results to the public at our in-person open house. Some limitations are that some members of the public did have difficulty responding to the survey with the online and web map format. In particular, this survey format was not friendly for mobile devices. In a highly rural community such as Deming, it is possible that more people were responding via mobile devices than on a desktop computer, if broadband access is limited. Age and ability gaps also contributed to some issues answering the survey questions. 

# UGSRP-2022-Floodnet
This repo contains all the work done when working as a summer research intern for the NYU FloodNet team through NYU Tandon's Undergraduate Summer Research Program.

**Table of Contents:**
- [Introduction](#introduction)
- [Sensor Deployment Location Identification](#sensor-deployment-location-identification)
- [Data Filters](#data-filtering)
   - [1.ML Model Data Labelling](#1-ml-model-data-labelling)
   - [2.Analysing Filter Performance](#2-analysing-filter-performance)
- [Data Analysis](#data-analysis)
   - [1.Tidal Analysis](#1-tidal-analysis)
   - [2.Floodnet, Floodwatch and 311 Data](#2-floodnet-floodwatch-and-311-data)
 
## Introduction
   The Floodnet project is a cooperative of communities across NYC working towards collecting real time flooding data that could aid in understanding urban flooding caused by extreme precipitation, tidal events, and the combination of both. As under graduate researchers we focused on analysing data from FloodNet sensors and other community-based data sources like Floodwatch and 311 Complaints. Unlike these sources, which depend on communities to report flooding events, Floodnet uses ultrasonic sensors deployed in different parts of the city to detect flood depth. 

## Sensor Deployment Location Identification
   As a part of the project expansion to all five boroughs, sensor deployment locations in Staten Island were identified. Deployment locations depend on several criteria, the most important being elevation and flood susceptibility, proximity to gateway, and availability of sunlight. Flood susceptibility was gauged based on moderate event flooding on NYC Stormwater Flood maps. Once an area was selected, Google maps was used to scout mounting posts. Documentation was created with information on each of the criteria along with streetview and map images of the sign post location. 
![deployment](https://user-images.githubusercontent.com/105950235/183995501-652b2840-4e58-47ce-9b02-1a4f5c28a8c1.jpg)
<p align='center'>
   Figure 1: Flooding Profile, Streetview, and Map Images for Sensor Deployment
</p>

## Data Filters
### 1. ML Model Data Labelling
   Since the sensors are deployed on sign posts across the city, they are subject to a lot of noise caused by people or things underneath the sensor. In order to isolate non-flood events, a machine learning model was built by a member of the team. Preliminary work for the model included labelling the data collected by the sensors into different classes: flood, single peak, pulse chain, box, snow, and noise. This dataset included start and end times for each event, its class, and the sensor it was recorded on. 

### 2. Analysing Filter Performance
   Two filters are placed on the data in order to minimize the number of non-flood events shown in the sensor data, making it easier to read and undersand. The first is a range filter that gets rid of any values below 1 centimeter as well as values that are at or above the sensor height. The second is a gradient filter that clears any points with a sudden and large increase of 12 inches per minute or faster. In order to improve these filters and potentially create new filters that would help clean up the data, calculations were made to see how each filter performed, and what factors led them to perform better or worse.

## Data Analysis
The FloodNet sensors are able to produce thorough and reliable sets of data for locations across the five boroughs that include specific timestamps and flood depths. This information was used to better understand causes of floods, and to compare with other datasets the city uses. 

### 1. Tidal Analysis
NYC is a coastal city, meaning it is susceptible to pluvial flooding, caused by precipitation, as well as tidal flooding, caused by high tides. Some FloodNet sensors are placed at coastal locations that primarily sense tidal floods. The data from these sensors were compared to tidal data from the United States Geological Survey (USGS) to understand the extent to which tide heights correlate to tidal flood depth, as well as what other factors may be invloved.

### 2. FloodNet, Flood Watch and 311 Data
The community Flood Watch project and 311, NYC's open data source, are two sources of flood data that rely on community action to track flooding and flood risk. These were compared to FloodNet data to understand how well these sources were able to report floods, and how FloodNet allows for more reliable and more informative data on flooding.  

   

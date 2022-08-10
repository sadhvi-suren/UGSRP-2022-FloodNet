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

## Data Analysis


### 1. Tidal Analysis

### 2. Floodnet, Floodwatch and 311 Data
   

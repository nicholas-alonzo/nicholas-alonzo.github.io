---
title: "UFO Sightings & Natural Disasters: A Coincidence?"
summary: "In this analysis, we explore UFO sightings and declared natural disasters in the United States from the years 1965 to 2013"
date: 2017-03-22
---

<details>
<summary>How the background image was generated</summary>

- Software: Amuse
- Prompt: an illustration of a ufo flying over a forest at dawn
- Model: Juggernaut XL v11
- Inference Steps: 20
- Guidance Scale: 6.00
- Seed: 1157435293

</details>

## Data Background & Description

In this analysis, we explore UFO sightings and declared natural disasters in the United States from the years 1965 to 2013. The original UFO sightings data was scraped from the National UFO Reporting Center Database (NUFORC) and uploaded to Kaggle for download. The download came with 2 files (complete and scrubbed); the scrubbed version was used. The original disasters data was downloaded from the Federal Emergency Management Agency (FEMA) and has full documenation.

Since both data sets started off unrelated, time was spent pre-processing to connect them by state regions, divisions, or counties. Below is a summary of what was done.

#### UFO Sightings
Retrieve ZIP Codes for cities by reverse geocoding latitude with Google's Geocoding API via Python Package
Used geocoded ZIP Codes to match ZIP Codes in a ZIP Code Database to retrieve county names
Used matched county names to match county names in FIPS download to retrieve FIPS
Added state region and division attributes with State table download

#### Disaster Declaration
Geocoded county and state to get latitude and longitude using Google's Geocoding API via Python Package
Used county names to match county names and FIPS from FIPS download
Added state region and division attributes with State table download

#### Downloaded Resources List
Google's Geocoding API via Python Package
Zip Code Database Download
FIPS Download
State Table Download

## Objective & Analysis Overview
There has been talk of UFOs appearing when disasters strike in articles and blogs covered by UFO fanatics to even National Geographic. Our objective is to determine whether there is in fact some overlap between the two to gain a better understanding of this phenomenon. We first analyzed the data sets seperately beforing comparing both.

## Exploring UFO Sightings

### Mapping UFO Sightings

From the top left map numerous sightinings can be observed in the Pacific West and across the Midwest, Northeast, and South Regions of the United States. It helps give a general overview where most sightings have been occuring, in this case the East Coast. The top right map however, displays circles corresponding to reported sightings with the size representing the number of reports received at that specific location. Larger circles appear in Washington, the Southern West Region, Texas, the Great Lakes in the East North Central Division, Florida, and in the North East Region by New York and New Jersey. Let's now look at all sightings by state.


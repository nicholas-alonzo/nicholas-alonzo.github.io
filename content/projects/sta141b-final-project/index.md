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

In this analysis, we explore UFO sightings and declared natural disasters in the United States from the years 1965 to 2013. The original UFO sightings data was scraped from the [National UFO Reporting Center Database (NUFORC)](http://www.nuforc.org/webreports.html) and uploaded to [Kaggle](https://www.kaggle.com/NUFORC/ufo-sightings) for download. The download came with 2 files (complete and scrubbed); the scrubbed version was used. The original disasters data was downloaded from the [Federal Emergency Management Agency (FEMA)](https://www.fema.gov/openfema-dataset-disaster-declarations-summaries-v1) and has full documenation.

Since both data sets started off unrelated, time was spent pre-processing to connect them by state regions, divisions, or counties. Below is a summary of what was done.

### UFO Sightings
- Retrieve ZIP Codes for cities by reverse geocoding latitude with Google's Geocoding API via Python Package
- Used geocoded ZIP Codes to match ZIP Codes in a ZIP Code Database to retrieve county names
- Used matched county names to match county names in FIPS download to retrieve FIPS
- Added state region and division attributes with State table download

### Disaster Declaration
- Geocoded county and state to get latitude and longitude using Google's Geocoding API via Python Package
- Used county names to match county names and FIPS from FIPS download
- Added state region and division attributes with State table download

### Downloaded Resources List
- [Google's Geocoding API via Python Package](https://github.com/DenisCarriere/geocoder)
- [Zip Code Database Download](https://www.unitedstateszipcodes.org/zip-code-database/)
- [FIPS Download](https://www.census.gov/geo/reference/codes/cou.html)
- [State Table Download](https://statetable.com/)

---

## Objective & Analysis Overview
There has been talk of UFOs appearing when disasters strike in articles and blogs covered by UFO fanatics to even National Geographic. Our objective is to determine whether there is in fact some overlap between the two to gain a better understanding of this phenomenon. We first analyzed the data sets seperately beforing comparing both.

<!-- table -->

<!-- image -->

---

## Exploring UFO Sightings

### Mapping UFO Sightings

<!-- 2 images -->

From the top left map numerous sightinings can be observed in the Pacific West and across the Midwest, Northeast, and South Regions of the United States. It helps give a general overview where most sightings have been occuring, in this case the East Coast. The top right map however, displays circles corresponding to reported sightings with the size representing the number of reports received at that specific location. Larger circles appear in Washington, the Southern West Region, Texas, the Great Lakes in the East North Central Division, Florida, and in the North East Region by New York and New Jersey. Let's now look at all sightings by state.

<!-- image -->

States shaded darker in the map above have had more reported sightings across the years 1965 - 2013. The table below summarizes the map into the top 5 states with most reported sightings and the top 5 cities that contributed to their sightings count.

<!-- table -->

As you can see from the map and table, California has the most reported sightings across all states. Referring back to the map of sightings clustered by location, you can see the size and location of the circles indeed correspond to where Los Angeles, San Diego, Sacramento, San Jose, and San Francisco would be. In fact according to Wikipedia, the cities listed in the table are among California's top largest cities by population. We can make a similar conclusion that the other cities are the most populous for their states. It's a no-brainer; high population cities = more reported sightings.

### UFO Sightings Over Time

<!-- chart - daily sightings -->

You can see fluctuations taking place sometime in middle of every year from 1965 - 2013. You'll notice that before 1995 reported sightings never exceeded 50 counts on any given day. After 1995 there's a significant increase of sightings onwards where some huge spikes lie. There's an obvious trend happening across each years, however, this plot can be a bit difficult to gain insight when looking at the data daily. Let's look into the sightings by month.

<!-- chart - sightings by month -->

Here, all sightings from 1965 - 2013 were aggregated into one monthly plot. You can see a large increase beginning in May with the highest peak in July as it lowers down into August. Looking back at the previous plot, we now know that May - August account for the fluctuations seen across each year. In the previous section of Mapping UFO Sightings, we found that larger cities suggest more sighitngs. Now to add in the rise of sightings, the months May - August are associated with Summer where people are likely to be out and about.

<!-- chart - ufo shapes by region -->

Here we can see the top UFO shapes throughout each region are the same with the exception of Disk in the Northeast. This is a bit surprising as one might expect that the geography of different regions may impact the shapes seen. It may have help to look at divisions instead, as regions might be too general. However, this gives us a good overview on the main shapes being seen. Below are examples of these different reported shapes. You can click each image to take you to it's source or here to view more recoreded UFO shapes.

<!-- carousel - ufo shapes  -->

---

## Exploring Disaster Declarations

### Mapping Declared Disasters

<!-- image - declared disasters -->

In the top left map the size of each circle corresponds to the number of disasters that affected that county from 1965 - 2013. We see the majority of disaster cases and larger circles occuring in the South and North East Regions in addition to Southern California. Accumulating all the counts of affected counties by state, the map on the right clearly shows Texas counties have been affected the most throughout this time period. The table below confers this with the top 5 states with most declared disaters affecting counties.

<!-- table -->

The table is evident of the maps above where we see these states being affected all along the Gulf and East coast of the United States. This is informative, but let's break down the disater declarations further.

<!-- image - declared disasters by state counties -->

In this map we counted disaters for every county in the United States (uncolored counties were not in our data set). We can see that most counties affected by disasters follow along the Gulf Coast, but only have 8 - 24 occurences. In the bubble map that appears different, but because there is overlap between the circles. The table below shows the top 5 disaster counties.

<!-- table -->

Again, the table is clear of the map with Southern California's top 3 neighboring counties with most declared disasters. Looking into the data we find that fires make up most of these disasters. It's not too suprising as California has many fires and can be justified on FEMA's map of wildfire activity by county here. As for Collier and Monroe County in Florida they reside at the tip of the state and are more prone to Hurricanes along with the other Florida and Lousiana counties evident from the map.

<!-- chart - declared disasters over time -->

In this plot we see a low activity of declared disasters, with some ocassinaoly spikes, but more significantly we see a huge spike of affected counties in 2005 which correspond to Hurricane Katrina. You can read more about it here from the National Oceanic and Atmospheric Administration (NOAA). Below is a picture of Katrina; you can see how much area and counties the hurricane covers.

<!-- picture - noaa satellite image -->

### Disaster Types By Divisions

<!-- chart - top disaster types by top 5 divisions -->

When we look at the disasters by divisions the majority belong to the South Region, evident of the previous maps. More specifically, well over 1000 counties near in the Gulf Coast have been affected by Hurricanes from 1965 - 2013. Interestingly, looking at the West North Central and Mountain Divisions we also see Hurricane as the top count. This is because counties in these divisions were also warned of Hurricane Katrina at that time. We might say that Hurricane Katrina is an anomly across all the years of data. However, we still notice tornadoes and fires occuring.

---

## Exploring UFO Sightings & Disasters

### Mapping UFO Sightings & Disasters

<!-- chart ufo sightings & declared disasters -->

Similarly as before the size of the circles corresponds to the number of sightings and affected counties by disasters. By looking at both sightings and disasters overlayed on each other we do indeed some overlap with larger circles. We can see that major sightings area like Southern California are covered with disasters along with areas like Florida, Texas, and New York area.

<!-- chart - top county: ufo shapres & disasters -->

From analyzing the data sets we found Los Angeles, both the city and the county to have the most UFO Sightings and Disasters. In the above plots we see the breakdown. Again, the top 5 UFO shapes are Light, Triangle, Circle, Sphere and Fireball with fires and earthquakes as the top 2 disasters. Among these disasters there was a single report that mentions a disaster, specifically the Northridge Earthquake in 1994. It follows,

["About half an hour after the quake me my folks and I went outside. I was siting alone by a sand box when for some reason I decided to look up and as I looked up a huge fire ball travelling north to south went across the sky."](http://www.nuforc.org/webreports/105/S105280.html)

However the person reports it was only seconds worth, is it credible? Assuming same reported sightings is more credible let's explore the top sightings on a given day.

### Top UFO Sightings: Shapes & Disasters

Below we have the top 5 reported UFO sightings by multiple people from 1965 - 2013.

<!-- table -->

We see the top reportings occur in Tinley Park, Illinois where the first major occurence happened in August 2004. Below is one of the 27 reports made to NUFORC following from the incident and a video about the phenonmenon that occured that day.

["3 redish orange lights came out of the north and spread apart into almost a perfect triangle, then the bottom 2 seemed to connect. After this the top one started drifting upward almost hovering and then the other one did the same until they formed a perfect line in the sky and then one by one dissapeared. Then another one came 5 minutes later same thing too, except solo and started to dim and fade away just like the others. It was the weirdest thing ive ever seen. Definatly not an aircraft ive ever seen."](http://www.nuforc.org/webreports/038/S38808.html)

Another notable mention are the occurences in Pheonix, Arizona known as the Phenoix Lights. You can view a video of the occurence and interestingly enough there is a movie coming out April 2017 about the phenomenon.

<!-- youtube links -->

Since Tinley Park had the most occurences, let's look at the different diasters and UFO shapes that have occured there.

<!-- table -->

<!-- chart - cook county top 7 ufo shapes -->

Shockingly there are only 2 declared disasters for Cook County in comparison to the phenomenon that had been occuring. The dates of these disasters don't fall to close to any of the major sightings either. Looking at the UFO shapes over time, we see that Light, Circle, and Triangle appear the most in this county. There appears to be periodic behavior happening between 3rd quarter of a year and the start of a new year.

---

## Conclusion

There are plenty of UFO cases we can still look into and try and find more overlap, however even after having connected the data sets together it's hard to make a solid conclusion. There is some overlap, but not enough to say that UFOs appear upon disasters. Maybe natural disasters aren't a significant factor in determining whether a sighting will occur. Maybe it's climate weather? Regardless, there are plenty more ways to explore the phenomeon like the time of day to even checking the "validity" of such reports with Natural Language Processing, but that's up to you. Full code and data can be found on GitHub here. Feel free to use the data sets to explore if you'd like. Please give credit by attaching a link to the repository.

--- 

I collaborated with Ethan Bell, Zora Wang, and Madeline Ye.
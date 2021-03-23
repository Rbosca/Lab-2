# Lab-2

![](https://github.com/Rbosca/Lab-2/blob/main/Screen%20Shot%202021-03-22%20at%2010.00.15%20PM.png)

Reflective Analysis & Collaborations

As part of the Greenest City by 2020 action plan, increasing food assets within neighborhoods has been one of the City of Vancouver’s main objectives. Therefore, the exploration of food deserts in the city is useful to examine the ‘success’ of government initiatives. A food desert has been defined as an area with limited access to affordable or nutritional food. This is in direct contrast to an area with an abundance of and high access to any fresh food retailer, referred to as a food oasis. Researchers and scholars employ various methods to assess food accessibility to identify food deserts, I looked physical access. To measure physical access, distance-based measurement and time-based measurements to the nearest grocery store are commonly used. A food desert consists of a location residing at least 1 mile (1.6km) or 0.5 mile (0.8) away from access to a healthy, fresh food source. Other measures use time to delineate the ability to walk, cycle, ride transit, or drive to a grocery store within 10 minutes.

While my initial idea was to create a food desert map of Vancouver, BC, due to various constraints (time, ability to code, and accessibility to the general public) I decided to simplify the project to focus specifically on physical accessibility to fresh food sources. To do this, I downloaded point data of grocery store locations using NAICS codes (445110) from Simply Analytics. Then, to measure accessibility, I used the turf.js plugin to buffer these points by 0.8km (as I felt that this would be a better estimate of an accessible walk). As this is an interactive map, I intend for the public to engage with this map by locating their home on the map in order to see if they live in an area in close proximity to fresh food. I used the Mapbox-GL-directions plugin to provide the user with step-by-step directions (walking, cycling, driving, traffic), so they are able to click on their home address and then on any store point and will be instantly routed to it. For those users whose homes are located within the 1.6km buffers, the directions API serves to route them to the accessible grocery store(s). For those located outside of the buffered area, the directions API serves to provide directions to the closest grocery stores, while providing the distance and time it would take to travel there using various modes of transportation. 

To style the base map I used the “Basic Overcast” template as it provided a subtle green color to the map features. As color contrast is crucial, I wanted to pair the muted background with more vibrant colors of the grocery, convenience, and specialty stores. This separates the point features from the surrounding elements, instantly creating emphasis and interest. As the majority of the points were grocery stores, I used green points to provide a continuity with the green base map. Limiting the colors used can also aid visual harmony. To continue this trend, I attempted to change the purple and turquoise colors of the toggle options on the directions sidebar to more subtle colors, such as black and white. While I was able to alter the CSS styling file and upload the edited version on GitHub, I was not able to make this work. Finally, I used a very transparent black for the buffers. This allowed the base map and streets layer to be visible underneath the clustered buffers and the points on top to contrast with the buffers. 

The issue of urban food deserts and accessibility are extremely complex issues consider a multitude of social, economic, and physically variables and barriers including: income, ethnicity, age, mobility, etc. While I simply provided a map of one measure of food accessibility, I would be interested in a continuation of this project to consider the more general picture of food insecurity and accessibility. I think interactivity would improve accessibility to geographic information, as well as inspire community involvement in these issues. To improve the interactivity and accuracy of physical accessibility I would use the Mapbox Isochrone API. The Isochrone API uses Mapbox routing profiles and travel times to allow users to estimate how far they are able to travel by car, bicycle, or foot in a certain amount of time. This is visualized by various sized contours reflecting the transportation profile and trip duration. Using this plugin would enable simplicity as the clustered buffers would no longer be necessary. 

The Mapbox GL JS documentation and tutorials were very helpful in the creation of this map. Specifically, the directions API, a tutorial to display a popup on hover, and an example of how to add layer beneath another layer. I also used previous class activities with the turf.js plugin to buffer the store points. Professor Bergmann was also extremely helpful throughout this project, especially to understand tinker with and debug my code.

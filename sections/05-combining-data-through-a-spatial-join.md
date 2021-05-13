← [Making an Interactive Map: Introduction](04-making-an-interactive-map-introduction.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Performing a Spatial Join](06-performing-a-spatial-join.md) →

---

# 5. Combining Data Through a Spatial Join

![Image detailing the process of combining data in a "spatial join"](../images/data.png)

When we think about how the data will be visualized in the map, we will be turning the location of the protests into a layer of points. And we will be stacking the point layer on top of a polygon layer, which are the neighborhoods. Since our neighborhood data—the features stored in the shapefile and the CSV with the data on race—are in two separate files, we'll need to perform a "spatial join" to combine them into one file.<!-- TODO: explain what is a polygon layer + add "polygon layer" to glossary -->

## What's a "Spatial Join"?

Well, I'm glad you asked because a spatial join is one of the most common GIS operations! Since most of the data that we work with do not have coordinates attached to it (e.g. Census data), a spatial join is a way to connect data without mappable coordinates to features with mappable coordinates.<!-- TODO: do we need to clarify what mappable coordinates are, i.e. I presume lat/long? Perhaps another term to add to glossary? -->

In order to do this both files need to be the same resolution (e.g. NYC neighborhood) and they need to have a column of the same unique identifiers—this will serve as a key to match the two data files. When you work with data from the government, such at Census data, each geographical unit (e.g. each different neighborhood) will be given a unique identifier, so if both your data and your shapefile are from the government then the unique identifiers will match.<!-- TODO: add an explanation here of what "resolution" means + add "resolution" to glossary? -->

Since we now have the concepts for what a spatial join means, we can move on to performing the spatial join on our data.

---

← [Making an Interactive Map: Introduction](04-making-an-interactive-map-introduction.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Performing a Spatial Join](06-performing-a-spatial-join.md) →
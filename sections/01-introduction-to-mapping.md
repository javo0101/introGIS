↻ [Start](../README.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Mapping Tools](02-mapping-tools.md) →

---

# 1. Introduction to Mapping

Making a map is like learning a new language, it's a slow and frustrating process because there are a lot of concepts unique to mapping and almost none of it makes sense in the beginning. This first part of the workshop is a very quick overview of mapping concepts to help orient you to the process of mapmaking.

![An example of a Points Lines and Polygon Map](../images/pointslinespolygonsmap.png)

In this map of the United States we see three basic shapes—the cities are represented by points, the main rivers are represented by lines and the states are represented by polygons. While this is a very simple map, most maps that you've seen, even the most intricate ones only consist of these three basic shapes—points, lines and polygons. This type of mapping data is called "vector data."

## Sidebar: Raster Data

There is another important type of data that we will not be using in this workshop, but you should be aware of. It's called "raster data." Raster data is an image, such as a satellite image, with "geolocations"—which just means location data. It's beneficial to store geographic data as raster data when you are working with continuous data, such as heat or elevation.<!-- TODO: add "raster data" to glossary -->

![An example of a Polygon Map](../images/polygonsmap.png)

![An example of a Line Map](../images/polygonslinesmap.png)

![An example of a Points, Lines, and Polygon Map](../images/pointslinespolygonsmap.png)

Voilà!

## Features and Attributes

Another mapping concept that's important to know is that the visualizations that are displayed on the map are called the map's "features" and the data that's connected to those shapes are called the maps "attributes." Attribute data is stored in an attribute table, which is a lot like spreadsheet. One feature on the map can contain many attributes—the feature for the state of Florida has the attributes `STATEFP` (the state ID), `STUSPS` (the state abbreviation), `NAME` (the state name), etc. Any type of data that you have at the scale of the state can be put in this attribute table. The attribute table stores all of the data and then you decide what data you want to visualize.<!-- todo: add these to the glossary -->

![Screenshot explaining the concepts features and attributes in mapping](../images/featuresattributes.png)

---

↻ [Start](../README.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Mapping Tools](02-mapping-tools.md) →
# Setting Up

The first step is to download and install QGIS here. While it downloads, I will explain what we will do, and give you the links to download the files that we will use.

Let’s imagine that there will be a flood in the East River and Hudson Rivers, because of neglect on climate change policy. We know that the flood will reach as deep as 500 meters inland (sorry, we’ll use meters for this whole exercise), and houses located anywhere under 15 meters above the sea level may be affected. Our task is to identify the blocks in a specific area of Manhattan that will be affected the most by this flood.

For this exercise, we will use:

A vector layer showing the census blocks in New York City;
A vector layer with the hydrography of New York City; and
A raster layer with the elevation of a specific quadrant in New York City.
We will get all three required layers from the Cornell University Geospatial Information Repository (CUGIR) website. If you want the real-world experience, go ahead and log into the CUGIR website and try to look for current datasets of New York City, specifically, the Census Blocks 2000 and the Hydrography (Census 2000) (Hint: they’re both here). As for the raster image, look for the Digital Elevation Map (DEM) 10m raster of the Central Park quadrant in New York City (Hint: it’s here). For convenience’s sake, you can download all three required layers in a single Zip file here. Decompress this Zip file in a familiar and easy-to-access folder. You should see three different folders that I labeled BLOCKS, HYDROGRAPHY and ELEVATION, each with their own files and folders inside (note that if you downloaded the files yourself from CUGIR they won’t have these names, but instead a generic CUGIR name and numbers).

Once you finish installing QGIS and downloading the required layers, go ahead and open the QGIS Desktop app. After loading time, you should see something like this:

![Layers in QGIS](setup1.png)
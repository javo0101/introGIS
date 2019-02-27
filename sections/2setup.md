[<<< Previous](1basic.md)  | [Next >>>](3layer1.md)  

# Setting Up

The first step is to [download and install QGIS here](https://www.qgis.org/en/site/forusers/download.html#). This tutorial was intended for QGIS 2.18, although it can be done in any newer version of QGIS as of version 3.6.0 (though there may be slight aesthetic and functional changes all along). Note: Bear in mind that some of the screen captures were done using 2.18 and some using 3.6.0, so button locations may differ from what you see on your screen.

Let’s imagine that there will be a flood in the East and Hudson Rivers, because of climate change and political neglect. We know that the flood will reach as far as 500 meters inland, and houses located anywhere under 15 meters above the sea level may be affected. Our task is to identify the blocks in a specific area of Manhattan that will be affected the most by this flood.

For this exercise, we will use:

1. A layer showing the census blocks in New York City;
2. A layer with the hydrography of New York City; and
3. A layer showing the elevation (15 meters above the sea level)  of the study area.  

These required layers come from the [Cornell University Geospatial Information Repository (CUGIR) website](http://cugir.mannlib.cornell.edu/). If you want the real-world experience, go ahead and log into the CUGIR website and look for current datasets of New York City—specifically, the Census Blocks 2000 and the Hydrography (Census 2000). As for the elevation layer, you will need to convert it from a raster image (instructions at the end of this tutorial, under "Deprecated Sections"). In the CUGIR website, look for the Digital Elevation Map (DEM) 10m raster of the Central Park quadrant in New York City. For convenience, you can download all required files and layers in a single Zip file [here](https://github.com/DHRI-Curriculum/mapping/blob/master/Files%20for%20Intro%20to%20QGIS.zip)  . Decompress this Zip file in a familiar and easy-to-access folder.

[<<< Previous](1basic.md)  | [Next >>>](3layer1.md)  

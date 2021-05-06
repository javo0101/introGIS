← [Ethics of Mapping](03-ethics-of-mapping.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Combining Data Through a Spatial Join](05-combining-data-through-a-spatial-join.md) →

---

# 4. Making an Interactive Map Demo: Introduction

## Research Question

Do Black Lives Matter protests tend to take place more in majority Black neighborhoods, perhaps as a tactic to build solidarity, or in majority non-Black, perhaps as a tactic to raise awareness?

## Exploring the Data

What kind of data do we need to make this map?

- Location of protests.
    - Since this data didn’t exist, I had to create it. I tried to find all of the protests that took place from May 28, 2020 to June 3, 2020. Since this was based on my own ability to capture the data from news articles, I assume that there are protests that happened during that week that are not in my dataset. When I publish my map it would be important to state this assumption and include the methodology for how this data was collected.   
- Shapes to represent the neighborhoods.
    - For NYC neighborhoods we can download a shapefile (which is a form of spatial data) from NYC Open Data. The file can be downloaded here. Click on “Export” and select “Shapefile”.  A compressed folder will download. Move the folder out of your downloads and into a folder on your computer were you will be keeping all of the data for this workshop. 
    - When you open the folder you will notice there are 4 different files in there that all have the same name, yet are a different file type. In order for a shapefile to work, all of this data needs to stay together. Please zip the folder, so that the whole folder can be uploaded into our mapping software when we are ready to use it. 
- Census data on race by neighborhood
    - Census generated demographic data can be downloaded as a CSV file from the Census website. I’ve already downloaded the spreadsheet and cleaned it up for us so that it only has the variables that we are interested in--GeoName (neighborhood name), GeoID(a unique identifier for each neighborhood), and BINHP (Percent Black). 

To get a better idea of what we will be building together, you can see a final version of the [map here](<http://arcg.is/1KyC9O >).

---

← [Ethics of Mapping](03-ethics-of-mapping.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Combining Data Through a Spatial Join](05-combining-data-through-a-spatial-join.md) →
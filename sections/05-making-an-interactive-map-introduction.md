← [Ethics of Mapping Continued: Questions to Consider](04-ethics-of-mapping-continued-questions-to-consider.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Combining Data Through a Spatial Join](06-combining-data-through-a-spatial-join.md) →

---

# 5. Making an Interactive Map: Introduction

Every map should start with a good research question. But what makes for a good mapping research question? The key, I find, is to start with a simple, answerable question. It's often the case that a seemingly simple and boring question can lead to bigger and more interesting questions. However, if you start with the big, complex question, it could be too overwhelming. So start small and then build on your question, if needed. Also, what do I mean by "answerable"? In the mapping world, this can mean several things. It could mean a question that can be answered by using preexisting data or data that can realistically be collected by the mapmaker. Suppose you want to map how Americans in different counties feel about a certain issue, but that national survey hasnt been done and you don't have the resources to do it, then this would fall under the category of an unanswerable question. Also if you want to map boundaries that havent been created, such as homeschool pods, then this might be an unanswerable question (again if you don't have the resources to create the boundary from scratch).

By these standards, for this workshop we have a simple, easily answerable question.


## Research Question

Do Black Lives Matter protests tend to take place more in majority Black neighborhoods, perhaps as a tactic to build solidarity, or in majority non-Black, perhaps as a tactic to raise awareness?

## Exploring the Data

What kind of data do we need to make this map?

- **Location of protests.** This data didn't exist, so I had to create it. I tried to find all of the protests that took place from May 28, 2020 to June 3, 2020. Since this was based on my own ability to capture the data from news articles, I assume that there are protests that happened during that week that are not in my dataset. When I publish my map, it will be important to state this assumption and include the methodology for how this data was collected.
- **Shapes to represent the neighborhoods.** For NYC neighborhoods we can download a shapefile (which is a form of spatial data) from NYC Open Data. The file can be [downloaded here](https://data.cityofnewyork.us/City-Government/Neighborhood-Tabulation-Areas-NTA-/cpf4-rkhq). Click on "Export" and select "Shapefile". A compressed folder will download. Move the folder out of your downloads and into a folder on your computer were you will be keeping all of the data for this workshop. When you open the folder you will notice there are four different files in there that all have the same name, yet are a different file type. In order for a shapefile to work, all of this data needs to stay together. Please compress the folder, so that the entire folder can be uploaded into our mapping software when we are ready to use it.
- **Census data on race by neighborhood.** Census generated demographic data can be downloaded as a CSV file from the Census website. I've already downloaded the spreadsheet and cleaned it up for us so that it only has the variables that we are interested in—`GeoName` (neighborhood name), `GeoID` (a unique identifier for each neighborhood), and `BINHP` (Percent Black). You can find this file [here](https://github.com/DHRI-Curriculum/mapping/blob/v2.0-olivia-edits/dataset/racebyneighborhood.csv)

## Preview the Result

To get a better idea of what we will be building together, you can take a look at a final version of the [Location of BLM Protests Map](http://arcg.is/1KyC9O).

---

← [Ethics of Mapping Continued: Questions to Consider](04-ethics-of-mapping-continued-questions-to-consider.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Combining Data Through a Spatial Join](06-combining-data-through-a-spatial-join.md) →
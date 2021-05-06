# Introduction to Mapping

In the past decade, interactive maps have become one of the most popular ways to visualize and explore spatial data. Responding to the demand, mapping companies such as ESRI have developed a suite of tools for both creating and contextualizing interactive maps. While extremely helpful, some of the ESRI products are prohibitively expensive for many individuals. This workshop will use a combination of the public version of ESRI Online, which is free, and the free, open-source mapping software QGIS to build an interactive map. By the end of this workshop you will know the basics for making an interactive map that can be shared and embedded in a website. No mapping experience is necessary.

In this workshop, you will:

In this workshop, you will learn to:
- Become familiar with fundamental mapping concepts, such as how spatial data is organized and displayed. 
- Distinguish among two different forms of spatial data—vector data and raster data.
- Consider some of the core ethical dilemmas of mapmaking.
- Understand the difference between the most popular mapping software. 
- Import and export data between different mapping tools. 
- Combine data through performing a "spatial join." 
- Turn a spreadsheet with location data into a map layer (the name of this process is "geocoding").
Customize an interactive map.
- Add pop-ups to your map.
- Share your interactive map as a URL or embed it in a website.

—-

<p align="center">This workshop is estimated to take you 4 hours to complete.</p><p align="center"><a href="sections/01-introduction-to-mapping.md">Get Started</a> →</p>

—-

## Lessons

1. [Introduction to Mapping](sections/01-introduction-to-mapping.md)
2. [Mapping Tools](sections/02-mapping-tools.md)
3. [Ethics of Mapping](sections/03-ethics-of-mapping.md)
4. [Making an Interactive Map Demo: Introduction](sections/04-making-an-interactive-map-demo-introduction.md)
5. [Combining Data Through a Spatial Join](sections/05-combining-data-through-a-spatial-join.md)
6. [Performing a Spatial Join](sections/06-performing-a-spatial-join.md)
7. [Importing data to ArcGIS Online](sections/07-importing-data-to-arcgis-online.md)
8. [Changing the Map Style](sections/08-changing-the-map-style.md)
9. [Configuring the Pop-up](sections/09-configuring-the-pop-up.md)
10. [Importing CSV file and Geocoding Addresses](sections/10-importing-csv-file-and-geocoding-addresses.md)
11. [Changing the Style of the Points Layer](sections/11-changing-the-style-of-the-points-layer.md)
12. [Formatting the Pop-ups for the Protest Locations](sections/12-formatting-the-pop-ups-for-the-protest-locations.md)
13. [Formatting the Legend](sections/13-formatting-the-legend.md)
14. [Saving and Sharing Your Map](sections/14-saving-and-sharing-your-map.md)
15. [Title (for lesson 2)](sections/15-title-(for-lesson-2).md)

—-

## Before you get started

If you do not have experience or basic knowledge of the following workshops, you may want to look into those before you start with Introduction to Mapping:

- [Data Literacies](https://github.com/DHRI-Curriculum/data-literacies) (optional)

### Ethical Considerations

Before you start the Introduction to Mapping workshop, we want to remind you of some ethical considerations to take into account when you read through the lessons of this workshop:

Starting from figuring out how to represent a 3D reality on a 2D plane, there are countless subjective decisions that every mapmaker must make, whether they are conscious of it or not. Mapmakers need to decide what data to represent and what to leave out. They also need to decide how to aggregate, categorize, project, combine, and visualize the data. All of these decisions will influence the story that the map tells. Additionally, as a critical tool of Western colonialism and imperialism, maps wield great authority. As mapmakers, it's essential to be conscious of this history not to reproduce harmful power dynamics through mapmaking. Once something is visualized in the form of a map, it is often understood as a Truth representation of reality. Therefore, mapmakers have an important responsibility to be as honest and transparent as possible. Since the 1980's, there have been two emerging disciplines in academia—critical cartography and feminist GIS—that have brought to light many of the harmful applications of mapping. Rather than reject mapping, they have made significant contributions to the field of GIS and mapping, such as counter mapping, sketch mapping, participatory mapping, qualitative GIS and 3D body-mapping. The following readings will introduce you to some of the fundamental insights from critical cartography and feminist GIS that you can integrate into your mapping journey. The reading list also includes modern-day counter mapping projects.

- Harley, J. B. (1989). [Deconstructing the map. Cartographica: The international journal for geographic information and geovisualization](<https://quod.lib.umich.edu/p/passages/4761530.0003.008/—deconstructing-the-map?rgn=main;view=fulltext>), 26(2), 1-20.
    - This is a classic text by Brian Harley – one of the first Foucauldian analyses of mapping.
- Pavlovskaya, M., & Martin, K. S. (2007). [Feminism and geographic information systems: From a missing object to a mapping subject](<https://onlinelibrary.wiley.com/doi/full/10.1111/j.1749-8198.2007.00028.x>). Geography Compass, 1(3), 583-606.
    - This article makes the case for feminist GIS. 
- Pavlovskaya, M. (2002) [Mapping urban change and changing GIS: Other views of economic restructuring](<https://www.researchgate.net/publication/240107165_Mapping_Urban_Change_and_Changing_GIS_Other_views_of_economic_restructuring>). Gender, place and culture: A journal of feminist geography 9, 281-289
    - This study demonstrates how GIS can be part of a critical and feminist analysis of economic development. 
 - Kwan, M. P. (2008). [From oral histories to visual narratives: Re-presenting the post-September 11 experiences of the Muslim women in the USA](<http://meipokwan.org/Paper/SCG_2008.pdf>). Social & Cultural Geography, 9(6), 653-669.
    - This study by a feminist GIS scholar uses 3D body maps to challenge the 2D limitations of most maps. She also combines interviews and survey data to create the visualizations. 
- [Counter Mapping: Zuni Maps](<https://emergencemagazine.org/feature/counter-mapping/>)
    - The indigenous Zuni people describe their mapping project and the ways it challenges Western modes of mapping.

### Pre-reading suggestions

Before you start the Introduction to Mapping workshop, you may want to read a couple of our pre-reading suggestions:

- [Finding the Right Tools for Mapping](<https://digitalfellows.commons.gc.cuny.edu/2019/06/03/finding-the-right-tools-for-mapping/>)
- [Finding Data for Mapping: Tips and Tricks](<https://digitalfellows.commons.gc.cuny.edu/2018/11/24/finding-data-for-mapping-tips-and-tricks/>)
- [Create A Rich Multimedia Narrative with ESRI Story Maps](<https://digitalfellows.commons.gc.cuny.edu/2019/02/12/create-a-rich-multimedia-narrative-with-esri-story-maps/>)

### Projects that use these skills

You may also want to check out a couple of projects that use the skills discussed in this workshop:

- [Visualizing NEH Open Data](<https://digitalfellows.commons.gc.cuny.edu/2017/04/04/visualizing-neh-open-data/>)

- [Mapping Occupation](<https://gcdi.commons.gc.cuny.edu/mapping-occupation-the-union-army-and-the-meaning-of-reconstruction/>)

- [NYC's Worst Evictors](<https://www.worstevictorsnyc.org/map/>)

- [Torn Apart/Separados](<http://xpmethod.columbia.edu/torn-apart/volume/2/index>)

- [Native Land](<https://native-land.ca/>)

- [COVID Mapping Projects](<https://digitalfellows.commons.gc.cuny.edu/2020/11/02/mapping-the-effects-of-covid-19/>)

—-

<p align="center"><a href="sections/01-introduction-to-mapping.md">Get Started</a> →</p>

—-

## Acknowledgements

This workshop is the result of a collaborative effort of a team of people, mostly involved presently or in the past, with the Graduate Center's Digital Initiatives. If you want to see statistics for contributions to this workshop, you can do so [here](https://www.github.com/DHRI-Curriculum/mapping/graphs/contributors). This is a list of all the contributors:

- Current Author: [Olivia Ildefonso](<https://oildefon.medium.com/>)
- Collaborator: [Javier Otero Peña](<https://enviropsych.org/students/javier-otero-pena/>)
- Editor: [Kalle Westerling](<https://github.com/kallewesterling>)
- Editor: [Dr. Lisa Rhody](<https://github.com/lmrhody>)

—-

<sub>[Digital Research Institute (DRI) Curriculum](http://purl.org/dc/terms/) by [Graduate Center Digital Initiatives](https://gcdi.commons.gc.cuny.edu/) is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/). Based on a work at <https://github.com/DHRI-Curriculum>. When sharing this material or derivative works, preserve this paragraph, changing only the title of the derivative work, or provide comparable attribution.</sub>

[![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

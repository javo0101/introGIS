← [Combining Data Through a Spatial Join](06-combining-data-through-a-spatial-join.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Exporting Data from QGIS](08-exporting-data-from-qgis.md) →

---

# 7. Performing a Spatial Join

We will use QGIS which is a free and open source mapping software that will allow us to do pretty much any spatial operation that you could ever want! If you haven't yet installed QGIS you can do so by following these [installation instructions](https://github.com/DHRI-Curriculum/install/blob/main/sections/qgis.md) 

## Open QGIS

First, go ahead and open QGIS. When you open the application, you'll see an interface that looks like this:

![Screenshot overviewing QGIS's interface](../images/qgisinterface.png)

## Adding Demographic Data to QGIS

Let's add our data that needs to be joined. Follow the steps below to help you through the process.

1. To add our [CSV](https://github.com/DHRI-Curriculum/glossary/blob/v2.0/terms/csv.md) of demographic data, `racebyneighborhood.csv`, open the **Data Source Manager**—this button is located in the top left corner of the interface and looks like three pieces of colored paper stacked on top of each other.
2. When the Data Source Manager is open, select the **Delimited Text** option.
3. On the right side of the **File name** section, click on the three dots to locate the file. Then click **Add**.

![Screenshot of QGIS's data source manager](../images/datasourcemanager.png)

You should now see the file appear in your Layers panel. You'll also see that nothing happens in your map display panel; this is because a CSV file is a text file. Remember that only vector data and raster data has features that can be mapped. A CSV file by itself is not mappable. That's why we need to combine it with the neighborhood shapefile. Note that if you happen to have precise location data in your CSV, such as addresses or latitude and longitude coordinates, the mapping software will be able to read it and convert it into vector data through a process called *geocoding*. When you don't have precise location data, you will need to use a *join by attribute* to add the text data to a shapefile. 

## Adding Vector Data from Our Shapefile to QGIS

Now let's add our shapefile of New York City:


1. Go back to the **Data Source Manager** and this time select **Vector**.
2. Under **Source type**, the "file" option should be selected.
3. Where it says **Vector datasets**, use the browse feature again to find the shapefile on your computer and click **Add**.

![Screenshot of adding vector layer](../images/addvectorlayer.png)

Now you should see that the file shows up in your Layers Panel, and it also displays as a map layer on your display panel.

## Inspecting the Attribute Table

Let's look at the data in the attribute table to see what we're working with. Each file has its own attribute table, so let's look at them one at a time. To do so, right-click on the `racebyneighborhood.csv` file and select "Open attribute table." _If you see the three variables—`GeoName`, `GeoID`, and `BINHP`—then we're good to go!_

Let's open the attribute table for the "Neighborhood Tabulation Area" shapefile. Right-click on that layer and select "Open attribute table."

![Screenshot of attribute table](../images/ntaattributetable.png)

In the table, you will see the variables: `boro_code` (borough code), `boro_name` (borough name), `county_fip` (the unique identifier for each county), `ntacode` (the unique identifier for each neighborhood), `ntaname` (neighborhood name), `shape_area` (surface area of each neighborhood in decimal degrees) and `shape_leng` (the length of the perimeter of each neighborhood in decimal degrees).

You will notice that both files have a variable in common—the `ntacode` in the shapefile is the same as the `GeoID` in the CSV file. These two variables will serve as our keys that will be used to match and join the files together.

A spatial join won't work unless the fields are the same [data type](https://github.com/DHRI-Curriculum/glossary/blob/v2.0/terms/attributetype.md) —integer, double, string, etc. To see the field type, double-click on each layer and navigate to the "Fields" tab. The `ntacode` and the `GeoID` are both string variables, so we are all set for our join.

## Performing a Spatial Join

Now we are ready for our spatial join!

1. In the layers panel, double click on the shapefile layer, "Neighborhood Tabulation Area".Then click on **Joins** and click on the **green plus sign**. A new dialog will appear on the screen. This is where you will configure your spatial join.
2. Select `racebyneighborhood` for the **Join layer** option since that is the map layer you are joining to the neighborhood shapefile.
3. Select `GeoID` for the **Join field** option.
4. The **Target field** should be `ntacode`.
5. Where it says **Custom Field Name Prefix**, you can click the checkbox and change the prefix. This prefix will be added to the variable name of every join layer. You can change it to something shorter or you can simply delete the text so no prefix is added. I'm going to delete mine.
6. Lastly, click **OK** to save the configuration of the spatial join.
7. To run the join, click **OK** in the following dialog.

_Note: `GeoID` and `ntacode` are the two variables that match from the two mapping layers. This is why we are using them in step 3 and 4 above as the **Join field** and **Target field**._

![Screenshot detailing the steps in this section to perform a "spatial join"](../images/joins.png)

To check to see if the join was successful, we'll need to look at the neighborhood shapefile's attribute table and see if the variables from the CSV file are there.

Right-click on the shapefile layer and select **Open attribute table**. If you scroll to the right you should see the three variables from the CSV file—`GeoName`, `GeoID`, and `BINHP`. If you see them, then you've successfully completed a spatial join!

Since our shapefile layer has been updated with new data, lets rename it. To do so, right-click on the shapefile layer in the Layers Panel and select **Rename**. I'm going to rename mine `NYCntaPerBlack`. This name will let me know that the data has New York City neighborhood tabulation areas and percent black.

## Recap: Two Different Types of Spatial Joins

Mapping softwares typically offer two different types of spatial joins—join by attribute and join by location.

- **Join by attribute** is the type of join what we just did; it’s based on matching two layers based on a shared attribute or variable.
- **Join by location** is when you have two shapefiles that you want to combine based on where the features are located on the map. For example if you have a map of US states and you want to add information about its cities, you can run a spatial join by location. To learn more about this type of join, check out [How Spatial Join Works in GIS by GIS Geography](https://gisgeography.com/spatial-join/).

## Evaluation

The *Data Source Manager* is used to:
- import files into QGIS*
- organize data files
- stack map layers
- export map layers

What's needed to perform a *spatial join by attribute*:
- There must be a column in both datasets that matches and will serve as a key to link the two datasets.*
- The columns that serve as a key must be the same data type.*
- The text file must have precise location data, such as an address or latitude and longitude.

## Keywords
- [Spatial join by attribute](https://github.com/DHRI-Curriculum/glossary/blob/v2.0/terms/joinbyattribute.md)
- [Spatial join by location](https://github.com/DHRI-Curriculum/glossary/blob/v2.0/terms/joinbylocation.md)

---

← [Combining Data Through a Spatial Join](06-combining-data-through-a-spatial-join.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Exporting Data from QGIS](08-exporting-data-from-qgis.md) →
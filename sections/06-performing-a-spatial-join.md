← [Combining Data Through a Spatial Join](05-combining-data-through-a-spatial-join.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Importing data to ArcGIS Online](07-importing-data-to-arcgis-online.md) →

---

# 6. Performing a Spatial Join

## Adding data to QGIS

First, open QGIS. Let’s add our data that needs to be joined. Follow the steps below to help you through the process.

1. To add our CSV of demographic data, "racebyneighborhood.csv", open the **Data Source Manager**--this button is located in the top left and looks like three pieces of colored paper stacked on top of each other.

![data source manager](../images/datasourcemanager.png)

2. When the Data Source Manager is Open, select the **Delimited Text** option.
3. On the right side of the **File name** section, click on the three dots to locate the file. Then click **Add**.

You should now see the file appear in your Layers panel. You’ll also see that nothing happens in your map display panel; this is because a CSV file is not mappable. That’s why we need to combine it with our shapefile of vector data. 

Now let’s add our shapefile of NYC 
1. Go back to the **Data Source Manager** and this time select **Vector**. 
2. Under **Source type** the "file" option should be selected. 
3. Where it says **Vector datasets**, use the browse feature again to find the shapefile on your computer and click **Add**. 

Now you should see that the file shows up in your Layers Panel, and it also displays as a map layer on your display panel. 

## Looking at the Attribute Table

Let’s look at the data in the attribute table to see what we’re working with. Each file has its own attribute table, so let’s look at them one at a time. 

1. Right click on the "racebyneighborhood" file and select Open attribute table.
    - If you see the three variables--GeoName, GeoID, and BINHP--then we’re good to go! 

Let’s open the attribute table for the "Neighborhood Tabulation Area" shapefile. 
1. Right click on that layer and select Open attribute table. 
    - In this table you will see the variables: boro_code (borough code), boro_name (borough name), county_fip (the county unique identifier), ntacode (the unique identifier for each neighborhood), ntaname (neighborhood name), shape_area (Surface area of each neighborhood in decimal degrees) and shape_leng (The length of the perimeter of each neighborhood in decimal degrees).

You will notice that both files have a variable in common--the "ntacode" in the shapefile is the same as the "GeoID" in the CSV file. These two variables will serve as our keys that will be used to match and join the files together. 

A spatial join won’t work unless the fields are the same type--integer, double, string, etc. To see the field type, double-click on each layer and navigate to the "Fields" tab. The ‘ntacode’ and the ‘GeoId’ are both string variables, so we are all set for our join. 

## Performing a Spatial Join

Now we are ready for our spatial join!

1. In the layers panel, double click on the shapefile layer, "Neighborhood Tabulation Area".Then click on **Joins** and click on the **green plus sign**. A new box will pop up. This is where you will configure your spatial join. 
    - The **Join layer** should be "racebyneighborhood" since that is the map layer you are joining to the neighborhood shapefile. 
    - The **Join field** should be "GeoID."
    - The **Target field** should be "ntacode."
    - Note: "GeoID" and "nta code" are the two variables that match from the two mapping layers. This is why we are using them here as the **Join field** and **Target field**.
    - Where it says **Custom Field Name Prefix** you can click the checkbox and change the prefix. This prefix will be added to the variable name of every join layer. You can change it to something shorter or you can simply delete the text so no prefix is added. I’m going to delete mine.
    - Lastly, click **OK** to save the configuration of the spatial join. 
    - To run the join, click **OK**.

![spatial join prompt](../images/joins.png)


To check to see if the join was successful, we’ll need to look at the neighborhood shapefile’s attribute table and see if the variables from the CSV file are there. 
1. Right click on the shapefile layer and select **Open attribute table**. If you scroll to the right you should see the three variables from the CSV file--"GeoName", "GeoID", and "BINHP". If you see them, then you’ve successfully completed a spatial join! 

Since our shapefile layer has been updated with new data, lets rename it.
1. Right click on the shapefile layer in the Layers Panel and select **Rename**. I’m going to rename mine "NYCntaPerBlack." This name will let me know that the data has New York City neighborhood tabulation areas and percent black. 

**Note**: Mapping softwares typically offer two different types of spatial joins--join by attribute and join by location. **Join by attribute** is the type of join what we just did; it’s based on matching two layers based on a shared attribute or variable. **Join by location** is when you have two shapefiles that you want to combine based on where the features are located on the map. For example if you have a map of US states and you want to add information about its cities, you can run a spatial join by location. To learn more about this type of join, check out [this article.](https://gisgeography.com/spatial-join/) 

## Exporting Data from QGIS

Now our neighborhood shapefile (with the demographic information in it) is ready to be exported from QGIS and uploaded into ArcGIS Online where we will be able to turn it into an interactive map. 

Before we export the shapefile file, let’s create a folder for it. Since shapefiles are actually a set of 4-6 files, it’s helpful to create a folder for them so they don’t get mixed up with your other files. 

1. Create a new folder somewhere on your computer where you are keeping the data for this workshop. 
2. Let’s name the folder "NYCntaPerBlack."

Now we’re ready to export the data.
1. In QGIS, right click on the neighborhood shapefile in the Layers panel. Then select **Export** and **Save Features As**.
2. Under **File name** we need to tell QGIS which folder to export the file into. Use the three dots to navigate to the folder "NYCntaPerBlack" 
3. Next, you can click off the check box at the very bottom of the "Save Vector Layer as…" configuration box, where it says **Add saved file to map**. Since we already have this as a map layer in QGIS, there’s no need to add it as another layer in the software. 
4. You can leave everything else in the configuration alone. Lastly, click **OK** to complete exporting the data. 

![export shapefile](../images/exportnew.png)

Navigate to your "NYCntaPerBlack" folder and check to see if all of the shapefiles are in there. If they are, then your export was successful. 

The last thing we have to do is **zip or compress** the folder. ArcGIS Online will only import zipped shapefiles. If you’re working on a Mac, right click on the "NYCntaPerBlack" folder and click **compress**. If you’re on a PC, right click on the "NYCntaPerBlack" folder and select Send to and then **Compressed (zipped) folder**.

---

← [Combining Data Through a Spatial Join](05-combining-data-through-a-spatial-join.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Importing data to ArcGIS Online](07-importing-data-to-arcgis-online.md) →
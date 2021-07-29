← [Performing a Spatial Join](07-performing-a-spatial-join.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Importing Data to ArcGIS Online](09-importing-data-to-arcgis-online.md) →

---

# 8. Exporting Data from QGIS

Now our neighborhood shapefile (containing the demographic information) is ready to be exported from QGIS and uploaded into ArcGIS Online where we will be able to turn it into an interactive map.

## Preparing for the Export

Since shapefiles are actually a set of 4-6 files, it's helpful to create a folder for them so they don't get mixed up with your other files. So, before we export the shapefile file, let's create a folder for it. 

1. Create a new folder somewhere on your computer where you are keeping the data for this workshop.
2. Let's name the folder `NYCntaPerBlack.`

## Exporting the Data

Now we're ready to export the data.

1. In QGIS, right-click on the neighborhood shapefile in the Layers panel. Then select **Export** and **Save Features As**.
2. Under **File name** we need to tell QGIS which folder to export the file into. Use the three dots to navigate to the folder `NYCntaPerBlack`
3. Next, you can click off the check box at the very bottom of the "Save Vector Layer as…" configuration box, where it says **Add saved file to map**. Since we already have this as a map layer in QGIS, there's no need to add it as another layer in the software.
4. You can leave everything else in the configuration alone. Lastly, click **OK** to complete exporting the data.

![Screenshot detailing the steps above to export the shapefiles for the project](../images/exportnew.png)

Navigate to your `NYCntaPerBlack` folder and check to see if all of the shapefiles are in there. There should be around 4–6 files in the folder. If there are, then your export was successful.

The last thing we have to do is **compress** the folder. ArcGIS Online will only import compressed shapefiles. If you're working on a Mac, right-click on the `NYCntaPerBlack` folder and click **compress**. If you're on a PC, right-click on the `NYCntaPerBlack` folder and select Send to and then **Compressed (zipped) folder**.

## Evaluation

Why do we create a folder for the exported shapefile?
- The export won't work without it.
- Shapefiles are actually 4-6 files, so it's a way to keep them organized and prevent accidentally separating them.*
- ArcGIS will only import compressed shapefiles, so we need to create a folder to compress or zip the file.*

---

← [Performing a Spatial Join](07-performing-a-spatial-join.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Importing Data to ArcGIS Online](09-importing-data-to-arcgis-online.md) →
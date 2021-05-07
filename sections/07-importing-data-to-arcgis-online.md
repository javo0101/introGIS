← [Performing a Spatial Join](06-performing-a-spatial-join.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Changing the Map Style](08-changing-the-map-style.md) →

---

# 7. Importing data to ArcGIS Online

## Login to ArcGIS Online
First, you'll have to set yourself up with a free ArcGIS Online public account. To do so, open [ArcGIS Online](https://www.arcgis.com/home/index.html), and Sign in. If you don't already have an account, you can create one for free or use your Google, Facebook or Github account.

## Create a new map and add your data from QGIS to ArcGIS

Once you've logged in, let's open a new map project by selecting "Map" in the main menu.

Let's get acquainted with the interface.

![Screenshot detailing ArcGISOnline's interface](../images/arcgisinterface.png)

Now let's import and format our neighborhoods shapefile.

1. Click on **Add**.
2. Click **Add Layer from File**.
3. Select **Choose File**. And navigate to where you have the zipped/compressed `NYCntaPerBlack` file saved on your computer.
4. Feel free to leave the option "Generalize features for web display" selected. I've tried making maps with both this option and "Keep original features" and I've never noticed any difference.
5. Click **Import Layer**.

You should now see something that looks like a map of New York City, colored in by the Borough or another attribute. ArcGIS automatically selects an attribute to use to show on the map.

![Screenshot detailing what the map's styling looks like after the steps above](../images/shapefileimport.png)

---

← [Performing a Spatial Join](06-performing-a-spatial-join.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Changing the Map Style](08-changing-the-map-style.md) →
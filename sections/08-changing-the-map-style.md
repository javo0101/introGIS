← [Importing data to ArcGIS Online](07-importing-data-to-arcgis-online.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Configuring the Pop-up](09-configuring-the-pop-up.md) →

---

# 8. Changing the Map Style

Let's change the attribute so that it shows the percent Black population of New York City's neighborhoods.

1. Under **Choose an attribute to show**, select `BINHP` which stands for Black Non-Hispanic Population.
2. Click around with the Drawing Styles to see which you think works best. I would suggest using the first option, a choropleth map style that shows the value by the intensity of the color.<!-- todo: new term for the glossary: cloropleth -->
3. Let's change the color to something different.
    - In the **Counts and Amounts** (Color) box click **Options**.
    - Click **Symbols**, and change the color. I'm selecting the black/white color ramp since I think it fits in with the story I'm trying to tell.
    - Once you've chosen your color ramp, click **OK**.
    - Optional: You can click on **Classify** if you want to change how the data is visualized and how many categories are created. "Natural breaks" is a good option because it increases variability between classes while decreasing it within classes.
    - Click the **OK** button at the bottom of the Layers Panel.
    - Finally, click **Done** to save your changes to the map. If you don't click Done, it will revert to what you had before.

You should now see your maps styled with your new color ramp. You'll also see the `NYCntaPerBlack` map layer in the Layers Panel.

![Screenshot that shows what the map looks like after the steps above](../images/uglypopup1.png)<!-- TODO: add image here that does not show the popup but only the finished styled map? -->

---

← [Importing data to ArcGIS Online](07-importing-data-to-arcgis-online.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Configuring the Pop-up](09-configuring-the-pop-up.md) →
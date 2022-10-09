# Help on how to download data from INE

## Reason for this document

This guidelines helps to ensure that all data files downloaded and reshaped from INE's database on the [Agricultural census](https://ra2019.ine.pt/xportal/xmain?xpgid=ra2019_main&xpid=RA2019&xlang=en) result in a 
well structured file to be uploaded to the database. This is important to make 
sure that relations in the database can be established between the various types
of data.

The most important is that all downloaded data tables have rows based on the geographic 
unit NUTS 2013 (3436 rows). But, because INE plarform limits the number of data 
cells to 40K, this limits the number of data attributes (columns) that can be 
selected for each download. This might imply that to obtain all the data for a 
specific item, it is necessary to make several downloads (typically, selecting 
only one year per download). In some cases, it is necessary to further breakdown
the downloads by other attributes, which will require latter additional work to merge data in one table.

## How to select criteria and download

The selection of criteria to include in the download can, sometimes, a trial-and-error approach, because of the limitations of the 40K cells. 

1. Go to [INE](https://www.ine.pt), and select `Products --> Database`
2. Select the theme `Agriculture, forestry and fishing`
3. Select the subtheme `Agricultural census`
4. Select the gepgraphical level `Freguesia`
5. Enter a keyword to search, e.g. *grassland*, *temporary crops*, *livestock*, etc
6. Select the indicator of your choice
7. Select `Change selection conditions`
8. At the **Dimension** *Geographic localization*, check the box `Select all`. 
The total cells should show the value `3436`.
9. You might need to download one year at a time. Select the year at the dimension `Data reference period`
10. Select another dimension. Select the checkboxes with the categories/values 
you want. Note that if you check `Select all`, it will select all values in 
hierarchy of values. This is cause the number of cells to be higher than 40K. 
Therefore, select by hand only the higher levels to limit the total cells to 40k.
11. Click on the `Obtain table` tab. Check the table corresponds to what you expected.
12. Click on the icon `Download table (CSV format)`. Click on the link for download when it appears.
13. Save the table in your `raw-data` folder, with an expressive name, e.g. `temp-crop-hold-2019.csv` for the item *Agricultural holdings with temporary crops*.
14. Go again to the tab `Change selection conditions`, select a different year, and repeat the download, changing the name of the file in a consistent way. 



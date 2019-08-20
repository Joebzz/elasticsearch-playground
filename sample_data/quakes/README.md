# Importing the data from CSV
Instructions copied from here https://www.elastic.co/blog/aftershock-therapy-with-elasticsearch-and-csv-data-import

## Importing the data
1.  Within Kibana, click on **Machine Learning**.
2.  In the subnav, click on **Data Visualizer**.
3.  Under _Import Data_, click **Upload File**.  
    _Note:_ This feature is new in 6.5\. If you find any issues while using it, please let us know in our Elastic machine learning [Discuss forum](https://discuss.elastic.co/c/x-pack/machine-learning).
4.  Drag and drop the _quakes_data.csv_ file (provided earlier) into the importer.
5.  Scroll through the list of contents. Notice that the _loc_ field is importing as text. We will update this to be geo_point data in the next step. Click **Import**.
6.  In the _Import Data_ window, switch to **Advanced**:
    1.  Index name: quakes
    2.  Create index pattern: unchecked (this is very important, as we’ll be importing an index pattern in the next set of steps)
    3.  Index pattern name: blank (and uneditable)
    4.  Under _Mappings_, manually change _loc_ from “keyword” to “geo_point”.  
7.  Click **Import**. You’ll see that 902 documents have been imported.

## Create Kibana visualizations using quake data
1.  On the left side navigation, click on **Management**.
2.  Under _Kibana_, click on **Saved Objects**.
3.  Click **Import** from above the object list.
4.  Click **Import** and choose _quakes_objects.json_.
5.  Click the **Import** button. You’ll see 11 objects were imported.
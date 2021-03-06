.. include:: ../../substitutions.rst


Dataviz - display some graphs
=============================

Principle
---------

With the dataviz panel, you can create a few kinds of graph with only a few clicks:

- scatter
- pie
- histogram
- box
- bar
- histogram2d
- polar
- sunburst |lizmap_3_4|

.. image:: /images/publish-01-dataviz-interface.jpg
   :align: center
   :scale: 80%

Prerequisites
-------------

|wfs_layer|

Configuring the tool
--------------------

.. tip::
    You can start using the plugin ``DataPlotly`` to create your graph in QGIS itself.
    So you can have a preview about what is possible *more or less* about dataviz with your layers.
    But keep in mind that Lizmap and DataPlotLy, even if's using the same dataviz engine, features are different between these two tools.

You can easily configure it with the plugin Lizmap in QGIS in the :guilabel:`Dataviz` panel.

.. image:: /images/publish-02-dataviz-interface-plugin.jpg
    :align: center
    :scale: 80%

- |field_alias|

**1** :
You have the possibility to change the value to **dock**, **bottomdock** or **right-dock** these options change where your dataviz panel will be located in your Lizmap's project. You have 3 positions available, at the right of the screen, bottom and right.

**2**:
Here, you have the possibility to write in HTML to change the style of the container of your charts. If you are proficient in the HTML language, there are a lot of possibilities and you can customize your container the way you want.

For instance, this bootstrap HTML code will produce the layout below:

.. code-block:: html

    <div class="container-fluid">
        <div class="row-fluid">
            <div class="span6">$0</div>
            <div class="span6">$1</div>
        </div>
        <div class="row-fluid">
            <div class="span12">$2</div>
        </div>
    </div>


.. image:: /images/publish-03-dataviz-html-example.jpg
   :align: center
   :scale: 80%

**3**:
This table contains all the layers you have configured to be able to show statistics in your Lizmap project. All details about the configuration are shown in this table. You have to use it if you want to remove a layer, you will need to click on a line of the table then click on the button |remove_layer_svg| at the bottom on the panel.

**4**:
To add a graph, you have to configure it in this part of the panel.

   * **Type** : You can choose the type of your graph, the available options are - scatter, box, bar, histogram, histogram2d, pie and polar.
   * **Title** : Here you can write the title you want for your graph.
   * **Layer** : You chose which layer you want to make a graph with.
   * **X field** : The X field of your graph.
   * **Y field** : The Y field of your graph.
   * **Group?** : For a few types of charts like 'bar' or 'pie', you can chose to aggregate the data in the graph. There are a few aggregate functions available - average(avg), sum, count, median, stddev, min, max, first, last
   * **Color field** : you can choose or not a color field to customize the color of each category of your chart. If you want to do it, you need to check the checkbox, then chose the field of your layer which contains the colors you want to use. The color can be written like 'red' or 'blue' but it can be an HTML color code like '#01DFD7' for example.
   * **2nd Y field** : You can add a second Y field, it does not work for every type of graph, it's only working for histogram2d.
   * **Color field 2 ?** : You can chose the color of the second Y field the same way you chose the one for his first Y field.
   * **Display filtered plot in popups of parent layer** : if you check this checkbox, the children of your layer will get the same graph as the parent plot but filtered only for them. It's useful if you want to see the statistics of one entity instead of all.
   * **Only show child** : The main graph will not be shown in the main container and only the filtered graph of the relation of the layer will be displayed in the popup when you select the element.

|add_layer|

Examples
--------

You can visit the Cats project on https://demo.lizmap.com

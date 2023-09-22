The scatter chart shows the relationship among two metrics, for instance between units and price.  

Datasets larger than 100k observations are plotted as [datashader](https://datashader.org/) heatmaps. The  darkness of each shape is proportional to the number of observations encountered. The chart below plots 900k observations.

![scatter_datashader](assets/images/scatter_datashader.png)

 Datasets smaller than 100k observations are plotted as scatterplots by default. 

![scatter_4eeed60c2297a702c3f14e7147b92f0c](assets/images/scatter_4eeed60c2297a702c3f14e7147b92f0c.png)

You can decide not to show the isolines and you get this.

As default, each observation will represent a dot. 

If you to aggregate by some dimension, for instance by product, one dot will represents the total of sales for each product in the period. This returns a plot a lot less dots, in which each dot represents the total sales, and the average gross margin, of a product.

To further reduce dot clutter you can plot one or both axes of the plot in log scale. Log scales disables both isolines and trendlines.

The plot is run at the total plotted data level. You color the dots in the plot by the facet dimension  

The plot also runs on the chosen facet dimension. 

You can plot a regression trendline.

In the cases in which the two X and Y metrics can by multiplied in order to show a third metric (here: Units x Average Price in Units = Sales) you can plot isolines of the third metric. 

You can choose whether to plot the isolines labels at the right or at the left of the isolines using this widget.

 Isolines can change the range of the chart. 

You can choose to plot one period, or both periods together. If you choose to plot both periods together you can color each dot based on the period. 

The Y-axis metric and the X-axis metric widget allow you to change the axes of your plot. 

You can change the number of top items for the coloring and faceting dimension.

You can choose whether to exclude outliers from the plot. 

##### Small multiples plot

![scatter_4eeed60c2297a702c3f14e7147b92f0c_189dc7fe824def6fd3f79a2eb6e8d5b3](assets/images/scatter_4eeed60c2297a702c3f14e7147b92f0c_189dc7fe824def6fd3f79a2eb6e8d5b3-16931557417201.png)




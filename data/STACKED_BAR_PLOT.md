The plot shows repartition of a metric across two dimensions in absolute value or as % of total at a given point in time. It is inspired by the [stacked bar chart](https://www.ibcs.com/resource/ibcs-stacked-bar-excel-chart/) IBCS template.

![stacked_bar_in_absolute_value](assets/images/stacked_bar_in_absolute_value-16842482969241.png)



The plot is run twice once for each period.

Categories are sorted by decreasing total metric value with "other rank > x" on the bottom of the plot. 

###### ONE DIMENSION BAR PLOT

If only one dimension is selected, the app with return a simple (not stacked) bar plot.

![bar](assets/images/bar-16842483349152.png)

###### SMALL MULTIPLES PLOT

To plot the items as small multiples, set the Plot Small multiples widget to True. 

![stacked_bar_small_multiples](assets/images/stacked_bar_small_multiples-16842483492743.png)

The items of the first selected dimension will be plotted against the other selected dimension. If relevant, the average of each sub plot is shown.

By default the subplots will show the top items calculated at the global level, and therefore the items will be identical for each sub plot. You can change this with a widget

###### NORMALIZED STACKED PLOT

Values can be plotted in absolute value, as a % of total dataset, as a % of total dataset after filters, or as a % of the result row. The last two options only make sense if you plot a result row.   

![normalized_stacked_bar](assets/images/normalized_stacked_bar-16842484258434.png)

##### NEGATIVE VALUES

Negative values - for instance negative margins - will be plotted correctly. However you might need to adjust the label positions by hand.


The plot shows the value of the metrics available in the dataset across periods in absolute value or as % of the total. It is inspired by the [stacked column chart](https://www.ibcs.com/resource/chart-template-01/) IBCS template.

![stacked_column_in_absolute_value](assets/images/stacked_column_in_absolute_value-16842488066901.png)

#### COLUMN PLOT

The plot is run for the chosen metrics at the total level and, for the chose dimension, it is run for the chosen metric. 

Categories are sorted by decreasing total amount value with "other rank > x" on top of the plot. 

The integrated legends can also be positioned on the right or on the left of the plot.

The column width changes based on the aggregation period. Greater for years and quarters smaller for months and weeks.

It will also change based on the kind of metric. As per IBCS, ratios (price, % discount,...) are shown with thinner bars.

If you choose two metrics  the app will automatically plot an overlay chart. 

#### NORMALIZED STACKED COLUMN PLOT

![normalized_stacked_column](assets/images/normalized_stacked_column-16842492870503.png)

Values can be plotted in absolute value, as a % of total dataset, as a % of total dataset after filters, or as a % of the result row. The last two options only make sense if you plot a result row.   

#### SMALL MULTIPLES

![stacked_column_small_multiples](assets/images/stacked_column_small_multiples-16842492529062.png)

To plot the items as small multiples, set the Plot Small multiples widget to True and hit the Submit button.

#### SUMMARY STACKED COLUMN PLOT

![summary_stacked_column_percent](assets/images/summary_stacked_column_percent-16842492980294.png)

If more than one dimension is chosen, a summary plot will be generated for the chosen dimensions (up to six), that shows the break down of the chosen metric. 

Use the "choose dimension to plot" widget to choose the metrics to plot. 

#### MAX NUMBER OF TIME PERIODS

The app plots a maximum of 25 time periods, and a maximum of 6 data series, again following [IBCS](https://www.ibcs.com/resource/chart-template-01/) recommendations.

#### SHOW CAGR IN DATA COLUMN

You can choose to show the CAGR values. 

If the widget is set to True, calculated CAGR values will be shown on the data column on the right of the plot. If the plot is in successive quarters, months or weeks, the CAGR metric will be compounded by quarter, month or week, and shown as CQGR, CMGR or CWGR.

#### FIXING THE CHART SCALE ⚖️

You might have two charts you want to display together. Take this example.

This does not work because the charts have different scales. What is not the same here looks the same. This is not good. 

You could try using scale bands. Scale bands need to be added manually, for example in Powerpoint.

However this is not an optimal solution. The values of the two charts are in the same region, so it makes more sense to plot both plots with the same upper Y-axis scale limit, which would give this, a much better representation.

To "fix" upper limit scale values you need first to figure out which is the chart with the highest value. Set the "Plot small multiples" widget to False and  set the "Fix chart scale" widget to True. Submit to plot the chart.   

#### NEGATIVE VALUES

Negative values - for instance negative margins, will be plotted correctly, however value and legend labels might miss placed and need to be adjusted by hand.


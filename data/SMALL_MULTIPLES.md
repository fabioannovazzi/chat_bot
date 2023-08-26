Charts (with the exception of area, dot, marimekko, barmekko, bubble, motion, pareto, pareto stacked column plots) can also be plotted as small multiples (also called Trellis plots).

Some plots types (scatter, box plot, kernel density, histogram, ECDF, stripplot) the app will plot both totals and Small Multiples by default.  

For other plot types (year-over-year waterfall,year-over-year column, year-over-year line, year-over-year by period, timeline, stacked column, stacked bar, slope, multitier bar, upset, venn) you need to explicitly choose the Small Multiples option.

![year-over-year_column_small_multiples_Plan](assets/images/year-over-year_column_small_multiples_Plan-16842472461821.png)

When the Plot as small multiples widget is set to True the app will behave as follows. 

- If more than one metric has selected the app will plot Plot small multiples of the total for each selected metric. For instance, if Sales and Gross Margin have been selected as metrics these two metrics will be plotted with the same scale. 

- If a single metric is selected, the app enable a widget for the choice of a dimension column and will plot small multiples along that dimension. 


It will also plot the total of the metric for reference purposes. 

For many chart types, a simplified representation will be used for small multiples. For example in the case of the horizontal waterfall chart, small multiples do not have the percent pins...

![year-over-year_waterfall_small_multiples](assets/images/year-over-year_waterfall_small_multiples-16842474923733.png)



...that are built into the standard chart. 

![year-over-year_waterfall](assets/images/year-over-year_waterfall-16842473396772.png)


The multi-tier bar chart, inspired by this [IBCS template](https://www.ibcs.com/resource/multi-tier-bar-charts/), can be used to analyze the data structure of different dimensions.

The first tier of this template compares different scenarios in a grouped bar chart. The second and third tiers show different absolute and relative variance charts. 

The most recent, Actual, value is show with in black. The less recent, or Plan, value, is shown with in grey or outlined white. Red is  "bad" while green is "good."

![multi-tier_bar](assets/images/multi-tier_bar-16842480581731.png)

The plot is run for the chosen metrics at the total level and, for each dimension, it is run for the chosen metric.

###### SMALL MULTIPLES PLOT

To plot the items as small multiples, set the Plot Small multiples widget to True. ![multi-tier_bar_small_multiples](assets/images/multi-tier_bar_small_multiples-16842481116002.png)

###### SMALL MULTIPLES PLOT BY SINGLE DIMENSION

If you select only one dimension (in this case Country) the items of that dimension will be plotted against another selected dimension. 

![multi-tier_bar_small_multiples_by_single_dimension](assets/images/multi-tier_bar_small_multiples_by_single_dimension-16842481633793.png)

By default the subplots will show the top items calculated at the global level, and therefore will be identical for each sub plot.  You can change this with a widget.




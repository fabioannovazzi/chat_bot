The year-over-year column chart, inspired by this [IBCS template](https://www.ibcs.com/resource/multi-tier-column-chart/),  contains three parts. 

In a first tier, this plot compares different scenarios in a grouped column chart. The second and third tiers show different absolute and relative variance charts. This 3-tier chart can be used to analyze the temporal development of different scenarios. It is good at looking at and comparing single monthly variances.

The plot is run at the total level and, for each dimension, it is run for the chosen metric.

![year-over-year_column](assets/images/year-over-year_column-16842496811732.png)

![year-over-year_column](assets/images/year-over-year_column-16842495809081.png)

The most recent, Actual, value is show with in black. The less recent PY value is shown with in grey, in white if Plan. Red is  "bad" while green is "good."

Plan data will be shown in white, Forecast data will be shown hatched. Actual data will be shown in black. Previous year data will be shown in dark grey. Forecast data must be tagged in the dataset as "FC".

#### SMALL MULTIPLES

To plot the items as small multiples, set the Plot Small multiples widget to True. 

![year-over-year_column_small_multiples](assets/images/year-over-year_column_small_multiples-16842497500633.png)



The small multiples plots show the yearly values and differences in values, but not the percent differences.






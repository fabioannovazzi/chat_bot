Root cause analysis is hard to implement in Excel. However, it is nothing new. When you say *"the top sales driver was the Chinese market* (dimension➡️country), *the second direct sales* (dimension➡️channel) *to large accounts"* (dimension➡️segment) you are doing variable dimension variance analysis: you are changing the dimensions of each result.

![vertical_waterfall_bae6db8eda0034cca55664df2a3143ea](assets/images/vertical_waterfall_bae6db8eda0034cca55664df2a3143ea.png)

![table](assets/images/table.png)

The app computes all possible combinations, ranks them according to user-defined parameters, and returns a set of facts that explain the change.

Since the selected combinations are the most significant, this allows to explain significant positive and negative change with a limited number of results. 

If the standard number of requested results - five - is not enough to cover all the variance, a "residual" entry will appear.

#### ALTERNATIVE RESULTS

Root cause analysis returns many result combinations, which are all algorithmically correct, but might be more or less insightful, and therefore useful to you.

To increase the probability of surfacing the more insightful scenarios 'Mparanza uses heuristics: it offers a certain number of "scenarios". Each "scenario" is a set parameter settings, designed to maximize the probability that the result will have certain characteristics.  This can be simpler than adjusting parameters.

The default scenario is the "choose the largest combinations" scenario that essentially returns the combinations in order of variance size. 

In default mode, given the choice of a scenario, the app will select the top ranked combination as the top result, net the value of that combination from all remaining combinations, and run the loop again, to return the second result, and so on.

You can, for instance ask the app, to skip the first result, and select the second top ranked combination as the top result. This will result in a different set of results. 

You can drilldown on one of more result rows.  You can insert one or more of the drilldown result rows back into the main report. 

You can filter the data of a result row and use it to plot any other chart. 

#### ALTERNATIVE COMBINATIONS PLOT

The alternative combinations plot shows, for each dimension of a given row result, the variance value that would result by changing the filter on that one dimension. This is useful to visualize the impact of each item on variance. 

![alternative_combinations](assets/images/alternative_combinations-16842609259861.png)

The size of the bubbles is proportional to the average monetary amount in the two periods. Hover on the bubbles to see the alternate combinations.


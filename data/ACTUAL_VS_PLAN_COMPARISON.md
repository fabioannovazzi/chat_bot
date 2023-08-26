It is often necessary to compare Plan and Actual data. 

We use the recommended [IBCS](https://www.ibcs.com/) standard notation which is PL for Plan and AC for actual. Also according to the standard, we color the fictitious Plan data in white and the measured Actual data in black. 

#### DATASET WITH PERIOD/SCENARIO COLUMN ONLY

In some cases, the data is aggregated at the total period level. For each combination we have only two observations, the AC total and the PL total. 

Such a dataset will look like this and will have only a Period/Scenario column, and no Date column.

In this case the app will automatically compare the two periods without further ado. 

If the period order is not right you can reverse it and the order will be changed.

#### DATASET WITH PERIOD/SCENARIO AND DATE COLUMN 

More often the dataset will have a column with the Scenarios (the Period/Scenario) column and a Dataset column in date format with the dates, so it is possible to compare a specific Actual interval to the corresponding Plan period. The app can manage two Scenarios - typically AC vs PL. If your dataset has more than two scenarios - AC, PL, revised PL1, revised PL2 - you will have to decide before loading the data which scenario you want to compare with the Actual. 

In this case the dataset will have both a Period/Scenario column - with will be set either to Actual or to Plan - and a Date column in date format.

In this case the app will ask you to specify the time range of the comparison. This allows you to compare the Actual data you have with the relevant Plan interval. 

If the app incorrectly guessed the order of your periods you can reverse the order. 

If the dataset has both Period/Scenario and Date column it is possible, among other options, to compare Actuals and Plan on a month-by-month basis

You can also analyze such a dataset in terms of Actual versus Previous Year (thus ignoring the PL data). Simply set the "Compare" widget to "Periods".


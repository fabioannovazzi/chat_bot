The tool can be used to compare scenarios or to compare periods.

#### PERIOD AND SCENARIO COMPARISON

An example of scenario comparison is Actuals vs Plan variance, while an example of period comparison is 2019 vs 2018.

The period you want to compare might be directly mapped in a column. In this case the column - a "Period" column in our parlance - might have two values - 2019 and 2018 you want to compare.

Alternatively, if you have a column in data format - "a Date" column in our parlance - you can choose the time aggregation the app must use to aggregate the periods you want to compare. 

#### DATE AGGREGATION

If you supply the tool with a date column, the tool will allow you to:

- compare the calendar years (or  quarter, months or weeks) against each other 
- compare period-to-date values
- moving (or rolling if you prefer) analysis of previous 12 months 

We refer to the IBCS  recommendation of the standard for our time period notation. 

In particular, we use the IBCS notation for time series analysis of calendar, to-date, and rolling periods:

- calendar comparison (by year, quarter, month or weeks) is notated normally, as you would expect. For example 2018Q3 vs 2018Q4.

- period-to-date (for instance YTC) comparisons are notated by prefixing an underscore to the time period name. For example _2018Q3 vs _2018Q4. 

- rolling period analysis is notated by prefixing a tilde to the period name. For example ~Year vs ~Year N-1.


Average values are notated with the Ø symbol

#### CALENDAR COMPARISON

For calendar comparison set the Compare with Period to Date widget to False and the Compare with Rolling Period widget to False

To compare with the previous quarter (up to most recent date) set the Date Aggregation widget to Quarter.

#### PERIOD TO DATE COMPARISON

For year to date comparisons set the Compare with Period to Date widget to True.

This chart will compare the most recent period (calculated from its start to the most recent available date) to the equivalent period of the previous year. 

If you click on "dataset info" in the "Load📤Data" tab you will get short report with the periods found in the dataset.

The shown periods will changed depending on the date aggregation choice. 

If you have multiple periods in your dataset  - 2014, 2015, 2016 and 2017 - and you want to understand what happened across the whole timeframe, year after year the tool can help you in this analysis by letting you run the three different analyses - 2015 vs 2014, 2016 vs 2015 and 2017 vs 2016 - very easily. However, you will have to stitch the three results together by yourself, out of the system.

The value of the most recent date is also shown under the "dataset info" expander.

#### ROLLING PERIOD COMPARISON

For rolling period comparisons set the Compare with Period to Date widget to False and the Compare with Rolling Period widget to True.

If there is not enough data to go "backwards" by 24 months from the most recent date the app will return a warning and fall back to a simple calendar year comparison.

#### CHANGING REFERENCE PERIOD

You can choose the reference period you want to select for the comparison with the "most recent period" widget. If you choose "n" it will select the most recent period in the dataset as the "second" period in the variance analysis comparison. 

If you choose "N-1" it will choose the second most recent periods as the reference period and show the new end date of the reference period.

The chart total label and the variance values will naturally change. 

#### COMPARING QUARTERS, MONTHS OR WEEKS

The tool can also compare quarters, months or weeks. If you select month and set "compare with year before" to True it will compare with the corresponding month of the year before. Otherwise it will compare with the preceding month. 

All charts will plot the chosen date aggregation comparison.

#### INVERTING PERIOD ORDER

You can invert the order of the comparison, and set the most recent period as the "first" period in the comparison. 


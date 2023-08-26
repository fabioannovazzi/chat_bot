If your dataset has a date column, you can choose whether to compare calendar periods, period to date, or rolling period. The app will automatically start calculating backwards from the most recent observation it finds in the dataset. 

Note that the app uses the IBCS  notation to indicate the time period comparison. "2020" stands for "calendar 2020", "_Feb-2020" stands for "YTD February 2020" and "~Feb-2020" stands for "February 2020 12 months rolling". 

The app also uses the IBCS notation to indicate the period. So "AC" is actual, "PL" is plan, "FC" is forecast, "PY" is previous year and "PPY" is the year before the previous year. 

The IBCS semantic notation is used for the period color. A "AC" bar will always be colored solid black ⚫. A "PL" bar will be white ⚪. A "FC" bar will be hatched. "PY" will be dark grey, "PPY" light grey. 

 The app will automatically check if the chosen period comparison can be calculated. For example, unless you have 24 months in your dataset you will not be able to calculate 12 months rolling. 

You can also set the period to Quarter, Month and Week. 

You can go back in time and instead of comparing the current, most recent, period with the year before, compare the n-1 year with the n-2 year.

If your dataset has both a Date column and a Scenario Column (for instance Actual vs Plan) you can choose whether to compare periods (aka this year vs previous year) or scenarios (aka this year Actual vs this year Plan). 

You can choose the time horizon of the scenario comparison calculation. For instance compare Actual vs Plan from January to March 2020.

If your dataset has only two scenarios (say Actual and Plan) and no date column can also invert the scenario order that the app has automatically chosen.

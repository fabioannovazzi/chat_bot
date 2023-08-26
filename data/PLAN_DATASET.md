Builds a PL/FC dataset from a baseline 12-month calendar or rolling Actual dataset. By PL we mean Plan (next year's budget), by FC we meant Forecast (modified forecast during year).

Input is a dataset with 12 months of Actual data, either calendar or rolling. Output is a dataset with both the Actual and the PL (or FC) data, calculated modifying the Actual data with the hypothesis inserted by the user. The user can then run this file in the app, check the results of the hypothesis and if necessary iterate.

#### Set up

You want to set the value of the forecasted rows as PL (plan) or FC (forecast).

In terms of seasonality, by default the monthly profile of the PL/FC file is the same as the profile of the actual data file. Future seasonality is the same as past seasonality. It is also possible to build the PL dataset with all identical months or to set seasonality.  On "Set", you can provide a seasonality parameter for each month. 

Select what forecast to use when one dataset row matches more than one forecast condition. For instance, if the user wants China sales up 10% and Supermarket sales down 5%, the system needs to know what to do with China sales in Supermarkets. The choices are "All" (in this case it will apply the product of the forecasts, here 1.1 x .95) or "First" (in this case it will use the first forecast condition that the user has keyed in).

If other metrics beyond Sales or Costs (typically discounts and/cogs) are present in the dataset, choose whether to set the forecast of these metrics proportionally to the change of Sales and Costs, or whether to set the forecast separately for each metric.

Set the default forecast PL/FC vs AC change in units and in price. This will forecast will be applied to all rows of the dataset. 


Now  add the first dimension for which you want to forecast something different from the default above.


For example, say Return is added as an dimension with the value "No".  When this condition is met units and prices should go up 5% more than the default (so 1.05 x 1.10 for units and 1.05 x .95 for price). 

The user can add other items (click on New item) to the Return dimension, and for instance specify that in case of Yes, units and prices will go up 10% more than defaults (so 1.10 x 1.10 for units and  1.10 x .95 for price).

The user can add new dimensions (click on New dimension), example Category, and specify that Office Supplies forecast modify default by 1.10 in units and .90 in price.

Sales of No Return and Office Supplies Category will be treated based on the setting of the "If collision between dimensions" widget. If "All" the app will calculate the product of the factors (here for units 1.05 x .90 for units). If "First" it will take the First forecast, here "Return: No" (1.05 for units ). The resulting factor will be multiplied by the default forecast.

You can also select multiple dimensions, and treat sales of No Return Technology Category as a single item and set their forecast modifier. Here +1.30 in volume and +1.30 in price. Note that since the intersection has been specified by the user, in this case there will be no multiplication of factors, even if "Multiply" has been selected. The Category=Office Supplies + Return=No condition pair overrides the separate Category=Office Supplies and Return=No conditions. 

Similarly in this case. 

The two conditions will be processed independently.

The rows where Category = Technology and Segment = Consumer will be modified as 1.1 (default) times 1.2 (condition), while the rows where Segment = Consumer (*and Category != technology*) will be modified as 1.1 (default) times 0.1 (condition).

The system will work similarly in the case of hierarchical items.  For sales in Rome, only the "Rome" 1.2 multiplier will be applied, and it will not be multiplied by the 'Italy' 1.10 multiplier. 

You can add up to 6  sets of dimensions. For each set of dimensions you can add 5 items or sets of items each with a different set of forecasts. 

If you have chosen to set the monthly time profile yourself twelve widgets will show up. The widgets are initialized to 100 and the sum of their values must always be 1200.

You can modify the widgets to increase of decrease the weights of the different months and create the seasonality you desire. You might want to model this in Excel first to save time. The app will give a warning and ignore your monthly modifiers if the total is not 1200. 

When you are done, hit the Submit button.

Click on the download widget to get the PL/FC dataset. The dataset will have both PL/FC data and the 12 actual base months.

You can load the dataset on the app to see how your hypothesis pan out together, and iterate until you are happy. For speed open a second, new, 'Mparanza session. 

#### Output

This is the result. White is Plan, black is base year Actual. 

Notice the boost of Return = No, Category = Office Supplies sales. 

To use the file for your reporting, open it in Excel and delete all the AC (12 base month actual) rows in the Period column. Then concatenate the PL/FC file to your new monthly actual sales data.

During the year, as your view of the future changes and becomes more precise, you add your new FC (forecast) data to your dataset and to your reports. Open the file in Excel, delete the AC row, select the FC rows of the periods you want and collate them to you original AC + PL file. 

Forecast data is shown hatched in the chart above per IBCS standard. 




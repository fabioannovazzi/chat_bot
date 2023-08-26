#### VARIANCE CALCULATION APPROACH

The app computes the variance "bottom up" as the sum of the variance of the single rows of the dataset. This makes it possible to slice and dice the data and calculate variable dimension variance. It also avoids that the price variance value reflects changes of mix, instead of only changes of price.

However, since we reason by dataset row, we calculate Price and Cost variance only for the row combinations that are referenced in both periods. If a combination is observed only in one period, all the variance will be considered as Volume variance.   

The reason is that each dataset row contains the values of our metrics (Amount, Quantity, Costs) for a given combination of dimensions in the first and/or the second period. If a given combination is not referenced in both periods, we cannot calculate the price and the cost variance, and, as mentioned, all the variance will be booked as volume variance. 

#### CHOICE OF VARIANCE CALCULATION

Choose the variance calculations that can best answer your business question:

- *after COGS* shows margin variance after COGS. Use when you just want to know which combinations impacted on margin change, but are not interested on whether it was volume, price or cost.
- *price, volume & mix, margin rate* shows impact on margin of price, volume and margin rate variance. Use when products have very different margin rates, since this approch normalises marginality.
- *price, volume & mix, costs* shows price, volume and cost impact on gross margin change.
- *price, volume & mix, discounts, COGS* shows price, volume, discounts and cogs impact on margin change. Since the formula does not perform allocation of "common" values, result is biased towards volume variance.
- *after discounts* shows variance after discounts. Use when you just want to know which combinations impacted on change of variance after discounts, but are not interested on whether it was volume, price or discounts.
- *price, volume & mix, discounts* shows price, volume and discount impact on net sales.
- *price & volume & mix* shows sum of price and volume variance.
- *price, volume & mix* details price and volume variance.
- *price, new, lost, changed* details volume variance in new, lost and changed volumes. "New" volumes are combinations with no sales in the first period. "Lost" volumes are combinations with no sales in the second period.
- *price, volume, mix* details volume variance, price variance and variance due to the change of product mix.
- *price, volume & mix, drivers* details volume variance, price variance, and variance and variance due to the impact of your driver column/s
- *price, volume, mix, drivers* details volume variance, price variance, variance due to the change of product mix, and variance due to the impact of your driver column/s.

#### CONJUGATE VARIANCE ALLOCATION

Variance calculation inevitable results in a "common" area that has to be attributed in some way. 

##### ALLOCATION ON TWO DIMENSIONS

When variance is calculated on two dimensions - price and volume - the common area that must be attributed can be depicted as a rectangle. The area, represented in yellow below, represents the intersection of the volume and of the price variance effect. 

One method is simply to attribute all this common area either to volume or to price variance. This reflects a widespread but somewhat arbitrary practice.  

'Mparanza avoids this issue by allocating the common area equally between price and volume variance.

##### ON THREE DIMENSIONS

Things get more complicated when variance is calculated on three dimensions -for instance price, volume and margin rate"- to identify the factors behind margin change.

The common rectangle area becomes a tri-dimensional box, or rather a collection of boxes in the tridimensional space.

#### MIX VARIANCE

Price variance is the impact of the change of price on revenues, keeping volumes constant. Volume variance is the impact of the change of volume on revenues, keeping prices constant.

What kind of variance is it when prices and volumes do not change but customers shift their purchases towards more expensive or less expensive things? That is mix variance.

You are still selling 10 jars of nutella, prices per SKU have not changed, but instead of selling 5 small jars and 5 large jars, you are suddenly selling 2 small jars and 8 large ones. In this case your mix variance will simply be the difference of the price between large and small nutella jars times 3. Mix variance is very important . It is also tedious to calculate as the number of products increases.

Calculating Mix variance makes sense if it refers to a change in the sales proportion of the products that in some way share similar characteristics.  Mix variance calculation can return misleading results when calculated across a too wide spectrum of prices.

For this reason, when calculating Mix variance, the app allows you to drop the highest and lowest price quartiles. 

To enable this behavior, click on the ➕ sign below the "Show variance as" widget and set the "Drop price outliers from mix variance calculation" widget to True.

You can also change the quartile range of dropped prices with the "Quantile value to exclude" widget. Top and Low quantiles will be dropped. 

#### NEW AND LOST VARIANCE

"New" variance is tied to combinations that have sales only in the second period. "Lost" variance is tied to combinations that have sales only in the first period. You can choose this option with the "show variance as" widget.

Example. A combination might be the following: 

Product: Shirts, Color: Red, Brand: Armani, City: Milan. 

If this combination exists in the first year but this precise combination does not exist in the second year, the system will return a "Lost" variance value. Similarly if this exact combination does not exist in the first year but exists in the second, the system will return a "New" variance value. Changed volume variance refer to combinations that can be found with positive sales in both periods. 

In case of "New" many things might have happen:

1. We introduced the "shirts" product line
2. We introduced "red" color in the "shirts" product line
3. We started selling "Armani" brand apparel
4. We opened a shop in Milan
5. All or any combination of the above.

In other words, "Lost" and "New" simply mean that "something changed", but does not directly tell you anything about "what" exactly changed. It gives some indication of "stability". Please let us know if you find it useful. 

##### "LOST" AND "NEW" VS PRICE VARIANCE

The app calculates variance "bottom" up, summing up the variance values of all combinations. If a combinations is "Lost" or "New" for that combination it is impossible to calculate the price component of the variance, because for one period units are zero and there is no price. Therefore for all Lost and New combinations, all the variance is booked as volume variance.  This means that the price variance value calculated with this approach will generally be different from the price variance value calculated simply summing up all the rows and then computing the variance.  

##### MIX VARIANCE AND NEW AND LOST COMBINATIONS

Please not that, by necessity, mix variance only measures the effect on variance of the change in relative proportions of the *combinations that exists in both periods*. If a combination exists only in one period, the impact will be entirely booked as positive or negative volume variance. 

It is all New volume. 

#### DRIVER VARIANCE 

Variance can also be a function of drivers, such as the number of customers, and their conversion rate, or the number of shops, and the average sales per shop. 

#### VARIANCE ON MARGINS

To see the impact of the change of product mix on gross margin, select "show variance as" => "price, volume & mix, costs". Submit. 

The application shows the % value of margin on revenues in the two periods. This calculation has not be fully validated yet and should be considered as a purely indicative. The algorithm is illustrated below.

#### PLOTTING VARIANCE IN TERMS OF SHARE

Click on the cross below the "Show variance as" widget to access to the "Show variance as share of total" widget.

Set the "Show variance as share of total" widget to True.

Then filter the dataset to the subset you want to measure the share change on.

Choose if you want the analysis as a fix or a variable dimension bridge. 

Click on the submit button.

You should get a % share chart.

#### VARIANCE ON MARGINS IN PERCENT

Select Run => "Fix dimension bridge". Select Show variance as => "after COGS", click on the expander menu below and set Variance as % of revenues to True.

Selecting Run => "Variable dimension bridge" will return the combinations that contribute to the change of margin as % of revenues. 

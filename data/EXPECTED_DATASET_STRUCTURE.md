The tool expects a dataset in "tidy" form:

- Each variable must have its own column.
- Each observation must have its own row.
- Each value must have its own cell.

You can download an example file from this [here](https://mparanza.com/download_docs/Superstore.xlsx).

The uploaded file can have a maximum size of 200MB.

#### Required Columns

Your uploaded file needs to have:

- A few "dimension columns" (e.g. channel, product, country,..). Call them as you wish. 
- A Sales column. Call it "Amount". This column must be in plain number format (no thousand separators). In Excel they need to be in the "General" number format or in the "Number" format with no 1000 separator, no currency format, and zero written as 0 not as -. If you select "Run"> "Data Profiling" a data profiler report will show you how your data was read. If the number columns have not been read like numbers, you have a problem with your format.
- Either a Date or a Period column.  Call them "Date" and/or "Period". A date column is a column in date format, while a period column already groups the data in the "before after" periods we need for the bridge analysis. If you have a date column, the values must be in the form YYYY-MM-DD."

'Mparanza does not need a Price column. It will re-calculate the unit price and ignore Price columns if present.

#### Cost and revenue column expected format

As mentioned, the cost and the revenue column must be in plain number format with no thousand separators. Since there are different standards of thousands separators (1'000 in USA and UK, 1.000 in Continental Europe) the app would not know how to parse the number.

#### Negative value format

Negative values are normally formatted with a leading minus sign ("-20"). Some ERP systems, such as SAP always store negative numbers with the minus sign at the end of the value.  If the app finds a trailing minus sign, it will automatically try to correct it and will return a message. 

#### Other Metric Columns

Your uploaded file can also have other metric columns:

- A *units column*. Measures the number of items/packs of product sold. This column must be in plain number format (no thousand separators). If the dataset has a units column, the code will also calculate the "unit price" variance. If the dataset only has a cost/revenue column, all variance will be classified as "units" variance.
- A *volume column*. Measures the volume (kilos, liters, bottles,...) of product sold. This column must be in plain number format (no thousand separators). If the dataset has a volume column, the code will also calculate the "volume price" variance. If the dataset only has a cost/revenue column, all variance will be classified as "volume" variance.
- A *discount column*. If the dataset has a discount column, the tool will also return the "discount variance" (variance after discounts and commissions). The discount column must contain the discount in absolute value (not in %) and must be in positive sign. A discount of 100$ must appear as 100.
- A *COGS column*. If the dataset has a COGS column, the tool will also return the "COGS variance" (variance after COGS). The COGS column must contain the COGS in absolute value (not in %) and must be in positive sign. A cost of 100$ must appear as 100.
- *Promo and No Promo* quantity and amounts columns. If the dataset has Promo/No Promo columns, the tool will offer some promo-related visualizations.

#### Driver columns

A dataset can also have "driver columns".

 A driver column contains a metric that is expected to have a (more or less) linear relationship with the cost/revenue column, everything else being equal, and that therefore help explain the change in sales.

These are  columns such as Visits, Bookings, Distribution. 

For instance if a company sells in one shop only and sells 100$ in year 1, one might assume that if in year 2 it sells 200$ and has added a second shop, the increase is due to the larger distribution - assuming every thing else stays equal.

Similarly if the number of visits to the website doubles and everything else (conversion rate, average price, volumes per purchase act) stays the same, you would expect revenues also to double. If the sales of a website double and the visits to the website double - assuming every thing else stays equal - that increase in due to more visitors. If the visitors stay the same but the number of checkouts double along with the sales, that increase is due to a better conversion ratio.

These metrics have to be in value (not in %) - for instance: number of bookings, not conversion rate. 

Note that the dataset above contains no ratios, just the raw values of Visits, Bookings, Nights and Amount. Bookings on Visits is the conversion ratio. Nights on Bookings is the average number of nights of stay. 

'Mparanza returns the variance - the impact on sales in other words - tied to the change in the number of visits, in the proportion of visitors that buy, in the number of outlets that stock the product.

'Mparanza calculates driver variance, making it easy to understand what is driving change.

If the dataset has one or more driver columns the tool will return one or more "driver variances", that maps the impact/s of the driver/s.

The tool manages the following driver columns:

- *Category weighted distribution*. Measures the weighted number of outlets where a given product is available for sales. If distribution points double, sales double and everything else stays the same, the increase will be allocated to distribution variance rather than volume variance (which would measure the "per outlet" sales change).
- *Checkouts*. Measures the number of purchase decisions (tickets, bookings, checked out shopping carts,...). If checkouts double, sales double and everything else stays the same, the increase will be allocated to checkouts variance rather than volume variance. Everything equal an increase in check out variance indicates an improvement in conversion.
- *Visits*. Measures the number of customer interactions (shop/website visits, traffic, inquiries, leads,...). If visits double, sales double and everything else stays the same, the increase will be allocated to visits variance rather than volume variance. Everything equal an increase in visits variance indicates an improvement in traffic.

If your dataset has other driver columns you would like us to include in the tool, please contact us.

#### Dataset info expander

The app shows a report with information related to the dataset such as the number of rows, the columns, the hierarchy within the columns, dropped columns, variance values, time periods.  

When the variance calculation option is set to "Multiple dimension variance" the app tries to estimate the correlation of the different dimension columns to the variance value, in order to automatically drop the least correlated columns and optimize performance . 

All items in each column are grouped in two groups, so that the sum of the Amount column for the two groups is as similar as possible. The correlation is then calculated between the variance metric and the 0 vs 1 value of each newly created "group" column.  

The app drops the least correlated columns if it senses that this is necessary to avoid a degradation in performance.  In the example below, the "Product_Code" column is dropped from the analysis since it is found to have the least correlation . 

Please note that the columns are **dropped from the whole database**, so they will **not be plotted in any graph**. To avoid this, simply set the Variance calculation widget to Fix dimension bridge. 

#### Column detection

How does 'Mparanza recognize that a column is a dimension column such as "country", "channel", "product"? 

Because the column it is not numeric. You can disable this behavior if you want. 

You will need to do this if the dimension columns along which you want to analyze your dataset are, for instance, the accounting codes. 'Mparanza will do its best to detect them anyway. At the bottom of the printout you have the list of the dimension columns that were detected. 

If two dimension columns are "equivalent" (every value in one column corresponds to a given value of the second column) 'Mparanza will discard one of the two columns, the second one. If you want to see the second column instead, you should reverse the order of the two equivalent columns in your dataset.

Please check if the equivalent columns in your dataset have been identified and dropped.

If not, the two columns probably are not perfectly equivalent. You can check this with the profiling report. Please correct and re-submit. Performance can degrade very significantly if the code has to process two "identical but not really identical" columns with high cardinality.

To detect the other columns - the monetary column  that contains the amounts, the period column  that contains the time periods, and the unit column that contains the volumes - 'Mparanza uses the same approach a human would use. It looks at the column name.

The advantage of this approach is that it is a lot quicker and more efficient. Once you have named your column in a way that 'Mparanza understands, it will forever load the dataset automatically, without asking you any more questions or taking any more of your time.

The code tries to recognize the metric and driver columns (cost/revenue ,quantity/volume, discount, COGS period, date , category weighted distribution,...) by searching for stems (for instance if "amount" is part of a column name, it will assume that the column is the cost/revenue column ). If it does not find the expected stems, the code will ask you to rename the columns in a way it understands.

For instance the monetary column name must contain a stem that 'Mparanza recognizes as associated to a monetary column field. The list of these stems is shown in the "detected columns" expander. If it finds a column named with one of these stems it will tell you that it has tagged that particular column as monetary value column.

If your dataset comes from a SQL query, changing the query just to make 'Mparanza happy is not really an option and renaming the column manually every time is a drag. If your favorite column name is not in our list, please send us a message and we will happily include it.






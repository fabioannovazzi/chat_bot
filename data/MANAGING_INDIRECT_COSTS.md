The tool helps break down the change in EBITDA between to periods into the specific factors driving change.

#### DATASET FORMAT

You need to have a column in your dataset with your indirect costs for the two periods you want to compare. This column should be called with one of these names: *'Indirect_Costs', 'Costi_indiretti', 'Coûts_indirects', 'Overhead', 'FP&A'.*

There is no need to allocate your indirect costs at the line-by-line level. 

#### EBITDA BRIDGE CHART FORMAT

The tool will return an EBITDA bridge with one item, labeled "Indirect costs" showing the change of the total value of indirect costs from one period to the other.  Allocation is therefore not necessary. 

#### EBITDA BRIDGE ANALISIS ALONG CHANGING DIMENSIONS

The tool can also return a 'variable dimension' EBITDA bridge showing different dimensions, or different combinations of dimensions, that explain the change in EBITDA. 

#### EBITDA BRIDGE ANALYSIS IN % OF SALES

An EBITDA bridge can also be shown, instead of in absolute value, in % of sales.

The same analysis of the impact on EBITDA in % can be done along a dimension.  

#### INDIRECT COST ALLOCATION

In you can simply add two rows on the top of your dataset with the value of the indirect costs in the two periods. No need to specify the dimensions. Note that the Amount and Unit column has been set to 0.000001, because, to optimize performance, tool drops zero rows.

Note that if you want to calculate both yearly and the monthly variance, you will need to input 12 monthly indirect costs values for each year you want to consider.  

Do not forget that the excel format of the number columns must be "general" or "number", otherwise the app will have problems parsing the CSV file.

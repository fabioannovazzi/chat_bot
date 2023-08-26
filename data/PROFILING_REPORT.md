The tool generates a profiling report of the dataset you can use to check whether the columns have been properly tagged as number or date format. 

Use the profiling report to check for issues in loading your dataset. For example, if the code has not found your cost/revenue column even though it is named correctly, check if the column is tagged as categorical and not as numeric. It this is the case, it might contain thousand separators or other problematic formatting options.

In high cardinality dimension columns, the 20% bottom ranking items will be automatically aggregated for performance. Aggregated items are tagged with the "Aggregated lower value items" label.
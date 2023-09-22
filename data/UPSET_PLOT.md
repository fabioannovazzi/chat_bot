An [Upset plot](https://ieeexplore.ieee.org/document/6876017) is an alternative to the [Venn diagram](https://mparanza.com/site/VENN_PLOT/) used to deal with more than 3 sets. The total size of each set is represented on the left bar plot. Every possible intersection is represented by the bottom plot, and their occurrence is shown on the top bar plot.

![upset](assets/images/upset.png)

UpSet plots the intersections of a set as a matrix. Each column corresponds to a set, and each row corresponds to one segment in a Venn diagram.

The plot is run also as small multiples. Just choose the dimension to plot as small multiples.

![upset_small_multiples](assets/images/upset_small_multiples-16948981133631.png)

 



You can choose the dimension you want to plot as sets of the plot as well as the dimension over which to calculate communality. In this example "Material" is the dimension plotted as sets, while "Country" (the materials sold in each country) is the dimension used to calculate communality.

You can choose to plot a Upset diagram with up to ten sets.  

You can also exclude the other sets. 

If there are many intersection, the app might return an unreadable chart.

You can filter out the intersections with less than a given number of elements.

You can plot the distribution of the variables along the metric as strip, box or violin plot.


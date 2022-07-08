# The Power of Plots





![Laboratory](Images/Laboratory.jpg)

Our Team used data companions rushed off to jobs in finance and government, We remained adamant that science was the way for us. Staying true to our mission, We've joined Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As as data analyst at the company, We've been given access to the complete data from their most recent animal study. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. We had tasked by the executive team to generate all of the tables and figures needed for the technical report of the study. The executive team also has asked for a top-level summary of the study results.



### Initial Preparation

* We ran the provided package dependency and data imports, then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.

* We displayed the number of unique mice IDs in the data, then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, then create a new DataFrame where this data is removed. 

* We used this cleaned DataFrame for the remaining steps.

* Display the updated number of unique mice IDs.

### Summary Statistics

* We create two summary statistics tables:

    * For the first table, use the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. This should result in five unique series objects. Combine these objects into a single summary statistics table.
    * For the second table, use the `agg` method to produce the same summary statistics table using a single line of code.

### Bar and Pie Charts

* We generated two bar plots:

    * Both of these plots are identical and shows the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.
    * We created the first bar plot using Pandas's `DataFrame.plot()` method.
    * We create the second bar plot using Matplotlib's `pyplot` methods.

* We generated two pie plots:

    * Both of these plots are identical and shows the distribution of female or male mice in the study.
    * We reated the first pie plot using both Pandas's `DataFrame.plot()`.
    * We created the second pie plot using Matplotlib's `pyplot` methods.

### Quartiles, Outliers and Boxplots

* Calculation the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Calculate the quartiles and IQR and quantitatively determine if there are any potential outliers across all four treatment regimens.

    * We started by creating a grouped DataFrame that shows the last (greatest) time point for each mouse, then merge this grouped DataFrame with the original cleaned DataFrame.
    * Next, created a list that holds the treatment names, as well as a second, empty list that hold the tumor volume data.
    * Looped through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list. Determine outliers using the upper and lower bounds, then print the results.
    
* Using Matplotlib, generate a box and whisker plot of the final tumor volume for all four treatment regimens and highlight any potential outliers in the plot by changing their color and style.

  **Hint**: We used [Matplotlib documentation page](https://matplotlib.org/gallery/pyplots/boxplot_demo_pyplot.html#sphx-glr-gallery-pyplots-boxplot-demo-pyplot-py) for help with changing the style of the outliers.

### Line and Scatter Plots

* We selected a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

* We Generated a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

### Correlation and Regression

* We calculated the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. Plot the linear regression model on top of the previous scatter plot.



## References

Mockaroo, LLC. (2021). Realistic Data Generator. [https://www.mockaroo.com/](https://www.mockaroo.com/)

- - -

© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.



# Matplotlib-Challenge
Sample analysis using Matplotlib

## Overview:

	Using Jupyter Notebooks to develop a report provides an opportunity to present a wide array of data frames, charts, and other visualization tools that make it easier for the consumer to understand the data. Ultimately, our goal in developing reports should be to allow the user to make the decisions necessary based on their data efficiently. As usual, once we understand the customer's needs, we should take a moment to explore the data and better understand its design and potential limitations. In this scenario, we will develop a report containing information that an internal and external customers can understand. We will utilize pandas' data frames functionality to help create reports and the matplotlib module to aid us in creating charts. We anticipate that the user will be comfortable moving around and manipulating the information. 
	Take a moment to open the .csv files and familiarize yourself with the data structures and layout. Exploring the data will allow us to see that the data contains multiple duplicates. In specific applications, this could be acceptable; however, upon further review, we will notice that there is one mouse whose records also contain duplicates within the Timepoint column. Unfortunately, this data would not allow us to develop accurate guidance because we would not be certain which records would be the most relevant. As a result, all of these records need to be removed before developing an accurate analysis. Once those records are removed, we create the data frame that will be the foundation of our analysis as we advance. 
	We begin our Python script by importing the necessary dependents that will enable us to perform the required functions within the script. This is an important step, as these additional modules will make processing the data more accessible. We then connect to the .csv files and read the data into our program. You will need to merge the data from the two files and then remember to create a clean version of the original data frame. 
	Once we have created the new data frame, we can begin to develop a summary analysis for the District and the general examination for all of the schools; we then generate a statical summary. The summary data will include the mean, median, variance, standard deviation, and standard error of the mean. 
	We then move on to developing the charts. In this exercise, we will look at creating bar charts and pie charts. We will utilize both the functionality of Pandas and Matplotlib to highlight the nuances between the two modules. Although the syntax for Pandas is likely to appear more straightforward, you will quickly realize that Matplot lib provides a higher level of functionality and allows us to present a more detailed analysis if we need to. Our next set of charts highlights the quartiles and outliers within the data based on a certain number of drug treatments.  
	We finish our analysis by providing additional views of the data utilizing correlation and regression analysis. This information will allow the user to develop an idea of potential relationships within the data that can help to determine the likely causes of certain results. You can see how gaining this type of insight can facilitate better decisions based on data rather than making assumptions. 
	
## Instructions

Your tasks are to do the following:

* Prepare the data.

* Generate summary statistics.

* Create bar charts and pie charts.

* Calculate quartiles, find outliers, and create a box plot.

* Create a line plot and a scatter plot.

* Calculate correlation and regression. 

* Submit your final analysis. 

### Prepare the Data

1. Run the provided package dependency and data imports, and then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.

2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining step.

3. Display the updated number of unique mice IDs.

### Generate Summary Statistics

Create two summary statistics DataFrames:

    * For the first table, use the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. This should result in five unique series objects. Combine these objects into a single summary statistics DataFrames.

    * For the second table, use the `agg` method to produce the same summary statistics table by using a single line of code.

### Create Bar Charts and a Pie Charts

1. Generate two bar plots. Both plots should be identical and show the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.

    * Create the first bar plot by using Pandas's `DataFrame.plot()` method.

    * Create the second bar plot by using Matplotlib's `pyplot` methods.

2. Generate two pie plots. Both plots should be identical and show the distribution of female or male mice in the study.

    * Create the first pie plot by using both Pandas's `DataFrame.plot()`.

    * Create the second pie plot by using Matplotlib's `pyplot` methods.

### Calculate Quartiles, Find Outliers, and Create a Box Plot 

1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR and determine if there are any potential outliers across all four treatment regimens. Follow these substeps:

    * Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

    * Create a list that holds the treatment names, as well as a second, empty list to hold the tumor volume data.

    * Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list. 

    * Determine outliers by using the upper and lower bounds, and then print the results.
    
2. Using Matplotlib, generate a box plot of the final tumor volume for all four treatment regimens. Highlight any potential outliers in the plot by changing their color and style.


### Create a Line Plot and a Scatter Plot

1. Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

2. Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

### Calculate Correlation and Regression

1. Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. 

2. Plot the linear regression model on top of the previous scatter plot.

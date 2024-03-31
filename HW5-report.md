# HW 5 - CS 625, Spring 2024

###   Deevan Kumar Menda

Due: March 30,2024

--- 


## Analyzing Data Using Distribution Charts

## Part 1:  Create Distribution Charts

### Data 

For my homework assignment, I chose Dataset-14, which presents Single-Family Housing Price Indexes by State spanning from 1990 to 2008. Each row corresponds to a different state, and each column represents a specific year, detailing the housing price index for that state in that particular year. To tackle the first question, which seeks the housing price indexes for all states in 1995, 2000, and 2008, I refined the dataset by selecting only the relevant years and columns: States, along with data for 1995, 2000, and 2008. This focused approach streamlined the dataset for clearer analysis.

For the second question, which inquires about the housing price indexes for all states in a specific year, I streamlined the dataset further by retaining only the data for that particular year and discarding information for other years. This involved modifying the original Excel file and converting it into a CSV format for easier handling. Both the original Excel file and the edited CSV files are provided in the repository for reference.

 <br/><br/>
###  Q1.boxplot: Show the Single-famiy housing price indexes of all states in 1995, 2000, and 2008
*Boxplot:*

![download](https://github.com/DeevanMenda/public-Spring24-aveerasa/assets/156245935/9ea402d1-3432-46bf-83d9-47ba795f8e0b)



For the analysis of Single-Family Housing Price Indexes across various states, the focus was placed on three pivotal years: 1995, 2000, and 2008. By isolating data from these specific years, the dataset was refined to include only the relevant information needed to assess the housing market's performance over time. This approach allowed for a comprehensive examination of how housing prices fluctuated across different states during these critical years, providing insights into regional variations and trends in the housing market. Through careful consideration of the Single-Family Housing Price Indexes for each state in 1995, 2000, and 2008, a nuanced understanding of the housing market dynamics during these pivotal periods was achieved.

 ### [Google Colab Code Link](https://colab.research.google.com/drive/10k3GEM00gZg8z4YcZgXtHXy9gC9IdZdF?usp=sharing)

### Code Explanation: 

This Python code utilizes pandas, seaborn, and matplotlib libraries to create a boxplot visualization of Single-family Housing Price Indexes for the years 1995, 2000, and 2008 across various states.

* The dataset is melted using pd.melt() function to reshape it into a format suitable for visualization, with State as the identifier variable and Year as the variable to be split.

* A boxplot is generated using seaborn's boxplot() function, with the x-axis representing the years and the y-axis representing the housing price index.

* The palette parameter in the boxplot function specifies the color scheme for the plot.

* Additional plot elements such as title, x-axis label ('Year'), and y-axis label ('Price Index') are added for clarity.

* Finally, plt.show() displays the plot.


### Observations

The Single-family Housing Price Indexes for all states are compared across the years 1995, 2000, and 2008. Among these years, 2008 emerges as the year with the highest housing price indexes for most states. This suggests a notable upward trend in housing prices over the selected timeframe. Conversely, 1995 generally exhibits lower housing price indexes compared to the other two years, indicating a potential period of lower housing market activity or less robust economic conditions. The comparison highlights the dynamic nature of the housing market and the significant fluctuations in housing prices over time, influenced by various economic and social factors.

### Idiom: Box plot / Mark: Bar
| Data: Attribute | Data: Attribute Type | Encode: Channel |
| --- | --- | --- |
| Year | value, Ordinal | (x-axis) |
| Price Index | value, Quantitative | (y-axis) |

 The x-axis represents the years (1995, 2000, and 2008), which are treated as ordinal values. The y-axis indicates the Single-family Housing Price Index, which is a quantitative value. The box plot is chosen as the idiom for visualization, presenting the distribution of the price index across different years.

<br/><br/>

### Q2. Single-famiy housing price indexes of all states in one of the years

*Empirical Cumulative Distribution Function (eCDF):*


![download-1](https://github.com/DeevanMenda/public-Spring24-aveerasa/assets/156245935/c34c4349-a757-41aa-ade3-7f68ea8feb12)



In the year 2002, the housing price indexes across all states exhibit considerable variability. The eCDF plot illustrates the cumulative distribution of these indexes, showing the proportion of states with housing price indexes less than or equal to a given value. This provides insights into the overall distribution and spread of housing prices in 2002.
Additionally, the histogram complements the eCDF plot by depicting the frequency distribution of housing price indexes. Using a reasonable bin size ensures that the histogram accurately represents the data distribution without oversimplifying or losing important details.
Together, these visualizations offer a comprehensive understanding of the distribution of Single-family Housing Price Indexes in 2002, enabling analysis and comparison of housing market trends across different states.


  ### [Google Colab Code Link](https://colab.research.google.com/drive/10k3GEM00gZg8z4YcZgXtHXy9gC9IdZdF?usp=sharing)


### Code explanation

   This Python code utilizes pandas, matplotlib, numpy, and statsmodels libraries to create an Empirical Cumulative Distribution Function (ECDF) plot for the housing price indexes of the year 2002.

* Reading Data: The code reads the provided data from an Excel file named 'deevan-2.xlsx' and creates a pandas DataFrame.

* Extracting Data: It extracts the housing price indexes specifically for the year 2002 from the DataFrame.

* Plotting ECDF: The housing price indexes for 2002 are sorted, and the ECDF values are calculated. The numpy function np.arange() is used to generate the range of cumulative probabilities. Matplotlib's plt.step() function is then employed to plot the ECDF, with 'post' specified as the where parameter to ensure the step function starts from the leftmost edge of each interval.

* Plot Customization: The plot is customized with a title ('Empirical Cumulative Distribution Function (ECDF)'), x-axis label ('Housing Price Index'), y-axis label ('ECDF'), and a legend indicating the plotted data. Grid lines are also added for better visualization.

* Displaying the Plot: Finally, the plot is displayed using plt.show().



### Observations

Single-family Housing Price Indexes for all states in the year 2002. Upon examination, it reveals considerable variability in housing price indexes across different states. For instance, Massachusetts exhibited the highest index at 553, followed by New York at 440, while West Virginia had the lowest index at 177. This data highlights the diverse housing market conditions prevailing across states during the specified year. Additionally, the histogram visualization of this data would provide further insights into the distribution of housing price indexes, enabling a more comprehensive analysis of the housing market landscape in 2002.

### Idiom: eCDF / Mark: Line

| Data: Attribute | Data: Attribute Type | Encode: Channel |
| --- | --- | --- |
| Housing Price Index | value, Quantitative | (x-axis) |
| Cumulative Probability | value, Quantitative | (y-axis) |
| Year | key, Temporal | (Hue) |

This idiom table describes the Empirical Cumulative Distribution Function (eCDF) visualization used in the provided code. The eCDF is represented by a line plot, where the x-axis represents the Housing Price Index (quantitative value) and the y-axis represents the Cumulative Probability (quantitative value). The line plot displays the eCDF for the year 2002, serving as a hue to distinguish between different temporal observations.

### *Histogram:*


![download-2](https://github.com/DeevanMenda/public-Spring24-aveerasa/assets/156245935/78483df0-e73e-40b5-a144-564409ae752b)


This picture represents the creation of a histogram to visualize the distribution of Single-family Housing Price Indexes for the year 2002.Subsequently, a histogram is created using matplotlib, where the x-axis represents the Housing Price Index and the y-axis represents the frequency or count of occurrences.The resulting histogram provides insights into the distribution of housing price indexes in 2002, showing the frequency of different price index ranges.

### [Google Colab Code Link](https://colab.research.google.com/drive/10k3GEM00gZg8z4YcZgXtHXy9gC9IdZdF?usp=sharing)

### Code Explanation

* Import the necessary libraries: pandas for data manipulation and matplotlib.pyplot for plotting.
* Create a DataFrame from the provided data stored in an Excel file named 'deevan-2.xlsx' using the pd.read_excel() function.
* Extract the housing price indexes for the year 2002 from the DataFrame.
* Plot a histogram of the housing price indexes for the year 2002 using the plt.hist() function. Adjust the bin size as needed using the bins parameter. The histogram is plotted with 15 bins, represented by bars colored sky blue with black edges.
* Add a title to the plot using plt.title() to indicate that it shows the histogram of Single-family Housing Price Indexes in 2002.
* Label the x-axis as 'Housing Price Index' using plt.xlabel().
* Label the y-axis as 'Frequency' using plt.ylabel().
* Display grid lines on the plot using plt.grid(True).
* Finally, display the plot using plt.show().
** the code creates a histogram to visualize the distribution of Single-family Housing Price Indexes for the year 2002. The histogram provides insights into the frequency distribution of housing price indexes, helping to understand the overall distribution pattern and central tendency of the data.


### Observations

 A histogram to visualize the distribution of Single-family Housing Price Indexes specifically for the year 2002. With a histogram, it becomes possible to understand the frequency distribution of housing price indexes, shedding light on their central tendency and variability. By adjusting the bin size, the histogram effectively partitions the range of housing price indexes into 15 intervals, providing a clear representation of how frequently values fall within each interval. The histogram's title and axis labels offer clarity regarding what the plot represents, facilitating interpretation. Additionally, the inclusion of grid lines aids in visual alignment and assessment of the distribution's characteristics. Overall, the histogram serves as a valuable tool for exploring and analyzing the distribution of Single-family Housing Price Indexes for the year 2002.

### Idiom: Histogram / Mark: Bar
| Data: Attribute | Data: Attribute Type | Encode: Channel |
| --- | --- | --- |
| Housing Price Index | value, Quantitative | (x-axis) |
| Frequency | value, Quantitative | (y-axis) |
<br/><br/>

## Part 2:  Further Analysis


### 1. Average Annual Growth Rate for Each State 1990-2008

*Bar Chart:*


![download-3](https://github.com/DeevanMenda/public-Spring24-aveerasa/assets/156245935/4f0e7525-53ca-4333-8083-cd6bae9516c4)



It calculates the average annual growth rate of population for each state over the years 1990 to 2008. It loads the population data from an Excel file into a pandas DataFrame. Then, it iterates over each state, calculates the growth rate using the population values from the first and last years, and stores the results in a dictionary. After that, it converts the dictionary into a DataFrame. Finally, it creates a horizontal bar plot where each bar represents the average growth rate of a state, allowing for easy visual comparison of population growth rates across different states.

### [Google Colab Code Link](https://colab.research.google.com/drive/10k3GEM00gZg8z4YcZgXtHXy9gC9IdZdF?usp=sharing)

### Code Explanation


This Python code reads population data from an Excel file, calculates the average annual growth rate for each state between the years 1990 and 2008, and then visualizes the results using a horizontal bar plot.

* The population data is loaded into a DataFrame named df using Pandas.
* The code iterates over each state in the DataFrame and calculates the average annual growth rate using the population values for each state from 1990 to 2008.
* The calculated growth rates are stored in a dictionary called growth_rates, where the keys are state names and the values are their respective average growth rates.
* The dictionary is converted into a DataFrame named growth_rates_df.
* Finally, a horizontal bar plot is created using Matplotlib, where each bar represents the average growth rate of a state. The x-axis represents the average growth rate, and the y- 
  axis represents the states.
* The resulting plot provides a visual comparison of the average annual growth rates for each state over the specified period.

  
### Observations

The provided code calculates the average annual growth rate for each state based on population data from 1990 to 2008 and visualizes it using a horizontal bar chart. This visualization offers a comparative overview of the growth rates across different states, indicating their population dynamics over the specified period. By analyzing the chart, one can discern variations in growth rates among states, identifying regions with higher or lower population growth trends.


### Idiom: Bar / Mark: Bar
| Data: Attribute | Data: Attribute Type | Encode: Channel |
| --- | --- | --- |
| State | Categorical | (y-axis) |
| Average Growth Rate | Quantitative | (x-axis) |

This code generates a horizontal bar chart to illustrate the average annual growth rate for each state from 1990 to 2008. Each bar in the chart represents a state, and its length corresponds to the average growth rate. The x-axis represents the average growth rate, while the y-axis displays the states. This visualization facilitates a comparative analysis of the growth rates across different states over the specified period.

### 2. Distribution of Single-family Housing Price Growth Rates (1995 to 2008)

*histogram:*

![download-4](https://github.com/DeevanMenda/public-Spring24-aveerasa/assets/156245935/c53160f8-a3a9-4872-80b8-a07b6bd96124)



This code snippet utilizes the pandas, matplotlib, and seaborn libraries to analyze the distribution of average growth rates of single-family housing prices across different states from 1990 to 2008. Initially, the population data is loaded from an Excel file. Subsequently, the average annual growth rate for each state is calculated based on the provided data. The seaborn library's histplot function is then employed to create a histogram, representing the distribution of average growth rates. The x-axis displays the growth rates in percentage, while the y-axis indicates the frequency of occurrence. This visualization allows for an understanding of the distribution pattern of housing price growth rates across states over the specified period

### [Google Colab Code Link](https://colab.research.google.com/drive/10k3GEM00gZg8z4YcZgXtHXy9gC9IdZdF?usp=sharing)


### Code Explanation

This Python code utilizes the pandas, matplotlib, and seaborn libraries to visualize the distribution of average annual growth rates of single-family housing prices across different states from 1995 to 2008. 

* The population data is loaded from an Excel file named 'deevan-1.xlsx' using pandas.
* The code calculates the average annual growth rate for each state by iterating over the states and extracting the housing price values for the years 1990 to 2008. It computes the growth rate based on the initial and final population values.
*  The calculated growth rates are stored in a dictionary and then converted into a DataFrame named 'growth_rates_df' containing two columns: 'State' and 'Average Growth Rate'.
*  Using seaborn's `histplot()` function, the code creates a histogram to visualize the distribution of average growth rates. The `kde` parameter is set to True to display the kernel density estimation along with the histogram bars. The number of bins for the histogram is set to 15 for appropriate granularity.
*  The plot is labeled with a title, x-axis label ('Growth Rate (%)'), and y-axis label ('Frequency'), and the grid is enabled for better readability.
*  Finally, the plot is displayed using `plt.show()`.

* Overall, this code provides a clear visualization of the distribution of average growth rates of single-family housing prices across states during the specified time period.

 ### Observations

The provided code calculates the average annual growth rate for each state based on the population data spanning from 1990 to 2008. It then visualizes the distribution of these growth rates using a histogram with a kernel density estimate (KDE) and 15 bins. From the histogram, it can be observed that the majority of states have growth rates centered around a certain value, with some variations across the distribution. The KDE overlay helps to visualize the smooth approximation of the distribution. Overall, this visualization provides insights into the variability and central tendency of single-family housing price growth rates across different states during the specified period.

### Idiom: Histogram / Mark: Bar
| Data: Attribute        | Data: Attribute Type | Encode: Channel |
|------------------------|----------------------|-----------------|
| Growth Rate            | value, Quantitative  | (x-axis)        |
| Frequency              | value, Quantitative  | (y-axis)        |


### References


- [stackoverflow](https://stackoverflow.com/)
- [oreilly textbook](https://data.vk.edu.ee/PowerBI/Opikud/Fundamentals_of_Data_Visualization.pdf)
- [quora](https://www.quora.com/)

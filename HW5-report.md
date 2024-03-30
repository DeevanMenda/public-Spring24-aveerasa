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

 ### [Colab Code Link](https://colab.research.google.com/drive/10k3GEM00gZg8z4YcZgXtHXy9gC9IdZdF?usp=sharing)

### Code Explination: 

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

This idiom table describes the box plot visualization used in the provided code. The x-axis represents the years (1995, 2000, and 2008), which are treated as ordinal values. The y-axis indicates the Single-family Housing Price Index, which is a quantitative value. The box plot is chosen as the idiom for visualization, presenting the distribution of the price index across different years.

<br/><br/>

### Q2. Show the distribution of the population of all states in one of the years?

*Empirical Cumulative Distribution Function (eCDF):*

![HW5 eCDF](https://github.com/odu-cs625-datavis/fall23-mcw-mosesrathan19/assets/144186545/6140fdb0-66fc-40dd-9a3a-a4fa4e25bfae)

The Empirical Cumulative Distribution Function (eCDF) for population density in 1970 is shown in the graph. The x-axis represents various population density numbers, while the y-axis shows the cumulative probability. This chart helps to visualize the distribution of population density in the year 1970 and how the values are spread throughout the dataset.

eCDF is effective for calculating the cumulative distribution throughout the entire range. Its representation is effective in displaying the shape of the distribution. Finally, the eCDF can be an insightful tool for identifying extreme values within the dataset. The disadvantages using ecdf are Comparing multiple distributions in a single plot could be complex.


 [Google Colab Code Link for the eCDF](https://colab.research.google.com/drive/1Fo4gb17AO6q44SbJx8TRf8j7To5xGH6N?usp=sharing)


### Code snippet

    plt.figure(figsize=(10, 6))
    plt.step(df_1970, ecdf, label='eCDF - 1970', where='post')
    plt.xlabel('Population Density')
    plt.ylabel('Cumulative Probability')
    plt.title('Empirical Cumulative Distribution Function (eCDF) - 1970')
    plt.legend()
    plt.grid(True)
    plt.show()


### Observations

 From the graph, most states have relatively low population density in 1970

 There is an increasing order of population density values.

 ### Idiom: eCDF / Mark: Line 
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Population Density | value, Quantitative | (x-axis) |
| Cumulative Probability | value, Quantitative | (y-axis) |
| Year | key, Temporal | (Hue) |

<br/><br/>

*Histogram:*

![HW5 Histogram](https://github.com/odu-cs625-datavis/fall23-mcw-mosesrathan19/assets/144186545/29122c8a-94ce-44b5-920d-d3e05f9648c8)


THis histogram chart represents the distribution of population density in the year 1970. The x-axis represents the population density, and the y-axis shows the frequency. The Histogram helps to visualize the spread and frequency of population density values, showing the range and distribution pattern across the dataset for the year 1970.

Histogram is great for displaying the distribution of a continuous variable, showing the frequency or density of data points within certain ranges or bins. It is easily understandable to identify the frequency distributions and patterns. The only disadvantage with this is the choice of bin size can affect the appearance and understanding of the distribution. Fine details may be lost with certain bin sizes.


 [Google Colab Code Link for the Histogram](https://colab.research.google.com/drive/1Fo4gb17AO6q44SbJx8TRf8j7To5xGH6N?usp=sharing)

### Code snippet

    plt.figure(figsize=(10, 6))
    plt.hist(df['1970'], bins=10, color='skyblue')  
    plt.title('Population Density Distribution in 1970')
    plt.xlabel('Population Density')
    plt.ylabel('Frequency')
    plt.grid(axis='y')
    plt.show()

### Observations

The histogram shows that a significant number of states had lower population densities in 1970.

There are a only few states with very high population densities.

 ### Idiom: Histogram / Mark: Bar 
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Population Density | value, Quantitative | (x-axis) |
| Frequency | value, Quantitative | (y-axis) |

<br/><br/>

## Part 2:  Further Analysis


*1. Identification of states with the highest to lowest population densities across the years 1980, 2000, and 2008.*

Through box plots for each year, it becomes evident which states consistently maintain the highest and lowest population densities over time. The consistent upper states in box plots in histograms can reveal the states with the highest population densities. Similarly, the lower states in histograms can uncover the states with the lowest population densities. Through box plots for each year, it becomes evident which states consistently maintain the highest and lowest population densities over time. The consistent upper states in box plots in histograms can reveal the states with the highest population densities. Similarly, the lower states in histograms can uncover the states with the lowest population densities. 

*Bar Chart:*

 ### Idiom: Bar chart / Mark: Bar 
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Population Density | value, Quantitative | (x-axis) |
| States | value, Quantitative | (y-axis) |

<br/><br/>

![Bar Chart HW5](https://github.com/odu-cs625-datavis/fall23-mcw-mosesrathan19/assets/144186545/b6c39190-db58-4e2f-a03a-ef08b4200079)

[Google colab link for Bar Chart](https://colab.research.google.com/drive/1Fo4gb17AO6q44SbJx8TRf8j7To5xGH6N?usp=sharing)

<br/><br/>

*2. Population Density Growth Over Time:*

Observing the general trend of population density increases from 1980 to 2008 across different states. The line chart illustrates the population density growth over time for five states—California, Texas, New York, Florida, and Illinois from 1990 to 2008.Each line in the chart represents one state and its raise and fall. Population density in states such as California and New York has steadily increased over the years, with New York going through a significant increase between 1990 and 2000. Texas and Florida also show consistent growth, while Illinois has a comparatively stable population density over the years.

*Line Chart:*


 ### Idiom: Line chart / Mark: Line 
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Years | value, Ordinal | (x-axis) |
| Population Density | value, Quantitative | (y-axis) |
| States | Key, Categorical | (Hue) |

<br/><br/>

![HW5 Line Chart](https://github.com/odu-cs625-datavis/fall23-mcw-mosesrathan19/assets/144186545/f801e5d4-f555-4691-abbd-fbd4c3f8cc97)


[Google colab link for Line Chart](https://colab.research.google.com/drive/1Fo4gb17AO6q44SbJx8TRf8j7To5xGH6N?usp=sharing)

<br/><br/>

### References


- [stackoverflow](https://stackoverflow.com/)
- [oreilly textbook](https://data.vk.edu.ee/PowerBI/Opikud/Fundamentals_of_Data_Visualization.pdf)
- [quora](https://www.quora.com/)

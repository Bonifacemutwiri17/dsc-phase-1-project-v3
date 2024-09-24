# PHASE 1 PROJECT.

## Project Overview

In this project it deals with a company that wants to go into a new business and start a new with different goals and expand there network. There main objective is to get into the aviation sector of the business world and expand there influence majorly on buying aeroplanes and using them for purposes. Mainly Private, military and Commercial purposes. Featuring categorized data on aircraft types, causes, and outcomes, it provides insightful synopses and lessons for the start of the businness.Thus due to the eagerness of the business to start they overlooked the risks accompanied by the airline business thus poor decision making. My project aims to look at the risks in the business and also easily search and filter information, supported by interactive visualization tools. This initiative enhances safety standards, serves as an educational resource, and facilitates research in aviation safety. By ensuring accurate data collection and ongoing maintenance, the project fosters a culture of safety and informed decision-making in the aviation industry.

## Project Goals
My project aims to develop a comprehensive, user-friendly platform that consolidates detailed records of aviation accidents and incidents. This platform aims to enhance aviation safety by providing valuable insights and analysis to stakeholders, including aviation professionals, researchers, and regulatory bodies. By facilitating access to categorized data and in-depth synopses, the project seeks to promote informed decision-making, identify trends, and implement effective safety measures.I want to research o the accidents and its ratios and occurences.


## Business Understanding

The Business at hand deals with airplanes by which is a large area of expertise and needs analysis.Targeting aviation professionals, researchers, regulatory bodies, and the general public, the database addresses the critical need for accessible information to identify trends and preventative measures. Its value lies in offering detailed synopses and categorized data that inform decision-making and improve safety protocols. Potential revenue streams include subscription services, partnerships with aviation organizations, and data licensing.The companies selling the airlines, the airports they will be operating in , the government of the country of base operations the crew workers and the passengers are all stakeholders in the business.

## Data Understanding

### (1) Data Analysis.

For my project, I am working with a dataset on Aviation Accident Database & Synopses, up to 2023 obrained from Kaggle, where it is frequently updated and made accessible for research purposes. The data is stored in CSV format within a folder named "data.",in my github repository. It comprises 90,348 rows and 31 columns, where each column represents a distinct field and each row corresponds to an individual aircraft accident investigation entry.The dataset features a combination of continuous and categorical data, with 26 of the columns (approximately 84%) being categorical, stored as object types. The remaining 5 columns are continuous, represented in float form. This dataset focuses specifically on aircraft accidents, providing a rich foundation for analysis.I was able to find the sums of the missing values in the data and also the percentages of the missing values thus dropped some of the columns for efficiency and continuation on my project. After dropping the columns the shape of the data changed to 90,348 rows and 26 columns.Moving forward, I plan to explore the unique values and distributions of the categorical columns, analyze trends in the continuous data, and prepare for necessary data cleaning and exploratory data analysis to uncover valuable insights.

In my project, i utilized the pandas library to clean and prepare our dataset for analysis. One key step involved removing unnecessary columns from the DataFrame. Specifically, we dropped the following columns: 'Latitude', 'Longitude', 'Schedule', 'Air.carrier', and 'Airport.Code'.
This operation was performed using the df.drop() method with the inplace=True parameter, which modifies the original DataFrame directly. By eliminating these columns, we streamlined our dataset, focusing on the most relevant information. This helps improve both the clarity of our analysis and the performance of our data processing tasks, ultimately leading to more effective insights.
In my analysis, i implemented a function called find_outliers to identify outliers in specific numerical columns of our dataset. The function utilizes the Interquartile Range (IQR) method, which is effective for detecting anomalies in data.
To ensure the robustness of my analysis, i implemented a strategy for dealing with missing values in our dataset. Different methods were applied based on the nature of the data
Mean Imputation for Numerical Data: For the column Total.Fatal.Injuries, we filled missing values with the mean of the column. This approach helps maintain the overall average without significantly skewing the data distribution.
Median Imputation for Numerical Data: For the column Total.Serious.Injuries, we used the median to fill in missing values. The median is a more robust measure for skewed data, providing a better representation of the central tendency in the presence of outliers.
Mode Imputation for Categorical Data: For the column Total.Uninjured, we filled missing values with the mode (the most frequently occurring value) of the column. This method is particularly useful for categorical data, as it ensures that the imputed values reflect the most common occurrence within the dataset.
To analyze the impact of the number of engines on safety outcomes, we grouped the dataset by the Number.of.Engines column. Using the groupby method, we aggregated the total counts of various injury categories:Total Fatal Injuries,Total Serious Injuries,Total Minor Injuries,Total Uninjured.The aggregation was performed using the sum function for each category, providing insights into how the number of engines correlates with these safety metrics. The resulting grouped data was then reset to maintain a clear structure for further analysis.

### Analysis of the Visualizations
1. Bar Plot
The bar plot displays the total counts of different types of injuries (Fatal, Serious, Minor, Uninjured) for each category of the number of engines. This visualization allows for straightforward comparisons across categories, making it easy to identify which engine counts are associated with higher or lower injury totals. The use of color differentiation enhances clarity, helping in quickly discern between the different injury types.
2. Stacked Bar Plot
The stacked bar plot takes the bar plot a step further by stacking the different injury types on top of each other for each engine count. This visualization not only shows the total injury count but also illustrates the composition of that total. One can easily see how each injury type contributes to the overall count for each engine category, facilitating a deeper understanding of the data’s structure.
3. Box Plot
The box plot provides insights into the distribution of injuries for a particular injury type across different engine counts. It shows the median, quartiles, and potential outliers, which helps identify variability and skewness in the data. This visualization is particularly useful for assessing the range and distribution of injury counts, allowing for quick identification of any extreme values or outliers.
4. Heatmap
The heatmap visualizes the correlation between different types of injuries, using colors to represent the strength and direction of relationships. This visualization makes it easy to spot patterns and correlations at a glance. For example, a strong positive correlation between serious and fatal injuries could indicate that as serious injuries increase, fatal injuries also tend to rise. This insight is valuable for understanding interdependencies in the data.
5. Scatter Plot
The scatter plot showcases the relationship between fatal and serious injuries, using points to represent data for different engine counts. This visualization allows one to observe trends and patterns in the relationship between these two variables. The color coding based on engine counts helps identify whether certain engine categories are associated with specific injury types, making it easier to spot clusters or trends.
6. Line Plot
The line plot displays trends in total injuries across different engine counts over time or ordered categories. Each line represents a different injury type, allowing viewers to see how the counts change as the number of engines increases. This visualization is particularly effective for illustrating trends and comparisons, making it easy to identify which injury types are rising or falling in relation to the number of engines.




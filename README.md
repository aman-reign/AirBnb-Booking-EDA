
# Airbnb Bookings Analysis

# Project Type
**Exploratory Data Analysis**



# Project Summary
This project envolves conducting an analysis of a dataset consisting of around 49,000 observations. The primary objective is to extract meaningful insights that will equip management and stakeholders with crucial information for making informed decisions on how to expand or enhance the business, ultimately driving growth.

Through this analysis, we aim to identify patterns within the data, which will guide recommendations for strategic improvements. Not only will this analysis help guests make better choices, but it will also assist hosts in implementing necessary changes to foster business growth.

The information we have includes:
- Listing counts
- Distribution of data by specific neighborhood groups
- Prices
- Review data
- Room type preferences

From this data, we can uncover insights such as:
- Guest preferences for hosts
- Preferred room types
- Desired price ranges
- Most favored neighborhoods

Additionally, we will develop a filtering system for guests to receive listings that align with their budget and preferences. This will allow us to rank hosts based on their ability to meet guest requirements, effectively targeting customers with specific needs and enhancing their overall experience. Meeting these needs will lead to higher satisfaction for guests.

Furthermore, we will provide hosts with actionable insights on potential improvements or adjustments, enabling them to attract more attention and better meet the needs of their guests.


In this project, we will primarily utilize Pandas for data wrangling to organize the dataset clearly and extract meaningful insights regarding guest preferences and requirements. We may also create additional data frames to store information separately, ensuring easy access when needed.

For computations and calculations involving numerical data, we will employ NumPy. This will facilitate the creation of necessary arrays, allowing us to systematically store and access data, especially for ranking purposes.

# Business Objective
The business objective of this project is to identify opportuinites of improvements and also to derive patterns and insights of customer's preference which will ultimately help us in achieving customer satisfaction.

# All about the Dataset
The Airbnb NYC 2019 Dataset has:-
Rows = 48895
Columns = 16

We can see the division of Categorical and Numerical values in our dataset, We can see:-

3 columns have float64 data values (Numerical)
7 columns have int64 data type values (Numerical)
6 columns have object data type values (Categorical)

The dataset contains both numerical and categorical data.

The primary key of our dataset is the "id" column, having a unique IDs for the hotel names.

Here is the list of columns:-
['id', 'name', 'host_id', 'host_name', 'neighbourhood_group',
       'neighbourhood', 'latitude', 'longitude', 'room_type', 'price',
       'minimum_nights', 'number_of_reviews', 'last_review',
       'reviews_per_month', 'calculated_host_listings_count',
       'availability_365']

This dataset had no exact duplicated values, however in the name column there were 998 rows that were duplicates.
Where all the values were almost the same, except for the prices, there might be a chances that the prices were altered with time as per the market condition however the hotel was the same.

To handle these values we sorted our dataframe on the basis of latest entries, for which we needed a timestamp in our dataset.
In our dataset we were able to use the 'last_review' column as the timestamp for our dataset.

After doing few operation we were successfully able to handle our duplicated values.

These are columns that majorly has the null values:-
- last_review = 10052
- reviews_per_month = 10052

As the date column was missing values we replaced the NA values with the latest date present in our dataset, so that the time stamp could be efficient.

We are also missing few "Names" as well as "Host Names":-
- name = 16
- host_name = 21

We have now successfully formatted our dataframe and it is now ready for data wrangling.

# Understanding Variables
There are basically 3 types of variables according to their roles:-

- Numerical Variables: These variables represent quantitative data and can be further categorized into:-
  
  - Continuous Variables: These variables can take any value within the given number of range.
  - Discrete Variables: These variables are having a specific value and are related to a specific identity.

- Categorical Variables: These variables represent qualitative data and can be further categorized into:-
  - Nominal Variables: These variables are random and they do not follow any order or ranking.
  - Ordinal Variables: These variables are according to an order they can be ranked as well.

- Time Variables: These variables are basically date and time variables having a timestamp.

  # Manipulations and wrangling performed
  This dataset was having good amount of well distributed information, which was a plus point for our study. As this dataset if of Airbnb, the locations play a very crucial role in these values and the inforamtion was distributed well as per the locations and their respective areas.

We have done number of manipulations to seek information which can be beneficial for the stake holders to make decisions for the business, not only that our hosts will also get good idea about the preferences of their customers, as we promised in our agenda.

We divided the complete manipulation into 2 major parts, as per the features and the relationships, so that we can draw insights accordingly.

These are the manipulations we followed:-

- Created a new price range column: As this columns will help us to categorize the price distribution and to simplify the judgement for us to get an idea of the budget of our customer, we have tried to keep it as precise as possible.

- Sorted the dataset as per price: As the data wasn't sorted and was not having any significance regaring any value, we sorted it as per the pricing, keep the most expensive ones on the top.

- We filtered the data so that it becomes simple and easy to understand(less chaotic) for us to work only with those columns that are required for the data analysis and feature engineering.

- Divided the data accoring to the categorical groups to derive insights accordingly, it helped us to identify the outcomes in a structed manner with respect to the considered groups, it provided us with more specific information about the different groups we created so that we can identify insights for each group individually. These are the diferent groups we created and worked with:-
  
  - Created Nighbourhood Group: This group helped us to get an idea of which neighbourhood is the most prefered one in all of the neighbourhoods.

  - Created room type groups: This group helped us to identify which room type is the most prefered by our customers.

  - Created Neighbourhood area groups: This group helped us to identify which is the most prefered area within the neighbourhoods.


We also worked on few of the relationships that helped us in few comparisons that will help our stake holders to make decisions accordingly. These are the relationships we worked with:-

- Relationship: Price vs. Room Type
  - Checked the distribution of prices for different room types.
  - Determined which room type is having the most expensive price distribution.

- Relationship: Reviews per Month vs. Room Type
  - Compared the distribution of reviews per month for different room types.
  -  Explored the level of engagement and satisfaction of our customers as per different room types.

- Relationship: Price vs. Neighbourhood
  - Compared the distribution of prices across different neighbourhoods.
  - Identified neighbourhoods with higher or lower average prices and explored price variations as per the areas.

These are the manipulations that we did in order to derive useful information so that it can contribute into the growth of our business and also the busniness of our hosts, and ultimately grow and improve tavelling experience for our customers.

The specifilly derived insights will be mentioned with the visualisations so that it would be better to understand and visualize at the same time.


# Solution to the Business Objective
Coming up to the solution of our business objective, we have throughly studied the whole data set and drawn some conclusions based on that, here are all the pointers we can take into consideration.

- 0-300 is the most prefered price range, which gives us a clear idea on what basis we will have to create our pricing.
- Entire home/apt	being the most prefered room type makes it obvious that customers are very much concerned about their privacy and safety, we can create more relevant policies regarding their safety and privacy, ulimately resulting in gaining their trust and creating goodwill.
- We know that the most prefered area is the Financial District which is in the Manhattan Neighbourhood Group, hence we can create recommendations as per the pricing and area preferrences.
- The most reviews are also given to the same area itself we can take into consideration those points which proved to be the most satisfying for our customers so that we can make such changes in the other neighbourhoods, if possible, whcih will result in getting us more business in the other areas as well.
- I personally feel that this dataset should have one more column as per the occupation of the customer, it will create different groups of our customers based upon their occupation, which will help us to determine the preference of people coming from different sectors and we can identify which group of customers prefers which kind of accomodations.
- This dataset also gave us a good idea on the budget of the majority of our consumer market, and now just that we were able to see the ratio of prefered pricing.
- We were clearly able to see where most of our business lies and which consumer group creates the most of the business for us, we can make improvements in those and not just that we can also focus on the other sectors as well so that we can expand our business even more.

# Conclusion
The conclusion of this complete EDA project is simple and crisp, we have enough data to see what is liked by our customers and what is it that they are demanding as is is clear that around 90% of our business is saturated into one side whether it is the area preference or pricing, we can use that information to check what works for our customers and make those changes in other areas as well.

# Thank You


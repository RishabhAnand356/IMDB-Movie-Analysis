IMDB Movie Data Analysis Report
This report details the analysis of an IMDB movie dataset using SQL and Excel.

A. Cleaning the Data

Data cleaning is crucial for accurate analysis. This step might involve:

Identifying and handling missing values: Replace or remove missing values based on their significance.
Identifying and correcting inconsistencies: Address formatting errors, typos, or duplicate entries.
Removing irrelevant columns: Eliminate columns not relevant to the analysis.
B. Movies with Highest Profit

Calculate Profit: Add a new column named "profit" using the formula: gross - budget.
Identify Top Profit Movies: Sort the data by "profit" in descending order to find movies with the highest profit.
C. Top 250 Movies

Identify Top 250: Use a filter to isolate movies ranked within the top 250 based on a relevant column like "imdb_score".
D. Best Directors

Group by Director: Group the data by "director_name".
Calculate Average Score: Calculate the average "imdb_score" for each director group.
Top 10 Directors: Sort the grouped data by the average "imdb_score" in descending order. Select the top 10 directors.
Tie-Breaking: If there's a tie for average score, sort alphabetically by "director_name" within the tied group.
E. Popular Genres

Identify Unique Genres: Extract all unique genres from the "genre" column.
Analyze Genre Distribution: Count the occurrences of each genre to determine the most popular ones.
F. Critic-Favorite and Audience-Favorite Actors

Create Actor Flag Columns: Create new columns ("Meryl_Streep", "Leonardo_Caprio", "Brad_Pitt") using conditional statements to identify movies starring each actor based on the "actor_1_name" column. Assign a value (e.g., "Yes") for movies with the respective actor and leave it blank otherwise.
Combine Actor Data: Concatenate all actor flag columns into a new column named "Combined".
Group by Actor: Group the data by "actor_1_name".
Average Reviews: Calculate the average of "num_critic_for_reviews" and "num_users_for_reviews" for each actor group.
Identify Top Actors: Identify actors with the highest average critic and user reviews.
Decade Analysis:
Create a new column named "decade" by extracting the first digit of the "title_year" and appending "0s" (e.g., 1978 becomes "1970s").
Sort by "decade" and group the data.
Calculate the sum of "num_users_for_reviews" for each decade. Store this data in a new dataframe named "df_by_decade".
Visualization: Create a bar chart to visualize the change in the number of user reviews across decades using the "df_by_decade" data.
Note: This report provides a general outline. The specific implementation depends on the chosen tools (SQL or Excel) and data structure.

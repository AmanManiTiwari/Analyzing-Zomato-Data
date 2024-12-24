# Zomato Data Analysis

## Overview
This project involves analyzing a dataset of Zomato restaurants to uncover insights regarding restaurant types, ratings, votes, and ordering preferences. The analysis uses Python along with data visualization libraries such as Matplotlib and Seaborn.

## Dataset Description
The dataset consists of 148 records with the following columns:
- **name**: Name of the restaurant
- **online_order**: Indicates whether the restaurant accepts online orders (Yes/No)
- **book_table**: Indicates whether the restaurant offers table booking (Yes/No)
- **rate**: Customer rating for the restaurant (out of 5)
- **votes**: Number of votes the restaurant has received
- **approx_cost(for two people)**: Approximate cost for two people
- **listed_in(type)**: Type of restaurant (e.g., Buffet, Dining, Cafe, etc.)

## Project Steps

1. **Data Loading**:
   The dataset is loaded into a Pandas DataFrame.

2. **Data Cleaning**:
   - Converted the `rate` column from a string (e.g., "4.1/5") to a float for numerical operations.
   - Verified that there are no NULL values in the dataset.

3. **Data Analysis**:
   - **Visualization of Restaurant Types**:
     - Created a count plot to show the distribution of restaurant types.
     - Majority of restaurants fall into the "Dining" category.
   
   - **Votes Analysis**:
     - Grouped data by restaurant type and calculated the total votes.
     - "Dining" restaurants received the highest number of votes.

   - **Restaurant with Maximum Votes**:
     - Identified "Empire Restaurant" as the restaurant with the highest number of votes.

   - **Online Order Analysis**:
     - Created a count plot showing the distribution of online ordering preference.
     - Most restaurants do not accept online orders.

   - **Ratings Distribution**:
     - Created a histogram of restaurant ratings.
     - Most ratings range between 3.5 and 4.

   - **Cost Analysis**:
     - Analyzed approximate cost for two people using a count plot.
     - Majority of restaurants have an approximate cost of 300 rupees.

4. **Advanced Visualizations**:
   - **Box Plot**:
     - Compared restaurant ratings based on online ordering.
     - Restaurants accepting online orders generally have higher ratings.

   - **Heatmap**:
     - Created a heatmap to visualize the relationship between restaurant type and online ordering preference.
     - Dining restaurants primarily accept offline orders, while cafes often receive online orders.

## Key Insights
- Dining restaurants are the most popular and receive the highest number of votes.
- Restaurants accepting online orders generally receive better ratings.
- Cafes primarily rely on online orders, while dining restaurants prefer offline orders.
- Most customers prefer restaurants with an approximate cost of 300 rupees.

## How to Run the Code
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. Run the Python script to generate visualizations and insights.

## Tools and Technologies
- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **Matplotlib & Seaborn**: Data visualization

---

**Contact**: If you have any questions or suggestions, please feel free to reach out!


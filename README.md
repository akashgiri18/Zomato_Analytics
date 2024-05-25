# Zomato_Analytics
This project involves analyzing the Zomato dataset to extract meaningful insights using SQL. It dives into Zomato customer data, encompassing order history, Zomato Gold membership status, and product information. By analyzing these aspects, we can gain valuable insights to improve customer experience, boost sales, and optimize Zomato's offerings.

**Database Structure:**

The project utilizes a relational database schema with the following tables:

* **users:** Stores user IDs and signup dates.
* **goldusers_signup (optional):** Stores user IDs and their Zomato Gold signup dates (if applicable).
* **sales:** Stores user IDs, purchase dates, and product IDs.
* **product:** Stores product IDs, names, and prices.

**Provided SQL Scripts:**

The included SQL scripts perform various analyses on the Zomato data.  Each script generates a result table that can be used to further explore the findings.

**Customer Behavior:**

* **Total Spent per Customer:** Calculates the total amount each customer spent on Zomato. (Script generates a table with `userid` and `total_amt_spent` columns)
* **Number of Visits per Customer:** Counts the distinct days each customer visited Zomato. (Script generates a table with `userid` and `distinct_days` columns)
* **First Purchase per Customer:** Identifies the first product purchased by each customer. (Script generates a table with `userid`, `product_id`, and `created_date` columns for the first purchase)
* **Most Popular Item per Customer:** Finds the item most frequently purchased by each customer. (Script generates a table with `userid`, `product_id`, and `cnt` columns showing the most frequent purchase)

**Sales Analysis:**

* **Most Purchased Item:** Discovers the most purchased item and the number of times it was bought. (Script generates a table with `product_id`, `cnt` columns showing purchase frequency)
* **Rank Transactions:** Assigns a rank to each transaction based on purchase date for each user. (Script generates a table with `userid`, `created_date`, `product_id`, and `rnk` columns showing ranked transactions)

**Zomato Gold Membership Analysis (if goldusers_signup table exists):**

* **First Purchase After Membership:** Identifies the first product a user purchased after signing up for Zomato Gold. (Script generates a table with `userid`, `product_id`, and `created_date` columns for the first purchase after membership)
* **Last Purchase Before Membership:** Identifies the last product a user purchased before signing up for Zomato Gold. (Script generates a table with `userid`, `product_id`, and `created_date` columns for the last purchase before membership)
* **Orders & Amount Spent Before Membership:** Calculates the total orders and amount spent by members before they joined Zomato Gold. (Script generates a table with `userid`, `order_purchased`, and `total_amt_spent` columns)
* **Points Earned Analysis (Optional):** Analyzes points earned by customers based on a hypothetical points system (requires additional logic).
* **Gold Member vs. Non-Member Ranking:** Assigns ranks to transactions, differentiating between Zomato Gold members and non-members. (Script generates a table with `userid`, `created_date`, `product_id`, `rnk`, and `gold_signup_date` columns showing ranked transactions with gold member status)

**Using the Code:**

1. Clone this repository to your local machine.
2. Import the SQL scripts into your preferred SQL development environment.
3. Ensure your database schema matches the one described above.
4. Execute the desired scripts to generate the corresponding result tables.
5. Analyze the result tables to gain insights into customer behavior and sales trends.

**Further Exploration:**

This project provides a springboard for exploring Zomato user behavior further. You can extend this work by:

* Analyzing user demographics and purchase patterns based on location.
* Identifying trends in popular cuisines and products over time.
* Evaluating the impact of Zomato Gold membership on customer retention and spending.
* Creating visualizations to represent the findings effectively.

By delving deeper into the data, you can gain valuable insights to improve customer experience, optimize Zomato's offerings, and drive business growth.

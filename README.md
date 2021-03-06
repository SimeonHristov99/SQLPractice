# SQLPractice

Holds sample solutions to SQL query exercises. Solutions are written in PostgreSQL and Python.

---

## Task 1

Write a query that calculates the difference between the highest salaries found in the marketing and engineering departments. Output just the difference in salaries.

| db_employee          | db_dept              |
| -------------------- | -------------------- |
| id - int             | id - int             |
| first_name - varchar | department - varchar |
| last_name - varchar  |                      |
| salary - int         |                      |
| department_id - int  |                      |

## Task 2

We have a table with employees and their salaries, however, some of the records are old and contain outdated salary information. Find the current salary of each employee assuming that salaries increase each year. Output their id, first name, last name, department ID, and current salary. Order your list by employee ID in ascending order.

| ms_employee_salary    |
| --------------------- |
| id - int64            |
| first_name - object   |
| last_name - object    |
| salary - int64        |
| department_id - int64 |

## Task 3

Find the average number of bathrooms and bedrooms for each city’s property types. Output the result along with the city name and the property type.

| airbnb_search_details  |
| ---------------------- |
| id - int64             |
| price - float64        |
| property_type - object |
| bathrooms - int64      |
| city - object          |
| bedrooms - int64       |

## Task 4

Find the details of each customer regardless of whether the customer made an order. Output the customer's first name, last name, and the city along with the order details. You may have duplicate rows in your results due to a customer ordering several of the same items. Sort records based on the customer's first name and the order details in ascending order.

| customers             | orders                      |
| --------------------- | --------------------------- |
| id - int64            | id - int64                  |
| first_name - object   | cust_id - int64             |
| last_name - object    | order_date - datetime64[ns] |
| city - object         | order_details - object      |
| address - object      | total_order_cost - int64    |
| phone_number - object |

## Task 5

Facebook has developed a new programing language called Hack. To measure the popularity of Hack they ran a survey with their employees. The survey included data on previous programing familiarity as well as the number of years of experience, age, gender and most importantly satisfaction with Hack. Due to an error location data was not collected, but your supervisor demands a report showing average popularity of Hack by office location. Luckily the user IDs of employees completing the surveys were stored. Based on the above, find the average popularity of the Hack per office location. Output the location along with the average popularity.

| facebook_employees | facebook_hack_survey |
| ------------------ | -------------------- |
| id - int64         | employee_id - int64  |
| location - object  | age - int64          |
| age - int64        | gender - object      |
| gender - object    | popularity - int64   |
| is_senior - bool   |

## Task 6

Compare each employee's salary with the average salary of the corresponding department. Output the department, first name, and salary of employees along with the average salary of that department.

| employee                |
| ----------------------- |
| id - int64              |
| first_name - object     |
| last_name - object      |
| age - int64             |
| sex - object            |
| employee_title - object |
| department - object     |
| salary - int64          |
| target - int64          |
| bonus - int64           |
| email - object          |
| city - object           |
| address - object        |
| manager_id - int64      |

## Task 7

Find the total cost of each customer's orders. Output customer's id, first name, and the total order cost. Order records by customer's first name alphabetically.

## Task 8

Write a query to find which gender gives a higher average review score when writing reviews as guests. Use the `from_type` column to identify guest reviews. Output the gender and their average review score.

Tables:

| airbnb_reviews      | airbnb_guests         |
| ------------------- | --------------------- |
| from_user - int     | guest_id - int        |
| from_user - int     | nationality - varchar |
| to_user - int       | gender - varchar      |
| from_type - varchar | age - int             |
| to_type - varchar   |                       |
| review_score - int  |                       |

## Task 9

Find all posts which were reacted to with a heart.

Tables:

| facebook_reactions | facebook_posts          |
| ------------------ | ----------------------- |
| poster - int       | post_id - int           |
| friend - int       | poster - int            |
| reaction - varchar | post_text - varchar     |
| date_day - int     | post_keywords - varchar |
| post_id - int      | post_date - datetime    |

## Task 10

Find the average number of beds in each neighborhood that has at least 3 beds in total. Output results along with the neighborhood name and sort the results based on the number of average beds in descending order.

Table:

| airbnb_search_details            |
| -------------------------------- |
| id - int                         |
| price - float                    |
| bed_type - varchar               |
| host_identity_verified - varchar |
| host_response_rate - varchar     |
| host_since - datetime            |
| neighbourhood - varchar          |
| number_of_reviews - int          |
| review_scores_rating - float     |
| zipcode - int                    |
| bedrooms - int                   |
| beds - int                       |

## Task 11

Find the last time each bike was in use. Output both the bike number and the date-timestamp of the bike's last use (i.e., the date-time the bike was returned). Order the results by bikes that were most recently used.

Table:

| dc_bikeshare_q1_2012    |
| ----------------------- |
| duration - varchar      |
| duration_seconds - int  |
| start_time - datetime   |
| start_station - varchar |
| start_terminal - int    |
| end_time - datetime     |
| end_station - varchar   |
| end_terminal - int      |
| bike_number - varchar   |
| rider_type - varchar    |
| id - int                |

## Task 12

Return the total number of comments received for each user in the last 30 days. Don't output users who haven't received any comment in the defined time period. Assume today is 2020-02-10.

Table:

| fb_comments_count        |
| ------------------------ |
| user_id - int            |
| created_at - datetime    |
| number_of_comments - int |

## Task 13

Find all wineries which produce wines by possessing aromas of plum, cherry, rose, or hazelnut. Output unique winery values only.

Table:

| winemag_p1            |
| --------------------- |
| id - int              |
| country - varchar     |
| description - varchar |
| designation - varchar |
| points - int          |
| price - float         |
| province - varchar    |
| region_1 - varchar    |
| region_2 - varchar    |
| variety - varchar     |
| winery - varchar      |

## Task 14

Find the base pay for Police Captains. Output the employee name along with the corresponding base pay.

| sf_public_salaries       |
| ------------------------ |
| id - int                 |
| employeename - varchar   |
| jobtitle - varchar       |
| basepay - float          |
| overtimepay - float      |
| otherpay - float         |
| benefits - float         |
| totalpay - float         |
| totalpaybenefits - float |

## Task 15

What is the overall friend acceptance rate by date? Your output should have the rate of acceptances by the date the request was sent. Order by the earliest date to latest.

Assume that each friend request starts by a user sending (i.e., user_id_sender) a friend request to another user (i.e., user_id_receiver) that's logged in the table with action = 'sent'. If the request is accepted, the table logs action = 'accepted'. If the request is not accepted, no record of action = 'accepted' is logged.

| fb_friend_requests         |
| -------------------------- |
| user_id_sender - varchar   |
| user_id_receiver - varchar |
| date - datetime            |
| action - varchar           |

## Task 16

Find the total number of downloads for paying and non-paying users by date. Include only records where non-paying customers have more downloads than paying customers. The output should be sorted by earliest date first and contain 3 columns date, non-paying downloads, paying downloads.

| ms_user_dimension | ms_acc_dimension          | ms_download_facts |
| ----------------- | ------------------------- | ----------------- |
| user_id - int     | acc_id - int              | date - datetime   |
| acc_id - int      | paying_customer - varchar | user_id - int     |
|                   |                           | downloads - int   |

## Task 17

Find the most profitable company from the financial sector. Output the result along with the continent.

| forbes_global_2010_2014 |
| ----------------------- |
| company - varchar       |
| sector - varchar        |
| industry - varchar      |
| continent - varchar     |
| country - varchar       |
| marketvalue - float     |
| sales - float           |
| profits - float         |
| assets - float          |
| rank - int              |
| forbeswebpage - varchar |

## Task 18

Create a simple SELECT query to display student information of all ACTIVE students.

| students            |
| ------------------- |
| Id - int            |
| FirstName - varchar |
| LastName - varchar  |
| IsActive - boolean  |

Note: IsActive (true or false)

## Task 19

Return all columns from the *people* table, and join to the *toys* table so that you can return the COUNT of the toys.

people table schema

    id
    name

toys table schema

    id
    name
    people_id

## Task 20

Table: World

| World                 |
| --------------------- |
| name        - varchar |
| continent   - varchar |
| area        - int     |
| population  - int     |
| gdp         - int     |

name is the primary key column for this table.
Each row of this table gives information about the name of a country, the continent to which it belongs, its area, the population, and its GDP value.

A country is big if:

    it has an area of at least three million (i.e., 3000000 km2), or
    it has a population of at least twenty-five million (i.e., 25000000).

Write an SQL query to report the name, population, and area of the big countries.

## Task 21

| Products          |
| ----------------- |
| product_id - int  |
| low_fats   - enum |
| recyclable - enum |

product_id is the primary key for this table.
low_fats is an ENUM of type ('Y', 'N') where 'Y' means this product is low fat and 'N' means it is not.
recyclable is an ENUM of types ('Y', 'N') where 'Y' means this product is recyclable and 'N' means it is not.

Write an SQL query to find the ids of products that are both low fat and recyclable.

## Task 22

| Customer              |
| --------------------- |
| id          - int     |
| name        - varchar |
| referee_id  - int     |

id is the primary key column for this table.
Each row of this table indicates the id of a customer, their name, and the id of the customer who referred them.

Write an SQL query to report the IDs of the customer that are not referred by the customer with id = 2.

## Task 23

Find the titles of workers that earn the highest salary. Output the highest-paid title or multiple titles that share the highest salary.

| worker                  | title                    |
| ----------------------- | ------------------------ |
| worker_id - int         | worker_ref_id - int      |
| first_name - varchar    | worker_title - varchar   |
| last_name - varchar     | affected_from - datetime |
| salary - int            |
| joining_date - datetime |
| department - varchar    |

## Task 24

Find order details made by Jill and Eva. Consider the Jill and Eva as first names of customers. Output the order date, details and cost along with the first name. Order records based on the customer id in ascending order.

| customers              | orders                  |
| ---------------------- | ----------------------- |
| id - int               | id - int                |
| first_name - varchar   | cust_id - int           |
| last_name - varchar    | order_date - datetime   |
| city - varchar         | order_details - varchar |
| address - varchar      | total_order_cost - int  |
| phone_number - varchar |

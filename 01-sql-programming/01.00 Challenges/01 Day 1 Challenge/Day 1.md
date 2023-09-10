You own a business called ABC. To drive dependable decisions using data, you will develop an SQL database, call it ABC_DATA, which you will use to store all your customer info, 
customer orders, product info and your order information. 

In these series of challenges, in SQL you are going to do the following: 
1. Create a database and name it ABC_DATA
2. Create 4 tables, in which you will insert the following datapoints:

1.1 customers
  Example Data :
  
  customer_id | first_name | last_name | email |
  ----------- | ----------- | -----| -------|
  1         | Joe | Doe | johndoe@email.com|
  
  
1.2 products
    Example Data :
  
  product_id | product_name | price |
  ----------- | ----------- | -----|
  1         | Product A | 10.00 | 

 1.3 orders
    Example Data :
    
  order_id | customer_id | order_date |
  ----------- | ----------- | -----|
  1           | 1           | 2023-05-01 |


 1.4 order_items
    Example Data :
    
  order_id | product_id | quantity |
  ----------- | ----------- | -----|
  1         | 1 | 2 |

  Example : Your queries will have the following syntax 

          CREATE TABLE students (
            student_id integer PRIMARY KEY,
            student_first_name varchar(100),
            student_last_name varchar(100),
            student_email varchar(100)
         );

  
  

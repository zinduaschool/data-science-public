This a continuation of the previous day's challenge. 
Your task will be to answer the following questions: 
1. Find the first order (by date) for each customer.
2. What’s the total revenue per product?
3. Find the day with the highest revenue.
Hint : Your Query will have the following Syntax : 
                                
                                SELECT
                                c.first_name,
                                c.last_name,
                                p.price FROM xxxx o
                                JOIN order_items oi on oi.order_id = o.order_id
                                JOIN products p on p.product_id =oi.product_id
                                JOIN customers c on c.customer_id=o.customer_id
                                WHERE price=(SELECT XXX(xxx) FROM xxxx );

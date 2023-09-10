This a continuation of the previous day's challenge. 
Your task will be to answer the following questions: 
1. Which customer has made the most orders?

Hint, your query will have the following structure: 
        SELECT order_counts as (
        SELECT customer_id, count(order_id) AS order_count
        FROM xxxx
        GROUP BY xxxx
        ),
        max_order_count AS (
        SELECT max(order_count) as max_count
        FROM xxxx
        )
        SELECT c.first_name, c.last_name
        FROM xxxx c
        JOIN order_counts oc ON c.customer_id = oc.customer_id
        JOIN max_order_count moc ON oc.order_count = moc.max_count;

2. What’s the total revenue per product?

Hint: Your Query WIll have the following structure : 

        SELECT p.product_name,
        p.price * sum(oi.quantity) AS total_revenue
        FROM xxxx p
        JOIN order_items oi ON oi.product_id = p.product_id
        GROUP BY xxxx p.xxx, p.xxx,
        ORDER BY 2 desc;
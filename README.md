# Taniya-Mittal-Task-6
<br>
Here is the some dataset we are using- online sales.
<br>
Here are the step-by-step guide for analyzing monthly revenue and order volume using MYSQL on an online sales dataset.
<br>
<br>
1. UNDERSTAND YOUR DATASET
<br>
Assume your table is named orders with fields like:
<br>
order_id
<br>
order_date
<br>
customer_id
<br>
order_total (or amount)
<br>
status
<br>
Adjust field names based on your actual schema.
<br>
<br>
2. QUERY TO ANALYZE MONTHLY REVENUE AND ORDER VOLUME
<br>
SELECT
<br>
    DATE_FORMAT(order_date, '%Y-%m')
    <br>
    AS month,
    <br>
    COUNT(order_id) AS total_orders,
    <br>
    SUM(order_total) AS total_revenue
    <br>
FROM
<br>
    orders
    <br>
WHERE
<br>
    status = 'Completed'  -- 
    <br>
    Optional: filter out cancelled/refunded orders
    <br>
GROUP BY
<br>
    DATE_FORMAT(order_date, '%Y-%m')
    <br>
ORDER BY
<br>
    month;
    <br>
    <br>
    OUTPUT EXAMPLE IS ADDED AS IMAGE.

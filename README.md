# E-Commerce-Order-Analytics-Insights-for-Operational-and-Customer-Optimization
**Business Objective**
This project aims to perform data-driven analysis on an e-commerce company's order management system to identify opportunities for operational improvement and customer satisfaction. By writing complex SQL queries, the project addresses key business questions related to:

- Understanding order patterns based on transaction types (excluding irrelevant and fraudulent records).

- Identifying top-performing customers to assist in loyalty program planning.

- Evaluating departmental shipping efficiency by tracking shipment modes and delivery success.

- Assessing shipment compliance to ensure adherence to scheduled delivery timelines.

- Calculating cancellation rates by region to help mitigate losses and improve regional service quality.

The insights from this analysis can help business stakeholders streamline logistics, enhance the customer experience, and develop data-backed strategies for marketing, fulfillment, and fraud mitigation.

Question 1: Get the number of orders by the Type of Transaction. Please exclude orders shipped from Sangli and Srinagar. Also, exclude the SUSPECTED_FRAUD cases based on the Order Status. Sort the 
result in the descending order based on the number of orders.

![image](https://github.com/user-attachments/assets/4ac0c6f3-898e-4313-abca-f3b7f88d87c5)

Answer: DEBIT is the most frequently used transaction type, indicating a preference for digital or card-based payments over cash in this filtered dataset.

Question 2: Get the list of the Top 3 customers based on the completed orders along with the following details:
-- Customer Id, Customer First Name, Customer City, Customer State, Number of completed orders, Total Sales

![image](https://github.com/user-attachments/assets/a30306e4-89da-493f-ba29-12cf7f9c513d)

Answer: All top 3 customers are named Mary, suggesting either common customer naming or duplicate entries across different locations. Santa Clara (CA) tops the list in terms of total sales among them.

Question 3: Get the order count by the Shipping Mode and the Department Name. Consider departments with at least 40 closed/completed orders.

![image](https://github.com/user-attachments/assets/daf73bf0-fb64-4b27-afe6-f758771073c5)

Answer: The Standard Class shipping mode and the Fan Shop department have the highest number of closed/completed orders, indicating strong demand and consistent delivery in that segment.

Question 4: Create a new field as shipment compliance based on Real_Shipping_Days and Scheduled_Shipping_Days. 
It should have the following values:
	Cancelled shipment - If the Order Status is SUSPECTED_FRAUD or CANCELED
	Within schedule - If shipped within the scheduled number of days 
	On time - If shipped exactly as per schedule
	Upto 2 days of delay - If shipped beyond schedule but delay upto 2 days
	Beyond 2 days of delay - If shipped beyond schedule with delay beyond 2 days

Which shipping mode was observed to have the greatest number of delayed orders?

![image](https://github.com/user-attachments/assets/c62be314-5a99-4ac6-9fe0-4906dc682e58)

Answer: The Standard Class shipping mode experienced the highest number of delayed shipments, indicating potential bottlenecks or inefficiencies in that delivery category


Question 5: An order is cancelled when the status of the order is either CANCELED or SUSPECTED_FRAUD. Obtain the list of states by the order cancellation % and sort them in the descending order of the 
cancellation %. 

![image](https://github.com/user-attachments/assets/45e446f6-c979-4aac-9dc8-30b87e8afdb8)

Answer: Manipur had the highest cancellation percentage at 11.11%, which may warrant a deeper investigation into local logistics, fraud trends, or customer behavior.

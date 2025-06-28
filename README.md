# Supply_Chain_Insights
SQL Project

# Decoding Supply Dynamics: A Deep Dive into Order Performance, Customer Trends & Delivery Insights

## Database: `supply_db`

This project aims to analyze key aspects of a supply chain database by focusing on **order behavior**, **customer patterns**, **shipping compliance**, and **cancellation trends**.

---

## Business Objective

The objective of this project is to uncover operational insights that help improve supply chain performance, customer satisfaction, and delivery efficiency. The analysis focuses on:

- Identifying dominant transaction types while filtering out fraud and irrelevant regions.
- Ranking top-performing customers based on completed orders and total sales.
- Analyzing order distribution across shipping modes and departments with strong fulfillment rates.
- Measuring shipment compliance against scheduled vs actual shipping days.
- Calculating state-wise cancellation percentages to identify high-risk regions.

These insights are crucial for:

- Supply Chain Analysts  
- E-Commerce Operations Managers  
- Logistics & Delivery Strategy Teams

---

## Queries

### Business Problem 1: Find the number of valid orders by transaction type, excluding Sangli, Srinagar, and suspected frauds.
![image](https://github.com/user-attachments/assets/e4ed42ac-0a84-4094-9e6f-d402e0a68c52)

### Output
Type      | Orders
----------|--------
DEBIT     |	799
TRANSFER	| 532
PAYMENT	  | 488
CASH	    | 259

---

### Business Problem 2: Identify the top 3 customers with the highest number of completed orders and total sales.
![image](https://github.com/user-attachments/assets/3ff4d929-0b76-438c-a64d-8b59c984ca12)

### Output
customer_id  | First_Name   | City         | State     | completed_orders | total_sales
-------------|--------------|--------------|-----------|------------------|--------------
3465	       | Mary	        | Santa Clara	 | CA	       | 10	              | 2929.74
5612	       | Mary	        | Caguas	     | PR	       | 10	              | 2188.82
9106	       | Mary	        | Waukegan	   | IL	       | 7	              | 1119.83


---

### Business Problem 3: Get order counts by shipping mode and department, considering only departments with at least 40 completed or closed orders.
![image](https://github.com/user-attachments/assets/6cc32a54-e606-41dc-a769-36bf19dd5908)

### Output
Shipping_Mode  | department_name | order_count        
---------------|-----------------|--------------
Standard Class | Footwear	       | 86
Standard Class | Fan Shop	       | 371
Standard Class | Outdoors	       | 73
Standard Class | Golf	           | 186
Standard Class | Apparel	       | 300
Standard Class | Fitness	       | 24
Standard Class | Discs Shop	     | 85
Second Class   | Fan Shop	       | 165
Second Class	 | Golf	           | 75
Second Class	 | Apparel	       | 143
Second Class	 | Fitness	       | 10
Second Class	 | Footwear	       | 22
Second Class	 | Outdoors	       | 27
Second Class	 | Discs Shop	     | 14
Same Day	     | Footwear	       | 10
Same Day	     | Apparel	       | 26
Same Day	     | Golf	           | 9
Same Day	     | Fan Shop	       | 27
Same Day	     | Outdoors	       | 7
Same Day	     | Fitness	       | 3
Same Day	     | Discs Shop	     | 15
First Class	   | Footwear	       | 34
First Class	   | Apparel	       | 84
First Class	   | Fan Shop	       | 119
First Class	   | Outdoors	       | 26
First Class	   | Golf	           | 57
First Class	   | Fitness	       | 13
First Class	   | Discs Shop	     | 18

---

### Business Problem 4: Classify orders by shipment compliance and find the shipping mode with the most delayed deliveries.
![image](https://github.com/user-attachments/assets/ee912433-ed91-4f83-b346-fc4831014813)

### Output
Shipping_Mode  | delayed_orders         
---------------|-----------------
Standard Class | 466	       

---

### Business Problem 5: Calculate order cancellation percentage by state and rank states by highest cancellation rate.
![image](https://github.com/user-attachments/assets/64ebb254-3770-4e2f-b461-31a138f5f23d)

### Output
Order_State       | cancellation_percentage       
------------------|-------------------------
Manipur	          | 11.11
Haryana	          | 9.09
Punjab	          | 9.09
Jharkhand	        | 8.82
Puducherry	      | 8.33
Uttar Pradesh	    | 6.25
Telangana	        | 5.88
Andhra Pradesh	  | 5.21
Jammu and Kashmir	| 4.55
Kerala	          | 4.35
Delhi	            | 4.11
Karnataka	        | 4.09
Madhya Pradesh	  | 3.77
Odisha	          | 3.45
Chhattisgarh	    | 2.94
Maharashtra	      | 2.80
Tamil Nadu	      | 2.55
Bihar	            | 2.30
West Bengal	      | 1.64
Gujarat	          | 1.63
Rajastan	        | 0.67
Assam	            | NULL
Uttarakhand	      | NULL
Chandigarh	      | NULL
Tripura	          | NULL

---

## Tables Used

- `orders` – order_id, type, city, status, real/scheduled shipping days, shipping mode  
- `ordered_items` – order_id, sales  
- `customer_info` – id, first_name, city, state  
- `product_info` – product_id, category_id  
- `department` – department name  

---

## Tools & Skills

- SQL Joins (INNER, LEFT)  
- Aggregate functions (COUNT, SUM)  
- CASE statements for conditional logic  
- Data filtering and transformation  
- Sorting and limiting results  

---

## Outcome

This project reveals actionable supply chain insights to:
- Optimize delivery performance  
- Identify high-value customers  
- Reduce fraud & cancellations  
- Improve department-wise and mode-wise shipping strategy  

---

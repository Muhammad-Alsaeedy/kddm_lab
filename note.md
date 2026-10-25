# SWEN466 Assignment 1: Short Note

## 4.

a) **Customer_id** and **customer_unique_id** both look like customer identifiers, but **customer_id** is unique in every row (99,441 of 99,441) because it is generated per order, while **customer_unique_id** repeats (only 96,096 distinct values) because it identifies the actual person, so I would use **customer_unique_id** to count customers.

b) **Order_items** is the junction table: its composite key (order_id, order_item_id) resolves the many-to-many relationships between orders and products and between orders and sellers.

c) The data is stricter than the idea of "a customer places orders" for customers to orders: it sounds like one customer can have many orders, but in the data every **customer_id** has exactly one order. The circle on orders to order_items is justified by the data, because 775 orders have no items at all (mostly unavailable and canceled orders).

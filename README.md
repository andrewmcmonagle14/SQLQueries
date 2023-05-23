# SQLQueries
MIS 375 Database Design for Business Application: Homework #3
Use the relational schema of the Pine Valley Furniture (PVF) database to create and execute SQL queries. Here is the relational schema:

pvf_customer (cid, name, address, city, state, zipcode)
pvf_order (oid, orderdate, cid)
	cid is a foreign key references customer(cid)
pvf_product (pid, prod_desc, prod_finish, price, prod_line_id)
pvf_order_item (oid, pid, quantity)
	oid is a foreign key references pvf_order(oid)
	pid is a foreign key references pvf_prod(pid)

You need to use the script file named pvf_create.sql to create the tables and populate the tables with sample data. Then write SQL statements for the following queries.

1.	List pid, description, finish, and price of all the products. Show description and finish as one field separated by a comma. (Hint: use concat() function.) 

2.	Calculate the average price of all products. Round the price to 2 decimal places. (Hint: use format() function to round the price.)

3.	How many orders were placed in the 4th quarter of 2022?

4.	For each order that contains product 2 (pid=2), display the oid, orderdate, pid, and quantity. Sort the results by order date in descending order.

5.	For each line item, show the oid, product description, quantity, price, and subtotal (calculated as price * quantity). Sort the results by oid in ascending order.

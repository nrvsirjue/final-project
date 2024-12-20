<h1 align="center"> REST API Backend Created for Accessing Dosa Orders </h1>
<h2 align="center">Project Overview</h2>

A project designed to easily pull individual details about orders from the Dosa restaurant, including specific details about the customer, the items, or the orders in a fast and ordered manner.

<h2>Project Design</h2>

> **The project is designed as follows:**

Using the files within this repository, the company will be able to create a connection to a SQLite database and an existing JSON file, containing orders received over time, to pull out the relevant customer, item, and/or order information and populate each individual table.
  * The init_dp.py file initializes the database by creating new tables for the customer, item, and order information, and also creates an item list containing order and item IDs.
  * The main.py file runs the FastAPI server, using queries to the database for creating, reading, updating, and deleting the data.

<h2>Instructions on how to use:</h2>

  >**Init_dp.py File**
   
 1. Initialize an empty database using SQLite and create tables, if not already existing, for all the details desired to be pulled out. In this case, it is the customer information (name, phone number, and uniqure ID using phone number), the item information (name, price, item ID), and the order information (customer orders, what items are included in the order, etc.). There is also an option to create an item list to store details about the items along with each order that links to the other tables.
 2. Using a valid JSON file, such as example_orders.json, the program allows for JSON connection to extract and populate data into each respective table.
 3. Run the file to solidify the creation of the database.
 
  >**Main.py File**

1. Import FastAPI, sqlite3, and BaseModel (from pydantic).
2. Create a class for each parameter that is included in the database, in this case it is the Customer, Item, and Order class.
3. Set up your database connection.
4. Create your endpoints (Create (POST), Read (GET), Update (PUT), Delete) for each parameter. 


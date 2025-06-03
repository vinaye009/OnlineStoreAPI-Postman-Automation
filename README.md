Online Store API - Postman Automation Project

Table of Contents

Project Gist
API Modules & What They Do
Folder Structure
Tech Used
How to Run
Tests Covered (Key Ones)
What I Learned/Did (Automation Bits)
Other Important Stuff
Thanks To
--------------------------------------------------------------------
1. Project Gist
This project is all about testing APIs for an online store using Postman. We've built and tested APIs for three main parts: Products, Cart, and User. The aim is to make sure everything works correctly – like adding, getting, updating, and deleting data, plus features like sorting and user login.

2. API Modules & What They Do
We've got three main sections (modules) with their own APIs:

Products: Deals with all product information – getting lists, specific products, categories, and managing products (add, update, delete).
Cart: Handles shopping carts – getting cart details, filtering by date or user, and managing carts (add, update, delete).
User: For user accounts and logging in – getting user details, adding new users, and managing user data (update, delete).

3. Folder Structure
My project on GitHub is neatly organised by module:
Okay, here's a simpler, more concise README.md for your Postman API automation project, in an Indian English style.

Online Store API - Postman Automation Project
Table of Contents
Project Gist
API Modules & What They Do
Folder Structure
Tech Used
How to Run
Tests Covered (Key Ones)
What I Learned/Did (Automation Bits)
Other Important Stuff
Thanks To
1. Project Gist
This project is all about testing APIs for an online store using Postman. We've built and tested APIs for three main parts: Products, Cart, and User. The aim is to make sure everything works correctly – like adding, getting, updating, and deleting data, plus features like sorting and user login.

2. API Modules & What They Do
We've got three main sections (modules) with their own APIs:

Products: Deals with all product information – getting lists, specific products, categories, and managing products (add, update, delete).
Cart: Handles shopping carts – getting cart details, filtering by date or user, and managing carts (add, update, delete).
User: For user accounts and logging in – getting user details, adding new users, and managing user data (update, delete).
3. Folder Structure
My project on GitHub is neatly organised by module:
.
├── Cart Collection/
│   ├── Cart.postman_collection.json
│   ├── Cart_data.json         # (Data for running tests)
│   └── workspace.postman_globals.json # (If any variables specific to Cart)
├── Product Collection/
│   ├── Products.postman_collection.json
│   ├── Product_data.json
|   ├── Products_data_csv.csv
│   └── workspace.postman_globals.json
└── User Collection/
    ├── User.postman_collection.json
    ├── User_Data.json
    └── workspace.postman_globals.json
    
Each folder has its Postman Collection JSON and any data files needed for testing.

4. Tech Used
API Testing: Postman (my main tool)
Scripting: JavaScript (for test logic)
Data: JSON, CSV

6. How to Run
Just follow these simple steps to run the tests:

Get the code: Clone this GitHub repo to your computer.
Import to Postman: Open Postman, then go to File > Import. Select the *.postman_collection.json files from each module folder.
Set up Environment (if any): If you have an environment file, import it and select it in Postman. Make sure all necessary variables are set.
Run Tests:
Pick a collection (e.g., "Products Collection").
Click "Run" or "Runner" (bottom left).
Select the tests you want.
Under "Data", choose the relevant _data.json or .csv file if you're doing data-driven tests.
Hit "Run [Collection Name]". Done!

6. Tests Covered (Key Ones)
I've made sure to cover the main things:

Product Module: Checked if all products, specific products, limited products, sorted products, and categories can be retrieved. Also tested adding, updating, partially updating, and deleting products. Validated error messages for wrong product IDs.
Cart Module: Verified getting all carts, specific carts, filtering by date/user, and managing carts (CRUD). Also checked error handling for invalid IDs.
User Module: Tested user login and token generation. Verified getting all users, specific users, and user management (CRUD). Also checked error handling for wrong credentials or IDs.

7. What I Learned/Did (Automation Bits)
I learned to make my tests smart by:

Handling Dynamic Data: Captured things like auth tokens from one request and used them in others.
JSON Schema Validation: Used code to check if API responses have the correct structure and data types, for both single items and lists.
Data-Driven Testing: Ran tests using data from JSON/CSV files.
Smart Test Logic: Wrote scripts to change test assertions based on inputs (like checking ascending/descending sort).
Error Handling Checks: Made sure the API gives proper error messages for wrong requests (like 400 or 404 errors).

8. Other Important Stuff
The project design also considered:

Performance: APIs should be fast (respond within 200ms for most requests).
Security: Token-based login for protected areas.
Good Error Messages: API should give clear error messages if something goes wrong.

9. Thanks To
Special thanks to the "Online Store API - Technical Design" document, which guided this project.

    

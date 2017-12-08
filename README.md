# Item Catalog Project - Mike Frysinger
A web application that provides a list of items within a variety of categories, and integrate registration 
and authentication using a third party. Authenticated users have the ability to post, edit, and delete 
their own items.

# Features:
* Web application displaying categories with listed items assigned to each category
* SQLite database (to store and organize information)
* All categories and items are public viewing(Login not required)
* Registration adn authentication using Google OAuTH service
* Google profile user name and picture displayed in application heading
* Authenticated/authorized users can create items for each category
* Authenticated/authorized users can edit and delete items which they created
* API endpoint returning JSON objects for categories and items


# Files included:
/static/style.css
/templates/login.html
/templates/main.html
/templates/category.html
/templates/categoryItems.html
/templates/itemDescription.html
/templates/newItem.html
/templates/editItem.html
/templates/deleteItem.html
/application.py
/client_secrets.json
/database_setup.py    
/lotsofitems.py
/README.md

# JSON endpoints:
http://localhost:8000/catalog/categories/JSON  	# Get all Categories 
http://localhost:8000/catalog/items/JSON 	 # Get all Catalog Items 
http://localhost:8000/catalog/<*category ID*>/items/JSON  	#Get all items that belongs to the given catgeory
http://localhost:8000/catalog/catalog/<*category ID*>/items/<*item ID*>/JSON  #Get a single item 

# Install Vagrant and Virtualbox:
* Vagrant - [download](https://www.vagrantup.com/downloads)
* Virtual Box - [download](https://www.virtualbox.org/wiki/Downloads)

# Install and run application:
1. Extract project file:
  - Open terminal.
  - Unzip "catalog.zip" to your local '/vagrant/catalog' folder
2. Move to project folder:
  - Go to file directory '/vagrant/catalog'
3. Turn on the virtual machine:
  - Open Linux shell: Type `vagrant up`
  - Followed by `vagrant ssh`
4. Move to the /vagrant/catalog folder:
  - Enter `cd /vagrant/catalog`
5. To create and populate database:
  - Enter `python database_setup.py` # Creates SQLite database 'catalog.db, with user, category and item tables'
  - Enter `python lotsofitems.py` # Adds sample categories, items, and one user
5. Start server:
  - Enter `python applications.py`
6. Go to browser and enter `http://localhost:8000/`




























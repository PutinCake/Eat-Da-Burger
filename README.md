# Eat-Da-Burger

### Overview

A Node, Express, Handlebars, and MySQL burger app that lets users input the names of burgers they'd like to eat... and then devour them! Please check out the launched app on Heroku here!

### Functionality
Using an home-grown ORM, the app has 3 basic CRUD functions

* READ all entries from the MySQL database and display them to the DOM using Handlebars.
* UPDATE a selected burger by clicking "Devour It", which
 * hits an `/burger/eat/:id` route in Express to change its "devoured" status in the MySQL database
 * re-routes the webpage back to the index, where the burger is now in the devoured column (via Handlebars)
* CREATE a new burger using the "Place Order" form, which...
 * hits a `/burger/create` route in Express to insert a new burger into the MySQL database
 * re-routes the webpage back to the index, where the burger is now ready to be eaten column (via Handlebars)

### Directory structure
All the recommended files and directories should look like the following structure:

    .
    ├── config
    │   ├── connectiom.js
    │   └── ormr.js
    │ 
    ├── controllers
    │   └── burgers_controller.js
    │
    ├── models
    │   ├── index.js
    │   └── burger.js
    │ 
    ├── node_modules
    │ 
    ├── package.json
    │
    ├── public
    │   ├── assets
    │   │   ├── css
    │   │   │   └── burger_style.css
    │   │   ├── img
    │   │   │   └── ...
    │   │   └── js
    │   │       └── burgers.js
    │   └── test.html
    │
    ├── db
    │   ├── schema.sql
    │   └── seeds.sql
    ├── server.js
    │
    └── views
        ├── index.handlebars
        └── layouts
            └── main.handlebars
            
### Screenshots

Index page

![pic](https://github.com/PutinCake/Eat-Da-Burger/blob/master/public/assets/images/index.png)

Input

![pic](https://github.com/PutinCake/Eat-Da-Burger/blob/master/public/assets/images/input.png)

Added

![pic](https://github.com/PutinCake/Eat-Da-Burger/blob/master/public/assets/images/added.png)

Eaten

![pic](https://github.com/PutinCake/Eat-Da-Burger/blob/master/public/assets/images/eaten.png)

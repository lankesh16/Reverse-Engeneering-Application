# USER AUTHENTICATION

This application will let the user create an account and login into the account. 

**USER STORY**

As a User I want to safely log in to "A", I want to make sure my personal information is safely kept.

# TECH USE

MYSQL, PASSPORT, PASSPORT-LOCAL, SEQUELIZE, BCRYPTJS, EXPRESS AND EXPRESS-SESSION

# HOW TO START
 In order to use this application, please follow the these steps; 

 1- clone repo to local storage
 2-Go to Develop > Config> Config.js & add username & password

3-Create mysql database name "passport_demo"

4- In terminal run "npm i" all node packages //very important//

5- In terminal run "node server.js"

6- Type http://localhost:3360 in address bar
 
# FILE SCHEMA
Config
    - Middleware
        - isAuthenticated.js
    - config.json
    - passport.js

Models
    - index.js
    - user.js

Public
    - js
        - login.js
        - members.js
        - signup.js
    - stylesheets
        - style.css
    - login.html
    - members.html
    - signup.html
Routes
    - api-routes.js
    - html-routes.js

# FILE EPXLAINED

CONFIG > MIDDLEWARE > 
isAuthenticated.js
--it stops the user from going to routes  they are not allowed to visit if they are not logged in. Hoever if they are logged in it will continue wit the request--

CONFIG > 
    congig.json

-- Connection arrangement in order to connect with the server--

    passport.js 

--Uses javascript langugae to tell passport that we are looking to log in using an email address and password--

MODELS >
    index.js  

--Connects to the database and then imports users login info to data--

    user.js 
-- This file requires "bcrypt" to hash the password. Javascript manages what is stored in the database--

PUBLIC > js > 

    login.js
--This file validates the login form--

    member.js
--This file just does a GET request to figure out which user is logged in
  and updates the HTML on the page--

    signup.js
--This file validates the signup form--

PUBLIC > stylesheet > 

    style.css
-- Adds style to login form and sign up form--

 PUBLIC > 

    login.hmtl
--This file creates the login form and page--   

    members.html
--This file creates the members form and page--

    signup.html
--This file creates the signup form and page--


ROUTES >

    api-routes.js 
--This file has routes to sign in, logging out and retrieving user specific data to be displayed to the client side--

    html-routes.js 
--This file contains routes that check if the user is signed in, if the user already has an account and sends them to the right html page--

    package.json 
--Has all the package details, the version info, node modules etc.--

    server.js 
-- This file requires the packages, it gets the PORT set up,it creates express and middleware, it creates routes and then syncs the database info in terminal upon successful connection to server--








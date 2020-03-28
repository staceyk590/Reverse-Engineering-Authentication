# Reverse-Engineering-Authentication

# Reverse-Engineering-Authentication

This aplications uses mysql database to store users data. The user can create an account, then log in and out of the account.

It allows a user to store their data in the account securely.


FILES

CONFIG folder

passport.js This file allows the user to login in using an email as a username and a password, through javascript.

config.json This file is the cinfiguration to connect to the server

middleware/isAuthenticated.js If user is logged in, it redirects them to their login page, if they are not logged in it restricts their access.

MODELS folder

index.js Imports the users login data and then connects to the database

user.js Makes the databse secure if ever compromised by requiring "brcrypt".  The javascript used to store data in the database.



PUBLIC folder

js/login.js  After the login form is submitted this validate the email and password and uses a function to post to login route

members.js  This uses to GET request to update the html with the users details

signup.js  After the signup form is submitted this validate the email and password and uses a function to post to the signup route



ROUTES folder

api-routes.js  This file uses the routes to sign in, log out and to get user data.

html-routes.js This file uses the routes to confirm whether the user has an account and is signed in.



package.json  Has all the packages information.

server.js  Requires necessary npm packages and passport.  Sets up the port and requiring models for syncing. Creates express app and configure middleware. REquires routes and syncs databse and logs a message to the users when successful 




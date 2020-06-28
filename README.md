# robin-twitter-web-app

Node twitter is an effort to rewrite some of Twitter's functionality using modern javascript based toolchain. It was mostly an effort to learn Node.js and trying to reverse engineer some of twitter's feature.

It has support for tweeting, commenting and following with analytics

Prerequisites
You are required to have Node.js and MongoDB installed if you'd like to run the app locally.

Node.js
Mongodb


Usage
# First install all the project dependencies.
# run mongodb server
~/ mongod
~/node-twitter/ npm install
# Now run the app
~/node-twitter/ npm start

> node-twitter@1.1.0 start ~/node-twitter
> node server.js

Express app started on port 4000
To test it out:
Create a variables.env file in the root and enter these credentials

PORT=3000
DATABASE=mongodb://localhost/twitter_clone1
SECRET='Anything you can type'
Replace the DATABASE url to a mongoDB driver url or your local database url

Then run

npm run dev

See it online at:
https://twitter-clone-new.herokuapp.com/

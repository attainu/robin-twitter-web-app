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


Important
Twitter is a registered trademark of Twitter Inc. This project is just for learning purposes and should be treated as such.]


Key Dependencies
Express.js
Node.js
MongoDB
EJS
bcrypt


MEAN Task List
Simple full-stack app that displays a list of messages ('tweets') generated on the client side and processes them using backend node.js. Future link to mongodb database to save messages

Code Examples
server/index.js - function to post tweet data from html frontend req.body parameters; filtering text then adding to tweets array.
app.post('/tweets', (req, res, next) => {
	if(isValidTweet(req.body)) {
		const tweet = {
			name: filter.clean(req.body.name.toString()),
			content: filter.clean(req.body.content.toString()),
			created: new Date()
		};

		tweets
			.prepend(tweet)
			.then(createdTweet => {
				res.json(createdTweet);
			});

	} else {
		res.status(422);
		res.json({
			message: 'Helooo, name and message are required'
		});
	}
});
Features
A simple app with vanilla javascript. No js framework used.
Status & To-Do List
Status: basic working app that saves tweets locally.

To-Do: Correct code so latest tweet listed first (reverse() function not working). Remove duplication of tweets. Add connection to mongodb database.

npm run dev

See it online at:
https://twitter-app-init.herokuapp.com

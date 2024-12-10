Social Network API

Overview

This project is a social network API built with Node.js, Express, MongoDB, and Mongoose. It provides a set of routes to interact with a social media platform, including functionalities for creating and managing users and thoughts. The goal of the API is to handle basic CRUD operations and provide endpoints for data retrieval, which can be tested using tools like Insomnia.

Features

	•	User Management: Create and manage users.
	•	Thought Management: Post and manage thoughts, including reactions.
	•	Friendship Management: Add and remove friends between users.
	•	Real-time Data: Interact with MongoDB to retrieve and store data.

Technologies Used

	•	Node.js: JavaScript runtime used for building the API.
	•	Express.js: Web framework for building the API routes.
	•	MongoDB: NoSQL database to store user and thought data.
	•	Mongoose: ODM (Object Data Modeling) library to interact with MongoDB.
	•	Insomnia: API testing tool for sending requests and viewing responses.

Getting Started

Prerequisites

Ensure you have the following installed:
	•	Node.js
	•	MongoDB (Locally or through a service like Atlas)
	•	npm or yarn (for package management)

Installation

	1.	Clone this repository:
    git clone https://github.com/your-username/social-network-api.git
cd social-network-api
	2.	Install the dependencies:
    npm install
    	3.	Set up MongoDB:
	•	Ensure that MongoDB is running on your local machine or use a cloud-based service like MongoDB Atlas.
	4.	Start the server:
    npm run start
    The server should now be running at http://localhost:3001.

API Routes

Users

	•	GET /api/users - Get all users.
	•	GET /api/users/:userId - Get a specific user by ID.
	•	POST /api/users - Create a new user.
	•	PUT /api/users/:userId - Update a user’s details.
	•	DELETE /api/users/:userId - Delete a user.

Thoughts

	•	GET /api/thoughts - Get all thoughts.
	•	GET /api/thoughts/:thoughtId - Get a specific thought by ID.
	•	POST /api/thoughts - Create a new thought.
	•	PUT /api/thoughts/:thoughtId - Update a thought.
	•	DELETE /api/thoughts/:thoughtId - Delete a thought.

Reactions

	•	POST /api/thoughts/:thoughtId/reactions - Add a reaction to a thought.
	•	DELETE /api/thoughts/:thoughtId/reactions/:reactionId - Remove a reaction from a thought.

Friends

	•	POST /api/users/:userId/friends/:friendId - Add a friend to a user.
	•	DELETE /api/users/:userId/friends/:friendId - Remove a friend from a user.

Testing with Insomnia

You can test the routes using Insomnia. Here are the steps to follow:
	1.	Create New Requests: In Insomnia, create new requests for each API route.
	2.	Send GET Requests: For example, use a GET request to /api/users to fetch all users, or /api/thoughts to get all thoughts.
	3.	POST and PUT Requests: Use POST and PUT requests to create or update data. Include the necessary payload in the body of the request.
	4.	DELETE Requests: Delete users, thoughts, or reactions with DELETE requests.

Example: GET Users

	•	Set up a GET request in Insomnia with the URL http://localhost:3001/api/users.
	•	Hit “Send” to see a list of all users in the database.

Example: POST Thought

	•	Set up a POST request in Insomnia with the URL http://localhost:3001/api/thoughts.
	•	In the request body, include the thought content (e.g., {"content": "This is a thought"}).
	•	Hit “Send” to create a new thought.

Troubleshooting

	•	Error: EADDRINUSE: This error indicates that the port is already in use. Try stopping the application running on port 3001 or change the port in the server code.
	•	MongoDB Connection Errors: Ensure that MongoDB is running and correctly connected to your app.

Contributing

Feel free to fork this repository and submit pull requests with any improvements or fixes.

License

This project is licensed under the MIT License - see the LICENSE file for details.
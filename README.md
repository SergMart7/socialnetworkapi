# Social Network API

## Description

This project is an API for a social network web application where users can share their thoughts, react to friends' thoughts, and create a friend list. The API is built using Express.js for routing, MongoDB as the database, and Mongoose as the ODM. It also provides functionality for creating, updating, and deleting users, thoughts, reactions, and managing friend lists.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Routes](#api-routes)
- [Technologies Used](#technologies-used)
- [Walkthrough Video](#walkthrough-video)
- [License](#license)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/sergmart7/social-network-api.git
    ```

2. Navigate to the project directory:
    ```bash
    cd social-network-api
    ```

3. Install the necessary dependencies:
    ```bash
    npm install
    ```

4. Set up your MongoDB connection by creating a `.env` file in the root directory with the following content:
    ```
    MONGODB_URI=mongodb://localhost:27017/socialNetworkDB
    ```

5. Start the server:
    ```bash
    npm start
    ```

## Usage

Once the server is running, you can test the API routes using Insomnia, Postman, or another API client. You will be able to:

- Create, read, update, and delete users and thoughts
- Add and remove friends from a user's friend list
- Add and remove reactions to thoughts

### User Routes

- **GET** `/api/users` - Get all users
- **GET** `/api/users/:id` - Get a single user by ID
- **POST** `/api/users` - Create a new user
- **PUT** `/api/users/:id` - Update a user by ID
- **DELETE** `/api/users/:id` - Delete a user by ID

### Friend Routes

- **POST** `/api/users/:userId/friends/:friendId` - Add a friend to a user
- **DELETE** `/api/users/:userId/friends/:friendId` - Remove a friend from a user

### Thought Routes

- **GET** `/api/thoughts` - Get all thoughts
- **GET** `/api/thoughts/:id` - Get a single thought by ID
- **POST** `/api/thoughts` - Create a new thought
- **PUT** `/api/thoughts/:id` - Update a thought by ID
- **DELETE** `/api/thoughts/:id` - Delete a thought by ID

### Reaction Routes

- **POST** `/api/thoughts/:thoughtId/reactions` - Add a reaction to a thought
- **DELETE** `/api/thoughts/:thoughtId/reactions/:reactionId` - Remove a reaction from a thought

## Technologies Used

- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework for Node.js
- **MongoDB** - NoSQL database
- **Mongoose** - ODM (Object Data Modeling) library for MongoDB and Node.js

## Contact and Support

You can reach out to me here on [GitHub](https://github.com/SergMart7) or by email at sergiomartinezdesantiago7@gmail.com.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

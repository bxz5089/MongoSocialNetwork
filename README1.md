# E-Commerce Back End

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Description

Internet retail, also known as **e-commerce**, is the largest sector of the electronics industry, generating an estimated $29 trillion in 2019. E-commerce platforms like Shopify and WooCommerce provide a suite of services to businesses of all sizes.

This is an example back end for an e-commerce site. The project uses Express.js API and Sequelize to interact with a MySQL database.

### API Routes

**`/api/users`**

* `GET` all users

* `GET` a single user by its `_id` and populated thought and friend data

* `POST` a new user:

```json
// example data
{
  "username": "lernantino",
  "email": "lernantino@gmail.com"
}
```

* `PUT` to update a user by its `_id`

* `DELETE` to remove user by its `_id`

**BONUS**: Remove a user's associated thoughts when deleted.

---

**`/api/users/:userId/friends/:friendId`**

* `POST` to add a new friend to a user's friend list

* `DELETE` to remove a friend from a user's friend list

---

**`/api/thoughts`**

* `GET` to get all thoughts

* `GET` to get a single thought by its `_id`

* `POST` to create a new thought (don't forget to push the created thought's `_id` to the associated user's `thoughts` array field)

```json
// example data
{
  "thoughtText": "Here's a cool thought...",
  "username": "lernantino",
  "userId": "5edff358a0fcb779aa7b118b"
}
```

* `PUT` to update a thought by its `_id`

* `DELETE` to remove a thought by its `_id`

---

**`/api/thoughts/:thoughtId/reactions`**

* `POST` to create a reaction stored in a single thought's `reactions` array field

* `DELETE` to pull and remove a reaction by the reaction's `reactionId` value

## Table of Contents

- [Installation](##Installation)

- [Usage](##Usage)

- [License](##License)

- [Tests](##Tests)

- [Questions](##Questions)

---

## Installation

- First, use git clone in the terminal to download the project
- Then open the project in VS Code and in the package.json folder enter the terminal
- Within the terminal, use npm install install to install the all packages
- Open Mysql in terminal and run the schema.sql file to create the database
- Run `npm run seed` to seed data to your database so that you can test the routes.
- The routes can be tested by using Insomnia

---

## Usage

For learning about database

### Screenshot:

![Screenshot](Assets/ScreenShot1.png)

### Walkthrough Video:

[![Watch the video](Assets/ScreenShot2.png)](https://drive.google.com/file/d/1HpUJNOVXbrrU2902jLhfP5lewv5Nx91f/view?usp=sharing)

---

## License

https://opensource.org/licenses/MIT

---

## Tests

There are no tests for this application.

---

## Questions

If you have any questions or concerns please contact me at bxz5089@gmail.com or checkout my GitHub page at [bxz5089](https://github.com/bxz5089/).

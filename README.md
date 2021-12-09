# Final Exam Revision

This repository contains a revision material for the final exam of Fall 2021. You should be able to answer most of these questions to be able to get the final mark you aim for. It also should provide you with some questions that are commonly used in Job Interviews.

## Understanding Questions

1. What is the difference between Relational and Non-Relational Databases?
2. How do we pass data between components in React?
3. What are the different components of Redux? Explain the flow of Redux from React Component to Store to React Component
4. What is the difference between a Database and a Database Management System?
5. Scratch a model of FullStack Development containing the different entities of FullStack Development and how do they interact together.
6. What are the 3 different ways to provide css styling in an HTML file
7. Why do we use JavaScript in FrontEnd Development?
8. What is the DOM?
9. What is the difference between a Framework and a Library?
10. How to pass data between Components in React?
11. What is the difference between JavaScript and TypeScript?
12. What are the benefits of using Redux?
13. Explain how does an Authentication system with web tokens work? What are the different steps?
14. What is the different between sessions and tokens?

## Problem

A Client came to you looking for a web developer to create an e-commerce platform for him. So, you decided to join forces with your friend.
You decided that you'll create the `admin dashboard` while your friend will take care of the `user side`.

### Question 1

What would be the DBMS you'll use for this system? Propose the schema of the models you're going to use

* Example: MongoDB 

```
Product {
    name: string,
    description: string,
    category: Category, // Reference to Category model
    price: number,
    quantity: number,
    imageURL: string
}

Category {
    name: string,
    imageURL: string,
    description: string
}

// User, Admin, ...
```

* Example: MySQL 

```
Product {
    id: number,
    name: string,
    description: string,
    category_id: string, // Reference to Category
    price: number,
    quantity: number,
    imageURL: string
}

Category {
    id: number,
    name: string,
    imageURL: string,
    description: string
}

// User, Admin, Transactions, ...
```

### Question 2

After modeling the database, what are the endpoints of your Rest API?

* Example: 

|               URL                | HTTP Verb | Request Body |                                  Result                                  |
| :------------------------------: | :-------: | :----------: | :----------------------------------------------------------------------: |
|         /api/products            |    GET    |    empty     |                        Return JSON of all Products                       |
|        /api/categories           |    GET    |    empty     |                        Return JSON of all Categories                     |
|        /api/categories           |   POST    |     JSON     |          Create new Category and return JSON of created Category         |
|    /api/categories/:id/products  |    GET    |    empty     |        Get the list of products belonging to the category with the id    |
|      /api/categories/:id         |    PUT    |     JSON     |      Update existing Category by id and return JSON of the updated data  |
|       /api/products/:id          |  DELETE   |    empty     |    Delete Product with matching `id` and return JSON of deleted Product  |
|       /api/auth/login            |   POST    |    JSON      |       Check the admin credentials and send a Token for authorization     |
|                                                        ...                                                                             |

### Question 3

You're going to use React for the client-side, what are the main components needed for the admin dashboard

* Example: 

- Login: a login form with a login form
- Sidebar: The sidebar containing navigation items to navigate between views
- ProductsList: a table containing the list of products
- EditProduct
- CategoriesList
- EditCategory
- ...

## Good Luck!
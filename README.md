# E-commerce Back End [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Description

Video Walthrough:

https://drive.google.com/file/d/1R-ovtczJKdkk_L6K5wMXAHUE6vV76Oej/view

Week 13 of Columbia Engineering Coding Bootcamp challenges us to create an e-commerce back end using four node packages:

* Express
* Mysql2
* Sequelize
* Dotenv

We used starter code supplied by the Bootcamp https://github.com/coding-boot-camp/fantastic-umbrella

There is no front-end code, so I used Insomnia to test routes. The topic of week 13 is object-relational mapping, in this case using Sequelize, which makes it easier to work with a SQL database. We have a number of objects that are mapped to tables in MySQL:

* Category
* Product
* Tag
* ProductTag

Relationships are defined by the model, and sequelize implements those relationships in the database schema.

## Installation

```sh
git clone https://github.com/chrispobrien/13-e-commerce-back-end.git
```

This creates the folder 13-e-commerce-back-end within which you will find the project files. Note that I removed the 'develop' folder in the starter code. Issue these commands to download node dependencies:

```sh
cd 13-e-commerce-back-end
npm i
```

Create or recreate the MySQL database:

```sh
mysql -u root -p
source db/schema.sql
exit
```

Create a .env file in the root folder with contents:

```
DB_NAME='ecommerce_db'
DB_USER='root'
DB_PASSWORD='your_root_password'
```

Run this from the command prompt to initialize all tables within the ecommerce_db database:

```sh
node server.js
```

Press Ctrl-C to exit node.

Then issue this command to seed the database:

```sh
node seeds/index.js
```

## Usage

[![E-Commerce Back-End][screenshot]](./assets/images/screenshot.png)

```sh
node server.js
```

### Test out endpoints:

Get all:

    http://localhost:3001/api/categories
    http://localhost:3001/api/tags
    http://localhost:3001/api/products

Get one by id:

    http://localhost:3001/api/categories/1
    http://localhost:3001/api/tags/1
    http://localhost:3001/api/products/1

Add new: (must be POST) (body must contain json formatted data)

    http://localhost:3001/api/categories
    http://localhost:3001/api/tags
    http://localhost:3001/api/products

Change one by id: (must be PUT) (body must contain json formatted data)

    http://localhost:3001/api/categories/1
    http://localhost:3001/api/tags/1
    http://localhost:3001/api/products/1

Delete one by id: (must be DELETE)

    http://localhost:3001/api/categories/1
    http://localhost:3001/api/tags/1
    http://localhost:3001/api/products/1

## Credits

Starter code provided by Trilogy/Columbia Engineering Coding Bootcamp. I coded the class model and most endpoints, two were provided in the starter code.

## License

MIT License [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<!-- MARKDOWN LINKS & IMAGES -->
[screenshot]: ./assets/images/screenshot.png
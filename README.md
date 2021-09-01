# CMS-Style Tech Blog
AS A developer who writes about tech
I WANT a CMS-style blog site
SO THAT I can publish articles, blog posts, and my thoughts and opinions

## Table of Contents
* [How it works](#how-it-works)
* [Features](#features)
* [Technoliges Used](#technologies-used)
* [Deployed URL](#deployed-url)

## How it works:

- When the user click login, Login or Signup option will appear
- Once the user is logged in, logout button will appear instead of login 
- User can create a new post as well as view all the posts they created by clicking dashboard on top
- User can leave a comment
- User can edit a post


## Features:
- User accounts with authentication
- dynamic generation of content using javascript and sequelize

## Technologies Used:
1. Sequelize
### Example:
```javascript
id: {
    type: DataTypes.INTEGER,
    allowNull: false,
    primaryKey: true,
    autoIncrement: true
},
username: {
    type: DataTypes.STRING,
    allowNull: false
},
email: {
    type: DataTypes.STRING,
    allowNull: false,
    unique: true,
    validate: {
    isEmail: true
    }
},
password: {
    type: DataTypes.STRING,
    allowNull: false,
    validate: {
    len: [4]
    }
}
```

2. Handlebars
### Example:
```javascript
<ol class="post-list">
  {{#each posts as |post|}}
  <li>
    {{> post-info post }}
  </li>
  {{/each}}
</ol>
```

## Deployed URL
https://cms-style-tech-blog.herokuapp.com/

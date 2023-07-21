# Module 8 Lab - Databases

## MongoDB

**Assignment:** Design a Logical and Physical Model for a general Blogging application.

> Requirements:
> * The system should have a User Model (should store basic user related keys)
> * The users should be able to create multiple posts (Post should be very basic with Title, description and image)
> * Other users should be able to like the posts and comment on the posts.

**Answer:** 

* Created new database using: `use socialApplication`
* Created 3 collections on the store (using `db.collectionName.insertOne({Params here})`)
    - interactions
    - posts
    - users
* Params for each Collection: 
    - interactions: `'_id', 'received_likes'`
    - posts: `'_id', 'title'`
    - users: `'_id', 'name'`

----------

## MySQL

* Created new database using: `CREATE DATABASE bloggingApplication;`
* Accessed database: `use bloggingApplication`
* Created 4 tables on the store with the following columns: 
    * createdPosts
        - Field: `userID` (Type: int)
        - Field: `dateCreated` (Type: date)
        - Field: `title` (Type: varchar(1000))
        - Field: `description` (Type: varchar(10000))
        - Field: `url` (Type: varchar(1000))
        - Field: `id` (Type: int)

    * postComments
        - Field: `postID` (Type: int)
        - Field: `userID` (Type: int)
        - Field: `comment` (Type: varchar(5000))
        - Field: `commentedAt` (Type: date)

    * postLikes
        - Field: `postID` (Type: int)
        - Field: `userID` (Type: int)
        - Field: `likedAt` (Type: date)

    * users
        - Field: `id` (Type: int)
        - Field: `firstName` (Type: varchar(50))
        - Field: `lastName` (Type: varchar(50))
        - Field: `passwordHash` (Type: varchar(500))


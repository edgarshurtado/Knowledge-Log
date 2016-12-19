## Import a database from json
`mongoimport -d <database-name> -c <collection-name> file.json`

## Use sql or nosql database
In general [nosql databases are faster than sql](http://macool.me/mysql-vs-postgresql-vs-mongodb-velocidad/04)
this is its strenth over sql for applications where you have to manage a lot of
data.

Despite of this, when the transactions are too complex and implies operations
with several tables and such, as [the MongoDB, Inc. recognizes.](https://www.mongodb.com/compare/mongodb-mysql)
 
Moreover, when the consistency of the data is more important than speed
of operation, sql could be more adequate.

In any case, something we could be forgetting when deciding the DB for our 
next application is that we could just use both.


## Interesting Blog Posts
[6 rules of thumb for MongoDB schema](http://blog.mongodb.org/post/87200945828/6-rules-of-thumb-for-mongodb-schema-design-part-1?_ga=1.45156708.1749185560.1463620081)

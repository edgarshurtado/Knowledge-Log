## Delete rows with duplicated field

```mysql
DELETE n1 
    FROM names n1, names n2 
    WHERE n1.id > n2.id AND n1.name = n2.name
```

[source](http://stackoverflow.com/a/5016434)

## Some thoughts about eficiency
There are some operations that are faster in mysql than by code
[source](http://www.onextrapixel.com/2010/06/23/mysql-has-functions-part-5-php-vs-mysql-performance/):

* Calculating average and counting rows
* Formating dates
* Habiliting the cache makes operations even faster

However the operations with individual values seems to be very poorly optimized
and such operation are better performed in code.
[source](http://stackoverflow.com/a/6449162)

The thing is that too much code on the db obtuses the logic of the application
and is up to the programmer to have a balance between speed and clarity.

## Check the mysql version

Execute the following sentence:

```mysql
SHOW VARIABLES LIKE `version`
```

## Use of indexes

[Mysql: Índices y optimización de consultas](https://www.dimensis.com/consejos-1-1.html) (Spanish)

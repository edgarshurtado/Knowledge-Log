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

### Create an Index

```mysql
CREATE INDEX index_name ON table_name (colum_name [,colum_name_2 ...])
```

### Drop an index

```mysql
DROP INDEX index_name FROM table_name
```

### SHOW table indexes

```mysql
SHOW INDEXES FROM table_name;

SHOW INDEXES FROM table_name FROM db_name;

SHOW INDEXES FROM db_name.table_name;
```

### Some considerations

* Execute the explain comand for seeing the index used by a query
* Every query can use just one index
* Beware when you have an application which makes a lot of writes cause the indexes will make this 
operation to slow down.

## MySQL CACHE

### Considerations about mysql cache
* Every create/update/delate action into the db will flush the cache related with the table that has been modified

### Delete CACHE

`SQL_NO_CACHE` avoids the save of the results in cache, however if the sentence was already in cache
it will be used anyway. To force Mysql to not use cache we can configure the server to do so or reset
manually the cache with:

```mysql
RESET QUERY CACHE;
```


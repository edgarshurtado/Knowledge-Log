## Activate XDEBUG

Add to php.ini the following lines of code

```
;#### XDEBUG #####
;# Activate

extension=php_xdebug.dll

;# Coding
xdebug.var_display_max_depth = 8

xdebug.var_display_max_children = -1

xdebug.var_display_max_data = -1
```

this will var_dump variables nicely formated.

> Tip by my co-worker Cristian Trave

## Avoid timelimit

### from .htaccess

```
php_value max_execution_time 1200
```

### from php.ini

```
max_execution_time=1200
```

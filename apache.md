## Activate XDEBUG

Add to php.ini the following lines of code

```
;#### XDEBUG #####



;# Activate

extension=php_xdebug.dll



;# Condig

xdebug.var_display_max_depth = 8

xdebug.var_display_max_children = -1

xdebug.var_display_max_data = -1
```

this will var_dump variables nicely formated.

> Tip by my co-worker Cristian Trave
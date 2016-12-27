## Write url
```html
<a href="{{ path('name') }}">Home</a>
```

## Filters

### String modifications

#### replace

Searchs and replace a substring from the given string.

##### Usage
 ```twig
 {{"Hello. How Are You?"|replace({"." : ","})}}

 {# Output: "Hello, How Are You?" #}
 ```

 > The mapping object is needed.

#### upper and lower

Converts the string to uppercase or lowercase depending on which one is used

### length

### trim

Removes characters from both ends of a string

## Check if a variable is defined
```
{% if foo is defined %}
    ...
{% endif %}
```

works for variables and attributes

[resource](http://twig.sensiolabs.org/doc/tests/defined.html)


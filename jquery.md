## jQuery datepicker

Once a datepicker has been inicialized we can't re-set its options dinamically.
So if we want to change the options of an already inicialized datepicker we
have to remove it first as following:

```javascript
    $('.datepicker').datepicker("destroy");
    $('.datepicker').datepicker({
        // New datepicker configuration
    });

```


## Replace a dom element with another

```javascript
    $('#dom-element').replaceWith($domElement);
```

> $domElement accepts an html string or jQuery element


## jQuery multiselect
[url plugin](http://www.erichynds.com/blog/jquery-ui-multiselect-widget)
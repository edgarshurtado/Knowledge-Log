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

## jQuery Datatable

### manual search

When we want a search box placed somewhere else

```js
    var dTable = (function(idDataTable, idSearchBox, assetTranslation){

        var dTableConfig = {
            "language": {
                // Url to load the file for translation
                "url" : assetTraduccion,
                // Select the elements to show. Here we've hidden the search box
                "sDom" : "lrtip"
            }
        }

       var dTable = $(idDataTable).DataTable(dTableConfig);


       $(idSearchBox).keyup(function(event){
        dTable.search($(this).val()).draw();
       });

       // Logic to show the table once it has been rendered
       dTable.on("draw", function(){
           $(idDataTable).show();
           // We only need the handler once
           dTable.off("draw");
       });

       return dTable;

    })(
        idDataTable,
        idSearchBox,
        assetTranslation
    );
```

### Inyect dom elements

Just type on the "sDom" property the dom element as follows

```js
$(document).ready( function() {
  $('#example').dataTable( {
      "sDom": '<"top"i>rt<"bottom"flp><"clear">'
  } );
} );
```

This code will create a div with the "clear" class. Furthermore, it will add the class
"top" to the i element and "bottom to f, l and p

## Know if an object has a property

```js
if(typeof obj.prop == 'undefined'){
    // do something...
}
```

> This way it returns true either if the property doesn't exist or is set
to 'undefined'

[resource](http://stackoverflow.com/a/2281671)


## Create variables within a scope and avoid collisions

I encountered this issue while programming

```js
(function printWidget(){
    $triggerButton = $("#fistDiv .btn");
    text = "this is the first div";

    $triggerButton.click(function(e){
        e.preventDefault();
        console.log($widget);
    });
})();

(function printWidget(){
    $triggerButton = $("#secondDiv .btn");
    text = "this is the second div";

    $triggerButton.click(function(e){
        e.preventDefault();
        console.log($widget);
    });
})();

$("#firstDiv .btn").trigger("click"); // this is the second div
$("#secondDiv .btn").trigger("click"); // this is the second div
```

The solution: define and assign instead of just assign

```js
(function printWidget(){
    var $triggerButton = $("#fistDiv .btn");
    var text = "this is the first div";

    $triggerButton.click(function(e){
        e.preventDefault();
        console.log($widget);
    });
})();

(function printWidget(){
    var $triggerButton = $("#secondDiv .btn");
    var text = "this is the second div";

    $triggerButton.click(function(e){
        e.preventDefault();
        console.log($widget);
    });
})();

$("#firstDiv .btn").trigger("click"); // this is the first div
$("#secondDiv .btn").trigger("click"); // this is the second div
```

Reason: As I didn't define the variables, they were being assigned to the
global scope, hence, they were being overwritten in the second IIFE

More information in YDKJS

## Useful Libraries
* fullPage.js -> Library for smooth scroll to section [web page](http://alvarotrigo.com/fullPage/#firstPage)

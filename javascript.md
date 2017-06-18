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

## Console methods

* console.log
* console.info
* console.warn
* console.error
* console.assert
* console.dir
* console.group (console.groupEnd)
* console.table
* console.time (console.timeEnd)

For know more about those methods check [this blog post](https://medium.freecodecamp.com/how-to-get-the-most-out-of-the-javascript-console-b57ca9db3e6d)



## Useful Libraries
* fullPage.js -> Library for smooth scroll to section [web page](http://alvarotrigo.com/fullPage/#firstPage)

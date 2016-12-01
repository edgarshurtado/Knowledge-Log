## Select DOM elements
Even though we didn't have the jQuery library at the project. We can use the
jQuery method for selecting DOM elements:

```js
$(".class");
$("#id");

// and so forth.  
```

## Control time

```js
console.time('myTime'); //Starts the timer with label - myTime

// Some logic

console.timeEnd('myTime'); //Ends the timer with Label - myTime

//Output: myTime:123.00 ms
```


## Clear the console cache

Type at the chrome console:

```js
clear();
```

## List a DOM element's eventListeners 
```js
getEventListener($(cssSelector));
```


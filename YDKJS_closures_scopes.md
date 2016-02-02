# Chapter 1. What is Scope?

* State : In computer science and automata theory, the state of a digital logic
circuit or computer program is a technical term for **all the stored
information**, at a given instant in time, to which the circuit or program has access 
[wikipedia](https://en.wikipedia.org/wiki/State_(computer_science))

* LHS (Left-hand side) references are for assign values to a variable
    - If it's not found the reference, in non-strict mode the Engine will create
one in the outter scope.
* RHS (Right-hand side) references are for check the value of a variable
    - Throws `ReferenceError`

# Chapter 2. Lexical Scope
* stateful -> an application that conserves the state
* stateless -> an aplication which doesn't conserve the state
* Avoid changing the scope in runtime
    - Do not use eval or with:
        - *val* modifies a lexical scope
        - *with* creates a new scope for the object passed using it as identifier.
    - Reason: Optimization during compilation can't be done if there's some val
or with in the code.

# Chapter 3. Function vs. Block Scope.
* function-expression: functions that are automatically executed and that its
name is just accesible inside the function scope, which means that the name of
the function doesn't *pollute* the global scope.

```javascript
(function foo(){ // <-- insert this

    var a = 3;
    console.log( a  ); // 3

 })(); // <-- and this
```
* block-scope: The following keywords let us difine blocks {...} as scopes:
    - with
    - try/catch: the error asigned to catch is only available to the catch block
    - let: defining a variable with let makes it only available in its block. A
practice for making sure of this is as follows

```javascript

var foo = true;

if (foo) {
    { // <-- explicit block
        let bar = foo * 2;
        bar = something( bar  );
        console.log( bar  );
     }

}

console.log( bar  ); // ReferenceError
```

A big advantage for using blocks is letting the garbage collector get rid of
variables isn't going to need anymore:

```javascript
function process(data) {
    // do something interesting

}

var someReallyBigData = { ..  };

process( someReallyBigData  );

var btn = document.getElementById( "my_button"  );

btn.addEventListener( "click", function click(evt){
    console.log("button clicked");

}, /*capturingPhase=*/false  );
```
> it's quite likely (though implementation dependent) that the JS engine will still have to keep the structure around, since the click function has a closure over the entire scope. To solve this: 

```javascript
function process(data) {
    // do something interesting
}

// anything declared inside this block can go away after!
{
    let someReallyBigData = { .. };

    process( someReallyBigData );
}

var btn = document.getElementById( "my_button" );

btn.addEventListener( "click", function click(evt){
    console.log("button clicked");
}, /*capturingPhase=*/false );
```

# Chapter 4: Hoisting
* The JavaScript Engine first makes the declarations and after the assigments. 
The "rearrenge" the Engine makes is called **Hoisting**
* Function definitions `function foo(){...}` are hoisted but function expressions
`var foo = function(){...}` are not.

# Chapter 5: Scope closure
 > There's a special behavior defined for let declarations used in the head of a for-loop. This behavior says that the variable will be declared not just once for the loop, but each iteration. And, it will, helpfully, be initialized at each subsequent iteration with the value from the end of the previous iteration.

* Example of creating modules in diferent files:

**bar.js**

```js
function hello(who) {
    return "Let me introduce: " + who;

}

export hello;
```

**foo.js**

```js
// import only `hello()` from the "bar" module
import hello from "bar";

var hungry = "hippo";

function awesome() {
    console.log(
        hello( hungry  ).toUpperCase()
    
            );

}
export awesome;
```

```js
// import the entire "foo" and "bar" modules
module foo from "foo";
module bar from "bar";

console.log(
    bar.hello( "rhino"  )

        ); // Let me introduce: rhino

foo.awesome(); // LET ME INTRODUCE: HIPPO
```


# Vocabulary
* quirks -> peculiaridades
* fliquering -> parpadenate
* appeal -> gustar/atraer
* nuance -> matiz/tonalidad
* eschew -> evitar
* beget -> engendrar
* albeit -> no obstante/sin embargo
* mire in -> quedar atrapado
* cast -> reparto
* look-up -> búsqueda
* glib -> simplista
* frowned upon -> desaprobado/a
* wreak -> causar
* havoc -> caos
* strive -> esforzarse
* tease -> burlar/molestar

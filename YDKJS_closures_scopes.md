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

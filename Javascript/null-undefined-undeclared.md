Variable states for Javascript -

- Undeclared - it's not in the current scope at all.
- Undefined - The variable has been defined, but there is no value set on it
- Null - You have to set this yourself - JS will never do this for you! From the spec - primitive value that represents the intentional absence of any object value. Note the 'intentional' word there.

- 'Set' - it's been set to one of the many JS primitive types, such as string, boolean, or number, or is an object/list/array of some sorts. These values can still be 'pseudo empty' such as a '' or '0', but that's beside the point. They aren't any of the value types above.

```
console.log(x)

-> ReferenceError: x is not defined

//******

var x;
console.log(x)
-> undefined

//******

var x = null;
console.log(x)
-> null

```

Bonus - while it's still dense and a little hard to read, I'd recommend poking your head at the ECMAScript standard for fun sometime. It's the bible to which Javascript and all web browses have to follow!

https://www.ecma-international.org/ecma-262/10.0/index.html#sec-intro

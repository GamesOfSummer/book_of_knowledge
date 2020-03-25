

## React Conf 2018
### tl;dr - classes are bad

Sophie Alpert

```
Classes have a ton of boilerplate. Get bloated.

THe lifecycle events get repepitive - onmount, unmount, did update - all have logic for handling subscribe. Gets confusing.

Harder for the compiler to optimize the code via builds. Classes can even have unused methods and the minified code will still have it because it can't tell what is being used.

Classes make hot reloading hard.
```

Dan Abramov
```
Wanted to solve all 3 problems -

* wrapper hell
* huge components
* confusing classes

*these are 3 symptoms of one problem*
```


Problem - react didn't have a simpler stateful primitive than a class compoent

They did use mixins for a while. Mixins are considered harmful. THey tend to make problems worse.

Hooks are optional and opt-in only. No breaking changes.

`useState` - What if I could just use state from a function component? Thus, `useState` was born. No more `this` and no more `this.setState`. Simpler. Local variables.

**Gotcha** - Hooks must be called at top level. Never in a conditional.

`useEffect` - handle a side effect that a lifecycle method would handle. Runs at start and after every update. Can remove need for `componentDidMount` and `compoenentUpdate` 

Again - you can use classes and hooks side by side. No breaking changes. Did not deprecate classes. Can test the hooks separately.

React sidenote - Compoents are like atoms, in matter. Hooks let you get into the 'electrons' of the atom - hiding in plain sight!
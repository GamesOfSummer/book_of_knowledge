## tl;dr - classes are bad

```
Sophie Alpert

Classes have a ton of boilerplate. Get bloated.

THe lifecycle events get repepitive - onmount, unmount, did update - all have logic for handling subscribe. Gets confusing.

Harder for the compiler to optimize the code via builds. Classes can even have unused methods and the minified code will still have it because it can't tell what is being used.

Classes make hot reloading hard.
```

Dan Abramov

Wanted to solve all 3 problems -

* wrapper hell
* huge components
* confusing classes

these are 3 symptons of one problem

problem - react didn't have a simpler stateful primitive than a class compoent

They did use mixins for a while. Mixins are consideres harmful. THey tend to make problems worse.


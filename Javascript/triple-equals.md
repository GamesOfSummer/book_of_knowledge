# Triple equals checks for both value AND type.

However, it does have two cases where it won't report correctly - namely, the NaN and -0.

- Nan === Nan will evaulate false (wrong)
- -0 === 0 will evaluate true (wrong)

### NaN - stands for 'not a number' - an invalid number.

From the Mozilla MSDN -

There are five different types of operations that return NaN:

    * Number cannot be parsed (e.g. parseInt("blabla") or Number(undefined))
    * Math operation where the result is not a real number (e.g. Math.sqrt(-1))
    * Operand of an argument is NaN (e.g. 7 ** NaN)
    * Indeterminate form (e.g. 0 * Infinity)
    * Any operation that involves a string and is not an addition operation (e.g. "foo" / 3)

You can check for if your value is NaN by isNan(value) OR, the really slick way - if NaN === NaN returns false. NaN will never equal itself, so you can detect for it that way!

And the other gotcha is -0, a signed 0. -0 === -0 will evaluate correctly, but -0 === 0 will NOT. So you have to check for it. You can do so via x === 0 && 1 / x === -Infinity. Yes, -Infinity is part of the JS language - it was new to me, too!

The Object.is method (basically, from the ES6 standards), which handles for these edge cases -

```
value: function(x, y) {
      if (x === y) {
        // 0 === -0, but they are not identical
        return x !== 0 || 1 / x === 1 / y;
      }

      // NaN !== NaN, but they are identical.
      // NaNs are the only non-reflexive value, i.e., if x !== x,
      // then x is a NaN.
      // isNaN is broken: it converts its argument to number, so
      // isNaN("foo") => true
      return x !== x && y !== y;
    }
```

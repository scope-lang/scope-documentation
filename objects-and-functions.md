Objects
===
Objects are like JS objects.

However any object _can_ be made into a function

An object which has the `action` property set becomes a function.

`action` is a block + ref map combo:

```
o.action = (a, b)::{
  a + b
};
```

or

```
o.action = inputmap::{
  x * y
};
```


`inputmap` can either be a reference map literal such as `(x,y)` or a function that returns a reference map.


Note:
-
Reference map literals also appear when assigning multiple variables at once:
`(x, y) <- [10, 21]`


Functions
===

Functions can also be defined as:
```
var f = (x)::{
  x * x + 2 * x + 1
};
```

these objects/functions when called use the object properties like
Javascript's
Function.prototype.thingy
syntax.

Function Prototypes
===

```
var f={m:1,b:2};
f.action=(x)::{
  return this.m*x+this.b;
};
print(f(10));//outputs 1*10+2=12
```

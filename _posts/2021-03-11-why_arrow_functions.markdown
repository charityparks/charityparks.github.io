---
layout: post
title:      "Why Arrow Functions?"
date:       2021-03-12 00:43:35 +0000
permalink:  why_arrow_functions
---

Arrow functions were introduced in ES6.  They are clean, look more appealing than regular functions, and use less keystrokes (shorter code).  They also get rid of the 'function' keyword and the 'return' keyword. 

For example, here is a regular function:

```
hello = function() {
  return "Hello World!";
}
```

Here is the same thing using an arrow function:

`hello = () => "Hello World!";`


Arrow functions are the shiny new toy so enjoy!  Let's face it, they are FUN! 

In addition to the awesome syntax, arrow functions get rid of the use of the bind method that is needed in regular functions to maintain the context of 'this'. If a regular function didn't use the bind method, then 'this' would be undefined throwing an error. 

Arrow Functions don't redefine the value of this with their function body. 'This' is resolved lexically, and that is one of the great features. The 'this' value inside an arrow function always equals the 'this' value from the outer (parent) function. In other words arrow functions inherit 'this' from the parent scope. This makes things more predictable and prone to less bugs.


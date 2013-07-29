What is this
===========

Notes on the characteristics of the Javascript language as I learn from "The secrets of the Javascript Ninja" by John Resig


Functions
===========
What's different about functions, coming from other world: function scope, what is *this* , anonymous functions, closure, apply, call

1. First-class objects
  - Can be assigned to variables
  - Passed as arguments to functions
  - Returned as a function
  - Can possess properties that can be dynamically created and assigned

2. Functions and variables Scope
  - Variable declarations are _thoroughly_ in scope from their point of declaration to the end of the *function* within which they’re declared, regardless of block nesting.
  - *hoisted* : functions scope can be fast forward. E.g inside a function *outter()*, if *innerHoistedFunc()* is defined at the end of foo, it is still OK for foo to call *innerHoistedFunc()* right at beginning of foo()'s definition

3. "Physical" anatomy of a function    
  - *arguments* : Contains the arguments. It behaves exactly as an array (such as *arguments.length* and *arguments.shift()*, but internally not a JS array
  - *this* : the context of the function when it is *invoked*, not when it is *defined* . See function invocation
  - *name* : which is the literal string of function name. For anon functions, this is '' (empty string). Console.log(myfunc.name)
   
    
4. Some other characteristics
  - 2 types: named functions vs anonymous functions (a.k.a *lambda* sometimes)
  - Every named function foo creates a *window.foo reference*
  - Arguments passed can be redundant, ie. more than the number of actuall arguments declared.


5. Function invocation
  - Functions can be invoked in 4 different ways
    - bar() : function
    - foo.bar() : method
    - apply
    - call


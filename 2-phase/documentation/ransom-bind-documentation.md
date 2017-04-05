# .bind()

#### Not that $(something).bind()

There was a jQuery `.bind()` method to "Attach a handler to an event for the elements."

It has been deprecated and replaced by `.on()`.

[jQuery documentation for .bind()](http://api.jquery.com/bind/)

### Bind What?

Bind a ('this') context to a function.

### Bind Why?

One of the fun things about javascript is that you can pass functions around
without evaluating them until you are ready. However, you might not be sure what
context the function is eventually going to be evaluated in. If the function uses
'this' then that 'this' will be different depending on where it is evaluated, which
may or may not be what you want.

If it is not what you want, then you can bind a particular 'this' to it while it
is still in the correct context.

Bind will also let you apply specific arguments to use when evaluating.

### Bind How?

'var functionToEvaluateLater = someFunction.bind(this)'

and then later...

'someFunction()'


### Links

 - [MDN Function.prototype.bind()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/bind)
 - [Apply vs. Call vs. Bind in JavaScript](https://codeplanet.io/javascript-apply-vs-call-vs-bind/)
 - [Javascript Bind](https://learn.co/lessons/javascript-bind)

# CSS Inheritance

### Natalie Yip


### Inheritance Overview

Inheritance is the process by which the value of certain CSS properties applied to an element get passed down to all elements nested within it. Inheritance relies on the document tree, which is the hierarchy of (X)HTML elements in a page based on nesting. You can think of it similar to global and local scope in Ruby. If I declare something in the local scope, any global or ancestral scopes would not have access to it. But if I declare something in global scope, then local scope can access it. But instead of scopes they are referred to parent, child, and sibling elements. 

```html
html { # like global scope
  font-family: sans-serif;
}

/* 
# This would be unneccesary↷
p { 
  font-family: sans-serif;
}
*/

```

```html
html { #like global scope, so font-family: sans serif is available to p
  font-family: sans-serif;
}

p { #like local scope so line-height would not be available to html
  line-height: 1.5;
}

```

###Inherit Keyword

Some types of properties are not inherited by default, and some elements do not inherit some properties. With properties you can force to inherit by using the inherit value. With elements you can also manipulate it despite its default browser styles. 

The inherit keyword specifies that a property should inherit its value from its parent element.
One of the situations where you would want to use inherit to enforce a value that’s automatically inherited is when the inherited value is overridden by the user agent’s style sheet (default styles applied by the browser to some elements.

```html
<body style=“font-size: 12rem;”>
  <div class=“child></div>
  <section style=“font-size: 15rem;”><div class=“child></div> </section>
</body>

div.child {
  font-size: inherit;
}
```
```html
* {
  font-family: inherit;
  line-height: inherit;
  color: inherit;
}

html {
  font-size: 125%;
  font-family: sans-serif;
  line-height: 1.5;
  color: #222;
}
```

###Why Inheritance is awesome? 
- Allows for developers to write less CSS 
- Permits users to view faster-loading pages 

### Links
- [Inheritance Cheatsheet](http://srjcstaff.santarosa.edu/~tfleming/htmlb/CSS_Cheat_Sheet_Inheritance_Cascade_Specificity.pdf)
- [Property Table Overview](https://www.w3.org/TR/CSS21/propidx.html)

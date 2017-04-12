## Canvas

### Natalie Yip

###Canvas Overview
<canvas> is an HTML element used to draw graphics by using scripting, generally Javascript. Here is a list of a few things you can do with canvas: 
- draw text
- draw shapes
- animate
- create gradient
- be interactive and respond to JS events

## Canvas Example Syntax
The <canvas> element must have an id attribute so it can be referred to by JavaScript.
The width and height attribute is necessary to define the size of the canvas.

<canvas id="myCanvas" width="200" height="100"></canvas>

var canvas = document.getElementById('myCanvas');

The <canvas> element has a method called getContext(), used to obtain the rendering context and its drawing functions. getContext() takes one parameter, the type of context. Tutorials usually focus on 2d rendering context, but other contexts may provide different types of rendering.

var ctx = canvas.getContext('2d');

Now that you have your context variable, you can start playing around with it! 

Here's how you would obtain a red rectangle! 

ctx.fill


## LINKS 
[Canvas Cheat Sheet](http://cheatsheetworld.com/programming/html5-canvas-cheat-sheet/)
[Canvas Doc](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D)
[Canvas Inspiration](https://code.tutsplus.com/articles/21-ridiculously-impressive-html5-canvas-experiments--net-14210)
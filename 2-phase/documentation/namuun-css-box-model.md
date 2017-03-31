# CSS Box Model

### What is a CSS Box Model? 

Every element on a page is a rectangular box. 
The **box model** is a term used to define how a box and its attributes relate to each other. Useful in the layout and design of your web application.

![Box-model](https://github.com/bootcoder/frog-talks/blob/namuun-css-box-model/2-phase/documentation/box-model.png)

Main parts:
- **Margin** transparent, clears the area outside the border
- **Border** goes around the padding and content
- **Padding** transparent, clears an area around the content
- **Content** where text and images appear

### How is the size of the box calculated?

When you define a width and a height for your box using CSS, you are defining not the entire area taken up by the content, padding, border and margin. You are actually just defining the content area itself - the bit right in the middle. The padding, border and margin must be added to that in order to calculate the total space occupied by the box.

#### Width:
width + padding-left + padding-right + border-left + border-right

#### Height:
height + padding-top + padding-bottom + border-top + border-bottom

### Debug your layout

```
* {
  outline: 1px solid red; 
}
```

### References

-[W3 CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp)

-[Wikipedia](https://en.wikipedia.org/wiki/CSS_box_model)

-[CSS Tricks](https://css-tricks.com/the-css-box-model/)

### Very useful links

-[Pesticide.io](http://pesticide.io/)
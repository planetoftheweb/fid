<!-- .slide: data-state="title" -->

# Advanced CSS Layouts

---

## Media Queries
- Layouts depending on properties
- `media` attribute
```
<link rel='stylesheet' media='screen and (min-width: 701px)' href='css/mediumsize.css' />
```
- [`@media`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media) selector

<iframe class="fragment" height='400' scrolling='no' title='media queries' src='//codepen.io/planetoftheweb/embed/WMzPLM/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/WMzPLM/'>media queries</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Media queries allow you to use certain styles depending on certain device properties. There are two ways to control this. First, you can add a media property that will load depending on, for example, the size of the device.

You can also use a @media selector in your CSS to control an individual element or a group of elements.

<iframe class="fragment" height='400' scrolling='no' title='media queries' src='//codepen.io/planetoftheweb/embed/WMzPLM/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/WMzPLM/'>media queries</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Media Types/Features
- `all`, `screen`, `print`, `speech`
- features: `width`, `height` <br>`orientation`, `resolution`, etc. 
- operators: `and`, `not`

<iframe class="fragment" height='400' scrolling='no' title='media queries-types features' src='//codepen.io/planetoftheweb/embed/zRWbNx/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/zRWbNx/'>media queries-types features</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

You can control where these features apply. For example, you can control wether stylesheets apply only when printing or to screens.

There are a number of features that you can check for, but the most common are width or height, which are almost always expressed with minimum or maximum parameters.

```
body {
  background: red;
}

@media all and (min-width: 701px) {
  body {
    background: yellow;
  }
}
```

---
<!-- .slide: data-state="title" -->

# Flexbox

---

## Introducing Flexbox
- One  of many [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout) properties
- One dimensional layouts
- [Backwards compatible](https://caniuse.com/#feat=flexbox)

### Author Notes

Flexbox, of course, is one of the many display properties. There are so many available that it's hard to go over all of them. 

Flexbox is perfect for handling simpler, two dimensional layouts. There is anoteher property for more complex two dimensional layouts called [grid](https://developer.mozilla.org/en-US/docs/Web/CSS/Grid), but it doesn't have very good [browser support](https://caniuse.com/#search=grid), so we won't be covering it in this class yet.

Flexbox has great compatibility with older browsers, although some older browsers require that you write flexbox in multiple ways, which is usually handled with processors that can take care of the conversion.

---

## Container vs Items
- Control `containers`
- Customize `items`
- Direction agnostic

<iframe class="fragment" height='400' scrolling='no' title='Display Flex' src='//codepen.io/planetoftheweb/embed/BYrvWg/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/BYrvWg/'>Display Flex</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


### Author Notes

The main power that flexbox gives you is the ability of a container to modify the width and height of it's items to fit the available space.

You can then customize the placement of individual items if you wnat to. However, most of the time, the main container will be the target that will take care of what you need.

Flexbox is direction agnostic. Whereas block is vertically based and inline horizontally based, flexbox can be rearranged to display elements horizontally or vertically as needed with just a few simple classes.

---

## Container vs Items
- Control `containers`
- Customize `items`
- Direction agnostic

<iframe class="fragment" height='400' scrolling='no' title='Display Flex' src='//codepen.io/planetoftheweb/embed/BYrvWg/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/BYrvWg/'>Display Flex</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


### Author Notes

The main power that flexbox gives you is the ability of a container to modify the width and height of it's items to fit the available space.

You can then customize the placement of individual items if you wnat to. However, most of the time, the main container will be the target that will take care of what you need.

Flexbox is direction agnostic. Whereas block is vertically based and inline horizontally based, flexbox can be rearranged to display elements horizontally or vertically as needed with just a few simple classes.

---

## Controlling Direction

- `flex-direction` property
-  Values: `row`
    `row-reverse`
    `column`
    `column-reverse`

- Great with `@media` rules

<iframe class="fragment" height='400' scrolling='no' title='flex controlling direction' src='//codepen.io/planetoftheweb/embed/MQVLQB/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/MQVLQB/'>flex controlling direction</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

You can easily control wether elements inside the container display as rows or columns with this property. The default is row. It works super well with media queries to allow you to do this conditionally.

---

## Wrapping

- `flex-wrap` property
-  Values: `nowrap` `wrap` `wrap-reverse`
- `flex-flow: row nowrap;` combo

<iframe class="fragment" height='400' scrolling='no' title='flex Controlling Wrapping' src='//codepen.io/planetoftheweb/embed/ZrxPgQ/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/ZrxPgQ/'>flex Controlling Wrapping</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Flexbox by default will try to fit the items in the container, even if the items get big. You can change this behavior by using the `flex-wrap` property. This will make items continue on a separate line once they fill up the horizontal space.

---

## Justification

- `justify-content` property
-  Values:   `flex-start` `flex-end` `center`<br>`space-between` `space-around` `space-evenly`

<iframe class="fragment" height='400' scrolling='no' title='Flexbox Justify' src='//codepen.io/planetoftheweb/embed/eVMozB/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/eVMozB/'>Flexbox Justify</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Justify content lets you lets you control the horizontal alignment or justification of elements inside the container. It makes it incredibly simple to center or spread out elements inside a container.


---

## Justify Content Vertically

- `align-items` property
-  Values: `flex-start` `flex-end` `center`<br>`baseline` `stretch`

<iframe class="fragment" height='400' scrolling='no' title='Flexbox Vertical Alignment' src='//codepen.io/planetoftheweb/embed/XZEQRR/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/XZEQRR/'>Flexbox Vertical Alignment</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Although this property is called align elements, it's easier if you think about it as vertical justification. A lot of the same properties as horizontal justification. This makes flexbox the easiest way to center something vertically.

---

## Aligning Content Vertically

- `align-content` property
- `flex-start` `flex-end` `center`<br>`space-between` `space-around` `stretch`
- More than one line

<iframe class="fragment" height='400' scrolling='no' title='Aligning Content Vertically' src='//codepen.io/planetoftheweb/embed/OQvGQK/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/OQvGQK/'>Aligning Content Vertically</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Whenever you have more than one line worth of elements and a big vertical area to fill, this will help you position those elements vertically.  This makes flexbox the easiest way to align multiple elements.

---
<!-- .slide: data-state="title" -->

# Flexbox: Individual Items

---

## Order

- `order` property
- Numbers `grouped` together

<iframe class="fragment" height='400' scrolling='no' title='Individual Order' src='//codepen.io/planetoftheweb/embed/MQVdbQ/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/MQVdbQ/'>Individual Order</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


### Author Notes

You can order elements individually. The order is a number you can assign that allows you to group elements within that order. Think of it as layers. Any group you assign as group 5 will be grouped together.

---

## Grow Proportionally

- `flex-grow`, `flex-shrink`, `flex-basis`
- Set up proportions

<iframe class="fragment" height='400' scrolling='no' title='Individual Order' src='//codepen.io/planetoftheweb/embed/oEqRBr/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/oEqRBr/'>Individual Order</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

When you need to control how an element grows in relationship with other elements you can use these different properties.

---

## Individual Vertical Position

- `align-self` property
-  `auto` `flex-start` `flex-end`<br>`center` `baseline` `stretch`
- Assign to individual items.

<iframe class="fragment" height='400' scrolling='no' title='Flexbox: Individual Vertical Position' src='//codepen.io/planetoftheweb/embed/NyYVYv/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/NyYVYv/'>Flexbox: Individual Vertical Position</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Use these if you want to align something vertically separately from the rest of the group.
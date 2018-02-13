<!-- .slide: data-state="title" -->

# Basic CSS Layout

---

## Margin Layout
- Using [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
- Setting to auto

<iframe class="fragment" height='400' scrolling='no' title='Setting Margin to Auto' src='//codepen.io/planetoftheweb/embed/EQmvQZ/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/EQmvQZ/'>Setting Margin to Auto</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes
Margins can be useful for layout in some instances. When you have a block element inside another block element, and the element on the inside has a width assigned to it, you can specify a value of `auto` as one of the values for each side (see example above).

This doesn't always work the way you want it to because sometimes we don't want to sepecify the size of the inside elements, we might want those to have variable widths. The typical example is when we're trying to build navigation with this trick. We'll take at the issues with that example next.

---

## Inline Block Elements
- [`inline-block`](https://developer.mozilla.org/en-US/docs/Web/CSS/display) elements

<iframe class="fragment" height='400' scrolling='no' title='inline-block' src='//codepen.io/planetoftheweb/embed/MQvoYv/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/MQvoYv/'>inline-block</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>
### Author Notes

Inline elements aren't allowed width, but `inline-block` elements can, so that's one way we can do a centered navigation is by using inline block as long as we don't have carriage returns in between these elements because those display as spaces in between inline-block elements.

You can use the text-align property with inline-block elements, so that makes it easy to center elements, but it's not always practical.

---

## Floating Elements
- [`float`](https://developer.mozilla.org/en-US/docs/Web/CSS/float)
- `left` `right` `none` `auto`
- `inline` or `block` elements

<iframe class="fragment" height='400' scrolling='no' title='Floating items' src='//codepen.io/planetoftheweb/embed/KQmZpY/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/KQmZpY/'>Floating items</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

When you float an element, you are asking CSS that an element should be placed on one or the other side of it's container. It's traditionally used to place an image to the left or right of another element.

You can float one or more elements and choose the side that you're floating to.

---

## Fixing Floating Issues
- Embedded elements
- `clearfix` trick

<iframe class="fragment" height='400' scrolling='no' title='Clearing Floats' src='//codepen.io/planetoftheweb/embed/JpyEdm/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/JpyEdm/'>Clearing Floats</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


### Author Notes

When you float an element that is inside another element. The parent no longer includes the element as part of it's content. So it's possible that the element appear overlaps the container. It's not a bug, it's just the way CSS works.

In order to fix that, we can use a trick called a clearfix, that fixes this. To do this it creates a piece of content after the current element that clears the floats (see example) 

---

## Showing and Hiding Elements

- [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- [`opacity`](https://developer.mozilla.org/en-US/docs/Web/CSS/opacity)
- Playing with `:hover`

<iframe class="fragment" height='400' scrolling='no' title='display vs opacity' src='//codepen.io/planetoftheweb/embed/PQKWEz/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/PQKWEz/'>display vs opacity</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

There are two ways to show or hide elements on your page and they behave slightly differently. First, the display property can have a value of none. This takes the element out of where it would be displayed and hides it. So the space that the element would take would not be there.

The other way to hide an element is with the opacity property. With opacity, you can choose a value between 0 and 1, where .5 would be 50%. The space the element would normally take would be there, but it would be hidden from view.

When you're targeting an element with CSS, you can use the :hover pseudo class to target parent elements. This is really powerful, so take a look at the example above for how you use that.

---

## Position Properties

- [`position`](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
- `static` `relative` `fixed`
- `top` `right` `bottom` `left`
- `sticy-top`

<iframe class="fragment" height='400' scrolling='no' title='Inline Elements' src='//codepen.io/planetoftheweb/embed/xYdLvp/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/xYdLvp/'>Inline Elements</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes
The position properties allow you move an object in different ways with css. Traditionally elements in CSS are drawn in the order that they appear within the HTML...that is what we call a `position: static` but you can change that to one of the other values. The first three are pretty easy to understand, the last two can be a bit confusing.

With `position: relative`, the object will move relative to where it used to be positioned. So it would draw at the same spot it normally would, but you can adjust the position relative to that spot with the top, right, bottom and left.

With `position: fixed`, the object will be removed from it's current position (so the space that it would normally take gets deleted) and it will have a position that is fixed to the viewport (the size of the window). Position fixed is great when you want to have something on the screen that's always attached to the window, but because it sits on top of content, you may need to move things around.

`sticky-top` is pretty cool, but doesn't have good browser support, so it won't work in all browsers, specially old ones. It allows you to create an element that sticks as you scroll it. Don't forget to add an attribute like `top: 0` to tell the element how to stick.

---

## Position Absolute

- `absolute`
- `z-index`

<iframe class="fragment" height='400' scrolling='no' title='Absolute Positioning' src='//codepen.io/planetoftheweb/embed/qxXmLK/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/qxXmLK/'>Absolute Positioning</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

The property that is hardest to understand is the `position:absolute` property. It works just like position fixed, so it removes the element from the normal flow and aligns it to the nearest parent with a position of `relative`. So it's a great way to display an object relative to another object like with a dropdown or pop-up.

Something that might not be obvious about web elements is that they are aligned in layers. This is really obvious when you start positioning elements. You control layers with the z-index property. 

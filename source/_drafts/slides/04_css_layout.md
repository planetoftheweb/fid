<!-- .slide: data-state="title" -->

# Advanced CSS & Layout

---

## Link Pseudo-Classes

- [:link](https://developer.mozilla.org/en-US/docs/WSS/:active) - Unvisited links
- [:visited](https://developer.mozilla.org/en-US/docs/Web/CSS/:visited) -- Already went here
- [:hover](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover) -- hover, watch on mobile
- [:active](https://developer.mozilla.org/en-US/docs/Web/CSS/:active) - Link while [being activated](http://css-tricks.com/almanac/selectors/a/active/)
- [Try it](http://jsbin.com/fokipas/3/embed?html,css,live)

---

## Ordered Elements
Help you choose elements with order in them.

- [:first-child](https://developer.mozilla.org/en-US/docs/Web/CSS/:first-child)
- [:last-child](https://developer.mozilla.org/en-US/docs/Web/CSS/)
- [:nth-child](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child)
- [:nth-of-type](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-of-type)
- [Try them](http://jsbin.com/mawumu/3/embed?live?html,css,live)

---

## Adding Content
Adds content before or after a certain element.

- [:before](https://developer.mozilla.org/en-US/docs/Web/CSS/:before)
- [:after](https://developer.mozilla.org/en-US/docs/Web/CSS/:after)
- [glyphs](http://css-tricks.com/snippets/html/glyphs/)
- [Entities](http://www.evotech.net/articles/testjsentities.html)
- [Try it](http://jsbin.com/opapos/5/embed?html,css,live)

---

## Responsive Design
- Browsers have a [viewport](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag?redirectlocale=en-US&redirectslug=Mobile%2FViewport_meta_tag#Viewport_basics)
- Otherwise 960px

```
<meta name='viewport'
  content='width=device-width, initial-scale=1'>
```
<!-- .element:  class="fragment"-->

---

## Controlling Breakpoints
Use different styles for viewport sizes

- Use the [@media selector](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)

```
body {
  background: #839496;
}

@media all and (max-width: 699px)
  and (min-width: 520px),
  (min-width: 1151px) {
  body {
    background: #DA3637;
  }
}
```
<!-- .element:  class="fragment"-->

- [Try it](http://jsbin.com/mibota/1/edit?html,css,output)

---
<!-- .slide: data-state="title" -->
## Controlling Layouts

---

## Using Natural Box Layout Model
The traditional box model doesn't feel natural, adding margins or padding changes the width of the element. You can fix it using the code below:

```
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}

```

- [Try it](http://jsbin.com/lijaba/3/embed?html,css,live)

---

## Stacking Order
[Box Model](images/css-stackingorder.png)
You can add a background color and image to a box element, but be aware of the stacking order.

- (http://jsbin.com/opapos/10/embed?html,css,live)Try it]

---

## Floating Elements

- Force block elements side by side.
- When floating elements, the parent container will lose track of the height of child elements
- You can use a clearfix trick to fix it.

```
.cf:before, .cf:after { content: " "; display: table; }
.cf:after { clear: both; }
.cf { *zoom: 1; }

```

- [Try it](http://jsbin.com/foqipu/2/embed?html,css,output)

---

## Positioning

The position property lets you place elements in relation to other elements.

- **Static:** Normal positioning of objects
- **None:** Removes objects from flow and hides them from view
- **Relative:** Removes objects from normal flow and let's you position in relation to where it would be
- **Fixed:** Removes objects from normal flow and places it relative to viewport (browser window)
- **Absolute:** Removes objects from normal flow, moves it with a parent if the parent has a position property other than static, otherwise, it's relative to viewport (like fixed)
- [Try it](http://jsbin.com/yivapa/1/embed?html,css,output)

---

## Display: Flex
- New Layout Model
- [Tons of options](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Try it](http://jsbin.com/venaciw/6/edit?html,css,output)

<!-- .slide: data-state="title" -->

# JavaScript Essentials

---

## What is JavaScript?

- Responsible for Interaction
- Scripting Language
- Runs on client

---
## What is it good for?

- DOM Management
- Event Handling
- AJAX Communication

---
## How do you use it?

- Inline, `<script>`, `<script src="">`
- Inline w/event attributes
- Inefficient practice

---
## Try it

<iframe height='500' scrolling='no' title='EwLxKz' src='//codepen.io/planetoftheweb/embed/EwLxKz/?height=500&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/EwLxKz/'>EwLxKz</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Using the `<script>` tag

- Better than inline, but maintainable
- Code executes when script read

---
## Try It


<iframe height='500' scrolling='no' title='aLGbZe' src='//codepen.io/planetoftheweb/embed/aLGbZe/?height=500&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/aLGbZe/'>aLGbZe</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


---

## As an external document

- Using `<script src=""></script>`
- `<script>` position important

---

## JavaScript Variables

- Losely typed
- Basic types

```
var myName = 'Ray';
var myNumber = 3;
var myBoolean = true;
```
<!-- .element: class="fragment" -->

---

## JavaScript Lists

- 0 Indexed

```
var myList = ['Ray', 'Fred', 'Bonnie'];
var otherList = ['Ray', 3, false];

myList[1]; //Fred;
otherList[0]; //Ray;
```
<!-- .element: class="fragment" -->

---
## Try it

<iframe height='300' scrolling='no' title='dVeyLW' src='//codepen.io/planetoftheweb/embed/dVeyLW/?height=300&theme-id=27192&default-tab=js,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/dVeyLW/'>dVeyLW</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## JavaScript Objects

- Complex data type
- Holds any var type

```
var info = {
  "full_name" : "Ray Villalobos",
  "title" : "Staff Author",
  "links" : {
    "blog"     : "http://iviewsource.com",
    "facebook" : "http://facebook.com/iviewsource",
    "youtube"  : "http://www.youtube.com/planetoftheweb",
    "podcast"  : "http://feeds.feedburner.com/authoredcontent",
    "twitter"  : "http://twitter.com/planetoftheweb"
  }
};
```
<!-- .element: class="fragment" -->

---

## Try it

<iframe height='300' scrolling='no' title='rGvaxx' src='//codepen.io/planetoftheweb/embed/rGvaxx/?height=300&theme-id=27192&default-tab=js,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/rGvaxx/'>rGvaxx</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Document Object Model (DOM)

- Page structure
- Add, delete &amp; modify
- `querySelector()`
- `querySelectorAll()`

---
## Try it

<iframe height='300' scrolling='no' title='dVePvJ' src='//codepen.io/planetoftheweb/embed/dVePvJ/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/dVePvJ/'>dVePvJ</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Events

- Things that happen
- Clicks, mouseOvers, etc.

---

## Try It

<iframe height='300' scrolling='no' title='rGvaZy' src='//codepen.io/planetoftheweb/embed/rGvaZy/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/rGvaZy/'>rGvaZy</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Conditional Statements

- True or False
- Execute when conditions met

---

## Try it

<iframe height='300' scrolling='no' title='WZJbYb' src='//codepen.io/planetoftheweb/embed/WZJbYb/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/WZJbYb/'>WZJbYb</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Loops

- Repeat execution

```
for (var index = 0; index < array.length; index++) {
  var element = array[index];
  
}
```
<!-- .element: class="fragment" -->

---
## Try it

<iframe height='300' scrolling='no' title='LzmEMm' src='//codepen.io/planetoftheweb/embed/LzmEMm/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/LzmEMm/'>LzmEMm</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Functions

- Like a macro
- Can have parameters

---
## Try it

<iframe height='300' scrolling='no' title='MEGYdJ' src='//codepen.io/planetoftheweb/embed/MEGYdJ/?height=300&theme-id=27192&default-tab=js,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/MEGYdJ/'>MEGYdJ</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>
---

## jQuery

- JS Library
- Fixes incompatibilities
- Uses the $ variable

---

## Try it

<iframe height='300' scrolling='no' title='pWVJgR' src='//codepen.io/planetoftheweb/embed/pWVJgR/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/pWVJgR/'>pWVJgR</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>
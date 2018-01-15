<!-- .slide: data-state="title" -->

# Basic CSS

---


## What is CSS?

- Cascading Style Sheets
- Layout for HTML
- [Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity) Rules

> > Author Notes:

- CSS Stands for Cascading Style sheets and that really breaks down to two things. - First we're creating styles for the HTML document, which means that you can specify how different elements are displayed and designed.
- The other important part of CSS is the cascading part, which is the set of rules that determine how the styles are applied. This is known as specificity. So for example, if two rules target the same code, the latest rule would have 'specificity' and therefore take precendence.

---

<!-- .slide: data-state="textonimage" data-background-image="http://planetoftheweb.com/i/webpage.svg" -->

---

# Example

You can dramatically change the look a site simply by using a different stylesheet. Take a look at the [CSS Zen Garden](http://www.csszengarden.com) and explore the different styles.

---

## What does it look like?

<iframe height='300' scrolling='no' title='GMpdOv' src='//codepen.io/planetoftheweb/embed/GMpdOv/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%; height: 50vh !important;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/GMpdOv/'>GMpdOv</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

> > Author Notes:

- Here's an example with two paragraphs. Both use a strong tag, but the second one has an additional style parameter. The strong text looks bigger and red. The style attribute is one of three ways to add styles to your document. It lets you modify a style on an instance of a tag, so this change only applies to the strong tag in the second paragraph.
- You might be wondering why most of the text is orange, that's because this example also has a document stylesheet. Click on the scss tab and you'll see a couple of additional styles. This shows you that you can create a stylesheet using the style attribute in every tag, but also have styles that apply to an entire document.

---

## CSS Syntax

```css
selector {
  property: value;
  property: value;
}
```

- [Selectors](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors)  use `{}`
- [Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)/value **declarations**
- **Declarations** separated by `;`

> > Author Notes:
Let's take a look at the structure of an style definition.
- In a typical style definition, you use a selector to indicate what element you want to style, you then add as many style declarations as needed using curly braces. If you're using the style attribute inside a tag, it's obvious that you want to change the current tag, so you don't need to specify a selector.
- To modify a style, you specify a set of properties and values. Properties are what you want to change and the values are what you want to change those to. Together, a property value pair makes something called a declaration.
- Multiple declarations are separated by semicolons, and you can create declarations in any order and whitespace is not really important, so use it for formatting and clarity.

---

## Using style attribute

```html
<element style="property: value; property: value;">
```

- Single instance
- Maximum `specifity`

---

## Using `<style>`

```css
<style>
  selector {
    property: value;
  }
</style>
```

- Within html page
- Affects `ONLY` current page
- Should appear in `<head>`

---

## External CSS

```html
  <link rel="stylesheet" href="style.css">
```

- Connects with outside document
- DO NOT use `<style>` in document
- Least `specificity`

---

## Specificity
1. Browser/User
1. `<link>` / `<style>`
1. `style=""` Inline

---
<!-- .slide: data-state="title" -->

# Exercise
<small>Add an external style sheet to your resume</small>

---

<!-- .slide: data-state="title" -->

# Exploring Common Properties
color, background

---
## Color Properties
- [color](https://developer.mozilla.org/en-US/docs/Web/CSS/color), [background-color](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color), [opacity](https://developer.mozilla.org/en-US/docs/Web/CSS/opacity)
- [Options](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Color)
- [Values](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value): keywords, hex, rgb(a), hsl(a)
- [Adobe Color](https://color.adobe.com/)

---

## Color Exercise

<iframe height='300' scrolling='no' title='GMpGba' src='//codepen.io/planetoftheweb/embed/GMpGba/?height=300&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%; height: 50vh;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/GMpGba/'>GMpGba</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

- [background](https://developer.mozilla.org/en-US/docs/Web/CSS/background)

---

<!-- .slide: data-state="title" -->

# Exploring Common Properties
Typography

---

## Typography
- [font-family](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)
- [font-size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)
- [font-style](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)
- [font-weight](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)
- [font](https://developer.mozilla.org/en-US/docs/Web/CSS/font)  combo

---

## Text Properties
- [text-align](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
- [text-transform](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)
- [line-height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
- [letter-spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing)
- [text-decoration](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)

---

# Custom Fonts

- Use [font-face](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face)
- Convert with [Font Squirrel](http://www.fontsquirrel.com/tools/webfont-generator)
- [Adobe's TypeKit](https://typekit.com)
- [Google fonts](http://www.google.com/fonts)

---

## Common Font Measurements
- Subset of [length](https://developer.mozilla.org/en-US/docs/Web/CSS/length)
- px, rem, em
- [Sizing with Rems](https://snook.ca/archives/html_and_css/font-size-with-rem)
- [Module sizing](https://css-tricks.com/rem-global-em-local/)

---

## Typography Exercise

<iframe height='300' scrolling='no' title='gGPmpw' src='//codepen.io/planetoftheweb/embed/gGPmpw/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%; height: 50vh;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/gGPmpw/'>gGPmpw</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

<!-- .slide: data-state="title" -->

# Exploring Common Properties
Geometry

---

## Basic Display Property

- Very [rich property](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- [block](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements), [inline](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements), inline-block, none
- inline -- no width, height
- **Advanced:** [flex](https://developer.mozilla.org/en-US/docs/Web/CSS/flex), grid

---

<!-- .slide: data-state="textonimage" data-background-image="http://planetoftheweb.com/i/css-boxmodel.svg" -->

---

## Sizing Elements

- [padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
- [margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
- [border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
- top, right, bottom, left

---

## Box Exercise

<iframe height='300' scrolling='no' title='YrwVNY' src='//codepen.io/planetoftheweb/embed/YrwVNY/?height=300&theme-id=27192&default-tab=html,result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%; height: 50vh'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/YrwVNY/'>YrwVNY</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

# Typical Measurements
- Rich [measurements](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
- px, %, vh, vw
- min-([height](https://developer.mozilla.org/en-US/docs/Web/CSS/min-height)/[width](https://developer.mozilla.org/en-US/docs/Web/CSS/min-width))
- max-([height](https://developer.mozilla.org/en-US/docs/Web/CSS/max-height)/[width](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width))

---

# Box Sizing Fix

<iframe height='300' scrolling='no' title='WZrEyy' src='//codepen.io/planetoftheweb/embed/WZrEyy/?height=300&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%; height: 50vh'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/WZrEyy/'>WZrEyy</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

- [box sizing trick](https://css-tricks.com/box-sizing/)

---
<!-- .slide: data-state="title" -->

# Exploring Common Properties
Selectors

---

# CSS Selectors

- [Type](https://developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors)
- [Class](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors), [ID](https://developer.mozilla.org/en-US/docs/Web/CSS/Id_selectors)
- [Combinators](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors)
- [Pseudo Class](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Pseudo-classes_and_pseudo-elements)

---
<!-- .slide: data-state="title" -->

# Exercise
<small>Style your resume</small>

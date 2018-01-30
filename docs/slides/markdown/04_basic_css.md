<!-- .slide: data-state="title" -->

# Basic CSS

---

<!-- .slide: data-state="textonimage" data-background-image="http://planetoftheweb.com/i/webpage.svg" -->

### Author Notes

![Web Page](http://planetoftheweb.com/i/webpage.svg)

---

## Page Styles

- Default styles
- Browsers differ
- Override with stylesheet
- Not guaranteed

### Author Notes

So far, we've been creating pages without using stylesheets and while it may seem like we're creating sites without any styles and that's really not the case at all. 

Every browser has a default set of styles called the `user agent stylesheet` (aka Default Browser Styles) that are in charge of how a page looks when it doesn't have any other styles. So it makes things like control the basic differences between the sizes of H1 and H3 tags and the spacing after paragraphs.

Each browser has it's own version of this default stylesheets and although they're pretty similar, they can have some major differences like the default font used.

So when you create your own stylesheets, you're not starting from scratch. You're removing, revising or overriding existing sytles. You're building on top of a framework of existing rules.

On top of that, a user or browser can override certain defaults like the size of your font if you want to make things more readable and you have no control over that. Designing for the web is unlike anything else you can do. You can't assume that a font is going to be a specific size or control the proportion or orientation of the page. Welcome to responsive design.

---

## Adding CSS To A Page

- Three options
- `style="CSS"` attribute
- `<style>CSS</style>` tags
- `<link>` tag in head

### Author Notes

Once you decide you want to add styles to your page, you have one of three options. each of these has advantages and disadvantages.

First, you can add styles directly to an existing HTML tag like the paragraph or anchor tag as an attribute. This is the most direct and deliberate way of adding css.

Second, you can add styles to a page using a tag called `<style>`. The style tag works like the paragraph or any other tag. It's a container tag so it has a beginning and ending part `</style>`. You simply put any CSS you want to affect the current page in between these style tags.

Third, you can ask that the page look for a separate style document and load it into the current page. This means that you can easily add the same sheet to multiple pages and is the preferred method of writing styles for an entire website.

You should add this in the `<head>` section of the document because it's where you place things that you want the browser to know before you display the page.

---

## Inline Styles

- `Property:Value;` rules
- Only THAT tag
- Most specific

<iframe class="fragment" height='400' scrolling='no' title='Inline Style Sample' src='//codepen.io/planetoftheweb/embed/yvLZNz/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/yvLZNz/'>Inline Style Sample</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

One way to add CSS to a stylesheet is to use the `style` attribute. This works like any other tag attribute like the `href` on an `a` (anchor) tag or a `src` attribute or an `img` tag, but the difference is that inside this `style` attribute, you can modify how that individual tag is displayed.

The problem with using the `style` attribute is that it only affects one instance of that tag. That means that in the sample above, no other strong tag would be affected on the page.

The style attribute is also the most specific, so that if other styles exist that apply to this element, the style attribute will override them.

This is a horrible way to add styles to your document because of these last two points. If you have 40 tags you want to control, using the style attribute would mean you'd have 40 style attributes and 40 places to update things in the future.

You might be asking yourself why would anyone use this? Well, style attributes are often used by javascript to dynamically add and delete styles to a page. For example, it would be easy to toggle the visibility of a section of code by using javascript to turn it on or off.

---

## Embedded Stylesheets

- `<style></style>` in `<head>`
- Requires a selector
- Whitespace for readability

<iframe class="fragment" height='400' scrolling='no' title='Style Tags Sample' src='//codepen.io/planetoftheweb/embed/QQWYGg/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/QQWYGg/'>Style Tags Sample</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Another way to create stylesheets is to embed them into the current document in their own section using the `<style></style>` tags. The style tags will let you write CSS that affects the current page. That's why most of the time they go in the `<head>` section of your page. That's where you want to put things that you want the browser to know BEFORE it starts showing any of the page to a user.

When you use the style attribute, you are targetting a specific tag, but when you use the style tags, you are targetting the whole document. Therefore, using the style tag means that you'll have to use a `selector` in order to specify what part of the document you're targeting. The rules are then place inside a set of curly braces `{}`

The easiest selectors to learn are called type selectors and are simply the name of the tag you're targeting. So, for example, if you wanted to target all of the paragraphs, the selector would simply be `p`.

```
p { color: red; font-size: 200%; }
```

Just like HTML, use whitespace and tabs for readability. Each declaration can be written on a separate line, and tapped in the visually see which styles belong within each declaration block. 

---

## External Stylesheets

```
<link rel="stylesheet" href="FILENAME">
```

- Use the `<link>` tag
- Do NOT use `<style>`
- Least Specific

### Author Notes

The final way to add styles to your page and the most common is to link to an external stylesheet using the `<link>` tag. The link tag allows you to use the same style sheet in several pages. The link tag is used

**DO NOT** use the `<style>` tag inside your external stylesheets. It's a common mistake. CSS is a language that is slightly different than HTML and the only thing that goes in an external document should be CSS. The `<style>` tag is an HTML tag and shouldn't go in a CSS document.

An external CSS file is the least specific of all the ways to add CSS, so if there are `<style>` tags or `style` attributes on the page, they'll override what's on your external stylesheets.


---

## External Stylesheet Syntax

```css
selector {
  property: value;
  property: value;
}
```

- [Selectors](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors)  use `{}`
- [Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)/value **declarations**
- **Declarations** separated by `;`

### Author Notes:
Let's take a look at the structure of an style definition.

In a typical style definition, you use a selector to indicate what element you want to style, you then add as many style declarations as needed using curly braces. If you're using the style attribute inside a tag, it's obvious that you want to change the current tag, so you don't need to specify a selector.

To modify a style, you specify a set of properties and values. Properties are what you want to change and the values are what you want to change those to. Together, a property value pair makes something called a declaration.

Multiple declarations are separated by semicolons, and you can create declarations in any order and whitespace is not really important, so use it for formatting and clarity.

---

<!-- .slide: data-state="title" -->

# Exercise
Link an HTML document to an External CSS file

---

## Class and ID selectors

- `.class` selector
- `#id` selector

<iframe class="fragment" height='400' scrolling='no' title='Class & ID Sample' src='//codepen.io/planetoftheweb/embed/MQWMbR/?height=400&theme-id=27192&default-tab=html,css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/MQWMbR/'>Class & ID Sample</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

In addition to selecting an HTML tag using the name of the tag, you can target any element that has a class associated with it using a class selector. That's the name of the class preceded by a period.

In the same way, you can target an element that has an ID by using a hashtag before the ID name.

---

## Descendant Selector

- Targets child element
- Use a space

<iframe class="fragment" height='400' scrolling='no' title='Aside Example' src='//codepen.io/planetoftheweb/embed/eVYweO/?height=400&theme-id=27192&default-tab=html,css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/eVYweO/'>Aside Example</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

The descendant selector is part of a [group of combinators](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors) that allows you to target an element only if it's inside another element. You target a descendant by leaving a space between the two.

---

## Multiple Selector

- One rule for many
- Use commas


<iframe class="fragment" height='400' scrolling='no' title='Multiple Selectors' src='//codepen.io/planetoftheweb/embed/xYbzjM/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/xYbzjM/'>Multiple Selectors</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

You can apply the same rules to multiple items using the multiple selector operator, which is really just a comma `,` character. This is a great way to do something to a variety of selectors like creating some basic styles for all of the Headlines.

---

## Pseudo Classes

- Select an element
- State or Property
- Single colon `:`

```
  :hover, :focus, :first-child, :nth-child, :not
```
<!-- .element: class="fragment" -->

### Author Notes

A pseudo-class is way of selecting an existing HTML element...that's really important because that's main difference between classes an elements It selects that element based on either a state or a property of the element.

Pseudo classes are related to to an existing element using a single colon character.

Some common pseudo elements are :hover which let's you modify an element when you hover over it. You'll also notice I've listed here :first-child and nth-child...two ways you can choose an element in a group based on their position.

---

## Pseudo Elements

- Virtual elements
- One or two colons?

```
::before, ::after, ::first-letter
```

### Author Notes:

- The main difference between a pseudo class and a pseudo element is that pseudo elements don't actually select an element, but create a sort of virtual element that didn't exist before. You can target that virtual element and then you can style it appropriately.

- CSS3 rolled out the use to two colons instead of one colons to differentiate pseudo elements from pseudo classes, but because older browsers do not support the double colons, it's ok most of the time to use a single colon instead.

- You can see some of the common pseudo elements here. They are a lot more scarce than pseudo classes. One good way to figure these out is to compare the difference between :first child and ::first-letter. They may seem like they're very similar, but first-child selects the first element that is a child of an element. So the target of the style is an actual element, where ::first letter lets you pick an non-existing position inside an element...the first letter of some element.

Let's take a look at an example:

---

## Pseudo Example

<iframe class="fragment" height='400' scrolling='no' title='Pseudo Class & Elements' src='//codepen.io/planetoftheweb/embed/QQwxoO/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 80vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/QQwxoO/'>Pseudo Class & Elements</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Colors

- Named, Hex
- rgb(a), hsl(a)
- [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color), [`background color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)

### Author Notes

There are many ways of specifying colors in CSS. You've already seen the use of named colors. The problem with named colors is that they are imprecise, so, for example the `blue` color is really bright and probably not a color you'd want to use often.

Another way to specify colors is through the use of hexadecimal values. Those are values specified using two characters from 00-FF. This is called base 16 and is a shortcut for rgb values where 00 is black and FF is 256 in each of the Red, Green and Blue channels. It's the oldest color model and handy, but hard to understand.

There two other less common ways to specify colors using each of the rgb (red, green and blue) channels and a newer hsl (hue, saturation, lightness) mode.

The red, green and blue colors are more directly related to the way human beings see as well as what monitors are able to display, but it's difficult to manipulate colors because working with them is not straightforward.

The hsl color mode is a little bit easier to work with because hue is essentially the base color and by adjusting the saturation, you can modify how neutral grey or bright that color appears. The l parameter stands for lightness, so you can make a color lighter by adjusting this value.

A great place to go look for color combinations is the [Adobe Color](https://color.adobe.com/) website.

The main place where you can control color is the color property, which affects text and the background-color property, which affects the backgrounds of elements. 


---

<!-- .slide: data-state="title" -->

# Exercise
Play with colors on your site

---

## Fonts on websites

```
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", sans-serif;
```

- [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)
- Platform defaults
- Quoted, `serif, sans-serif`

### Author Notes

Fonts in CSS are specified via the [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) property. You can specify fonts by simply using the font name. If the font exists in the user's computer, then it will display properly. If it doesn't exist in that computer, you can provide alternatives by using commas to determine which fonts will be displayed in order.

Every platform has their own default fonts they can use. For example, one of the Apple system default fonts is called San Francisco, but that also depends on the browser and platform.

Therefore, you can't assume that a user is seeing the same fonts as you...chances are they are not. Users can also change override the zoom as well as the size of elements.

When you want to use a font that has a space in the name, you'll need to use quotation marks to make sure it works properly.

There are two special names you can use called `serif` and `sans-serif` as well as `monospace`. It allows you to specify the browser's default font...whatever it is and should be used at the end of any font specification.

---

## Font Properties

- [`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size), [`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)
- [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
- [`font`](https://developer.mozilla.org/en-US/docs/Web/CSS/font)

### Author Notes

Here are the most common font properties. There are so many of them that it's hard to try to put them all here. They are pretty obvious to work with.

Most of them are under the font prefix, but some are not. For example the [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) property affects something in typography we call leading.

There's also a very powerful [`font`](https://developer.mozilla.org/en-US/docs/Web/CSS/font) property which allows you to control a multitude of other properties in a single place.

---

## Text Sizing in CSS

- Pixels and Accessibility
- Rems &amp; Ems More Flexible
- Default Sizes Matter
- Rems vs Ems

### Author Notes

Pixels are the traditional way to size typography on the web, but in some older versions of IE, pixels are not resizable. That's an accessibility issue if someone doesn't have good eyesight and needs to make fonts bigger on your page.

Ems are Rems are relative sizes, which means that you can base the size of elements on other elements. That makes sizing with pixels less flexible. If you want to change the size of a group of elements, it's harder with pixels because you would have to issue sizing instructions for every element within a component.

If you want to use relative font sizes, the important thing to remember is that every browser has a default font size...in most cases, that's 16 pixels. You can change that default to something else if you want to and that affects how you use ems and rems.

Once you know your default font size, rems are always relative to the root font size. So 1rem is equal to 16 pixels...unless you've changed that default font size. Ems, in contrast are sized relative to their parent containers and it's the height of the font unit.

---

## Google Web Fonts

```
@import url('https://fonts.googleapis.com/css?family=Rammetto+One');

h1 {
  font-family: "Rammetto One", sans-serif;
}
```

- [Hundredths of Fonts](https://fonts.google.com/)
- Load only what's needed
- Issues with Validation

### Author Notes

The easiest way to add custom fonts to your websites is to use Google web fonts. There are currently 848 styles you can add to your site for free.

Make sure when you use Google Web Fonts, that you use only what you need because the more fonts you add to a page, the longer it will take to load. 

You can easily add fonts by using this site. Choose fonts by hitting the plus sign. When you're ready to add them to to your site, simply hit the popup that appears at the bottom of the page. Click on the embed type. There are some issues with validation and the standard import, so I would suggest that you use the @import rule.

You can then use these fonts in your pages just like you would specify any regular font. Remember that if the font has a space in the name, put it in quotes in your css rule. Also, remember to include some backups. Even using Google Web fonts you can't guarantee that the user will see what you're specifying. Their web connection might go down.

---

<!-- .slide: data-state="title" -->

# Exercise
Load Custom Google Fonts

---

## Basic Display Property

- Very [rich property](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- [block](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements), [inline](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements), inline-block, none
- inline -- no width, height

### Author Notes
There is a very rich display property in CSS that lets you control how element's spacing and layout is controlled on the page. We'll cover the basics this week.

All elements are initialized as having one of these display properties by default and they are usually considered to be either a block element or an inline element. The main difference is that inline element have no width or height by default.

You can control some of the spacing and border in elements and you can control the width and height of some elements depending on their display property.

---

<!-- .slide: data-state="textonimage" data-background-image="http://planetoftheweb.com/i/css-boxmodel.svg" -->

### Author Notes

![Web Page](http://planetoftheweb.com/i/css-boxmodel.svg)

---

## Sizing Elements

- [padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
- [margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
- [border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
- top, right, bottom, left

### Author Notes

As you can see from the graphic, we can control several things about the elements. The main are the padding, margin and border.

The margin property has an interesting property in that vertical margins collapse, so if you have a headline and a paragraph and the headline has a margin at the bottom of 15px, but the paragraph has a margin at the top of 10px, the 10px margin will fold into the 15px margin and the total amount of room in between the two will be 15px.

You also have individual control over each of the dimensions top, right, bottom and left.

---

<!-- .slide: data-state="title" -->

# Exercise
Practice basic display

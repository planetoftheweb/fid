<!-- .slide: data-state="title" -->

# Intermediate CSS

---

<!-- .slide: data-state="textonimage" data-background-image="http://planetoftheweb.com/i/css-boxmodel.svg" -->

### Author Notes

![Web Page](http://planetoftheweb.com/i/css-boxmodel.svg)

By default, the width and height you assign to an element is applied only to the element's content. Border and Padding are added to this, therefore if you specify that an element needs to be 300 pixels wide, but then you add 10 pixel padding all around, the box ends up being 320 pixels.

That's not really great for layout and it's not the way you think about sizes, so CSS has a propety called [box-sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) that lets you redefine the way this works.


---

## Box Sizing

- [`box sizing`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) info
- `content-box` default
- `border-box` more natural

<iframe class="fragment" height='400' scrolling='no' title='Box Model Sample' src='//codepen.io/planetoftheweb/embed/OQXage/?height=400&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh;width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/OQXage/'>Box Model Sample</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


### Author Notes

```
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}
```

A good way to combat against this is to use the code above, it establishes the box model as border-box in the topmost element (html) and then asks every other element on the page to inherit that value.

---

## Inline Block Issues

- `inline` vs `block` [properties](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- `inline-block` measurements
- Spaces matter

<iframe class="fragment" height='300' scrolling='no' title='Inline Block Spaces' src='//codepen.io/planetoftheweb/embed/rJLQGm/?height=300&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/rJLQGm/'>Inline Block Spaces</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

The two main display value are inline elements and block elements. The main difference between these elements is that block elements have spacing before and after them and that you can specify an elements width and height on block elements, but not on inline elements.

The inline-block element was designed so that is displays inline, but you can specify the width and the height, so it's a pretty useful element, but there is one problem.

When you add a carriage return in between inline-block elements, it displays a space in between these elements, so in some instances, you may want to make sure that there is no carriage return or spaces between these elements so they display properly.

Although inline-block can be a quick solution to create certain layouts, it's not the best way to lay elements out on a page, there are much better ways to do things, but it's important that you undertand this particular issue with inline-block because it can cause headaches.

---

## Resetting Font Sizes Trick

- `ems` vs `rems`
- Compounding issue
- [root html size](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html) font size

<iframe class="fragment" height='300' scrolling='no' title='Relative Font Sizes' src='//codepen.io/planetoftheweb/embed/yvJQRM/?height=300&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/yvJQRM/'>Relative Font Sizes</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Let's review the two major relative typography measurements again. ems are relative to a parent element. The problem with this is that it can cause a compounding issue. So if you have an element where you set the font size to 2 ems and then have another element inside that and set the size to 2ems, that inside element will now be four ems. If you're doing that a lot it can be confusing to size things.

Rems, on the other hand are always relative to the root font size, which is usually in the body. The root font size is usually set to 16px in all browsers. Using rems, you can always base the size of any element on that size. So if you want to set the size of an element to 32px, you can use 2rem as the value.

The root font size of 16px doesn't always lend itself to easy mathematical calculations, so one technique is to set the root font size to 62.5% in the body. That means that the root font size will now be 10 pixels. That makes it easier to visualize your sizes, because if you want to make something 28 pixels, you can set that to 2.8rem anywhere on the page.

https://snook.ca/archives/html_and_css/font-size-with-rem

---
<!-- .slide: data-state="textonvideo" -->

<iframe width="560" height="315" style="width: 100vw; height: 100vh;" src="https://www.youtube.com/embed/qkM6RJf15cg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
---

## Vendor Prefixes
- Browser Support
- [World Wide Web Consortium (W3C)](https://www.w3.org/Style/CSS/Overview.en.html)
- Vendor Prefixes
- [Do I use](http://doiuse.herokuapp.com/)

<iframe class="fragment" height='300' scrolling='no' title='Compatible gradient' src='//codepen.io/planetoftheweb/embed/wyzJyg/?height=300&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/wyzJyg/'>Compatible gradient</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

CSS is a living language, therefore not all versions of browsers support all features. For the most part everything we've covered so far has excellent support even in pretty old browsers. However, some of the techniques we'll be learning about soon are not always supported in older browsers.

Different companies establish a baseline of support for which browsers and versions they want to support. So, for example, older government entities might require that you run your site so that it's compatible with an older version of Internet Explorer.

As you'll see as new features are proposed, they go through a rigorous testing and approval procedure by the W3C. However, this process can take years. Some browsers may start to support features even before they are officially approved. Because the definitions of how things work may change, the implementation by some browsers will change over time.

A good example of this is the definition for [notifications](https://caniuse.com/#feat=notifications) in CSS. It's an attempt to be able to define notification messages outside of a web page. Current brower support is very sketchy right now. No versions of Internet explorer support that, so that is a feature you shouldn't depend on for your sites if IE support is required at your company.

A great place to check for browser support is the [caniuse](https://caniuse.com/#feat=notifications) website. It not only shows you which browsers support, but also usage information (percentage of the web that uses this browser version) so that you can make a decision on wether your company should support this feature. These usage tables are guidelines, however, and your company will make those decisions on usage.

As features are being developed, browsers will often release an early implementation of those features under their own browser prefixes. The [flexbox feature](https://caniuse.com/#search=flexbox) is a great example of this. When that happen, the browsers will use something called a browser prefix like -moz (firefox), -webkit (safari, chrome), -ms (internet explorer), -o (opera) so that when the feature is released their own versions won't compete with the final version of the feature.

When browsers implement their own versions of experimental features, it can sometimes create issues because in order to support both old and new browsers, you end up with multiple ways of writing the same feature. Take [gradients](https://caniuse.com/#search=gradient), an example we'll be looking at this week.

They are not supported in IE until version 10, however in version 5 of safari, they were implemented, but with a different nomenclature. So in order to support gradients in as many older browsers as possible we would need to write something like the example above.

Clearly, it's not fun to write css that is backwards compatible with older browsers. There's a couple of ways around that. One is to use a processor for your CSS that takes care of writing the vendor prefix code for you. That is an advanced feature that we won't be covering in this class. Another is to use a javascript library like [prefix-free](https://leaverou.github.io/prefixfree/) that will automatically add the prefixes to your code at runtime. This ends up slowing your site slightly and it's not optimal, but it's easy to do.

If you want to use prefix-free from a CDN, you can add this to your code before the closing body tag (`</body>`)

```
<script src="https://cdn.jsdelivr.net/npm/prefixfree/prefixfree.js"></script>
```

In this class, you can assume that I'll be using the latest version of Google Chrome, so you won't need to worry about prefixes unless you want to use a bleeding edge feature of CSS.

---
<!-- .slide: data-state="textonvideo" -->

<iframe width="560" height="315" style="width: 100vw; height: 100vh;" src="https://www.youtube.com/embed/lD9FAOPBiDk" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

---

## Gradients
- on [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) or [`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image)
- [`linear-gradient`](https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient) or [`radial-gradient`](https://developer.mozilla.org/en-US/docs/Web/CSS/radial-gradient)
- Gradients and readability

<iframe class="fragment" height='300' scrolling='no' title='Sample Gradients' src='//codepen.io/planetoftheweb/embed/gvwmJg/?height=300&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/gvwmJg/'>Sample Gradients</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes
CSS allows you to define gradients with a powerful set of declarations. These declarations can be insered into the background or the background image attributes. Generally, the background property is more flexible and allows you to create more flexible gradients.

There are two main options for creating gradients...linear or radial gradients. They are pretty self explanatory, so check out the code above for examples of how to build gradients. You can also check out this [CSS3 Patterns Gallery](http://lea.verou.me/css3patterns/) to see some advanced examples.

Gradients as a design element have fallen out of favor in recent years with the rise of flat design on the web, so make sure you use gradients sparsely and that you never sacrifice legibility over gradient or background use. One real valid use of gradients is to create an image overlay (see sample code) that can help you create text overlays when you place text on top of an image by darkening or changing the color of an image.

---

## Advanced Backgrounds

- Rich [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) property
- [`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image), [`background-repeat`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat), [`background-position`](`background-position`), [`background-attachment`](background-attachment), [`background-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size)
- Compatibility concerns

<iframe class="fragment" height='300' scrolling='no' title='Full Screen Background Image' src='//codepen.io/planetoftheweb/embed/LQRyMW/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/LQRyMW/'>Full Screen Background Image</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

The background property is a super rich property full of features. In addition to being used for gradients, it can also be used to place an image as the background of an element. That's pretty useful in CSS and there are a lot of controls over how the image is placed and behaves inside that element.

You can see an example of each of the properties above. You can control the position of the background, so that you can make the image align to the center, top or bottom. This can also be specified in percentages.

Small backgrounds repeat by default, so you can control how this repetition happens with CSS and ask for either horizontal, vertical repetition or no repetition.

Another common property is the background attachment property, which lets you control how the background moves in relationship to the scroll. Although fixed is a popular property, this doesn't translate well to mobile devices, so be careful when relying on this and test on your target platforms.

You can also control a property called background-size, which lets you define a background that proportionally resizes to the dimensions of the viewport.

Be careful when placing text on top of an image because sometimes the image can fight with the readability of the text. In those instances, it's useful to put a mild gradient on top of the image to perhaps darken the image and make the text easier to read.

This is a great place to use sizes like vw and vh and the weird, but useful v-min font sizes, which give you proportional font sizes related to the viewports.

---

## Rounded Edges
- [`border-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)
- px/percentages x/y trbl
- Don't overuse

<iframe class="fragment" height='300' scrolling='no' title='border-radius' src='//codepen.io/planetoftheweb/embed/aqmyEP/?height=300&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/aqmyEP/'>border-radius</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

The rounded edges properties allows you to modify the edges of elements so that they have a round edge. There's a lot of interesting effects that you can achieve with this.

You can control the overall size of the radius with either pixel units or percentages and invididually control which edges are rounded.

---

## Shadows
- [`box-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)
- [`text-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow)
- Don't overuse

<iframe class="fragment" height='300' scrolling='no' title='shadows' src='//codepen.io/planetoftheweb/embed/rJMYBx/?height=300&theme-id=27192&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/rJMYBx/'>shadows</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes
Shadows can be an effective way to separate an element from their background. There are two types.

The primary way of working with shadows is to use the box shadow property which lets you specify the distance of the shadow from an element in x and y positions as well as the softness of the shadow.

If you want to add shadows to text, you can use the text-shadow property instead. It works pretty much the same way as the box-shadow.

Just like with rounded edges please don't overuse these features. Use these for clarity and avoid using them when it makes your/ design look too busy.

---

## Icons
- Easy to add
- [Font Awesome](https://fontawesome.com/)
- Add your own icon

<iframe class="fragment" height='300' scrolling='no' title='icons' src='//codepen.io/planetoftheweb/embed/GQjyqR/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/GQjyqR/'>icons</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes
Icons are a great way to spice up your designs and are very popular on the web. You can use an existing library or create your own.

One of the most popular icon libraries is called font awesome. You can use a version which includes 929 free icons and there are lots of other libraries you can use on the web.

You can add your own icons with some simple code (see example). SVGs are always better because they are clearer. Make sure that the icons are visible and simple. Not everything works as an icon.

---

## Debugging CSS
- Inpect/Elements
- Styles/Computed/Console
- Copying code

### Author Notes
Icons are a great way to spice up your designs and are very popular on the web. You can use an existing library or create your own.


In addition to using a good linter like [csslint.net](http://csslint.net/), you need to learn how to debug CSS using your browser. Although most browsers have their own ways of doing this, Google Chrome is the most popular tool that developers use to debug code. In there you have the option of analyzing not just your HTML, but also your CSS. To get to it, **right click** on any element and then choose **inspect** from the popup. Make sure you're in the `elements tab` to see the HTML next to the CSS that is in use to display this page.

Your three most powerful tools for debugging are the `styles` tab, which shows you the styles that are applied to your page in the order they are applied. The `computed` tab, which shows you the final state of the elements after all of the styles have been applied and the `console` tab, which shows you any errors on the page.

You can override or test styles by using the element.style section. This is the same as using the style attribute in HTML, so it is the most specific.

If you pull up your page and you see a red checkbox on the right, the page has errors, by using the `console` tab, you can see if there are any missing documents or files that are not loaded correctly.
---

<!-- .slide: data-state="title" -->

# Exercise
Practice Debugging You CSS

---

## Graphic Formats

| Feature | GIF | JPG | PNG |SVG |
|--:|:-:|:-:|:-:| :-:|
|  **Type**  | bitmap  | bitmap  | bitmap  | vector container  |
| **Animation** | yes | none | none | programatic  |
| **Max Colors** | 256 | 16-bit  |  32-bit | n/a  |
| **Transparency** | 1-bit | none | 8-bit | programatic  |
|  **Compression**  | none  | lossy  | lossless  | n/a  |
|  **Use**  | animated GIF  | Photos  | Rich Lossless Transparency  | Programmable Vectors  |

### Author Notes

On the web, there are four graphics formats you should use: GIF, JPG, PNG and SVG. Which one you use depends on what you're trying to do. 

#### GIF

GIF is by far the oldest of the formats and should rarely be used on web projects because of it's many limitations. First, it can only store a maximum of 256 colors, so it's not very good for images. Although it does allow you to use transparency, it's not the best format for that since it only allows 1 of the colors to be transparent. It is not a compressed format, although you can make a GIF file smaller by limiting the amount of colors to an even shorter palette. The only thing this format has going for it is that it is the only bitmap format that allows for animations. This is why it's still popular today, but it's hardly something you should be doing on websites.


#### JPG

Next is JPG or JPEG. It's a format designed for photographic images. JPG is smart about the information it stores because it understands how people see color. 

Most people have four types of sensors that allow them to see images. Rod shaped sensors, which allow you to detect grayscale values in light are the most common and appear at a 50-1 ratio compare to the rest. Cone shaped sensors appear in three different colors: red, green and blue. Because of this, humans are much more sensitive to grayscale information than they are to color information. 

The JPG format understands this and therefore it separates the color information from the grayscale information and uses different compression methods to make the images much smaller applying more compression in the color and less in the grayscale. Because JPG changes the original pixels in the image to do this, it's called a lossy compression format, which means that you lose quality when you use this method of compression.

Photos look pretty good with JPG compression and they are significantly smaller than with other formats.

#### PNG
This format was designed after it was discovered that the GIF format was proprietary and belonged to certain companies. It offers a lot more detail and can store much more color information than JPG. So it's capable of storing a lot more fidelity than the JPG format. In addition, it's compression is not lossy, so you will not lose quality when saving in the PNG format. Alas, the compression doesn't produce images which are as small as JPEG so JPG is still the best option for photos. PNG is really good for bitmaps and has one feature that makes it ideal for certain tasks and that's it's ability to have soft trasnparency.

#### SVG
Scalable Vector Graphics are the only format that store information as vectors. It is technically a container format, so you can store files in other formats inside an SVG file. Vectors allow you to store mathematical shapes instead of pixels. One huge advantage with SVG is that you can program those shapes using JavaScript and also style them with CSS. The CSS you use for styling SVGs is slightly different than traditional CSS, so it's easy to learn. You should use SVGs whenever possible if you have vector data.

You can use Photoshop to export in any format except for SVGs. You can use Illustrator to export vectors as SVGs.

---

## Sizing Images

- Resize to <1500px
- Horizontal Orientation
- Create thumbnails

### Author Notes

Any image you take with a camera or your phone usually has way more information than you need for a website. Professional cameras can easily be in the 20 megapixel range, but even a 2 megapixel photo at 1920 pixels in width is a lot more than what you'll need for a website. So it's important that you crop and resize your images to make them fit into a website. For most photos you don't really need anything bigger than maybe 1500 pixels wide and maybe 1000 pixels tall, anything more than that is overkill.

Because most monitors display horizontal aspect ratios, sites are designed with those proportions in mind, so you should, for the most part shoot your images in landscape mode.

It's important that for larger images, you provide a thumbnail image that points to a higher resolution version of the image. I would suggest that you try to crop thumbnails to the same size (it's common to have large wide thumbnails these days) and that you crop them to show a piece of the image, not the entire image.

---

<!-- .slide: data-state="title" -->

# Exercise
Create thumbnails

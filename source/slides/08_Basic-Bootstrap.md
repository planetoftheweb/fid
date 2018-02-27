<!-- .slide: data-state="title" -->

# Bootstrap

---

## What is Bootstrap
- Framework
- Class based
- Flex based grid

### Author Notes
Bootstrap is a framework, which means a way to write your code. If you write code the way the frameworks asks you to write code, then it will give you some additional functionality.

In Bootstrap's case, almost all of the features are added by adding a series of classes to your code. When you add these classes, bootstrap will give you features like a column grid, dropdowns, navigation menus and many others.

One of the  main reason people use Bootstrap is because it gives you an easy to use and well tested grid that helps you layout your sites with responsive features. Bootstrap is known as a mobile first framework, which means that it assumes you're designing for mobile devices, but it allows you built functionality from there.

---

## Installing Bootstrap

- [Download Files](http://getbootstrap.com)
- CDN Option
- [CDN Bootstrap Shell](https://gist.github.com/planetoftheweb/2c6f2238cfc69c04336bb3cd852efcbe)

### Author Notes

You can install Bootstrap in one of four ways. The first is to simply download the pre-compiled Bootstrap CSS and JavaScript files. That works well if you need to install a copy of bootstrap that will work even without an internet connection.

Another way is to use CDNs. A CDN is a content delivery network, which means a place that hosts common libraries like Bootstrap. When someone visits a site that uses  a CDN link, their browser will check it's cache or memory to see if the visitor has been to a similar site that's also using the same link. If that's the case, then the browser will load the cached version of the library. Since it's already stored in memory, that makes the new site load faster since the browser won't have to request the file.

You can also download the source files. This way, you download not just the css and javascript but all of the files that the developers used to create bootstrap, which includes everything including the original sass files and the documentation. You probably only want to do this if you want to contribute to the project or customize bootstrap. We wont be talking about this option in this course.

For this class, we'll use the CDN version of bootstrap. I've created a special GIST with the code you need to get started with the Bootstrap framework.

---

## Typography

- `Reboot.css` styles
- `border-box` sizing
- Native fonts
- Inherit

<iframe class="fragment" height='400' scrolling='no' title='Basic Typography' src='//codepen.io/planetoftheweb/embed/eVbYev/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/eVbYev/'>Basic Typography</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes


There is a special portion at the beginning of the bootstrap styles called reboot.css. It normalizes styles so that they look similar in different devices and browsers. Unlike most other normalizing css templates, it's a bit opinionated.

In CSS, vertical margins can collapse and that makes it confusing to calculate the proper spacing in between different elements. To avoid this, bootstrap adds margin only at the bottom of elements.

Bootstrap content uses the inherit css parameter whenever possible. This is important when you write your own css in addition to the bootstrap css because you won't have to work as hard to override styles.

Another default that is set in bootstrap is that box-sizing, which makes it easier to calculate the width of elements is by default turned to

Bootstrap uses Native Font Stacks. That means that the default font in bootstrap isn't set to Helvetica, but it tries to use whatever the current platform defines as the default sans-serif font. For example, on current macs, that would be San Francisco. That yields a smaller css file and again, makes things look great on different devices.

Bootstrap has elements that match headlines, style lead paragraphs and take care of common page patterns. This gives you a great looking stylesheet to begin your own designs.

Let's take a look at a document that uses bootstrap with some basic HTML code. First, you'll notice that Bootstrap uses sans-serif fonts, which is definitely different than the serif defaults in your browser and it also redefines styles for things like `emphasis` and `strong` as well as other HTML content.

Headings like H1-H6 look great and if you know your typography, you might notice that things seem a bit tighter than normal. That's because bootstrap's approach is to remove the margin from the top of elements. So headings and paragraphs have the margin at the top and bottom removed.

```
<p class="h1">h1. Bootstrap heading</p>
<p class="h2">h2. Bootstrap heading</p>
<p class="h3">h3. Bootstrap heading</p>
<p class="h4">h4. Bootstrap heading</p>
<p class="h5">h5. Bootstrap heading</p>
<p class="h6">h6. Bootstrap heading</p>
```

There are also four display styles for more dramatic typography that look great.

```
<h1 class="display-1">Display 1</h1>
<h1 class="display-2">Display 2</h1>
<h1 class="display-3">Display 3</h1>
<h1 class="display-4">Display 4</h1>
```

You can specify that certain paragraphs receive a lead style with the lead class.

```
<p class="lead">
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
```
---
<!-- .slide: data-state="title" -->

# Bootstrap 4
Text Utilities

### Author Notes
Bootstrap provides several utility classes that can help you take care of common typography needs, so let's take a look at what they are and try them out.

---


## Alignment Utilities

<ul>
	<li class="fragment">`text-justify`</li>
	<li class="fragment">`text-nowrap`</li>
	<li class="fragment"><p contenteditable>`text(-XX)-POS`</p>
			<small style="line-height: 120%; vertical-align: text-bottom;">
				<b>XX:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px 
				<code style="background:#5cb85c; color:white;">md</code> >768px 
				<code style="background:#5cb85c; color:white;">lg</code> >992px 
				<code style="background:#5cb85c; color:white;">xl</code> >1200px
			</small><br>
			<small style="line-height: 120%; vertical-align: text-bottom;"> 
				<b>POS:</b> <code style="background:#D95357; color:white;">left</code> &nbsp;
				<code style="background:#D95357; color:white;">center</code> &nbsp;
				<code style="background:#D95357; color:white;">right</code>
			</small>
	</li> 
</ul>

### Author Notes

`text-justify` lets you do full justification within the browser, so that the edges of text align instead of being ragged.

If you need to turn off wrapping for some content, you can use text-nowrap. That can be useful if you have a long line of text that's just going to be copied, but you don't need to display the whole thing.

One of textual utility classes lets you control the alignment of your content. What's really cool is that the alignment can change based on the width of the browser or viewport. The formula looks like this.


---

## Lists

- `list-unstyled` no bullets
- Inline Lists
	- `list-inline` on UL
	- `list-inline-item` on each LI

<iframe class="fragment" height='400' scrolling='no' title='Basic Typography' src='//codepen.io/planetoftheweb/embed/wyRBwG/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/wyRBwG/'>Basic Typography</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

There's a couple of styles that will take care of things that we often do with lists. First is getting rid of those pesky bullets, you can do that with the list-unstyled class. However, this only works on the first level of the list elements.

Next you can build lists that appear side by side like a menu or perhaps your own version of a breadcrumb using a combination of two links. `list-inline` goes on the UL element `list-inline-item` goes on each LI in the list.

---

<!-- .slide: data-state="title" -->

# Colors

---


## Text Colors

<ul>
	<li class="fragment"><p contenteditable>`text-COLOR` for text</p>
		<small style="line-height: 120%; vertical-align: text-bottom;">
    <code style="color:#007bff">primary</code>
    <code style="color:#868e96">secondary</code>
    <code style="color:#28a745">success</code>
    <code style="color:#dc3545">danger</code><br>
    <code style="color:#ffc107">warning</code>
    <code style="color:#17a2b8">info</code>
    <code style="color:#f8f9fa; background-color:gray;">light</code>
    <code style="color:#343a40">dark</code>
    </small>
	</li>
	<li class="fragment"><p>Use for links</p></li>
</ul>

### Author Notes
1. You use the word text, and then one of the color keywords like: primary, success, info, warning, danger, white or muted and that will turn the text that color.

1.You can use the same class names for links.

---


## Background Colors

<ul>
	<li class="fragment"><p contenteditable>`bg-COLOR` for backgrounds</p>
		<small style="line-height: 120%; vertical-align: text-bottom;">
    <code style="background-color:#007bff; color: white;">primary</code>
    <code style="background-color:#868e96; color: white;">secondary</code>
    <code style="background-color:#28a745; color: white;">success</code>
    <code style="background-color:#dc3545; color: white;">danger</code><br>
    <code style="background-color:#ffc107; color: white;">warning</code>
    <code style="background-color:#17a2b8; color: white;">info</code>
    <code style="background-color:#f8f9fa; color: white; background-color:gray;">light</code>
    <code style="background-color:#343a40; color: white;">dark</code>
    <code style="background-color:#fff; border: 1px solid black; color: black;">white</code>
    </small>
	</li>
</ul>

<iframe class="fragment" height='400' scrolling='no' title='Colors' src='//codepen.io/planetoftheweb/embed/ddwPGE/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/ddwPGE/'>Colors</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes
1. Another way you can use them is to color the background of elements and of course, there are classes for that.

---

<!-- .slide: data-state="title" -->

# Images

---

## Basic Images

- `img-fluid` responsive images
- `rounded`, `rounded-DIR` round edges
<small style="line-height: 120%; vertical-align: text-bottom;">**DIR:** <code>top</code> <code>right</code> <code>bottom</code> <code>left</code><br> <code>circle</code> <code>rounded-0</code></small>	
- `img-thumbnail` rounded 1px border


### Author Notes

One of the most useful image classes is the img-fluid class. If you add that to an image, the image becomes responsive, which means a max-width attribute of 100% and a height of auto.

If you want rounded edges, you can use the word rounded or add a direction to the word, top, right, bottom, left, which should be self explanatory or circle, which makes the image look like a circle and rounded-0, which gets rid of any roundness the picture currently had.

There is an additional style that adds a 1 px rounded edge around the image called img-thumbnail.

---


## Aligning Images

- `float-left` or `float-right`
- `text-center` center inline
- `mx-auto` center block

<iframe class="fragment" height='400' scrolling='no' title='Image Classes' src='//codepen.io/planetoftheweb/embed/oEJgyN/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/oEJgyN/'>Image Classes</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes


If you need to align images, you can use the float-left or float-right class, which will also work for other elements.

Traditionally, images are inline elements, so you should be able to use text-center on the container element.

If the image happens to be a block element, you can use the mx-auto class to center the element.

---

<!-- .slide: data-state="title" -->

# Layout Grid

### Author Notes
One of the main reasons people use bootstrap is to be able to easily layout content that's responsive.  This is the most important thing you should master in bootstrap.

---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-th"></i> The Grid

- Responsive 12-column
- Flexbox Based
  - containers
  - rows/columns

### Author Notes

The grid is a responsive 12-column system for creating just about any layout you can think of.

It uses a technology called flexbox that makes it easier to create complex layouts with minimal code.

In order to work with the grid, you neet to masters three simple concepts. 

First is containers, which can be used with or without the grid to align content either to the viewport or to center it around a set of breakpoints.

Next is rows and columns, they work together to allow you to create the layouts. The rows prepare the columns for layout. Columns are both complex and extremely flexible, so we'll cover them in a separate video. Let's take a look at containers.


---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-th"></i> Grid Containers

- `container`
- `container-fluid`
- 15px padding
- Adjusts to breakpoints
<small style="line-height: 120%; vertical-align: text-bottom;">
<code style="background:#5cb85c; color:white;"><576px</code>
<code style="background:#5cb85c; color:white;">576px</code>
<code style="background:#5cb85c; color:white;">768px</code>
<code style="background:#5cb85c; color:white;">992px</code>
<code style="background:#5cb85c; color:white;">1200px</code>
</small>


### Author Notes

There are two different types of containers, regular containers which center content and  snap to certain grid points.

Or fluid containers, which are always the full width of the viewport, which means the width of the device or browser window.

One of the reasons you use a container is because you get a 15px padding on each side to make sure it works well with backgrounds.

---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-th"></i> Rows

- Require Rows
- Only columns in rows
- `no-gutters` deletes gutters

<iframe class="fragment" height='400' scrolling='no' title='Basic Bootstrap Layout' src='//codepen.io/planetoftheweb/embed/eVbNGO/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/eVbNGO/'>Basic Bootstrap Layout</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Rows prepare your layout for the grid. They are required in order to use columns. They use negative margins to get rid of the spacing that containers add. That makes sense because if you are going to have columns, you probably want space in between the columns and not at the edges.

You place the content you want inside columns, not rows. the ONLY element that sits inside a row should be columns. Although you can use containers without rows or columns...in order to use columns, you must use rows. Columns won't work properly without rows.

You can use a special class called .no-gutters to remove spacing between rows...just in case you need some columns with no gutter spacing.

---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-th"></i> Columns

- 12 Column Grid
- <span contenteditable>`col(-BP)(-COL)`</span><br>
<small style="line-height: 120%; vertical-align: text-bottom;">
<b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px 
<code style="background:#5cb85c; color:white;">md</code> >768px 
<code style="background:#5cb85c; color:white;">lg</code> >992px 
<code style="background:#5cb85c; color:white;">xl</code> >1200px
</small><br>
<small style="line-height: 120%; vertical-align: text-bottom;"> 
<b>COL:</b> <code style="background:#D95357; color:white;">1-12</code> 	</small>

<iframe class="fragment" height='400' scrolling='no' title='Controlling Bootstrap Columns' src='//codepen.io/planetoftheweb/embed/YedXvr/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/YedXvr/'>Controlling Bootstrap Columns</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

You can place content in a 12 column grid and control how the content is placed into those rows.

Columns can be set to automatically sized using the col class, they can pass along a size at which they'll convert to the full width of the viewport.

Adding a breakpoint to a column definition will determine when the column converts from taking the full width of the device or window.

---

## Column Specs

| |  Extra small <small>< 576px</small> | Small <small> ≥ 576px</small> | Medium <small>≥768px</small> | Large <small>≥992px</small> | Extra large <small>≥1200px</small> |
|---|---|---|---|---|---|
| **Prefix**	| .col- | .col-sm- | .col-md- | .col-lg- | .col-xl- |

### Author Notes

The breakpoints control when a column switches from a taking up the full width of the viewport to optionally a certain amount of column units.

You can assign different column values at differing breakpoints, so this makes this grid extremely easy to use and control.

---

<!-- .slide: data-state="title" -->

# Position/Display

---

## Position
<ul>
	<li class="fragment"><p contenteditable>Position classes</p>
	<small style="line-height: 120%; vertical-align: text-bottom;">		<code style="background:#D95357; color:white;">fixed-top</code>
		<code style="background:#D95357; color:white;">fixed-bottom</code>
		<code style="background:#D95357; color:white;">sticky-top</code>
		</small>
	</li>
	<li class="fragment">`sticky-top` [lacks support](http://caniuse.com/#search=sticky)</li>
</ul>

### Author Notes

Let's talk about the position property. If you are familiar with CSS, this one works just like the regular CSS position property.

There are three options here, you can use a fixed-top or fixed bottom, which just like with the CSS version removes the content from the flow in the current document and attaches them to the top or bottom of the screen. When you do this, you'll probably need to adjust your CSS because the content will float on top of other content. Finally, there's the sticky-top property. That will automatically make certain content stick as it goes past a certain location, but it's not well supported in browsers, especially microsoft browsers.


---



## Basic Display
<ul>
	<li class="fragment">Mimics CSS</li>
	<li class="fragment"><p contenteditable>`d(-BP)-TYP`</p>
	<small style="line-height: 120%; vertical-align: text-bottom;"><b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
<code style="background:#5cb85c; color:white;">md</code> >768px
<code style="background:#5cb85c; color:white;">lg</code> >992px
<code style="background:#5cb85c; color:white;">xl</code> >1200px
<br><b>TYP:</b>
    <code style="background:#D95357; color:white;">none</code>
    <code style="background:#D95357; color:white;">inline</code>
		<code style="background:#D95357; color:white;">inline-block</code>
    <code style="background:#D95357; color:white;">block</code><br>
    <code style="background:#D95357; color:white;">table</code>
    <code style="background:#D95357; color:white;">table-row</code>
    <code style="background:#D95357; color:white;">table-cell</code>
    <code style="background:#D95357; color:white;">flex</code>
    <code style="background:#D95357; color:white;">inline-flex</code>
		</small>
	</li>
</ul>

<iframe class="fragment" height='400' scrolling='no' title='Display/Position Properties' src='//codepen.io/planetoftheweb/embed/PQXqry/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/PQXqry/'>Display/Position Properties</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

The display properties mimic what is possible with CSS and opens up Bootstrap to flexbox classes that can help with layouts.

To use a display class, you use the d- and then the type of display property you want to use. block, inline, inline-block or flex. Flex has a ton of options. We'll cover the basic container in this video and explore it further in the next.

---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-th"></i> Flex Container

<ul>
	<li class="fragment">Container/item classes</li>
	<li class="fragment"><p contenteditable>`d(-BP)(-inline)-flex`</p>
	<small style="line-height: 120%; vertical-align: text-bottom;">
		<b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
		<code style="background:#5cb85c; color:white;">md</code> >768px
		<code style="background:#5cb85c; color:white;">lg</code> >992px
		<code style="background:#5cb85c; color:white;">xl</code> >1200px
		</small><br>
		<small style="line-height: 120%; vertical-align: text-bottom;">
	</small>
	</li>
</ul>

### Author Notes

In order to lay elements with the display flex property you add classes to either the flex container or the individual elements depending on what you need.

Here's the basic formula for the main flex container. You can use breakpoint as well as the optional inline option.

---

## <i class="fa fa-th"></i> Direction

<ul>
	<li class="fragment"><p contenteditable>`flex(-BP)(-DIR)(-reverse)`</p>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
			<code style="background:#5cb85c; color:white;">md</code> >768px
			<code style="background:#5cb85c; color:white;">lg</code> >992px
			<code style="background:#5cb85c; color:white;">xl</code> >1200px
		</small><br>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>DIR:</b> <code style="background:#D95357; color:white;">row</code>
			<code style="background:#D95357; color:white;">column</code>
		</small><br>
	</li>
</ul>

### Author Notes

For controlling direction, we can use a keyword in our container that lets us control wether the content appears in columns or rows. By default the content will appear in side by side rows, but you can also specify a column and control that using breakpoints. You can optionally reverse the direction of the items with the reverse option.

---

## <i class="fa fa-th"></i> Justify

<ul>
	<li class="fragment"><p contenteditable>`justify-content(-BP)-ALG`</p>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
			<code style="background:#5cb85c; color:white;">md</code> >768px
			<code style="background:#5cb85c; color:white;">lg</code> >992px
			<code style="background:#5cb85c; color:white;">xl</code> >1200px
		</small><br>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>ALG:</b>
			<code style="background:#D95357; color:white;">start</code>
			<code style="background:#D95357; color:white;">end</code>
			<code style="background:#D95357; color:white;">center</code>
			<code style="background:#D95357; color:white;">around</code>
			<code style="background:#D95357; color:white;">between</code>
		</small><br>
	</li>
</ul>

### Author Notes

Justifying content lets you control the spacing between items. Like other options you can control them with an optional breakpoint. The alignment options are start, which puts the items to the left and extra space to the right. end, which puts the items to the right and the extra space on the left. Center, which is a great way to center content. Around puts the space around and in between options. Between does something similar but makes the edge elements align to the edge. These will make more sense with an example.


---

## Wrap

<ul>
	<li class="fragment"><p contenteditable>`flex(-BP)-WRP(-reverse)`</p>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
			<code style="background:#5cb85c; color:white;">md</code> >768px
			<code style="background:#5cb85c; color:white;">lg</code> >992px
			<code style="background:#5cb85c; color:white;">xl</code> >1200px
		</small><br>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>WRP:</b>
			<code style="background:#D95357; color:white;">wrap</code>
			<code style="background:#D95357; color:white;">nowrap</code>
		</small><br>
	</li>
</ul>

### Author Notes

Wrap lets you control wether the elements wrap in relation to the space in their container. There's two options either wrap the elements or to not wrap the elements. You can also include an extra keyword to reverse the order of the elements.

---

## Vertical Alignment

<ul>
	<li class="fragment"><p contenteditable>`align-content(-BP)-ALG`</p>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
			<code style="background:#5cb85c; color:white;">md</code> >768px
			<code style="background:#5cb85c; color:white;">lg</code> >992px
			<code style="background:#5cb85c; color:white;">xl</code> >1200px
		</small><br>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>ALG:</b>
			<code style="background:#D95357; color:white;">start</code>
			<code style="background:#D95357; color:white;">end</code>
			<code style="background:#D95357; color:white;">center</code>
			<code style="background:#D95357; color:white;">between</code>
			<code style="background:#D95357; color:white;">around</code>
			<code style="background:#D95357; color:white;">stretch</code>
		</small><br>
	</li>
</ul>

<iframe class="fragment" height='400' scrolling='no' title='Bootstrap Flexbox Container Classes' src='//codepen.io/planetoftheweb/embed/qxLONV/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/qxLONV/'>Bootstrap Flexbox Container Classes</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Vertical alignment does just what you think, controls the alignment of elements vertically. In addition to the breakpoints, the options are to put the elements towards the beginning or the end, center them vertically, put space in between or around and finally stetch the elements to fit the container.

---

<!-- .slide: data-state="title" -->

# Display Utilities

---

## Margin/Padding

<ul>
	<li class="fragment"><p contenteditable>`PRO(SID)(-BP)-SIZ`</p>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>PRO:</b>
			<code style="background:#0275D8; color:white;">m</code> margin
			<code style="background:#0275D8; color:white;">p</code> padding
		</small><br>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>SID:</b>
			<code style="background:#F0AD4E; color:white;">t</code>
			<code style="background:#F0AD4E; color:white;">r</code>
			<code style="background:#F0AD4E; color:white;">b</code>
			<code style="background:#F0AD4E; color:white;">l</code>
			<code style="background:#F0AD4E; color:white;">x</code>
			<code style="background:#F0AD4E; color:white;">y</code>
		</small><br>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
			<code style="background:#5cb85c; color:white;">md</code> >768px
			<code style="background:#5cb85c; color:white;">lg</code> >992px
			<code style="background:#5cb85c; color:white;">xl</code> >1200px
		</small><br>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>SIZ:</b>
			<code style="background:#D95357; color:white;">0</code>
			<code style="background:#D95357; color:white;">1</code>
			<code style="background:#D95357; color:white;">2</code>
			<code style="background:#D95357; color:white;">3</code>
			<code style="background:#D95357; color:white;">4</code>
			<code style="background:#D95357; color:white;">5</code>
			<code style="background:#D95357; color:white;">auto</code>
		</small>
	</li>
</ul>

<iframe class="fragment" height='400' scrolling='no' title='Margin-Padding' src='//codepen.io/planetoftheweb/embed/LQMprB/?height=400&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/LQMprB/'>Margin-Padding</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


### Author Notes

Bootstrap provides a few classes that will let you add margin and padding to different elements. They work just like their CSS counterparts, so this should easily make sense. To activate it, you use a property, then optionally a side. Notice that there is no hyphen between the property and the side like in the other classes. 

The sides are just like in HTML top, right, bottom, left. The x option is for right and left and the y option is for top and bottom. You can optionally add a breakpoint like with other spacing parameters and then a size. The sides are in numbers from 1-5. The base size for each of these is based on a variable that is preset at 1 rem so these are mutiples of that. Using the number 1 means a space of .25rem, two is .5rem, three is 1rem, 4 is 1.5rem and 5 is 3 rem.

---

## Visibility

<ul>
  <li class="fragment"><p contenteditable>`d(-BP)-TYP`</p>
	<small style="line-height: 120%; vertical-align: text-bottom;"><b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
<code style="background:#5cb85c; color:white;">md</code> >768px
<code style="background:#5cb85c; color:white;">lg</code> >992px
<code style="background:#5cb85c; color:white;">xl</code> >1200px
<br><b>TYP:</b>
    <code style="background:#D95357; color:white;">none</code>
    <code style="background:#D95357; color:white;">inline</code>
		<code style="background:#D95357; color:white;">inline-block</code>
    <code style="background:#D95357; color:white;">block</code><br>
    <code style="background:#D95357; color:white;">table</code>
    <code style="background:#D95357; color:white;">table-cell</code>
    <code style="background:#D95357; color:white;">flex</code>
    <code style="background:#D95357; color:white;">inline-flex</code>
		</small>
	</li>
</ul>

<iframe class="fragment" height='400' scrolling='no' title='Bootstrap Controlling Visibility' src='//codepen.io/planetoftheweb/embed/YedyRB/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/YedyRB/'>Bootstrap Controlling Visibility</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Most of the time you'll want to use the display property. Although we already covered it on the movie on display properties, it's useful to repeat it again here. It allows you to change the display of an item using breakpoints and either the keyword none or one of the other regular display properties.



---

<!-- .slide: data-state="title" -->

# Navbars

---

## Navbar Classes
<ul>
	<li class="fragment">`navbar`</li>
	<li class="fragment"><p contenteditable>`navbar-expand(-BP)`</p>
		<small style="line-height: 120%; vertical-align: text-bottom;">
			<b>BP:</b> <code style="background:#5cb85c; color:white;">sm</code> >576px
			<code style="background:#5cb85c; color:white;">md</code> >768px
			<code style="background:#5cb85c; color:white;">lg</code> >992px
			<code style="background:#5cb85c; color:white;">xl</code> >1200px
		</small><br>
	</li>
</ul>


### Author Notes

The navbar is the main component and it can have a number of other elements inside it.

By default, navbars components will stack so we need to add a navbar-expand with optional breakpoints to control when the navbar expands

The simplest component you can use is the navbar-nav, which is our list of links. Just like with navs, you can use the navbar classes with either ULs or with the NAV tag.

---


## Navbar Colors
<ul>
<li class="fragment"><p contenteditable>`bg-COLOR` for backgrounds</p>
  <small style="line-height: 120%; vertical-align: text-bottom;">
  <code style="background-color:#007bff; color: white;">primary</code>
  <code style="background-color:#868e96; color: white;">secondary</code>
  <code style="background-color:#28a745; color: white;">success</code>
  <code style="background-color:#dc3545; color: white;">danger</code><br>
  <code style="background-color:#ffc107; color: white;">warning</code>
  <code style="background-color:#17a2b8; color: white;">info</code>
  <code style="background-color:#f8f9fa; color: white; background-color:gray;">light</code>
  <code style="background-color:#343a40; color: white;">dark</code>
  <code style="background-color:#fff; border: 1px solid black; color: black;">white</code>
  </small>
</li>
	<li class="fragment">`navbar-light`</li>
	<li class="fragment">`navbar-dark`</li>
</ul>


### Author Notes

You can use bg-color classes to change the color of the background navigation just like with other components if you want to use one of Bootstrap's defaults...and you can easily customize your color by changing the background-color css property to whatever you want.

To control the color of the text, you can use navbar-light if your background color is light

Or you can use navbar-inverse if your background color is dark

`<nav class="navbar navbar-light" style="background-color: #C4226F;">`
`<nav class="navbar navbar-dark" style="background-color: #EEC856;">`

---

## navbar-nav Options
  - `navbar-nav` parent
	- `nav-item`, `nav-link`
	- `active`

<iframe class="fragment" height='400' scrolling='no' title='Navbars' src='//codepen.io/planetoftheweb/embed/XZomOV/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 40vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/XZomOV/'>Navbars</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### Author Notes

Just like with navs, we have a few classes to control how links look. You need a navitem on the LI if your using lists or in the anchor tag if your using the NAV tag. You use a nav-link just like with navs to identify the link You can also add an active class to show which page you're on.
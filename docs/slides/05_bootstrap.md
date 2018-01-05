<!-- .slide: data-state="title" -->

# Bootstrap Framework

---
## What is Bootstrap?

- Mobile first framework
- Responsive design
- Battle tested
- Modern web concepts

---

## What’s a Framework?
- A way to organize your code
- If you follow a certain structure…
- A framework gives you many abilities.
  - Pre-built CSS styles
  - JavaScript functionality

---

## Installation: Basic
- CDNs
- Download and install
- Requires jQuery
- [Try it](http://jsbin.com/losegir/4/edit?html,output)

---
<!-- .slide: data-state="title" -->

# The Grid

---

## Grid System
- 12-column grid
- Accessed through CSS classes
- Three key concepts
  - Containers
  - Rows
  - Columns

---


## Bootstrap Containers
- Control layout
- Add padding
- Fluid vs Fixed

---

## Rows

- Horizontal groups of columns
- Place within container
- Should always include columns
- Gets rid of container padding

---

## Grid Columns

- 30px gutters (15px per side)
- <div contenteditable>`col(-BP)(-COL)`</div>
  <small>
    <b>BP:</b> <code class="code-success">sm</code> >576px
    <code class="code-success">md</code> >768px
    <code class="code-success">lg</code> >992px
    <code class="code-success">xl</code> >1200px<br>
    <b>COL:</b> <code class="code-warning">1-12</code>
  </small>
- [Try it](http://jsbin.com/dobahar/2/edit?html,output)

---

## Column Metrics

| |  Extra small <small>< 576px</small> | Small <small> ≥ 576px</small> | Medium <small>≥768px</small> | Large <small>≥992px</small> | Extra large <small>≥1200px</small> |
|---|---|---|---|---|---|
| **Prefix**	| .col- | .col-sm- | .col-md- | .col-lg- | .col-xl- |

---

## Multiple Columns

- Assign multiple breakpoints
- Column adjusts depending on breakpoint  
- [Try it](http://jsbin.com/jemuhin/2/edit?html,output)

---

## <i class="fa fa-th"></i> Basic Display
<ul>
- Mimics CSS
- <div contenteditable>`d(-BP)-TYPE`</div>
<small><b>BP:</b> <code class="code-success">sm</code> >576px
<code class="code-success">md</code> >768px
<code class="code-success">lg</code> >992px
<code class="code-success">xl</code> >1200px<br>
<b>ALN:</b>
<code class="code-warning">none</code>
<code class="code-warning">block</code>
<code class="code-warning">inline</code>
<code class="code-warning">inline-block</code>
<code class="code-warning">flex (options)</code>
</small>
---

## <i class="fa fa-th"></i> Margin/Padding

<div contenteditable>`PRO(SID)(-BP)-SIZ`</div>
<small>
  <b>PRO:</b>
  <code class="code-primary">m</code> margin
  <code class="code-primary">p</code> padding<br>

  <b>SID:</b>
  <code class="code-primary">t</code>
  <code class="code-warning">r</code>
  <code class="code-warning">b</code>
  <code class="code-warning">l</code>
  <code class="code-warning">x</code>
  <code class="code-warning">y</code><br>

  <b>BP:</b> <code class="code-success">sm</code> >576px
  <code class="code-success">md</code> >768px
  <code class="code-success">lg</code> >992px
  <code class="code-success">xl</code> >1200px<br>

  <b>SIZ:</b>
  <code class="code-danger">0</code>
  <code class="code-danger">1</code>
  <code class="code-danger">2</code>
  <code class="code-danger">3</code>
  <code class="code-danger">4</code>
  <code class="code-danger">5</code>
  <code class="code-danger">auto</code>
</small>

---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-th"></i> Basic Flex Container

- <div contenteditable>`d(-BP)(-inline)-flex`</div>
<small><b>BP:</b> <code class="code-success">sm</code> >576px
<code class="code-success">md</code> >768px
<code class="code-success">lg</code> >992px
<code class="code-success">xl</code> >1200px
</small>
- [Try it](http://jsbin.com/jemuhin/7/edit?html,output)

---
<!-- .slide: data-state="title" -->

# Navbars

---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-bars"></i> Navbar Classes
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
	<li class="fragment">`navbar-nav`</li>
</ul>

---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-bars"></i> Navbar Colors
<ul>
<li><p contenteditable>`bg-COLOR` for backgrounds</p>
  <small style="line-height: 120%; vertical-align: text-bottom;">
  <code style="background:#007bff; color:white;">primary</code>
  <code style="background:#868e96; color:white;">secondary</code>
  <code style="background:#28a745; color:white;">success</code>
  <code style="background:#dc3545; color:white;">danger</code><br>
  <code style="background:#ffc107; color:white;">warning</code>
  <code style="background:#17a2b8; color:white;">info</code>
  <code style="background:#f8f9fa; color:black;">light</code>
  <code style="background:#343a40; color:white;">dark</code>
  <code style="background:white; border: 1px solid gray; color:black;">white</code></small>
</li>
	<li class="fragment">`navbar-light`</li>
	<li class="fragment">`navbar-dark`</li>
</ul>

---

<!-- .slide: data-state="hasicon" -->

## <i class="fa fa-bars"></i> navbar-nav Options
- `nav-item` & `nav-link`
- `active` & `disabled`
- [Try it](http://jsbin.com/gezaneh/3/edit?html,output)
- [Custom Color](http://jsbin.com/gezaneh/2/edit?html,output)
-


---
<!-- .slide: data-state="title" -->

# Carousels

---

## Basic Carousel

<ul>
	<li class="fragment">`carousel`</li>
	<li class="fragment">`data-ride="carousel"`</li>
	<li class="fragment">`carousel-inner`</li>
	<li class="fragment">`carousel-item`</li>
</ul>

> > Speaker Notes:
1. The main container to use is of course carousel
1. If you want the carousel to automatically animate when the page loads, use data-ride="carousel", there are a lot of other options you can activate using data attributes or javascript...more of that in a sec.
1. carousel-inner is the main container for the images
1. carousel-item is a wrapper for each image.

---

## Options

<ul>
	<li class="fragment">one element `active`</li>
	<li class="fragment">Crop and size photos</li>
</ul>

> > Speaker Notes:
1. At least one of the carousel image containers should have a class of active.
1. Also, bootstrap is not going to perform any sizing on your images, so make sure you crop and resize your images. You may also need to size your images using css.

---

## Captions
<ul>
	<li class="fragment">`carousel-caption`</li>
</ul>

```
<div class="carousel-caption d-none d-md-block">
  <h3>...</h3>
  <p>...</p>
</div>
```
<!-- .element: data-trim="true" contenteditable="true" class="fragment" -->

> > Speaker Notes:
1. There is a special class for captions called carousel-caption.

---

## Navigation

<ul>
	<li class="fragment">`data-target`</li>
	<li class="fragment">`carousel-control-prev`</li>
	<li class="fragment">`carousel-control-prev-icon`</li>
	<li class="fragment">`carousel-control-next`</li>
	<li class="fragment">`carousel-control-next-icon`</li>
</ul>

> > Speaker Notes:
1. You can add previous and next icons on the images using classes.

---

## Indicators

<ul>
	<li class="fragment">`carousel-indicators`</li>
	<li class="fragment">`data-target`</li>
	<li class="fragment">`data-slide-to`</li>
</ul>

> > Speaker Notes:
1. You can also add indicators. They look very different from the old indicators, but are just easy to set up.

---

## Data Attributes

<ul>
	<li class="fragment">`interval` : 5000</li>
	<li class="fragment">`pause` : hover | null</li>
	<li class="fragment">`ride` : false</li>
	<li class="fragment">`wrap` : true</li>
</ul>

---

## Try it

- [Try it](http://jsbin.com/butuwud/2/edit?html,output)

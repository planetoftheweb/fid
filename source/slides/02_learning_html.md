<!-- .slide: data-state="title" -->

#Learning HTML

---

<h1>What is HTML?</h1>

- HyperText Markup Language
- Hypertext
- Markup

### Author Notes

HTML stands for HyperText Markup Language and is the language that powers the web. You can break what HTML means into two parts. First is HyperText and then the markup language. Let's talk about those two things.

HyperText is a document that can be linked to other related documents. Since documents are linked to each other, it creates a web of links that we know as the world wide web.

HTML is called the Markup Language. Markup is special syntax for annotating a document. Think of markup as what your english teacher would do to a document when they correct it. They would 'mark it up' with corrections that need to be done.

---

## Semantic HTML
- One of three
- [Defines structure](https://www.lynda.com/HTML-tutorials/What-web-semantics/182177/370807-4.html)
- Never include layout
- HTML critical

### Author Notes

HTML is one of the big three core languages needed to build ANY web page. They are HTML, CSS and JavaScript. HTML is easily the most important of the three and is in chrage of defining the structure of a page. CSS controls how a page looks and JavaScript controls how users can interact with a website. Without proper HTML, the other two languages won't work.

One of the most important jobs for HTML is to focus on the semantics of your document. Semantic means adding meaning to the content of your page.

Every HTML page has three different parts to it. First, is the structure of the document, which is defined by the markup that you use to add meaning to your page. That's what we're talking about today. The second is the styles or CSS that can add the look and feel of the document and the last is the JavaScript that adds interactivity to your pages.

It's critical that you let each component or part handle the job it's designed for. So it's crucial that you NOT add anything that is not markup to HTML. Certain html markup will make certain things look at certain way, but what's really important is that you focus on adding meaning, not looks to your document using HTML.

HTML is the most critical of the three components. If you mess up the structure of the HTML, then neither the styles will work or the interactivity.

---

## Tag Structure

```html
<element [attribute[='value']...>content[</element>]
```
<!-- .element: style="width:70%" -->

- [element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) name
- 0-&infin; attributes
- No order in attributes

### Author Notes

You start HTML tags using the less than and greater than signs with an element name inside. You can use a number of elements inside the greater and less than signs. There are hundredths of elements and the best place to find them is to look online on this MDN website.

Inside the first part of the element you can add none or an infinite number of attributes. These attributes will provide additional information to the browser about the tags you're using. For example, to create an image, you use the `<img>` tag, but it doesn't make sense to add an `<img>` tag without telling the browser the location of the image, you do that with a `src` attribute.

---

## Standalone vs Container
<iframe height='500' scrolling='no' title='zdmGxJ' src='//codepen.io/planetoftheweb/embed/zdmGxJ/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>>See the Pen <a href='https://codepen.io/planetoftheweb/pen/zdmGxJ/'>zdmGxJ</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>



- Inserts vs wraps

### Author Notes

Standalone tags like the `<img>` tag are simply there to insert some element like an image into your page.

Container tags are designed to wrap some other text or elements, so they change the meaning of what you place in there.

---

## Heading Elements

<iframe height='300' scrolling='no' title='rzqaEv' src='//codepen.io/planetoftheweb/embed/rzqaEv/?height=300&theme-id=27192&default-tab=html,result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true'  style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/rzqaEv/'>rzqaEv</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

- [Denote Importance](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements)

> > Author Notes

The heading elements are pretty important in HTML, they help you create headings for your document.

There are six heading elements and they are containers, so they need beginning and ending versions of the tags. The number denotes importance, so a H1 is more important than an H2 and so on.

You should use these to define the level of importance of the headlines in your content. Think of it like a book, the H1 would be the title and the H2 could maybe be chapter titles.

---

<h1>Compound Tags</h1>

<iframe height='300' scrolling='no' title='BdqNzQ' src='//codepen.io/planetoftheweb/embed/BdqNzQ/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/BdqNzQ/'>BdqNzQ</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

- [Lists](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul): [`<ol>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol), [`<ul>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul), [`<dl>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl)

> > Author Notes

Some tags like the list tags are considered compound tags because they require two sets of tags. One that defines the type of list and another that identifies the different elements within the list.

In the case of lists an OL means that the order of the list items denotes some sort of order like in military ranks. An unordered list means that the list elements are in no particular order like when you make a list of groceries.

---

# Block Level Elements

<iframe height='300' scrolling='no' title='EvdjRz' src='//codepen.io/planetoftheweb/embed/EvdjRz/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/EvdjRz/'>EvdjRz</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

[Major Sections](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements): [`<h1>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements), [`<p>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)

### Author Notes

A block-level element occupies the entire space of its parent element (container), thereby creating a "block."

Are usually formatted in a new line before and after the tags by browsers

Think of it as a stack of boxes or big containers.

---

## Inline Elements

<iframe height='300' scrolling='no' title='wqYaYP' src='//codepen.io/planetoftheweb/embed/wqYaYP/?height=300&theme-id=27192&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='height: 50vh; width: 100%;'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/wqYaYP/'>wqYaYP</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

[Inline Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elemente): [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a), [`<em>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em)

### Author Notes

Inline elements occupy the space that are bound by the parent or container tag, they don't break the flow of content. They are often placed inside block level elements.

---

<h1>Basic Page</h1>

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>UPDATE TITLE</title>
</head>
<body>

<!-- content goes here -->
<h1>Headline</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores vel vitae temporibus aliquid deleniti id culpa soluta natus, corrupti eaque neque et ratione. Laudantium earum assumenda beatae aspernatur id est.</p>
<!-- content goes here -->

</body>
</html>
```

- [`<DOCTYPE>`](https://developer.mozilla.org/en-US/docs/Glossary/Doctype), [`<html>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html), [`<head>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head), [`<meta>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta), [`<title>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title), [`<body>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body)

### Author Notes

Every page needs to have a basic page structure using these elements.

The [`<DOCTYPE>`](https://developer.mozilla.org/en-US/docs/Glossary/Doctype) element defines the version of HTML that you're using.

The [`<html>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html) element is the container for your entire document.

The [`<head>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head) element has content that you want the browser to load first and is for information that you want your browser to know about, but not necessarily be displayed to the user.

The [`<meta>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta) element is a generic tag that you can use to pass certain information about your page to your browser. in this case we're passing along the `charset`, which is the types of characters used on this page. In this case it's roman letters with accent marks, but you can use a different charset for japanese or other alphabets. The viewport meta tag tells the browser that this page has been designed with mobile devices in mind.

The [`<title>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title) element displays the title on the window menu of the current page in most browsers. It's also important for search engines.

The [`<body>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body) element is where all of the content you want your user to be able to see goes.

---

## Resources

- **Saving**: `index.html`
- **Validator:** <a href="http://validator.w3.org/">Checks for errors</a>
- **Atom Packages:** emmet, linter, atom-live-server, linter-htmlhint, html-entities, linter-csslint, emmets-snippets-compatibility
- [Sample Resume](https://gist.github.com/planetoftheweb/2ee375e7ddb8034f8169ab9a44e77dd0)

### Author Notes

When saving HTML documents you need to use the `.html` or `.htm` exension. You can save yourself and your visitors some time by using a special name for your main html document. If a document is named index.html, then the browser will assume it's the default document for that folder.

So, for example, if you've placed a document called `resume.html` in a folder called `htmlresume` in your projects folder...and your site is called `mysite.com`, then the URL to this document would be: `http://mysite.com/projects/htmlresume/resume.html`, however, if you name your document `index.html`, then you can leave the last part out. So your document would be acessible at: http://mysite.com/projects/htmlresume. It's a bit shorter and easier to remember.

The validator is a way to check that there are no errors in your document structure. **ALL HTML PROJECTS MUST VALIDATE**

To make your life easier, you can install a few Atom packages, they are like extensions to Atom that can provide some extra features.

Here's a sample resume text so that I can practice creating the sample assignment with you in class.

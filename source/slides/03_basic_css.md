<!-- .slide: data-state="title" -->

# Basic CSS

---

## Default Styles

So far, we've been creating pages without using stylesheets and while it may seem like we're creating sites without any styles and that's really not the case at all. Every browser has a default set of styles called the user agent stylesheet (aka Default Browser Styles) that are in charge of how a page looks when it doesn't have any other styles. So it makes things like control the basic differences between the sizes of H1 and H3 tags and the spacing after paragraphs. Each browser has it's own version of this default stylesheets and although they're pretty similar, they can have some major differences like the default font used.

So when you create your own stylesheets, you're not starting from scratch. You're removing, revising or overriding existing sytles. As a matter of fact, some browsers allow you to override certain defaults like the size of your font if you want to make things more readable.

---

## Inline, Internal and external CSS

There are three ways to add CSS to an HTML page. The first option is the external method. The CSS is in a separate file with a .css file extension. It's always added within the <head> element and uses a <link> tag and two attributes. Rel for relationship with a value of stylesheet and the href attribute to link to the actual CSS file. This is a void element, so it doesn't need a closing tag. You may have seen this snippet with another attribute, type with a value of text/css.

This was required in previous versions of HTML, but HTML5 is backwards compatible, meaning it will work with the older syntax as well. But my rule of thumb is if you don't need it anymore then just leave it out. But if it's there it doesn't hurt either. This method is recommended because it separates the CSS from the HTML document. It can also be added to any HTML page, so when the CSS file is updated, it will be reflected on all the HTML pages.

Let's go over the pros and cons of the other two methods. Inline CSS can be added to any HTML element with the style attribute. The CSS property is added as the value. This technique should be avoided because it's inefficient. Let's say you want to make all of your paragraphs blue. You would have to add that style attribute to every single paragraph tag. What if you had 50 paragraphs? That would not be fun to update. Also, if you use the same CSS property and selector in your general style sheet, inline styles will take precedence and override it.

The goal of CSS is to try to keep it flexible and as maintainable as you can. Internal CSS uses the <style> tag and it's also included in the <head> element. All the CSS rules are added between the opening and closing style tags. This tells the browser that this block of code is CSS and not HTML like the rest of the page. While this method is more flexible than inline, it still can be inefficient. If you had multiple HTML pages, you would have to copy this style block to every single page to duplicate the styles.

The internal CSS can also take precedence over an external style sheet, but only if it's added after the external style sheet. The order of the CSS declarations matter and will be discussed in more detail in an upcoming lesson. If you had a couple specific styles for a particular page, this method may come in handy, but there are other, more efficient CSS techniques for handling this scenario. As we progress through this course, you'll see that there are often different ways to do the same thing.

I'll be sure to go over best practices to help you decide which option works best for each scenario.

---

## CSS Syntax

Now that we have all our files in HTML ready to go, let's dive into CSS. It's a different language from HTML, so it has its own syntax rules. CSS is used to add styles and separates the presentation from the content. You may have seen HTML tags in the past that we used for styling, such as the classic blink or center tag. These presentational HTML tags have been deprecated and are no longer officially supported by modern browsers.

Selectors are used to determine which HTML element to apply the styles to. Declaration blocks contain the style rules, they are wrapped in curly braces to contain these styles to the specific selector. The declarations are the style rules, and are written using property:value; pairs. The property name is followed by a colon and ends with a semicolon, to indicate that the rule is complete. Properties determine the type of style to be applied to the element.

And values are specific to that property, and will vary depending on the property type. Let's take a look at the TESSy access that we had added to our project in the previous exercise. Body is the selector, and it selects the entire page because the body tag represents the viewable area in the browser, also referred to as the view port. Background is the property, which is used to change the background styles of the element. And lightblue is the value, which changes the background property to that specific color.

Just like HTML, use whitespace and tabs for readability. Each declaration can be written on a separate line, and tapped in the visually see which styles belong within each declaration block. I'll be going over more CSS properties throughout this course, but there are so many to explore. So it's good to have a few go to resources to keep on hand. Two of my favorite resources are Codrops and the Mozilla Developer Network. Codrops CSS reference is nicely organized and very detailed.

The write up for each property contains extensive information and examples. The Mozilla Developer Networks reference is also pretty great. It's not as detailed, but still contains important information, such as syntax and browser compatibility, makes it a useful resource for quick referencing.

---

## Type, Class and ID selectors

There are many CSS style properties and different ways to apply them. But at it's most basic, CSS is just selecting the HTML element and applying a style to it. Let's start with taking a look at type selectors. Type selectors match the HTML by using the element name. Without the angled brackets. For example, to apply styles to an h1 tag, h1 would be the selector. The styles will then be applied to all elements that match this selector pattern.

But what if you wanted to apply the style to just one or two h1 elements? When type selectors are too general there are two attributes that can be used to attach extra information. Class and ID. Remember, attributes always follow the same syntax. Attribute name equals value in quotes with no spaces. They can be added in any HTML element and always in the opening HTML tag. Class attribute values can be named anything and defined by you.

The class can be used multiple times on the same page to apply the style to any HTML element that contains the attribute. The value is then used as the selector, starting with the leading period to distinguish it from the type selector. Classes are useful for creating styles that can be reused throughout the document. Just by adding the class name to a specific element. ID attributes are similar to class because it can also be given any value and at it's any element.

However, ID's can only be used once per page and must have a unique value. ID selectors can never match more than one element in a single document. In CSS ID selectors are denoted by a leading number symbol. When choosing a class value, do not use spaces. Because theses spaces actually indicate that there are multiple classes. You can apply different styles to each class and they will be independent of each other.

Dot style refers to just the style class and dot name refers to just name. If you combine them like in this third example, with no spaces, this style will only be applied if the attribute contains both class names. Multiple ID's cannot be used in the same HTML element.

---

## CSS Selectors

Let's look at a few more ways to select elements. When an element is nested inside of another element, it becomes its child or descendant. In CSS, you can select these elements based on this relationship by using descendant selectors. Use multiple selectors separated by a space to match descendant elements. For example, to select the link contained within a paragraph, the selector is P space A. Browsers read these selectors from right to left, so we'll first look for the A tag, which is the hyperlink element, then an A tag inside of a P tag.

Descendant selectors can be used for any nested element. Not just parent child elements. Let's take a look at this example in another JSFiddle. Let's follow the instructions in the HTML comments on the left. The first one says to select all h2 elements on the page. So for this, I can use a type selector of h2. Open my curly braces, and I'll just add a color value.

And run the code. So I've selected all h2s. Number two says to select the h2 only within the section element by adding section space h2. This style will now only be applied to headings within the section element, and let's run it. And there you go. Now if we wanted to select the h2 anywhere within the main element, we can do that by changing this descendant selector to main h2.

Both the h2s in the section tag and the article tag are both descendant elements of main. To select the h2 anywhere within the main element, I can use main as the selector instead of article or section, since they are both descendants of main. This selector won't affect the h2 in the header element. You can use more than two selectors to match descendant elements. Here's another example. Section space P space A will select a link nested inside of a paragraph inside of a section element.

The more selectors you use, the more specific the pattern becomes. This style would not apply to the link outside of the paragraph or outside of the section element, since it doesn't match the specific selector pattern. You can also target multiple elements by grouping them in one declaration block. This will apply the same style to all of the selectors in the list. Each selector is separated with a comma. Grouping selectors is good for creating more efficient CSS because it reduces the number of declarations.

It's also easier to update just one declaration block. When multiple selectors are combined in one block, each selector is still independent of each other. If using a descendant selector, always declare the full combination. Let's talk about one more type of selector, pseudo-classes. Pseudo-class selectors are keywords used to target a specific state of the element. The keyword is combined with a selector using a colon and no white space before or after the colon.

Hover is a common example, since it's often used to style links on mouse hover to indicate to users that it's a link. In this example, this style will only apply when you hover over the link. There are more pseudo-classes that can be used with links. Let's take a look at some examples back in JSFiddle. In HTML 5, it's valid to use the anchor tag as a placeholder by not including the href value. Notice that the default styles between the two are different.

You can use A as the selector when styling links, but if you need to make a distinction between the two, use the link pseudo-class to be more specific to anchor tags with an href value. Let's uncomment each value to see how it's applied. A keyboard shortcut for adding or removing comments is control, forward slash on a PC or command and forward slash on a Mac. So I'm going to uncomment this style from the A selector first.

And run the update. This changes the color for all links. But if I wanted to specify only links with the href value, I would use the link pseudo-class. Uncomment that and run the code. Notice that this style only applies to the links with the href values. Sometimes you'll also see a number symbol in this href value. That is also commonly used as a placeholder, but still includes the href attribute.

Most of the time, you should be okay with just using A as the selector for links, but the link pseudo-class is an option if you need to be more specific. Another pseudo-class that can be used with links is visited. Visited indicates whether the link has been clicked on already. Let's go ahead and uncomment that and run the code. You won't see a change yet because we haven't clicked on any links, but once you do, you'll see a change to the new color.

Notice that the background color has only changed on links one through four, and that's because the href value is the same for all four. Link five has a number sign in it, five. Even though I only clicked on one link, it will show as visited because they have the same href value. Another pseudo-class that can be used with links is active. And this describes the moment that you press on the link. Let's uncomment that and try it out.

Now when I click on it and I haven't released the mouse click yet, you will see the style. Then as soon as I release the mouse, it goes away. As mentioned previously, hover is for changing styles on mouse hover. So let's go ahead and uncomment that. And run it. So now when I hover over the links, the background color goes to none. But hover can actually be used on any element, not just links.

So let's add this to our paragraph here. Run it, and there you go. There is one more pseudo-class that can be used with links called focus. And this is for users that use the keyboard tab to navigate web pages rather than the mouse. The default focus looks like this. This blue, glowing outline. The may vary on different browsers, but you can update it with the outline property.

Uncomment this here, on a focus and run it. And now, when I tab through the links, we can see our new styles. Focus can also be used on other elements, as well. Such as this text input that's commonly used with forms. Let me just add the style to this block. Input, colon focus, run the code.

When I click on the input box, we can now see our new focus style. For accessibility reasons, you should not remove the focus outline without replacing it with a suitable alternative style. You want to make sure that the user still sees a visual representation of selecting the link when using the keyboard to navigate. There are more types of selectors, but this gives us a lot of options for adding styles to our final project.

---

## RGB, Hex and Keyword Color Values

So far, we've been using the color property with keyword values but there are also other types of color values. Hex codes always start with a number sign followed by six characters, a combination of the letters A to F and the numbers from zero to nine to define the colors. RGB stands for red, green, and blue and each number represents a value on a scale between zero and 255. These three value types can all represent the same color, though with RGB or hex codes, there are more colors to choose from.

You can find these values in image editing software like Photoshop. There are also many online tools, let's take a look at a few resources. One of my favorite resources is colors with a you .neilorangepeel.com. I like this resource because it lists all of the available keywords as well as the corresponding hex codes and RGB values. Coolors.co is another useful resource because it also generates color pallettes. Select Start the Generator to open the tool.

It'll take a moment to load and once it does you can also select the spacebar to generate a new pallette. Hover over the color bar for more options. Accessibility is also something that should always be considered, here is another resource specifically focused on color combinations that provide contrast between a background color and the text. In the final project, we'll be using four different colors to add a background color to the various sections of the page and for the links.

This is my color pallette. If you'd like to follow along with the upcoming examples, take a moment to pick a color pallette of your own or just follow along with these colors.

---

## Cascading Inheritance and Specificity

In the last exercise, I put the general styles at the top of the CSS file. That's because CSS executes from top to bottom so the order of your declarations can affect how the browser reads it. If the selector is the same, the declaration that comes after overrides the one that comes before. You might by thinking, why would I use the same selector twice? This is actually quite a common error. As your CSS files get bigger and longer, you may forget that you've already declared the selector and add it again.

That's why organizing the CSS interrelated blocks, like in the previous exercise, can help reduce these types of errors. The Cascade Rule also applies to CSS declarations written within the same declaration block. One of the strengths of CSS is the styles can be inherited from the ancestor to descendant elements. This makes it easier to apply a style to several elements with one line of code, rather than defining the style for each element.

However, there are some properties that won't be inherited by all elements. Let's see this in action in another JSFiddle example. If I add the color property to the parent selector by uncommenting this line and running the code, this style will be inherited by the h1 and the paragraphs, but not the link. Let me change that to another color, just so that we could see it a little more clearly. Let's try blue. There we go.

We can see that link is a different color still. Links will not inherit this color because it already has a specific default style. So to change the color of the links, you'll have to select it directly to specifically change its default style by using A as its selector. Let's give that a try. A, open the curly braces, and we'll give it, let's do yellow. Now it's overriding the style because it's a more specific selector.

There are also some other CSS properties that are not inherited by any element. The W3C has a full table listing of which properties can and can't be inherited. There's a little note at the bottom that there has been some updates to the specifications, but if you click on the link, there isn't another table in the new specifications. So you can still refer to this one for a general idea. However, instead of trying to memorize this entire list of properties, you could also just test it out.

Try adding the style to an ancestor selector, and see if the descendant elements take on the style or not and that should give you your answer. Specificity determines which CSS rule is applied by the browsers. Every selector has a ranking in the specificity hierarchy. The selector with the higher specificity will be applied, regardless of the order of the CSS. The order only matters if the ranking of the selector is the same. This can get a little bit tricky.

The ranking is based on what type of selector you're using. Of the simple selectors we've discussed so far, Type selectors have the lowest specificity and IDs have the highest. Let's a take a look at another example in JSFiddle. Right now, the style is set by the Type selector. But if I add the Class selector style back in, it will override the Type selector. Classes have a higher ranking than Type selectors, but IDs have the highest ranking of the three.

So if I add this style back in, it will override both the Type and Class selectors. In addition to the type, there are other factors when calculating specificity, such as the number of selectors and the combination. You can find the full documentation on the w3.org site, but here are a couple other resources that provide some more entertaining visualizations. CSSSpecificity.com uses icons based on the movie The Shining.

It lists the rankings of each of selector, as well as rankings for the various combinations of selectors. Notice these numbers right here. This is how specificity rankings are calculated. Let's take a look at one more resource, a specificity calculator. You can put selectors into this tool to compare the rankings. Let's add a simple Type selector in this first block. Let's go with A. A has specificity calculation of just one.

If I was to add div space A, using a descendant selector, this specificity calculation has gone up to two. So using a descendant selector has a higher specificity rating than a single, simple selector. So any styles here in div A will override the styles using just A. And if I was to add another descendant, let's say I use div space P A, now this ranking is higher because it has three selectors.

But if I change this selector to a Class, lets go with example A, Classes have a higher ranking. So even though there are only two elements in this descendant element, this now has a higher ranking than div P A. A good rule to stick to when writing CSS is to start with general styles using Type selectors. Then make it more specific as needed using descendant selectors, or Classes and IDs, and follow the selector best practices.

---

## Web Fonts

In the previous lesson, we talked about web-safe fonts. For more options, you can use web fonts. Because it doesn't require users to have fonts installed, we're not limited to only web-safe fonts. There are two methods: using an internal or external source. Internal font sources refer to downloaded font files, included in your project's directory just like any other file. Before you can use internal fonts in the CSS, you'll need to declare it within your style sheet and link to the font files using a method called @font-face.

Font-face is used to setup the font name and link to your font files. It starts with an at symbol, then font-face. The first declaration is font-family to declare the font name. You can use any value here, but it makes the most sense to give it the same name as the typeface. Next, use the src property to link to the actual font files. The syntax has to follow exactly what's listed here. Url, parentheses, and the exact name of the font file.

Sometimes when you download assets like fonts or images, the file names may not be descriptive. I would recommend renaming the files following the naming conventions discussed in the earlier lessons, just to stay organized. Once you've declared the downloaded font in your font-face declaration, you can add it to the font stack just like any other web-safe font. Let's take a moment to review navigating file directories. Previously, we talked about linking to files from the HTML page, making index.html the starting point.

To link to files in either the CSS or images folder, just add the folder name followed by a forward slash, then the file name. Now let's say you have a folder called fonts to organize all of your font files. Styles.css is now your starting point, since you're adding the font-face declaration to the CSS file. This file is inside of a folder, so you'll have to navigate up and out of it first. The first step is to use a ../ to move up and out of the CSS folder.

Then add fonts/ to move into the fonts folder, then the font file name. The ../ is always used to move up and out of a folder regardless of the folder name. Going into a folder is always defined by the folder name. Different browsers support different file formats. For most browsers, the WOFF and WOFF2 formats are supported. To list multiple font files, add a comma between each URL value. To learn more about font-face and support for older browsers, check out this article by CSS-Tricks.

There are detailed examples for different levels of browser support, if you need to support older browsers. If you don't have these different file types, fontsquirrel.com has a free font generator. Click on the Generator tab. Upload the font file that you do have, and it will use that file to generate all the different file types. Fonts have various licensing guidelines for its usage, so be sure to go over any included read me files or licensing info before using it.

The second option for using web fonts is using an external source, which are third-party services. With this option, you don't need to download any files, or include them in your project's directory. You can link directly to their font CSS files which are hosted online as part of the service. There are paid services such as Typekit that will give you access to high quality fonts. If you're looking for a free option, Google Fonts has a fairly good selection.

You can browse through the page and filter by these different categories, and if you know your font name, you can also just do a search here. Click the plus icon to add the font to your collection, or select the minus icon to remove it. Your selections are added to the drawer at the bottom of the page. There's no limit to how many fonts you can use, but using too many will slow down the page load, and two fonts is pretty standard, maybe three depending on the complexity of your design.

We'll be using Google Fonts in the upcoming exercise, so I'll go into more detail about using this service in that lesson. For now, take a moment to choose two Google or web-safe fonts for your project or just use the same as my sample project. I'll be using Open Sans, and Caveat.

---

## Font Size Property

In CSS there are different units for specifying the font size. Some are relative values and some are absolute values. When a relative unit is used, it is calculated in relation to the parent or nearest ancestor's font size. Absolute values are not affected by ancestor elements. Both relative and absolute font sizes are inherited by descendant elements. Let's take a look at how to use some common font sizing values. Screens are measured in pixels, so this is a common and straightforward way to define measurements in CSS.

Pixels are absolute values and is great for accuracy and gives you fine grain control over your design. Different browsers interpret decimal values inconsistently. Some round up, some round down, this mostly effects older browsers but it's convention not to use decimal points when using pixels. The default size of body text like paragraphs and lists are equivalent to 16 pixels. Headings are bigger or smaller depending on which heading level you use.

Named after the letter M the em unit has historically been used to measure horizontal widths. But now refer to the height of the font. Em is a relative unit, so that means it's sized in relation to its closest ancestor's font size. One em is equal to its inherited font-size. Declaring a font size value to an ancestor element will change that, but if no font size is declared anywhere, then one em is equal to the default browser font size.

Let's take a look at an example. If no font size is declared in the parent element, then adding one em to the paragraph will equal the browser default. There will be no difference when I add this style. If I change it to 1.5 em then it'll be one and a half times the size of the inherited font size and we comment this out and add this one in. If a font size is declared in the ancestor or parent element, the paragraph will then be sized relative to its parent, let me add in two em in this div selector.

Now the paragraph is one and a half times the size of the div element. You can actually mix sizing units as well. Instead of two em's in the div, if I add a font size of 20 pixels here, the paragraph is now one and a half times the size of 20 pixels. If you want the font size to be smaller, use values that are less than one. For example, .5 ems just means that I'll be half the size of its inherited font size.

It can get a little tricky using em's but unlike pixels since it's common to use decimal points for em values, this will help you calculate a more precise font sizing. Introduced around 2011, rem is a newer unit than em, that's similar in usage. One rem is equal to one em. The one key difference is rem is only relative to the root element, which is the HTML element. When this unit was first introduced, older browsers like Internet Explorer 8 was still in use and didn't support it, but now all browsers do.

Let's take a look at an example. In this example, I've already set up a base font size in the root element, the HTML. If I set the paragraph to one em it will equal its inherited font size, right now it's equal to the 30 pixels set in the HTML selector. Now if I set a font size in the div, which is a closer ancestor element than HTML, the em will be sized relative to that.

Now if I change one em to one rem instead, it will be sized relative to the root element, which is the HTML. So this is the one main difference between em's and rem's with rem even though there's a font size here declared in its parent element, it will always be relative only to the HTML. There are quite a few more length values that can be used for font sizing, these same values can also be used for other properties that require a sizing value such as width and height.

Codrops has an extensive write up of all the length measurements, usage, syntax, browser support, pros and cons. If you're just getting started with CSS, pixels are a good way to get up and running. I'll be using pixels for font sizing for the remainder of the course exercises.

---

## Font Style, Font Weight

So far, we've talked about font family and font size, but there are actually more font properties. Font families often include different typefaces with varying amounts of thickness, called font-weight. The values for font-weight can be defined with numbers ranging from 100 to 900. 100 is the lightest or thinnest of the fonts, and 900 is the darkest or thickest. Most font families don't come with different typefaces specified for all nine weights. If that's the case, if a weight is specified in the CSS that does not have a corresponding typeface, it will map to the nearest weight available.

Keywords can also be used and are mapped to the font-weight numbers. Normal is the default for body text, and it's equal to 400. Bold is the default for headings, and it's equal to 700. There are two more keywords, bolder and lighter. These values are relative to the inherited font-weight. And here's a table to show how lighter and bolder map to its inherited value. Font-style is a property that can be used to add or remove an italic style. There are three values: italic, oblique, and normal.

Italic fonts tend to appear slightly more cursive, while oblique faces are generally just sloped versions of the regular face, though the differences tend to be small. The normal value removes an italic or oblique style. If you choose a font family that does not have a specific italic or oblique typeface, the browser will simulate it by sloping the regular font face glyph. There are a lot more font CSS properties, but in this course we're focusing more on the commonly used properties to get you up and running with CSS.

If you'd like to view some of the more advanced, less commonly used font properties, check out the Mozilla developer network reference, which is categorized into related CSS properties.

---

## Color, line-height and text

There are more typography-related properties that don't begin with font. There's one that we've seen already in previous lessons, color. Here's a quick review. Color changes the text color and uses a variety of values, keywords, hex codes and rgb being the most common. The line-height property is used to set the height of space between the two lines of content. For example, the spacing between the lines in a paragraph. This style should be considered when setting font sizes since they are closely related.

The value can be declared using the length values discussed previously for other properties, but line-height also accepts a unitless value. Let's look at an example. If the line height is set to the same value as the font size, there will be no space between the lines which would make it hard to read, so as a rule of thumb, your line-height value should always be larger than the font size to add space between the lines. Let's try 20 and see how that looks.

Now if I change the font size to make it smaller or bigger, its going to effect the line height. If I set it to 20, now the line height and the font size is the same again. To make the line height more flexible to change, use relative units for the line-height property instead. Using a relative sizing like percentage will keep the line height consistent, because it'll always be relative to the font size. If I set it to 150%, it will always be one and a half times bigger than the font size.

So if I change the font size again, the line height will be relative. Let's put that to 20. Line-height also accepts a unitless value, so instead of 150%, I can set it to just 1.5, and that also means a one and a half times the size of the font size. If I set it to one, that means it will be the same. The unitless value is actually my preferred method.

You can choose whichever you'd like, but using a relative unit will keep it more flexible. In an earlier exercise, we used text-decoration to remove an underline from a link. It can actually be used to add underlines as well above, below or even a strike-through line right through the text. You can remove the existing underline by setting it to none. The text-transform property specifies the letter casing of words or individual letters. Use the value of capitalize to capitalize each word and uppercase for all uppercase letters, lowercase to make all characters lowercase, and none to remove any transform style.

This property is useful, because you can style the casing of your text with CSS rather than manually typing the letter casing. And if you change your mind, and you probably will, you can just remove that with one line of CSS. The text-align property can be used to center-align text. You can add it to the element itself or set the property in the parent element. Let's take a look at another example. Let's say you want to center-align the headings inside of the header tag.

You can apply the text-align center right to the header selectors or you can add it to the parent element. If you add it to the parent element, then everything contained within header will be center-aligned. I've referred to this resource codrops a few times already throughout this course, but here it is again. If you haven't noticed already, there are a lot of CSS properties. Some are more commonly used than others, and some are more advanced, so having a detailed resource, such as this one, is highly recommended.

So far we've covered a handful of font and text styles. There are more typography-related properties, but we have more than enough options for styling our final project.
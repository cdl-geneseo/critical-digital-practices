---
title: CSS Syntax
layout: default
parent: Internet and Web
nav_order: 9
---

# CSS Syntax

Let's look again at the style rules you worked with at the document level (inside the `<style>` element within `<head>`) and in an external file.

```css
body {
    background-color: black;
}

h1 {
    color: red;
    font-family: verdana;
}

p {
    color: white;
}
```

A basic style rule consists of a **selector** (in our example, `body`, `h1`, `p`) followed by one or more **property-value pairs** (for example, `color: white`, where `color` is the property and `white` is its value). The property-value pairs are contained within curly braces (`{}`). When a rule contains more than one property-value pair (as in our `h1` rule above), the pairs are separated by semicolons. Adding a semicolon to the final property-value pair (or the sole pair if the rule contains only one) is optional. Some web developers do this so that, if they add more pairs to a rule down the road, they don't forget to add a semicolon after the existing final pair.

The code formatting you see in the example is also optional. We could just as easily write the first rule this way, for example:

```css
body {background-color:black;}
```
Putting the opening and closing curly braces on their own lines makes your rules much more readable, however, once the number of rules, and the number of property-value pairs within a rule, starts to pile up. You'll thank yourself for getting the hang of writing rules this way.

For styles applied **inline** to individual elements, we use the `style` **attribute** on the element. The property-value pairs that make up the rule then become, collectively, the value of the attribute. For example, if we wanted a particular paragraph to have a one-pixel solid green border, with white text on a red background, our inline rule might look like this:

```html
<p style="border:1px solid green; background-color:red; color:white;">Hello, World!</p>
```
No curly braces here, but note that the style rule, consisting of three property-value pairs, is contained in quotation marks (as are HTML attribute values in general). The rule, to repeat, is the value of the HTML **attribute**, while `red`, to choose one example, is the value of a **property** inside the CSS **rule** (`background-color:red`). That makes `red` an attribute within an attribute.

Notice, too, that the value of `border` has three components: thickness (1px), dimension (solid, as opposed, say, to dashed or dotted), and color (green), and that these components are separated by spaces.

A number of CSS properties can take multiple values. You'll find an excellent rundown of CSS properties and values, and much more, in [this tutorial from W3Schools](https://www.w3schools.com/Css/default.asp).

## CSS classes

Suppose your website has multiple pages, and across those pages you want most paragraphs to have black text in Times New Roman, while some have gray italic text in Arial, and still others have bold white Arial text against a red background. Setting the first style in an external stylesheet, and then overriding it inline every time you want the second or third style, will drive you nuts. Plus, if, down the road, you decide that second style should actually be in blue text, you'll have to go into every inline element one at a time, changing the value of `color` from `gray` to `blue`. For a case this simple, you might get away with doing a global find/replace across all your files, but even that approach will become tedious as the rules you attach to a selector begin to mount.

This is the problem that CSS **classes** are designed to solve. For the example just described, we could specify three rules in our external file, like so:

```css
p {
    font-family: "Times New Roman";
    color: black;
}

p.slant {
    font-family: Arial;
    font-style: italic;
    color: gray;
}

p.festive {
    font-family: Arial;
    font-weight: bold;
    background-color: red;
    color: white;
}
```
We can call the rule for each class inline using the HTML class attribute:

```html
<p>This is my default paragraph style.</p>
<p class="slant">This is my gray italic paragraph style.</p>
<p class="festive">This is my bold-white-on-red-background style.</p>
```
We can now change the rule associated with any of these classes in one place&mdash;our external style sheet&mdash;and the paragraph styles across our entire website will be updated automatically to reflect the change.

You can make up any class names you want. Try to make them meaningful, though, so they jog your memory about their purpose. And don't put spaces in them. 

Using the syntax above, the `.slant` and `.festive` classes are attached specifically to the `<p>` element.  We can also define classes that are available to any element to which they're relevant by omitting the element reference in our selector and just using the class alone as our selector.

```css
.slant {
    font-family: Arial;
    font-style: italic;
    color: gray;
}
```
Using this global syntax, we make the `.slant` class available to table cells, for example, as well paragraphs.

```html
<table>
    <tr>
        <td>
            The text in this table cell will be styled by the browser's default or a rule we set using "td" as selector.
        </td>
    <tr>
        <td class="slant">
        The text in this table cell will be styled by the rule we attached to the "slant" class.
        </td>
    </tr>
<table>
```
## The CSS id selector

In larger HTML documents, or in documents that use CSS for layout (see below), it's common to divide the document up into sections using the `<div>` element. Once we do this, we can use the `id` attribute on `<div>` as a selector by means of the `#` symbol.

```css
#lighter {
    background-color: lightgray;
}

#darker {
    background-color: darkgray;
}
```

In our HTML, we can call these rules and have them apply to each `<div>` in its entirety.

```html
<div id="lighter">
    ...
</div>
<div id="darker">
    ...
</div>
```

Now our page is divided into two sections, one with a light gray background and the other with a dark gray background. Inside each `<div>` element we can nest all the other elements we need, such as `<p>`, `<table>`, `<ul>`, and `<img>`. These elements will inherit the style attached to their parent `<div>` unless expressly overriden.

## CSS colors

In all our examples so far, we've used English-language terms to specify colors. A good many colors can be specified this way, but to control colors precisely, you'll want to turn to one of several numerical alternatives. For example, you can specify a color by indicating the proportions of red, green, and blue that go into it:

```css
p {
    font-family: Arial;
    color: rgb(255, 99, 71);
}
```

Or you can specify a color by using its [hexadecimal](https://www.computerhope.com/jargon/h/hex.htm) value on a scale that runs from `#000000` (black) to `#ffffff` (white). In this syntax, the first two values represent (in base 16, using digits 0-f) how much red is in the color; the second how much blue; the third how much green. The value ff in hexadecimal is the same as 255. Try this style rule in your practice file, for example:

```css
p {
    font-family: Arial;
    background-color: #ff6347;
    color: #ffffff;
}
```

## Other CSS properties

The extent to which you can control the design and experience of web pages using CSS is enormous&mdash;far greater than can be covered here. In addition to offering the [CSS tutorial](https://www.w3schools.com/Css/default.asp) mentioned above, W3schools maintains a helpful [reference list of CSS Properties](https://www.w3schools.com/cssref/index.php).

## CSS for layout

A quick word is in order for CSS as a tool for controlling the layout of web pages.

The inherent fluidity of HTML documents has always made page layout a major challenge for designers. The dimensions of a printed paper document are fixed, making it possible to put the page's building blocks (images, text, callouts, and so on) in an immutable relation to one another. [Portable Document Format (PDF)](https://en.wikipedia.org/wiki/PDF), first developed in the early 1990s at Adobe Systems as a proprietary [page description language](https://www.computerhope.com/jargon/p/pdl.htm), is by now the most common means of reproducing the immutability of print documents for electronic media. (It's been an open standard since 2008.) 

But on the web, immutability comes at a steep price: the genius of HTML's fluidity lies in its adaptability (also known as [responsiveness](https://www.w3schools.com/css/css_rwd_intro.asp)) across the range of browsers, screen sizes, and device types, and in the power it gives users to control their own experience. That power is of particular importance to users who need it because of a disability. The web is awash in PDFs whose tightly fixed design comes at the expense of graceful scalability from desktop to tablet to phone and whose underlying code fails to meet standards of accessibility.

As [mentioned earlier]({{ site.url }}/mod-4/tables#make-a-table), early web designers often turned to tables to provide a grid-like framework for positioning HTML elements. But tables present accessibility issues of their own (screenreaders expect them to hold data), and are in any case much less flexible as a positioning tool than CSS.

Using CSS properties such as [position](https://www.w3schools.com/css/css_positioning.asp), [float](https://www.w3schools.com/css/css_float.asp), [align](https://www.w3schools.com/css/css_align.asp), and [display](https://www.w3schools.com/css/css_display_visibility.asp) (to name just a few of many), it's possible to create highly sophisticated, responsive web page layouts and&mdash;as you've already seen&mdash;adjust all aspects of a page's or even a site's design with a few changes to a style sheet.

## CSS comments

You know by now that you can [intersperse your HTML markup with comments]({{ site.url }}/mod-4/html-basics#create-an-html-file) that won't display in the browser.

Similarly, you can add comments to style rules in an external style sheet or in the `<style>` element within `<head>`. If you make a practice of annotating your rules to explain what they're designed to accomplish, you'll thank yourself down the road when you're looking to make adjustments. If you're collaborating with others on a site, they'll thank you, too.

Use `/*` and `*/` as the bookends of your CSS comments, much as you use `<!--` and `-->` as your bookends for HTML comments.

```css
/* Tomato-red background for festive paragraphs */

p.festive {
    font-family: Arial;
    background-color: #ff6347;
    color: #ffffff;
}
```

## Learn more

Begun as an internet mailing list in 1997, [A List Apart](https://alistapart.com) is a web magazine devoted to exploring all aspects of web design, from the conceptual to the technical to the [ethical](https://alistapart.com/article/daily-ethical-design/).
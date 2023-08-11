---
title: CSS Syntax
layout: default
parent: Internet and Web
nav_order: 9
---

# CSS Syntax

Let's look again at the style rules you worked with at the document level (inside the `<style>` element with `<head>`) and in an external file.

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

This is the problem that CSS **classes** are designed to solve. For the example just described, we could specify two rules in our external file, like so:

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

Or you can specify a color by using its hexadecimal value on a scale that runs from `#000000` (black) to `#ffffff` (white). In this syntax, the first two values represent (in base 16, using digits 0-f) how much red is in the color; the second how much blue; the third how much green. The value ff in hexadecimal is the same as 255. Try this style rule in your practice file, for example:

```css
p {
    font-family: Arial;
    background-color: #ff6347;
    color: #ffffff;
}
```

## Other CSS properties



## CSS for layout

<!--Responsive design -->

## CSS comments

## Where to learn more

<!-- W3Schools, [A List Apart](https://alistapart.com/) -->
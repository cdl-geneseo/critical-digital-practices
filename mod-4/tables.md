---
title: Tables
layout: default
parent: Internet and Web
nav_order: 7
---

# Tables

By now, you know how to use HTML to organize your web content using headings (`<h1>`, `<h2>`, etc.&mdash;you can go as low as `<h5>`), paragraphs (`<p>`), and lists (e.g., `<ul>`, `<ol>`). What if you have some data that you'd like to display in a table?

## Table basics

Like lists, tables make use of our ability to [nest]({{ site.url }}/mod-4/html-basics#nesting) one HTML element inside another. The outermost element of a table is the `<table>` element. Inside `<table>` we can nest an unlimited number of table rows, enclosing each row in the element `<tr>`. Inside each row, we can nest table cells, wrapping each cell's data in the element `<td>` (= "table data"). In a simple table layout, we'll want each `<tr>` element to contain the same number of `<td>` elements so that our cells display in neatly aligned columns.

It's common for data tables to have a header row assigning a name to each column. If we use the `<th>` element in our first row, in place of `<tr>`, the text in each cell of the header row will display in boldface, and our column headings will be properly interpreted as headings&mdash;not data&mdash; by a screen reader.

By default, a table created using these elements will display without borders in your browser. You can use CSS to create custom borders and to control other table features, such as horizontal and vertical alignment, cell background colors, and spacing within and between cells.

## Make a table

Open your practice file and type or paste the following:

```html
<table>
    <tr>
        <th>Friend</th>
        <th>Date invited</th>
        <th>RSVP</th>
    </tr>
    <tr>
        <td>Alex</td>
        <td>1/15</td>
        <td>Yes</td>
    </tr>
    <tr>
        <td>Morgan</td>
        <td>1/17</td>
        <td>No</td>
    </tr>
    <tr>
        <td>Jess</td>
        <td>1/18</td>
        <td>Yes</td>
    </tr>
</table>
```
In the web's early days, site developers often used tables as a means of controlling page layout. The arrival of CSS gave developers a much more powerful and flexible set of tools for this purpose. There's no longer any reason to use tables for layout, and accessibility principles forbid it. **To ensure accessibility, you should use tables for tabular information only.**

Play with the data in your practice table&mdash;adding or subtracting rows, inserting your own data, saving your changes, and refreshing your browser after each save&mdash;to get a feel for how to work with table markup.


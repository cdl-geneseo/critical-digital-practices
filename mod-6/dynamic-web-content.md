---
title: Dynamic Web Content
layout: default
nav_order: 4
parent: WordPress and Omeka
---
# Dynamic Web Content

WordPress and Omeka store their content in a **relational database** written in **SQL** ("Structured Query Language") and build web pages from that content dynamically using the programming language **PHP** (short for "Hypertext Preprocessor"). PHP also provides WordPress' and Omeka's core functionality. (**MySQL** is a particular implementation of SQL.)

The alternative to this dynamic approach is a **static** website: one consisting of individual plain text files written in HTML. Put aside any connotations that the words *dynamic* and *static* have for you. One type of site isn't inherently better than another. Static websites can and typically do run scripts that make them lively and interactive, and modern HTML, combined with CSS, is capable of creating many dynamic effects on the screen. A static site simply doesn't rely on a relational database to store page content.

Files using [common data formats]({{ site.url }}/mod-5/common-data-formats) such as CSV, XML, and JSON can be regarded as databases, since the information in them is structured. A properly organized spreadsheet can serve as a database. What's distinctive about a *relational* database is that it consists of multiple tables in which cells can be linked across tables, establishing relationships between the data in one table and that in another.

If your website contains lots of content of many different kinds, and you want to deliver pieces of that content in ways that reflect their underlying relationships, it makes sense to store the content in a relational database and build your pages dynamically. This approach also usefully separates visual and experiential aspects of the site&mdash;things like page layout, color scheme, and navigation&mdash;from content, making it easy, with a single click (and, to be sure, usually at least a little bit of clean-up) to change the site's overall look and feel.

For other types of website, a static approach may be the best solution. The site you're reading is a static site generated with [Jekyll](https://jekyllrb.com/). Static sites, too, can be delivered in a variety of themes. This site is using the documentation theme [Just the Docs](https://github.com/just-the-docs/just-the-docs).


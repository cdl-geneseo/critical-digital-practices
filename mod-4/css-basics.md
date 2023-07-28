---
title: CSS Basics
layout: default
parent: Internet and Web
nav_order: 8
---

# CSS Basics

**Cascading Style Sheets**&mdash;CSS for short&mdash;provide a powerful means of formatting the content of an HTML document or even an entire website. By separating formatting specifications from our markup, we gain the ability to make global adjustments to the appearance of our web pages without having to alter the markup itself.

Why "cascading"? Because we can specify formatting at multiple removes from the markup to be styled. Style instructions that are closer to the affected markup supersede instructions at the next-farthest remove, and so on up the hierarchy. As a result, we can specify a set of global instructions that will govern multiple documents, fine-tune these instructions as needed for a particular document, further tune those document-level instructions for particular sections of a document, and, finally, override instructions at any of these levels with specific instructions attached to a single element in one location within the document. In addition, we can specify how content within a particular element&mdash;say, `<p>`&mdash;will be formatted in different contexts by defining different style **classes**. Content in a `<p>` that belongs to one class (assigned to it using the **class** attribute) will then appear different (in color, size, font, or any combination of these and other features) from content that belongs to another.

At each level of the cascade, if we want to make adjustments to styles set at the level above, we need only specify what will be *different* from that level; the other style instructions will still hold.

## Setting styles for a page

Let's begin by looking at how we might use CSS in a single web page.
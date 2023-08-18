---
title: What are WordPress and Omeka?
layout: default
nav_order: 2
parent: WordPress and Omeka
---
# What are WordPress and Omeka?

WordPress and Omeka are two popular **content management systems**. Each system comprises multiple tools that, acting in concert, enable you to create, organize, and publish web content. 

[WordPress](https://wordpress.org) began in the early 2000s as software designed to facilitate blogging; it's now one of the most popular systems for managing entire websites. According to [Wikipedia](https://en.wikipedia.org/wiki/WordPress), as of October 2021 it was used by 42.8% of the top 10 million sites on the web. (You can read more about the history of WordPress in [*Building Blocks: The Evolution of WordPress*](https://wordpress.org/book/)).

[Omeka](https://omeka.org) (pronounced "Oh-MEK-ah") originated at the [Roy Rosenzweig Center for History and New Media](https://rrchnm.org/) in 2007. (According to its [website](https://omeka.org/about/project/), "'Omeka' is a Swahili word meaning to display or layout wares; to speak out; to spread out; to unpack.") From the start, its purpose has been to support the management and publication of archival content&mdash;written records, still and moving images, audio recordings, etc.&mdash;in ways that facilitate storytelling about that content. Digital objects stored in Omeka can be tagged with metadata, organized into collections, and used to create online exhibits similar to those traditionally mounted in physical spaces by museums, libraries, and archives.

Both WordPress and Omeka are powered by software that's free and open source. Anyone with a web hosting account or access to an academic or other institutional server can download the software for free, install it, and be underway. Users are free to modify the code, and robust developer communities have grown up around both products&mdash;WordPress in particular&mdash;that create themes, plugins, and other enhancements to the basic software. Many enhancements are available without charge, others on a "freemium" model, and still others for a purchase price or subscription fee charged by the developer.

## Software vs. Platform

The WordPress and Omeka **software** shouldn't be confused with the two **platforms**, at [WordPress.com](https://wordpress.com) and [Omeka.net](https://omeka.net) respectively, that will save you the trouble of installation by hosting a WordPress or Omeka instance for you. If your website needs are very simple, these platforms may meet them.

However, this module assumes that you're interested in installing and working directly with WordPress and Omeka, or at least interested in getting a look beneath the hood of both to better understand how they work. Installing the software for these content management systems with your own hosting, or hosting provided to you by an institution, will give you a great deal more flexibility to customize what you build.

Since you may not have access to hosting, the module will walk you through installing and setting up the two systems on your own machine. They'll operate there exactly as they would on a web server, even though the sites you build with them will be accessible to you only. Everything you learn from doing this will be transferable to using the systems on a remote host server when you're ready to do so.

Meanwhile, one benefit of installing and setting up WordPress and Omeka on your own machine is that it gives you an opportunity to learn a few things about the development stack used on many web servers, called a **LAMP** stack for the components it comprises: **Linux, Apache, MySQL** (or **MariaDB**), and **PHP/Perl/Python**. For this module, we'll use a free-of-charge product called **MAMP** for our stack. The first "M" in "MAMP" stands for "MacOS"; MAMP is designed for maximum compatibility with the Mac operating system. Despite the name, though, it also comes in a Windows flavor, which is what Windows users will want to download and install. If your machine's main operating system is Linux, you can achieve the same results we'll cover here using [XAMPP](https://sourceforge.net/projects/xampp/).

Another benefit of running a LAMP-based CMS locally on your machine is that it gives you the ability to do low-stakes testing of themes, plugins, and design choices that you may be considering for implementation on a website. You'll be able to identify and troubleshoot issues before taking your ideas live. If at any point you want to start anew from scratch, you can delete your entire local WordPress or Omeka installation, re-download the software, and begin again.

This module will focus on the steps involved in setting up WordPress and Omeka locally. It will not explore the ins and outs of working in the WordPress and Omeka environments. WordPress offers an extensive library of [tutorials](https://learn.wordpress.org/tutorials/). Omeka maintains a comprehensive [user manual](https://omeka.org/classic/docs/) for its "Classic" version (the one you'll want to use to maintain a single Omeka site, as opposed to a network of sites). In addition, Leah Tams' [Omeka 101 website](https://leahtams.org/omeka-101/) provides a nice introduction to the basics of working with Omeka.
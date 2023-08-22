---
title: Design Justice
layout: default
parent: Internet and Web
nav_order: 10
---

# Design Justice

In the world of print publication, **design** has long held a place of high importance. From the length and width of the printed page, to the material and thickness of the paper, to type face, margins, and the relationship of text to graphics, to binding, cover, and (for hardbound volumes) dust jacket, design is understood to play a key role in a reader's *experience* of a book. Design affects not only whether that experience is an aesthetically pleasing one, but also whether interacting with the book is a chore (because, perhaps, it's too large or heavy to carry around, or the pages are too thin to turn easily, or the type is too small or light to read without squinting) or a pleasure.

Design is as important to the web as it is to the world of print. In the web's early days, designers didn't have a great many options at their disposal for making sites beautiful and pleasurable to interact with, but as web technologies evolved, and especially with the advent of CSS, they acquired an extensive toolkit. Today, a well-designed website reflects hours of work and hundreds if not thousands of lines of code devoted specifically to ensuring an excellent user experience, or "UX," in the language of design specialists.

We've already seen that one design challenge unique to the web is that the interface between user and content lies outside the designer's control. The dimensions of a printed book's pages are set by the publisher; the dimensions of the screen on which a user engages with web content are determined by the user's device of choice: desktop, laptop, tablet, or phone. Hence the need, [as we've already seen]({{ site.url }}/mod-4/css-syntax#css-for-layout), for web designers to follow principles of responsive design.

We've also seen that good web design is attentive to **accessibility**. (This is also true of good print design, though the two media often achieve the goal in different ways.) Fundamentally, accessibility is about *equity* rather than aesthetics or pleasure (though it may have an impact on all three). Designers have a moral (and sometimes a [legal](https://www.ada.gov/resources/web-guidance#when-the-ada-requires-web-content-to-be-accessible)) responsibility to ensure that their creations can be used and enjoyed by the widest possible range of users. In the [words of the US Department of Justice](https://www.ada.gov/resources/web-guidance#why-website-accessibility-matters) (DOJ),

> Inaccessible web content means that people with disabilities are denied equal access to information. An inaccessible website can exclude people just as much as steps at an entrance to a physical location. Ensuring web accessibility for people with disabilities is a priority for the Department of Justice. In recent years, a multitude of services have moved online and people rely on websites like never before for all aspects of daily living. For example, accessing voting information, finding up-to-date health and safety resources, and looking up mass transit schedules and fare information increasingly depend on having access to websites.

Towards the end of promoting an inclusive web, the W3C has adopted [Web Content Accessibility Guidelines](https://www.w3.org/TR/WCAG21/).The W3C's guidelines are based on [four fundamental principles](https://www.w3.org/WAI/WCAG21/Understanding/intro#understanding-the-four-principles-of-accessibility):

> Anyone who wants to use the Web must have content that is:
>
> Perceivable - Information and user interface components must be presentable to users in ways they can perceive.
>
> - This means that users must be able to perceive the information being presented (it can't be invisible to all of their senses)
>
> Operable - User interface components and navigation must be operable.
>
> - This means that users must be able to operate the interface (the interface cannot require interaction that a user cannot perform)
>
> Understandable - Information and the operation of user interface must be understandable.
>
> - This means that users must be able to understand the information as well as the operation of the user interface (the content or operation cannot be beyond their understanding)
>
> Robust - Content must be robust enough that it can be interpreted reliably by a wide variety of user agents, including assistive technologies.
>
> - This means that users must be able to access the content as technologies advance (as technologies and user agents evolve, the content should remain accessible)

The DOJ lists four common barriers to web accessibility:

> **Poor color contrast.** People with limited vision or color blindness cannot read text if there is not enough contrast between the text and background (for example, light gray text on a light-colored background).
>
> **Use of color alone to give information.** People who are color-blind may not have access to information when that information is conveyed using only color cues because they cannot distinguish certain colors from others. Also, screen readers do not tell the user the color of text on a screen, so a person who is blind would not be able to know that color is meant to convey certain information (for example, using red text alone to show which fields are required on a form).
>
> **Lack of text alternatives (“alt text”) on images.** People who are blind will not be able to understand the content and purpose of images, such as pictures, illustrations, and charts, when no text alternative is provided. Text alternatives convey the purpose of an image, including pictures, illustrations, charts, etc. \[Revisit the page in this course on "Attributes, Links, Images" to refresh your memory on [how to use alt text with images]({{ site.url }}/mod-4/attributes-links-images#making-your-images-accessible) in HTML\].
>
> **No captions on videos.** People with hearing disabilities may not be able to understand information communicated in a video if the video does not have captions.
> Inaccessible online forms. People with disabilities may not be able to fill out, understand, and accurately submit forms without things like:
> - Labels that screen readers can convey to their users (such as text that reads “credit card number” where that number should be entered); 
> - Clear instructions; and
> - Error indicators (such as alerts telling the user a form field is missing or incorrect).
>
> **Mouse-only navigation (lack of keyboard navigation).** People with disabilities who cannot use a mouse or trackpad will not be able to access web content if they cannot navigate a website using a keyboard.

## Towards universal design

Design is a feature not only of books and websites, of course, but of virtually every aspect of the human-made environment, both physical&mdash;such as furniture, buildings, parks, and transportation networks&mdash;and social, such as the legal, political, economic, technological, and educational systems we must all "navigate" (as though they were indeed part of the physical environment) in order to participate fully in society.

The movement that began in the mid-twentieth century to remove participatory barriers for the disabled, producing, among other signal developments, the landmark [Americans with Disabilities Act](https://en.wikipedia.org/wiki/Americans_with_Disabilities_Act_of_1990) of 1990, ultimately led to a broader conceptual framework for thinking about equitable participation: **universal design**.

The term "universal design" emerged in the 1990s from an interdisciplinary group led by the architect Ronald L. Mace at the North Carolina State University College of Design. It captures the idea that truly inclusive design requires no special adaptation or accommodation to make it accessible to all. It can be defined as ["the design of products and environments to be usable by all people, to the greatest extent possible, without the need for adaptation or specialized design."](https://design.ncsu.edu/research/center-for-universal-design/) The group at UNC developed seven principles of universal design, nicely elaborated and illustrated in [this pdf](https://design.ncsu.edu/wp-content/uploads/2022/11/principles-of-universal-design.pdf): equitable use, flexibility in use, simple and intuitive use, perceptible information, tolerance for error, low physical effort, size and space for approach in use.

In their book [*Universal Design: Creating Inclusive Environments*](https://isbn.nu/cgi-bin/design-books) (Wiley and Sons, 2012), Jordana Maisel and Edward Steinfeld of the University at Buffalo's [Center for Inclusive Design and Environmental Access](https://idea.ap.buffalo.edu/about/universal-design/) developed a still broader definition: "Universal Design (UD) is a design process that enables and empowers a diverse population by improving human performance, health and wellness, and social participation."

## Design justice

Taking seriously a design framework that emphasizes diversity, wellness, and participation leads inevitably to  considerations of power and justice&mdash;to asking who has a voice in a system's design as well as who is affected by the system and how. At the 2015 [Allied Media Projects](https://alliedmedia.org/) conference in Detroit, a group of designers, artists, technologists, and community organizers [worked to generate a set of shared principles](https://designjustice.org/news-1/2016/05/02/2016-generating-shared-principles) for **design justice**. Established the following year, the [Design Justice Network](https://designjustice.org/) works to achieve its vision of a world where "design is used to support care, healing, liberation, joy, and deep sustainability" (["About Us"](https://designjustice.org/djnhistory)) and to "center those who are normally excluded from and adversely impacted by design decisions in design processes" (["Our History"](https://designjustice.org/djnhistory)). In a [living document](https://designjustice.org/read-the-principles), the DJN continues to build on the principles first generated in 2015. These include seeing "the role of the designer as a facilitator rather than an expert" and prioritizing "design’s impact on the community over the intentions of the designer."

Sasha Costanza-Chock's open access book [*Design Justice*](Sasha Costanza-Chock), published by MIT Press, [begins](https://designjustice.mitpress.mit.edu/pub/ap8rgw5e/release/1) with an account of navigating the US airport transportation security system as a "non-binary, trans*, femme-presenting person." (The asterisk [is part of the word](https://time.com/5211799/what-does-trans-asterisk-star-mean-dictionary/)).

> The point of this story is to provide a small but concrete example from my own daily lived experience of how larger systems&mdash;including norms, values, and assumptions&mdash;are encoded in and reproduced through the design of sociotechnical systems, or in political theorist Langdon Winner's famous words, how "artifacts have politics." In this case, cis-normativity is enforced at multiple levels of a traveler's interaction with airport security systems.

Costanza-Chock's book goes on to consider a range of ways in which design justice and injustice play out in the landscape of technology. From these narratives, one can begin to understand how much more than text and media are "coded" into the design of something as simple as a website.
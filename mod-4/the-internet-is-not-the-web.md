---
title: The Internet is Not the Web
layout: default
parent: Internet and Web
nav_order: 2
---

# The Internet is Not the Web

People often use the terms "internet" and "web" interchangeably. It's not hard to see why. These days, people connect to the internet primarily to access websites.

But the internet is not the web. It's a network of networked computers: computers able to exchange information with each other through a variety of standards and protocols, the most important of which you've already encountered: [TCP/IP](https://www.howtogeek.com/751880/the-foundation-of-the-internet-tcpip-turns-40/) (Transmission Control Protocol/Internet Protocol). The web *uses* this network to make possible an ecosystem of *linked content and data*. The internet makes the web possible. Or, to put it another way, the web is a layer built on top of the internet.

## Birth of the internet

Since ballistics and code-breaking were two of the earliest applications of computing&mdash;carried out, [as we saw earlier](/critical-digital-practices/mod-1/what), by humans before they were carried out by machines&mdash;it should come as no surprise that the military played a key role in the internet's origins. In the mid-1960s, the US Department of Defense Advanced Research Projects Agency (ARPA) developed [ARPANET](https://www.computerhope.com/jargon/a/arpanet.htm). At the time, multiple users could connect via terminal to a single mainframe computer through **timesharing** to share its resources and to exchange messages and files. But as the [Computer History Museum's Marc Weber](https://computerhistory.org/blog/history-of-the-future-october-29-1969-fifty-years-of-a-connected-world/) explains, "each of those timesharing systems was a little island, an isolated community restricted to its own host computer." ARPANET represented one effort to "connect those islands to each other into archipelagos," establishing a network of interconnected computers that could talk to each other. And yet, as [Weber also explains](https://computerhistory.org/blog/who-invented-which-internet/),

> as soon as once standalone computers started getting hooked together into networks around 1970, there was a problem. Those networks couldn’t talk to each other. They were like little islands. \[Or really, to use Weber's earlier metaphor, strings of islands, "archipelagos."\] There was the well-known ARPANET, and also the NPL network in the UK, and soon several others, and they were all isolated. The solution was to create standards that could translate data between them and tie them into networks of networks. This process is called “internetworking” or “internetting,” and the result is called an “internet.”

More than one set of protocols was developed to enable these networks to speak to each other in a single language. Bob Kahn and Vint Cerf are credited with driving the development of TCP, [first demonstrated successfully on November 22, 1977](https://computerhistory.org/blog/born-in-a-van-happy-40th-birthday-to-the-internet/) using software written by [Virginia Strazisar](https://www.computerhope.com/people/ginny_strazisar.htm) (later Travers) to power the router (then called a "gateway") that directed the network traffic. By the early 1990s, TCP/IP emerged as the dominant protocol holding the world's networked computers together in a network of networks, the internet.

The ["first large-scale implementation of Internet technologies in a complex environment of many independently operated networks"](https://www.nsf.gov/news/news_summ.jsp?cntn_id=103050) was the National Science Foundation's NSFNET, which first went online in 1986. NSFNET provided the [backbone](https://www.computerhope.com/jargon/b/backbone.htm) connecting government, university, and research center computers as the internet grew, finally opening up to commercial interests in the early 1990s. ARPANET was decomissioned in 1985. The NSFNET backbone was decommissioned ten years later, in 1995.

## Privatization, access, and equity

Before the privatization of the internet in the mid-90s, access to the network was through government agencies, educational institutions, and research centers. Privatization enabled mass access to the internet via commercial [Internet Service Providers (ISPs)](https://www.computerhope.com/jargon/i/isp.htm). In some ways, the result has been democratizing, greatly expanding the general population's access, in turn, to knowledge and services. But access in theory is not the same as access in practice. A privatized internet has inevitably followed the money, and in so doing has reinforced and even exacerbated existing social inequities based on factors such as race and income. Not only is internet access itself unevenly distributed across the US and around the world, but as [journalists at The Markup have documented](https://themarkup.org/still-loading/2023/05/11/see-the-neighborhoods-internet-providers-excluded-from-fast-internet), ISPs price high-speed access differently in different neighborhoods. The Markup's analysis of pricing from three ISPs "revealed that the worst internet deals disproportionately fell upon the poorest, most racial and ethnically diverse, and historically redlined neighborhoods in all but two of the 38 cities" they looked at.

The fact that the internet had its origins in the nonprofit world has produced one of its most truly democratizing features: the principle of [net neutrality](https://www.eff.org/issues/net-neutrality). In brief, this principle holds that data, once it's on the network, should travel at the same speed, whether that data was sent by you, your friend, or Netflix. Net neutrality prevents ISPs from setting up "fast lanes" for preferred customers (at a higher price) and from throttling the speed of services for which they offer a competing product. But net neutrality, as a principle, is far from secure&mdash;in part, as comedian Jon Oliver memorably explained in this 2014 episode of his show "Last Week Tonight," because the commercial interests seeking to abolish it know that most people don't understand, and are easily bored by, the technical details:

<iframe width="560" height="315" src="https://www.youtube.com/embed/fpbOEoRrHyU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Where's my packet?

Data flows across the internet in discrete bundles called [packets](https://www.howtogeek.com/797005/what-is-a-data-packet/). The attachment you send through email or the image file delivered to your browser from a website doesn't travel intact. Through a process called [packet switching](https://www.computerhope.com/jargon/p/packetsw.htm), the data is first broken up into packets as it leaves the sending computer. These packets don't all take the same route; if they did, packets would back up on the wires connecting computers like cars in traffic jam. When the separate packets eventually reach the destination computer, having traveled their separate ways, they're reassembled into one whole.

Packet-switching was a crucial innovation in the development of the internet. Another innovation related to the flow of data was the [Spanning Tree Protocol (STP)](https://en.wikipedia.org/wiki/Spanning_Tree_Protocol) conceived in the 1980s by [Radia Perlman](https://en.wikipedia.org/wiki/Radia_Perlman) while at the Digital Equipment Corporation. The STP keeps data traveling over a network without getting caught in loops. Although Perlman's innovation earned her the nickname "Mother of the Internet," in a 2014 interview with [*The Atlantic*](https://www.theatlantic.com/technology/archive/2014/03/radia-perlman-dont-call-me-the-mother-of-the-internet/284146/) she explained that she rejects the label because 

> The Internet was not invented by any individual. There are lots of people who like to take credit for it, and it drives them crazy when anyone other than them seems to want credit, so it seems best to just stay out of their way. 

"I did indeed make some fundamental contributions to the underlying infrastructure," she continued, "but no single technology really caused the Internet to succeed." 

## What's my address?

<!-- 

DNS, ICANN, IP addresses, whois, traceroute, ipecho.net

-->
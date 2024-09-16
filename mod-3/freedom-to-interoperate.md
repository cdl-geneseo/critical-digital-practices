---
title: "Coda: Freedom to Interoperate"
layout: default
parent: What is Text?
nav_order: 7 
---
# Coda: Freedom to Interoperate

This module has emphasized the importance of interoperability in the domain of text editing. But it's worth taking a moment to put interoperability as a general principle in perspective.

## The default state of the world

As Cory Doctorow explains in his essay [“IP”](https://locusmag.com/2020/09/cory-doctorow-ip/), the term *interoperability*

> describes two products or services that can somehow work together with one another. From opening your Word documents in Google Docs, to using third-party ink cartridges in your printer to replacing your watch band, to changing the stereo that came with your car, interoperability is a broad, universal, essential characteristic of all of our technology.

"Interoperability," Doctorow continues, "is the default state of the world. Anyone’s charcoal will burn in your barbecue, just as anyone’s gas will make your car go. Any manufacturer can make a lightbulb that fits in your light-socket and any shoes can be worn with any socks."

We shouldn't confuse this "default state" with "the nature of things," however. In the case of lightbulbs, for example, interoperability is the default not by nature or necessity but because bulb manufacturers possess the knowledge and the right to make bulbs that will thread into your light sockets, and because light-socket manufacturers possess the knowledge and the right to follow a design **standard** that's openly available, and for the most part do just that.

Standards play a key role in interoperability, and they exist only because of cooperation and the free exchange of information. As the US National Institutes of Standards and Technology (NIST) [explains](https://www.nist.gov/feature-stories/why-you-need-standards):

> Take fire hydrants. If you ever have to call 911 to report a fire, you don’t have to worry about the hoses that firefighters bring when they arrive.
>
> But that wasn’t the case in the [Great Baltimore Fire of 1904](https://baltimorepolicemuseum.com/en/?Itemid=544), which burned for more than a day and destroyed 1,500 buildings. Starting on a quiet Sunday morning, the fire spread quickly and overwhelmed the city’s ability to fight it alone. Fire companies from New York, Philadelphia, Wilmington, Harrisburg and elsewhere swiftly rushed in to help. They had more than enough water and people to fight the fire, but there was a problem: Most of their fire hoses wouldn’t fit the hydrants, prolonging the fire to 30 hours and damaging an area the size of 70 blocks in the city’s business district.
>
> A NIST study found more than 600 variations in firehose fittings across the U.S. NIST worked with the [National Fire Protection Association](https://www.nfpa.org/) to usher in a national standard for fire hydrant connections. Thanks to this standard, firefighters from different companies could work together more easily to extinguish large fires and prevent another disaster like the 1904 Baltimore blaze.

When it comes to digital technology, the equivalent of light-socket and fire-hydrant standards takes the form, in part, of numerous openly published protocols and specifications maintained by standards bodies such as the [Internet Engineering Task Force (IETF)](https://www.ietf.org/standards/) and the [World Wide Web Consortium (W3C)](https://www.w3.org/). These protocols and specifications include the [Transmission Control Protocol/Internet Protocol (TCP/IP)](https://www.computerhope.com/jargon/t/tcpip.htm), which enables computers to connect to one another on the internet and exchange data, and the [Hyper Text Transfer Protocol (HTTP)](https://www.computerhope.com/jargon/h/http.htm), which enables your computer to connect, as a **client**, to a remote **server** and **request** a web page, which you can then read in a browser such as Firefox, Chrome, or Safari. The Hypertext Markup Language we [looked at earlier]({{ site.url }}/kinds-of-text#html) is [itself an openly-published standard](https://html.spec.whatwg.org/).

## Interoperability and self-determination

It wasn't always this way. In the early years of the web, the makers of different browsers competed to create features that would work only for their own users. If the web had continued to develop along this route, we wouldn’t be able to do what we can do now: load virtually any web page in the browser of our choice.

Interoperability, in other words, does more than enable different technologies to work together. In Doctorow's words, it's also "the key to self-determination" in your digital life. It enables you to move, at will, between operating systems, applications, platforms, etc., or to modify technology in your possession&mdash;both hardware and software&mdash;in ways analogous to your ability to fold a piece of paper that otherwise wouldn't fit into an envelope.

Unfortunately, your power of self-determination runs counter to the interests of commercial hardware and software manufacturers like Apple and Microsoft and commercial platform owners like Google and Facebook. These for-profit entities benefit from open standards, and, to be fair, support and at times contribute to their development. But they also have a powerful incentive to lock us into sticking with their products or, at least, to tilt the playing field in their favor&mdash;as a landmark 2001 [antitrust case against Microsoft](https://en.wikipedia.org/wiki/United_States_v._Microsoft_Corp.) claimed the company had done by integrating its web browser, Internet Explorer, with its operating system.

In a multitude of ways, technology companies, once they have our business, erect barriers to exit. If you're unhappy with Facebook, you "can’t go to a Facebook rival and follow what your friends post to Facebook from there," Doctorow explains. "You certainly can’t reply to what your Facebook friends post using a rival service."

## Two freedoms: speech and association

Two important dimensions of self-determination are freedom of speech and freedom of association. However, your freedom to speak your mind (and express yourself generally) and my freedom to associate with peers of my choice can come into conflict. Social media platforms are a notorious arena for conflict of this kind.

The conflict has no easy resolution. Restricting speech to protect freedom of association inevitably leads some people to feel censored, while allowing unfettered speech (even within legally permissible limits) inevitably forces on some people's attention speech they regard as abhorrent or even harmful&mdash;especially if they belong to a minoritized, socially excluded, or vulnerable group&mdash;as well as misinformation and (what is sometimes the same thing) obnoxious and uninvited advertising. (Apart from violating freedom of association, forced exposure to uninvited, undesired speech as a condition of membership in a community arguably violates a key component of autonomy: the ability to choose how we spend our attention. This, at least, is the argument of Tim Wu in his book *The Attention Merchants: The Epic Scramble to Get Inside Our Heads* \[Vintage Books, 2016\].)

But as uncertain as any solution to this conflict may be, it's certainly the case that the problem is exacerbated when your only means of participating in community is to subscribe to a platform over whose rules you have no say. The mass exodus from the social media platform Twitter that began with the platform's purchase by Elon Musk in 2022 underscored, for many users, the intolerable dilemma presented by non-interoperable systems of social connectivity: stay on the platform, sacrificing freedom and autonomy and possibly risking harm, or say goodbye to the friends and professional connections you spent years cultivating.

The Twitter mess has caused some internet scholars and commentators to revisit Mike Masnick's 2019 essay, ["Protocols, Not Platforms: A Technological Approach to Free Speech"](https://knightcolumbia.org/content/protocols-not-platforms-a-technological-approach-to-free-speech). For Masnick, the key distinction between a protocol and a platform, in the social media space, is that protocols (as we've seen) are open and available for anyone with the know-how to build with, whereas platforms like Twitter are built on private and proprietary code, and are privately managed. The platform model is a centralized one&mdash;to use Twitter you must be "on" Twitter&mdash;whereas the protocol model is a decentralized one: no central service is necessary because every server using the protocol can talk to every other server using the protocol.  

As it happens, there's a free and open protocol for social interaction on the web, [ActivityPub](https://www.w3.org/TR/activitypub/), overseen by the W3C. Any server implementing the ActivityPub protocol can connect with any other server running it, making it possible for users to join the social network of their choice, with speech and safety rules they're comfortable with, and exchange messages not only with members of the same community but members of any other ActivityPub-based community. The same infrastructure also makes it possible for a user to leave their current community anytime for one they like better&mdash;and still retain all their social connections.

The analogy that's often drawn here is with email, a service based on one of the oldest internet protocols, [SMTP (Simple Mail Transfer Protocol)](https://www.computerhope.com/jargon/s/smtp.htm). Anyone who has an email address can exchange messages with anyone else who has an email address; it doesn't matter if the two people in question subscribe to different email providers, and if one person changes providers, all the other person needs to maintain their connection is the first person's new address.

Many of those fleeing Twitter have joined one of the numerous internet communities running the open-source social messaging software [Mastodon](https://github.com/mastodon/mastodon), built on the ActivityPub protocol. From the [Mastodon home page](https://joinmastodon.org/) users can select a server (i.e., a community) to join and begin sharing ideas and media with peers across the universe of [federated](https://docs.joinmastodon.org/#federation) servers (i.e., servers running the same software, based on the same protocol).

Collectively, the decentralized network of federated, interoperable web publishing services (including not only social messaging services but photo- and video- sharing services similar to Google Photos and YouTube) is sometimes known as the **fediverse**.

## The future of interoperability

The future of interoperability in digital technology is by no means assured. As we've seen, it doesn't exist by accident, and where it does exist, only the hard work of standards bodies, and the freedom to access and use the standards they maintain, makes it "the default state of the world." This is true not only for interoperability on the internet but also&mdash;to return to the topic of the current module&mdash;interoperability among the documents we create on our computers every day, interoperability made possible by standards such as ASCII and Unicode.
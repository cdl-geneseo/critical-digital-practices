---
title: Machine Learning, Deep Learning, and Neural Networks
layout: default
parent: Artificial Intelligence
nav_order: 3
---

# Machine Learning, Deep Learning, and Neural Networks

## Machine Learning

If the idea that there could be "intelligent" or "thinking" machines remains highly questionable, there's no question that the algorithms underpinning contemporary AI systems are distinctly different from those that dominated early efforts to program computers to take action in response to a set of circumstances.

In those early efforts, so-called "expert systems" equipped computers with a "knowledge base"&mdash;a set of facts about a given domain&mdash;and a set of logic-based rules to apply to those facts. In the classic example, a computer so equipped could make moves in a game like checkers or chess based on an enormous amount of previously stored information about past games and a set of rules for responding to new situations in a game as they arose.

By contrast, contemporary AI systems rely much more heavily on statistical inference and prediction; they use probability to respond to previously unencountered situations, and they're capable of improving their responses by "learning" from feedback on their actions.

Indeed, "machine learning" is the generic label applied to computer systems capable of improving their output continuously in response to feedback. It's important to recognize, however, that as in the case of "intelligence" and "thinking," machine "learning" is driven by processes fundamentally different from those that drive *human* learning. The more the designers and marketers of AI systems use the language of human perception and cognition to describe what these systems do, the easier it becomes to anthropomorphize the machines themselves. Unless we keep at least mental quotation marks around AI terminology borrowed from the things a human brain does (operating in coordination with the rest of the human body it belongs to), we're at risk of reaching some peculiar conclusions&mdash;one example, arguably, is the claim some are now making that AI systems, like humans, deserve, or will eventually deserve, to be treated [as "persons" bearing rights](https://pmc.ncbi.nlm.nih.gov/articles/PMC10682746/).  

## Deep Learning and Neural Networks

But to repeat, there's no question computers can "learn" in the limited sense of running software whose performance continuously improves in response to feedback, and in recent years a kind of machine learning called "deep learning" has supercharged this process using a design called "neural networks." Again, keep the quotation marks on this last term mentally, at least. Neural networks are intended to replicate, loosely, the networked structure of neurons in the human brain. The "nodes" of a neural network are indeed networked, but they aren't, of course, actual neurons. They're connected by complex mathematical equations. "Weights" and "parameters" in the network can be adjusted to fine-tune the output it produces.

When massive quanitites of data&mdash;numbers, words, images, whatever&mdash;are run repeatedly through a multi-layered neural network, the network becomes startlingly good at finding patterns in the data and generating new output based on statistical probablilities. It's this capability that enables a chatbot like ChatGPT, Claude, Copilot, or Grok to take text as input and immediately generate grammatical, idiomatic output that gives all the appearance, at least superficially, of coming from a human interlocutor.  

### Supervised, Unsupervised, and Reinforcement Learning

Broadly speaking, AI systems can be trained in any of three ways. In "supervised learning," labeled data goes into the network in order to train the network to look for specific patterns and match them when it finds them. In "unsupervised learning," the network takes in unlabeled data and identifies patterns itself. In "reinforcement learning," the network attempts, through trial and error, to achieve a general outcome.

### Foundation, Large Language, and Diffusion Models

Neural networks trained on massive datasets, equipped with powerful computing resources, and capable of being used for a wide range of applications are sometimes called "foundation models." Those trained on language data in order to use pattern-matching and probabilistic methods to generate text are called "large language models." Those trained on image data and capable of generating images and video are called "diffusion models."
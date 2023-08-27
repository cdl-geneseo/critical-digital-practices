---
title: Objects and Methods
layout: default
parent: Python Brief Intro
nav_order: 13
---
# Objects and Methods

Python is an **object-oriented** programming language. Just about everything in Python is an "object." As [Wikipedia](https://en.wikipedia.org/wiki/Object-oriented_programming) explains, **objects** are components "that can contain data and code. The data is in the form of fields (often known as attributes or *properties*), and the code is in the form of procedures (often known as *methods*)."

One way to think of **methods** is as functions attached to certain objects. Here's an example:

```zsh
>>> myTerms = ['copyright', 'privacy', 'open access', 'data', 'bias', 'copyleft', 'ethics', 'universal design']
>>> myTerms.sort()
>>> myTerms
['bias', 'copyleft', 'copyright', 'data', 'ethics', 'open access', 'privacy', 'universal design']
>>> 
```
What happened here? We began with a list, assigned to the variable `myTerms`. We then used the `sort()` method, a special kind of function available to the `list` data type, to sort the list alphabetically.

We access the sort method using the notation you see above, appending `.sort()` to the variable we want to use it on.

What if we want to add an item to our list?

```zsh
>>> myTerms.append('accessibility')
>>> myTerms
['copyright', 'privacy', 'open access', 'data', 'bias', 'copyleft', 'ethics', 'universal design', 'accessibility']
```
The term we appended to the list is added at the end, messing up our nice alphabetization. (You may have to scroll right to see it.) How would you move it to the correct location?

## String methods

There are many useful methods for working with strings.

We can create a string from a list using `.join()`.

```zsh
>>> myWords = ['It', 'was', 'the', 'best', 'of', 'times']
>>> " ".join(myWords)
'It was the best of times'
>>> 
```
In this example, the bit that precedes the `.` is our designated **separator**. Because we want our string to read as a sentence, we choose space as our separator. Returning to our earlier list, we could use `|` as separator.

```zsh
>>> "|".join(myTerms)
'accessibility|bias|copyleft|copyright|data|ethics|open access|privacy|universal design'
```
We can also go in the other direction, creating a list from a string with the `.split()` method. Let's see how this works, using the opening paragraph of the first chapter of Frederick Douglass' *Narrative of the Life of Frederick Douglass, An American Slave* (1845), a public domain text available from [Project Gutenberg](https://www.gutenberg.org/ebooks/23).

First, we'll store the paragraph in a variable, `myString`:

```zsh
>>> myString = "I was born in Tuckahoe, near Hillsborough, and about twelve miles from Easton, in Talbot county, Maryland. I have no accurate knowledge of my age, never having seen any authentic record containing it. By far the larger part of the slaves know as little of their ages as horses know of theirs, and it is the wish of most masters within my knowledge to keep their slaves thus ignorant. I do not remember to have ever met a slave who could tell of his birthday. They seldom come nearer to it than planting-time, harvest-time, cherry-time, spring-time, or fall-time. A want of information concerning my own was a source of unhappiness to me even during childhood. The white children could tell their ages. I could not tell why I ought to be deprived of the same privilege. I was not allowed to make any inquiries of my master concerning it. He deemed all such inquiries on the part of a slave improper and impertinent, and evidence of a restless spirit. The nearest estimate I can give makes me now between twenty-seven and twenty-eight years of age. I come to this, from hearing my master say, some time during 1835, I was about seventeen years old."
```
Before we go further, let's pause to take note of how many characters are in the string, using the `len()` function.

```zsh
>>> len(myString)
1146
```
Now let's use the `.split()` method to turn the string into a list and store the list in a new variable, `DouglassWords`:

```zsh
>>> DouglassWords = myString.split()
>>> DouglassWords
['I', 'was', 'born', 'in', 'Tuckahoe,', 'near', 'Hillsborough,', 'and', 'about', 'twelve', 'miles', 'from', 'Easton,', 'in', 'Talbot', 'county,', 'Maryland.', 'I', 'have', 'no', 'accurate', 'knowledge', 'of', 'my', 'age,', 'never', 'having', 'seen', 'any', 'authentic', 'record', 'containing', 'it.', 'By', 'far', 'the', 'larger', 'part', 'of', 'the', 'slaves', 'know', 'as', 'little', 'of', 'their', 'ages', 'as', 'horses', 'know', 'of', 'theirs,', 'and', 'it', 'is', 'the', 'wish', 'of', 'most', 'masters', 'within', 'my', 'knowledge', 'to', 'keep', 'their', 'slaves', 'thus', 'ignorant.', 'I', 'do', 'not', 'remember', 'to', 'have', 'ever', 'met', 'a', 'slave', 'who', 'could', 'tell', 'of', 'his', 'birthday.', 'They', 'seldom', 'come', 'nearer', 'to', 'it', 'than', 'planting-time,', 'harvest-time,', 'cherry-time,', 'spring-time,', 'or', 'fall-time.', 'A', 'want', 'of', 'information', 'concerning', 'my', 'own', 'was', 'a', 'source', 'of', 'unhappiness', 'to', 'me', 'even', 'during', 'childhood.', 'The', 'white', 'children', 'could', 'tell', 'their', 'ages.', 'I', 'could', 'not', 'tell', 'why', 'I', 'ought', 'to', 'be', 'deprived', 'of', 'the', 'same', 'privilege.', 'I', 'was', 'not', 'allowed', 'to', 'make', 'any', 'inquiries', 'of', 'my', 'master', 'concerning', 'it.', 'He', 'deemed', 'all', 'such', 'inquiries', 'on', 'the', 'part', 'of', 'a', 'slave', 'improper', 'and', 'impertinent,', 'and', 'evidence', 'of', 'a', 'restless', 'spirit.', 'The', 'nearest', 'estimate', 'I', 'can', 'give', 'makes', 'me', 'now', 'between', 'twenty-seven', 'and', 'twenty-eight', 'years', 'of', 'age.', 'I', 'come', 'to', 'this,', 'from', 'hearing', 'my', 'master', 'say,', 'some', 'time', 'during', '1835,', 'I', 'was', 'about', 'seventeen', 'years', 'old.']
```
You may find it easier to understand what happened in the above examples if you copy them and paste them into a text editor. (If your text editor is VS Code, and the pasted content shows up as long lines of text that you have to  scroll left and right to read, use `option-Z` \[Mac\] or `alt-Z` \[Windows\], to make VS Code wrap the lines to your window's width.)

Okay: we've turned the paragraph into a list, with each word becoming a separate list item. Why would we want to do that? The answer is that by turning the paragraph into a list, we can now take advantage of methods and functions available to lists. These can help us do some very rough, elementary textual analysis.

For example, whereas `len(myString)` gave us the number of *characters* in the long string `myString`, `len(DouglassWords)` will return the number of list items, revealing the total number of *words* in the paragraph, a more readily understandable measure of "paragraph length."

```zsh
>>> len(DouglassWords)
204
```
If we're interested in the *kinds* of words Douglass uses, listing them from the first to the last isn't terribly helpful. But we can use the `.sort()` method to sort our list. 

```zsh
>>> DouglassWords.sort()
>>> DouglassWords
['1835,', 'A', 'By', 'Easton,', 'He', 'Hillsborough,', 'I', 'I', 'I', 'I', 'I', 'I', 'I', 'I', 'I', 'Maryland.', 'Talbot', 'The', 'The', 'They', 'Tuckahoe,', 'a', 'a', 'a', 'a', 'about', 'about', 'accurate', 'age,', 'age.', 'ages', 'ages.', 'all', 'allowed', 'and', 'and', 'and', 'and', 'and', 'any', 'any', 'as', 'as', 'authentic', 'be', 'between', 'birthday.', 'born', 'can', 'cherry-time,', 'childhood.', 'children', 'come', 'come', 'concerning', 'concerning', 'containing', 'could', 'could', 'could', 'county,', 'deemed', 'deprived', 'do', 'during', 'during', 'estimate', 'even', 'ever', 'evidence', 'fall-time.', 'far', 'from', 'from', 'give', 'harvest-time,', 'have', 'have', 'having', 'hearing', 'his', 'horses', 'ignorant.', 'impertinent,', 'improper', 'in', 'in', 'information', 'inquiries', 'inquiries', 'is', 'it', 'it', 'it.', 'it.', 'keep', 'know', 'know', 'knowledge', 'knowledge', 'larger', 'little', 'make', 'makes', 'master', 'master', 'masters', 'me', 'me', 'met', 'miles', 'most', 'my', 'my', 'my', 'my', 'my', 'near', 'nearer', 'nearest', 'never', 'no', 'not', 'not', 'not', 'now', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'old.', 'on', 'or', 'ought', 'own', 'part', 'part', 'planting-time,', 'privilege.', 'record', 'remember', 'restless', 'same', 'say,', 'seen', 'seldom', 'seventeen', 'slave', 'slave', 'slaves', 'slaves', 'some', 'source', 'spirit.', 'spring-time,', 'such', 'tell', 'tell', 'tell', 'than', 'the', 'the', 'the', 'the', 'the', 'their', 'their', 'their', 'theirs,', 'this,', 'thus', 'time', 'to', 'to', 'to', 'to', 'to', 'to', 'to', 'twelve', 'twenty-eight', 'twenty-seven', 'unhappiness', 'want', 'was', 'was', 'was', 'was', 'white', 'who', 'why', 'wish', 'within', 'years', 'years']
```
Sorting the words in Douglass' paragraph, we immediately see that some of them&mdash;"I," "a," "to," "of," and the like&mdash;are, not surprisingly, used multiple times. We'll begin to get a clearer sense of Douglass' *vocabulary* by narrowing the list to see only the *unique* words in the paragraph.

We can do this by passing `DouglassWords`, our variable storing the list of words, as argument to the `set()` function, and creating a new variable, `unique`.

```zsh
>>> unique = set(DouglassWords)
>>> unique
{'do', 'makes', 'all', 'knowledge', 'inquiries', 'source', 'theirs,', 'Tuckahoe,', 'give', 'want', 'masters', 'never', 'A', 'can', 'white', 'on', 'from', 'planting-time,', 'within', 'estimate', 'a', 'far', 'little', 'authentic', 'fall-time.', 'this,', 'master', 'his', 'is', 'some', 'between', 'own', 'thus', 'ages.', 'old.', 'as', 'county,', 'deprived', 'of', 'have', 'I', 'born', 'record', 'childhood.', 'harvest-time,', 'or', 'say,', 'unhappiness', 'concerning', 'years', 'and', 'my', 'By', 'The', 'children', 'know', 'age,', 'than', 'Hillsborough,', 'containing', 'not', 'near', 'Easton,', 'met', 'ignorant.', 'twenty-eight', 'wish', 'even', 'nearest', 'privilege.', 'come', 'seen', 'twelve', 'no', 'spirit.', 'having', 'miles', 'He', 'hearing', 'make', 'could', 'same', 'horses', 'seldom', 'the', 'larger', 'me', 'who', 'Talbot', 'why', 'most', 'it.', 'remember', 'time', 'improper', 'tell', 'ever', 'allowed', 'now', 'to', 'in', 'such', 'during', 'impertinent,', 'keep', 'it', 'evidence', '1835,', 'nearer', 'was', 'cherry-time,', 'slaves', 'any', 'information', 'Maryland.', 'age.', 'birthday.', 'about', 'deemed', 'accurate', 'part', 'ought', 'spring-time,', 'their', 'be', 'slave', 'They', 'seventeen', 'restless', 'ages', 'twenty-seven'}
```
Notice that the set function produces a set, not a list. The output is enclosed in the curly brackets conventionally used in set notation. In addition to **list**, Python has three other data types for storing collections of data. One of them is **set**; the others are **tuple** and **dictionary**.

We can use the `len()` function with sets.

```zsh
>>> len(unique)
131
```
It would be nice to sort the set alphabetically, as we did the list earlier. We can't use the `.sort()` method with sets, but we *can* use the function `sorted()`. Here's what we get when we do:

```zsh
>>> sorted(unique)
['1835,', 'A', 'By', 'Easton,', 'He', 'Hillsborough,', 'I', 'Maryland.', 'Talbot', 'The', 'They', 'Tuckahoe,', 'a', 'about', 'accurate', 'age,', 'age.', 'ages', 'ages.', 'all', 'allowed', 'and', 'any', 'as', 'authentic', 'be', 'between', 'birthday.', 'born', 'can', 'cherry-time,', 'childhood.', 'children', 'come', 'concerning', 'containing', 'could', 'county,', 'deemed', 'deprived', 'do', 'during', 'estimate', 'even', 'ever', 'evidence', 'fall-time.', 'far', 'from', 'give', 'harvest-time,', 'have', 'having', 'hearing', 'his', 'horses', 'ignorant.', 'impertinent,', 'improper', 'in', 'information', 'inquiries', 'is', 'it', 'it.', 'keep', 'know', 'knowledge', 'larger', 'little', 'make', 'makes', 'master', 'masters', 'me', 'met', 'miles', 'most', 'my', 'near', 'nearer', 'nearest', 'never', 'no', 'not', 'now', 'of', 'old.', 'on', 'or', 'ought', 'own', 'part', 'planting-time,', 'privilege.', 'record', 'remember', 'restless', 'same', 'say,', 'seen', 'seldom', 'seventeen', 'slave', 'slaves', 'some', 'source', 'spirit.', 'spring-time,', 'such', 'tell', 'than', 'the', 'their', 'theirs,', 'this,', 'thus', 'time', 'to', 'twelve', 'twenty-eight', 'twenty-seven', 'unhappiness', 'want', 'was', 'white', 'who', 'why', 'wish', 'within', 'years']
```

If you look closely, you'll see that our set treats `'A'` and `'a'` as two different set elements. It does the same with `'The'` and `'the'`. If we wanted to be rigorous about counting unique words, we'd probably want to treat `The/the` and `A/a` as one word each. 

Searching by eye for set elements that differ only by case is tedious and error-prone. What could we have done to avoid this predicament?

We could have used the `.lower()` method with our original string, `myString`, before converting it to a list. This would have turned all instances of `The` to `the` and all instances of `A` to `a`. 

Nothing we did above changed the value of our original variable, `myString`, so let's retrace our steps, this time taking advantage of `.lower()`.

```zsh
>>> myString
'I was born in Tuckahoe, near Hillsborough, and about twelve miles from Easton, in Talbot county, Maryland. I have no accurate knowledge of my age, never having seen any authentic record containing it. By far the larger part of the slaves know as little of their ages as horses know of theirs, and it is the wish of most masters within my knowledge to keep their slaves thus ignorant. I do not remember to have ever met a slave who could tell of his birthday. They seldom come nearer to it than planting-time, harvest-time, cherry-time, spring-time, or fall-time. A want of information concerning my own was a source of unhappiness to me even during childhood. The white children could tell their ages. I could not tell why I ought to be deprived of the same privilege. I was not allowed to make any inquiries of my master concerning it. He deemed all such inquiries on the part of a slave improper and impertinent, and evidence of a restless spirit. The nearest estimate I can give makes me now between twenty-seven and twenty-eight years of age. I come to this, from hearing my master say, some time during 1835, I was about seventeen years old.'
>>> myStringLower = myString.lower()
>>> DouglassWords = myStringLower.split()
>>> DouglassWords
['i', 'was', 'born', 'in', 'tuckahoe,', 'near', 'hillsborough,', 'and', 'about', 'twelve', 'miles', 'from', 'easton,', 'in', 'talbot', 'county,', 'maryland.', 'i', 'have', 'no', 'accurate', 'knowledge', 'of', 'my', 'age,', 'never', 'having', 'seen', 'any', 'authentic', 'record', 'containing', 'it.', 'by', 'far', 'the', 'larger', 'part', 'of', 'the', 'slaves', 'know', 'as', 'little', 'of', 'their', 'ages', 'as', 'horses', 'know', 'of', 'theirs,', 'and', 'it', 'is', 'the', 'wish', 'of', 'most', 'masters', 'within', 'my', 'knowledge', 'to', 'keep', 'their', 'slaves', 'thus', 'ignorant.', 'i', 'do', 'not', 'remember', 'to', 'have', 'ever', 'met', 'a', 'slave', 'who', 'could', 'tell', 'of', 'his', 'birthday.', 'they', 'seldom', 'come', 'nearer', 'to', 'it', 'than', 'planting-time,', 'harvest-time,', 'cherry-time,', 'spring-time,', 'or', 'fall-time.', 'a', 'want', 'of', 'information', 'concerning', 'my', 'own', 'was', 'a', 'source', 'of', 'unhappiness', 'to', 'me', 'even', 'during', 'childhood.', 'the', 'white', 'children', 'could', 'tell', 'their', 'ages.', 'i', 'could', 'not', 'tell', 'why', 'i', 'ought', 'to', 'be', 'deprived', 'of', 'the', 'same', 'privilege.', 'i', 'was', 'not', 'allowed', 'to', 'make', 'any', 'inquiries', 'of', 'my', 'master', 'concerning', 'it.', 'he', 'deemed', 'all', 'such', 'inquiries', 'on', 'the', 'part', 'of', 'a', 'slave', 'improper', 'and', 'impertinent,', 'and', 'evidence', 'of', 'a', 'restless', 'spirit.', 'the', 'nearest', 'estimate', 'i', 'can', 'give', 'makes', 'me', 'now', 'between', 'twenty-seven', 'and', 'twenty-eight', 'years', 'of', 'age.', 'i', 'come', 'to', 'this,', 'from', 'hearing', 'my', 'master', 'say,', 'some', 'time', 'during', '1835,', 'i', 'was', 'about', 'seventeen', 'years', 'old.']
>>> len(DouglassWords)
204
>>> DouglassWords.sort()
>>> DouglassWords
['1835,', 'a', 'a', 'a', 'a', 'a', 'about', 'about', 'accurate', 'age,', 'age.', 'ages', 'ages.', 'all', 'allowed', 'and', 'and', 'and', 'and', 'and', 'any', 'any', 'as', 'as', 'authentic', 'be', 'between', 'birthday.', 'born', 'by', 'can', 'cherry-time,', 'childhood.', 'children', 'come', 'come', 'concerning', 'concerning', 'containing', 'could', 'could', 'could', 'county,', 'deemed', 'deprived', 'do', 'during', 'during', 'easton,', 'estimate', 'even', 'ever', 'evidence', 'fall-time.', 'far', 'from', 'from', 'give', 'harvest-time,', 'have', 'have', 'having', 'he', 'hearing', 'hillsborough,', 'his', 'horses', 'i', 'i', 'i', 'i', 'i', 'i', 'i', 'i', 'i', 'ignorant.', 'impertinent,', 'improper', 'in', 'in', 'information', 'inquiries', 'inquiries', 'is', 'it', 'it', 'it.', 'it.', 'keep', 'know', 'know', 'knowledge', 'knowledge', 'larger', 'little', 'make', 'makes', 'maryland.', 'master', 'master', 'masters', 'me', 'me', 'met', 'miles', 'most', 'my', 'my', 'my', 'my', 'my', 'near', 'nearer', 'nearest', 'never', 'no', 'not', 'not', 'not', 'now', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'old.', 'on', 'or', 'ought', 'own', 'part', 'part', 'planting-time,', 'privilege.', 'record', 'remember', 'restless', 'same', 'say,', 'seen', 'seldom', 'seventeen', 'slave', 'slave', 'slaves', 'slaves', 'some', 'source', 'spirit.', 'spring-time,', 'such', 'talbot', 'tell', 'tell', 'tell', 'than', 'the', 'the', 'the', 'the', 'the', 'the', 'the', 'their', 'their', 'their', 'theirs,', 'they', 'this,', 'thus', 'time', 'to', 'to', 'to', 'to', 'to', 'to', 'to', 'tuckahoe,', 'twelve', 'twenty-eight', 'twenty-seven', 'unhappiness', 'want', 'was', 'was', 'was', 'was', 'white', 'who', 'why', 'wish', 'within', 'years', 'years']
>>> unique = set(DouglassWords)
>>> unique
{'do', 'easton,', 'makes', 'all', 'knowledge', 'inquiries', 'source', 'theirs,', 'give', 'want', 'masters', 'never', 'by', 'can', 'white', 'on', 'from', 'planting-time,', 'within', 'estimate', 'a', 'far', 'little', 'authentic', 'fall-time.', 'this,', 'master', 'his', 'is', 'some', 'between', 'own', 'thus', 'ages.', 'old.', 'as', 'county,', 'deprived', 'of', 'have', 'born', 'record', 'childhood.', 'harvest-time,', 'or', 'say,', 'unhappiness', 'concerning', 'years', 'and', 'my', 'tuckahoe,', 'children', 'i', 'know', 'age,', 'than', 'containing', 'not', 'near', 'met', 'ignorant.', 'twenty-eight', 'wish', 'even', 'nearest', 'maryland.', 'privilege.', 'come', 'seen', 'he', 'twelve', 'no', 'spirit.', 'having', 'miles', 'hearing', 'make', 'could', 'they', 'same', 'horses', 'seldom', 'the', 'larger', 'me', 'who', 'why', 'most', 'it.', 'remember', 'time', 'improper', 'tell', 'ever', 'allowed', 'now', 'to', 'in', 'such', 'during', 'impertinent,', 'keep', 'it', 'evidence', '1835,', 'nearer', 'was', 'cherry-time,', 'slaves', 'any', 'information', 'age.', 'birthday.', 'about', 'deemed', 'accurate', 'part', 'ought', 'spring-time,', 'their', 'be', 'slave', 'seventeen', 'talbot', 'hillsborough,', 'restless', 'ages', 'twenty-seven'}
>>> len(unique)
129
```

In addition, to `.lower()`, other useful methods for working with strings include `.upper()`, which converts all letters to uppercase, `.title()`, which capitalizes the first letter of each word in a string (title case), `.replace()`, which enables you to search and replace within a string, `.rfind()`, which will return the last position a search term is found within a string, and `.strip()`, which will strip white space from both ends of a string.

W3Schools has helpful pages on [string methods](https://www.w3schools.com/python/python_strings_methods.asp) and [list methods](https://www.w3schools.com/python/python_ref_list.asp) you can use in Python.

Our little bit of text analysis using the first paragraph of Douglass' *Narrative* doesn't tell us much about Douglass as a writer or this particular sample of his writing. Hopefully, though, you can see how applying the techniques above to the entirety of the *Narrative*, and to other Douglass texts as well, might begin to yield valuable insights.

Perhaps more to the point for this module, hopefully our Douglass example has given you a feel for how we can use functions and methods with different types of Python objects.

Researchers interested in computational text analysis have created sophisticated Python tools for obtaining results that are much more precise, nuanced, and varied than those shown here, tools that can also be applied at scale to a collection of texts, known as a **corpus**. One example is the [Natural Language Toolkit (NLTK)](https://www.nltk.org/). By now, you know enough Python to be able to explore the online book ["Analyzing Text with the Natural Language Toolkit"](https://www.nltk.org/book/) if you're interested.
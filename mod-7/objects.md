---
title: Objects
layout: default
parent: Python Brief Intro
nav_order: 13
---
# Objects

Python is an **object-oriented** programming language. Just about everything in Python is an "object." As [Wikipedia](https://en.wikipedia.org/wiki/Object-oriented_programming) explains, objects are components "that can contain data and code. The data is in the form of fields (often known as attributes or *properties*), and the code is in the form of procedures (often known as *methods*)."

One way to think of methods is as functions attached to certain objects. Here's an example:

```zsh
>>> myTerms = ['copyright', 'privacy', 'open access', 'data', 'bias', 'copyleft', 'ethics', 'universal design']
>>> myTerms.sort()
>>> myTerms
['bias', 'copyleft', 'copyright', 'data', 'ethics', 'open access', 'privacy', 'universal design']
>>> 
```
What happened here? We began with a list, assigned to the variable `myTerms`. We then used the `sort()` method, a special kind of function available to the `list` data type, to sort the list alphabetically.

We access the sort method using the notation you see above, appending `.sort()` to the variable we want to use it on.

You can learn about [other methods you can use with lists](https://www.w3schools.com/python/python_ref_list.asp) at W3Schools.

Maybe we find we need to add an item to our list:

```zsh
>>> myTerms.append('accessibility')
>>> myTerms
['copyright', 'privacy', 'open access', 'data', 'bias', 'copyleft', 'ethics', 'universal design', 'accessibility']
```
The term we appended to the list is added to the end, messing up our nice alphabetization. How would you move it to the right location?

## String methods

There are many useful methods we can use with strings.

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
We can also go in the other direction, creating a list from a string with the `.split()` method.

```zsh
>>> myString = "I was born in Tuckahoe, near Hillsborough, and about twelve miles from Easton, in Talbot county, Maryland. I have no accurate knowledge of my age, never having seen any authentic record containing it. By far the larger part of the slaves know as little of their ages as horses know of theirs, and it is the wish of most masters within my knowledge to keep their slaves thus ignorant. I do not remember to have ever met a slave who could tell of his birthday. They seldom come nearer to it than planting-time, harvest-time, cherry-time, spring-time, or fall-time. A want of information concerning my own was a source of unhappiness to me even during childhood. The white children could tell their ages. I could not tell why I ought to be deprived of the same privilege. I was not allowed to make any inquiries of my master concerning it. He deemed all such inquiries on the part of a slave improper and impertinent, and evidence of a restless spirit. The nearest estimate I can give makes me now between twenty-seven and twenty-eight years of age. I come to this, from hearing my master say, some time during 1835, I was about seventeen years old."
>>> myString.split()
['I', 'was', 'born', 'in', 'Tuckahoe,', 'near', 'Hillsborough,', 'and', 'about', 'twelve', 'miles', 'from', 'Easton,', 'in', 'Talbot', 'county,', 'Maryland.', 'I', 'have', 'no', 'accurate', 'knowledge', 'of', 'my', 'age,', 'never', 'having', 'seen', 'any', 'authentic', 'record', 'containing', 'it.', 'By', 'far', 'the', 'larger', 'part', 'of', 'the', 'slaves', 'know', 'as', 'little', 'of', 'their', 'ages', 'as', 'horses', 'know', 'of', 'theirs,', 'and', 'it', 'is', 'the', 'wish', 'of', 'most', 'masters', 'within', 'my', 'knowledge', 'to', 'keep', 'their', 'slaves', 'thus', 'ignorant.', 'I', 'do', 'not', 'remember', 'to', 'have', 'ever', 'met', 'a', 'slave', 'who', 'could', 'tell', 'of', 'his', 'birthday.', 'They', 'seldom', 'come', 'nearer', 'to', 'it', 'than', 'planting-time,', 'harvest-time,', 'cherry-time,', 'spring-time,', 'or', 'fall-time.', 'A', 'want', 'of', 'information', 'concerning', 'my', 'own', 'was', 'a', 'source', 'of', 'unhappiness', 'to', 'me', 'even', 'during', 'childhood.', 'The', 'white', 'children', 'could', 'tell', 'their', 'ages.', 'I', 'could', 'not', 'tell', 'why', 'I', 'ought', 'to', 'be', 'deprived', 'of', 'the', 'same', 'privilege.', 'I', 'was', 'not', 'allowed', 'to', 'make', 'any', 'inquiries', 'of', 'my', 'master', 'concerning', 'it.', 'He', 'deemed', 'all', 'such', 'inquiries', 'on', 'the', 'part', 'of', 'a', 'slave', 'improper', 'and', 'impertinent,', 'and', 'evidence', 'of', 'a', 'restless', 'spirit.', 'The', 'nearest', 'estimate', 'I', 'can', 'give', 'makes', 'me', 'now', 'between', 'twenty-seven', 'and', 'twenty-eight', 'years', 'of', 'age.', 'I', 'come', 'to', 'this,', 'from', 'hearing', 'my', 'master', 'say,', 'some', 'time', 'during', '1835,', 'I', 'was', 'about', 'seventeen', 'years', 'old.']
```
You may find it easier to understand what happened in the above example if you copy the whole thing and paste it into a text editor. We took the first paragraph of Frederick Douglass' *Narrative of the Life of Frederick Douglass, An American Slave* and turned it into a list, with each word becoming a separate list item.

Why would anyone want to do that? The answer is that by turning the paragraph into a list, we can now take advantage of methods and functions available to lists. These can help us do some elementary textual analysis.

```zsh
>>> myString = "I was born in Tuckahoe, near Hillsborough, and about twelve miles from Easton, in Talbot county, Maryland. I have no accurate knowledge of my age, never having seen any authentic record containing it. By far the larger part of the slaves know as little of their ages as horses know of theirs, and it is the wish of most masters within my knowledge to keep their slaves thus ignorant. I do not remember to have ever met a slave who could tell of his birthday. They seldom come nearer to it than planting-time, harvest-time, cherry-time, spring-time, or fall-time. A want of information concerning my own was a source of unhappiness to me even during childhood. The white children could tell their ages. I could not tell why I ought to be deprived of the same privilege. I was not allowed to make any inquiries of my master concerning it. He deemed all such inquiries on the part of a slave improper and impertinent, and evidence of a restless spirit. The nearest estimate I can give makes me now between twenty-seven and twenty-eight years of age. I come to this, from hearing my master say, some time during 1835, I was about seventeen years old."
>>> DouglassWords = myString.split()
>>> DouglassWords.sort()
>>> DouglassWords
['1835,', 'A', 'By', 'Easton,', 'He', 'Hillsborough,', 'I', 'I', 'I', 'I', 'I', 'I', 'I', 'I', 'I', 'Maryland.', 'Talbot', 'The', 'The', 'They', 'Tuckahoe,', 'a', 'a', 'a', 'a', 'about', 'about', 'accurate', 'age,', 'age.', 'ages', 'ages.', 'all', 'allowed', 'and', 'and', 'and', 'and', 'and', 'any', 'any', 'as', 'as', 'authentic', 'be', 'between', 'birthday.', 'born', 'can', 'cherry-time,', 'childhood.', 'children', 'come', 'come', 'concerning', 'concerning', 'containing', 'could', 'could', 'could', 'county,', 'deemed', 'deprived', 'do', 'during', 'during', 'estimate', 'even', 'ever', 'evidence', 'fall-time.', 'far', 'from', 'from', 'give', 'harvest-time,', 'have', 'have', 'having', 'hearing', 'his', 'horses', 'ignorant.', 'impertinent,', 'improper', 'in', 'in', 'information', 'inquiries', 'inquiries', 'is', 'it', 'it', 'it.', 'it.', 'keep', 'know', 'know', 'knowledge', 'knowledge', 'larger', 'little', 'make', 'makes', 'master', 'master', 'masters', 'me', 'me', 'met', 'miles', 'most', 'my', 'my', 'my', 'my', 'my', 'near', 'nearer', 'nearest', 'never', 'no', 'not', 'not', 'not', 'now', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'of', 'old.', 'on', 'or', 'ought', 'own', 'part', 'part', 'planting-time,', 'privilege.', 'record', 'remember', 'restless', 'same', 'say,', 'seen', 'seldom', 'seventeen', 'slave', 'slave', 'slaves', 'slaves', 'some', 'source', 'spirit.', 'spring-time,', 'such', 'tell', 'tell', 'tell', 'than', 'the', 'the', 'the', 'the', 'the', 'their', 'their', 'their', 'theirs,', 'this,', 'thus', 'time', 'to', 'to', 'to', 'to', 'to', 'to', 'to', 'twelve', 'twenty-eight', 'twenty-seven', 'unhappiness', 'want', 'was', 'was', 'was', 'was', 'white', 'who', 'why', 'wish', 'within', 'years', 'years']

```
How many words are in the paragraph? We can find the answer using the `len()` function, which we encountered earlier.

```zsh
>>> len(DouglassWords)
204
```
But a lot of words, such as "I," "to," and "of," are used multiple times. What if we want to know how many unique words there are in the paragraph?

One thing we see right away here is that quite a few words are used multiple times in the paragraph. What if we wanted how many unique words are used in the paragraph?

```zsh
>>> unique = set(DouglassWords)
>>> unique
{'most', 'birthday.', 'years', 'during', 'authentic', 'give', 'miles', 'deemed', 'He', 'nearest', 'white', 'little', 'masters', 'restless', 'seen', 'be', 'makes', 'Hillsborough,', 'impertinent,', 'is', 'me', 'A', 'knowledge', 'same', 'seldom', 'than', 'cherry-time,', 'wish', 'deprived', 'Maryland.', 'The', 'childhood.', 'on', 'They', 'such', 'slave', 'ignorant.', 'can', 'it.', 'fall-time.', 'of', 'all', 'allowed', 'do', 'ever', 'Easton,', 'remember', 'containing', 'time', 'from', 'accurate', 'age.', 'was', 'hearing', 'county,', 'no', 'age,', 'near', 'who', 'never', 'slaves', 'not', 'want', 'record', 'tell', 'born', 'a', 'unhappiness', 'in', 'between', 'source', 'within', 'privilege.', 'ought', 'estimate', 'improper', 'his', 'information', 'seventeen', 'part', 'and', 'why', 'to', 'ages', 'the', 'know', 'I', 'planting-time,', 'theirs,', 'old.', 'having', 'twenty-eight', 'make', 'ages.', 'about', 'far', 'By', 'Talbot', 'as', 'thus', 'own', 'any', 'now', 'nearer', 'evidence', 'their', '1835,', 'or', 'some', 'it', 'keep', 'this,', 'twelve', 'my', 'horses', 'even', 'harvest-time,', 'Tuckahoe,', 'inquiries', 'say,', 'have', 'twenty-seven', 'spring-time,', 'concerning', 'master', 'met', 'children', 'spirit.', 'larger', 'come', 'could'}
```
Notice that the set function produces a set, not a list. The output is enclosed in the curly brackets conventionally used in set notation. In addition to **list**, Python has three other data types for storing collections of data: **set, tuple,** and **dictionary**.

We can use the `len()` function with sets.

```zsh
>>> len(unique)
131
```
We can't use the `.sort()` method with sets. But if we want to sort this set alphabetically, we *can* use the function `sorted()`. Here's what we get when we do:

```zsh
>>> sorted(unique)
['1835,', 'A', 'By', 'Easton,', 'He', 'Hillsborough,', 'I', 'Maryland.', 'Talbot', 'The', 'They', 'Tuckahoe,', 'a', 'about', 'accurate', 'age,', 'age.', 'ages', 'ages.', 'all', 'allowed', 'and', 'any', 'as', 'authentic', 'be', 'between', 'birthday.', 'born', 'can', 'cherry-time,', 'childhood.', 'children', 'come', 'concerning', 'containing', 'could', 'county,', 'deemed', 'deprived', 'do', 'during', 'estimate', 'even', 'ever', 'evidence', 'fall-time.', 'far', 'from', 'give', 'harvest-time,', 'have', 'having', 'hearing', 'his', 'horses', 'ignorant.', 'impertinent,', 'improper', 'in', 'information', 'inquiries', 'is', 'it', 'it.', 'keep', 'know', 'knowledge', 'larger', 'little', 'make', 'makes', 'master', 'masters', 'me', 'met', 'miles', 'most', 'my', 'near', 'nearer', 'nearest', 'never', 'no', 'not', 'now', 'of', 'old.', 'on', 'or', 'ought', 'own', 'part', 'planting-time,', 'privilege.', 'record', 'remember', 'restless', 'same', 'say,', 'seen', 'seldom', 'seventeen', 'slave', 'slaves', 'some', 'source', 'spirit.', 'spring-time,', 'such', 'tell', 'than', 'the', 'their', 'theirs,', 'this,', 'thus', 'time', 'to', 'twelve', 'twenty-eight', 'twenty-seven', 'unhappiness', 'want', 'was', 'white', 'who', 'why', 'wish', 'within', 'years']
```

If you look closely, you'll see that our set treats `'A'` and `'a'` as two different set elements. It does the same with `'The'` and `'the'`. If we wanted to be rigorous about counting unique words, we'd probably want to treat `The/the` and `A/a` as one word each. However, searching by eye for set elements that differ only by case is tedious and error-prone. We would have been well served by using the string method `.lower()` on our original string, before converting it to a list. This method converts all letters in a string to lowercase.

Other string methods you can use with strings include `.upper()`, which converts all letters to uppercase, `.title()`, which capitalizes the first letter of each word in a string (title case), `.replace()`, which enables you to search and replace within a string, `.rfind()`, which will return the last position a search term is found within a string, and `.strip()`, which will strip white space from both ends of a string.

W3Schools has a useful [list of string methods in Python](https://www.w3schools.com/python/python_strings_methods.asp).
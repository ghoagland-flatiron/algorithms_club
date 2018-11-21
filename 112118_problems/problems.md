# Problems

## Find Missing Element

Given and array of numbers and a second array formed by shuffling the elements of the first array and deleting a random element, return the element that is missing from the second array.

This method can be done in linear time - no nested loops!

## Anagram Detection

Write a function that accepts two parameters, a parent and a child string. Determine how many times the child string - or an anagram of the child string - appears in the parent string. There is a solution which can be done in near instant time.

```js
f('AdnBndAndBdaBn', 'dAn')
// 4 ("Adn", "ndA", "dAn", "And")
f('AbrAcadAbRa', 'cAda')
// 2 (Acad, cadA)
```

[Source][anagram-source]


## I before E?

You may have heard the mnemonic 'i before e, except after c'. Is this reasonable?

We will be using the word list found [here][word-list].

In order to determine if this whole statement is plausible, we need to determine if the following two sub-statements are plausible:
  1. 'i' before 'e' when not proceeded by 'c'.
  2. 'e' before 'i' when proceeded by 'c'.

If both of those statements are plausible, the whole statement us said to be plausible.


We say that a statement is plausible if the number of words having the feature is more than two times the number of words having the opposite feature (where feature is 'ie' or 'ei' preceded or not by 'c' as appropriate).


So our first statement needs to know the number of times we have 'ie' with no 'c' vs. 'ei' with no 'c'. The second statement will compare the number of 'cie' to the number of 'cei'.

[Source][i-e-source]


[anagram-source]: https://github.com/blakeembrey/code-problems/tree/master/problems/anagram-detection#anagram-detection

[word-list]: http://wiki.puzzlers.org/pub/wordlists/unixdict.txt

[i-e-source]: http://rosettacode.org/wiki/I_before_E_except_after_C#Python

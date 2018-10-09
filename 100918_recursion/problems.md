# Recursion
## Questions

1. `reverse` - Write a recursive function to reverse a string. So `reverse('recursion') => 'noisrucer'`. What is your base case? How can you build up from there to the next step or how can you get reduce a long string to a base case?

2. `arr_sum` - Given an array that is composed of numbers and arrays that themselves may contain arrays and/or numbers that may be arbitrarily deeply nested, write a function that returns the sum of all the numbers. For example, `arr_sum([1, [2, [3, [4, [5]]]]]) => 15` and `arr_sum([[[[[[2], [3]]]]]]) => 5`. You may not convert to a string or otherwise flatten.

3. Boggle Checker - given a function `is_word?` that returns true if a string is a word and false if it is not and an array that represents the letters on a Boggle board, return an array of all possible words.

### What is Boggle?

Boggle is a game where you have a 4 x 4 grid of letters and you look for words. Words are made of letters that are directly adjacent to or diagonal from the last letter. A letter in a particular position can only be used once per word.

```
B A B Z
T R E M
O P M J
Y W H T
```

Above, we have the words 'art', 'bat', and 'rope', and 'babe' but not 'rare' - we can't use the same 'r' twice.

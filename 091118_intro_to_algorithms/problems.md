# Intro to Algorithms
## Questions

### Capitalize
Write a function that captializes the first letter of every word in a string.

### String Search (or, `indexOf`)
Note: You may not use built-in methods like `indexOf` to shortcut for this.

Given two strings, find the index of the first appearance of the first string inside the other. Think of this as finding the needle in the haystack.

Given `'had'` and `'you had me at hello'`, you would return `4` since index 4 is where `'had'` begins.

Things to consider: What are the edge cases? How will you handle them? How can you make this function more efficient?


### Roman Numerals
Write a method that converts an integer to its Roman numeral equivalent. In other words, if we give our method the Arabic number 476, our method will return the Roman numeral CDLXXVI.

| Arabic Number  | Roman Numeral |
| -------------- | ------------- |
| 1              | I             |
| 2              | II            |
| 3              | III           |
| 4              | IV            |
| 5              | V             |
| 6              | VI            |
| 9              | IX            |
| 10             | X             |
| 20             | XX            |
| 40             | XL            |
| 50             | L             |
| 100            | C             |
| 500            | D             |
| 1000           | M             |

More examples:

| Arabic Number | Roman Numeral |
| ------------- | ------------- |
| 4             | IV            |
| 9             | IX            |
| 14            | XIV           |
| 44            | XLIV          |
| 99            | XCIX          |
| 400           | CD            |
| 944           | CMXLIV        |

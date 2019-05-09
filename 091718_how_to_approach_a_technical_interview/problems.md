# How to approach a technical interview
## The REACTO approach
From my time at Grace Hopper/Fullstack, I learned this useful mnemonic to approach technical interviews.
For more information, this is their blog post on the topic: https://www.fullstackacademy.com/blog/how-to-ace-a-technical-interview-reacto
  ```
  R E A C T O
  e x p o e p
  p a p d s t
  e m r e t i
  a p o     m
  t l a     i
    e c     z
      h     e
```

## Questions
### Coconuts
You are stuck on a desert island and for some inscrutable reason your survival depends on figuring out which one of 9 otherwise identical coconuts is heavier than the others. You didn't bring your bathroom scale because... you're stuck there, it's not really a choice. But you have some planks and a rock and have made a balance scales. What is the minimum number of times you need to weigh the coconuts to be certain which is the odd one out - the sun is so hot and you really need this heavy coconut.  

### Balanced Brackets

1. Write a function that analyzes a string and tells if the the parentheses in the string are balanced - i.e. `(abcd)` is balanced but `(efgh))` is not. Also note that while `)(ijkl)(()` may have an equal number of open and closed parentheses, it is not valid.

2. Refactor your function to work for not just parentheses but square and curly braces as well. Note that `([{({qrst()})}])` is valid but `([mnop)]` is invalid.

### Count Duplicates

Write a function that will return the count of _distinct_ case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.
(From [Codewars](http://www.codewars.com/kata/54bf1c2cd5b56cc47f0007a1/train/python))

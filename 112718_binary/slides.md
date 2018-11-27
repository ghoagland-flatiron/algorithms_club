
# Binary

---
## What is binary?

A binary number system has numbers in base 2 - that is to say we only use the symbols `0` and `1` to represent a digit. The number system we are used to using is decimal, where we use the symbols `0` to `9` in any single digit. If we are counting in binary, just as in decimal, when we have gone through our symbols, we add a symbol to the left to represent the overflow.

| decimal |  0   |  1   |  2   |  3   |  4   |  5   |  6   |  7   |  8   |
|---------|------|------|------|------|------|------|------|------|------|
| binary  | 0000 | 0001 | 0010 | 0011 | 0100 | 0101 | 0110 | 0111 | 1000 |

----

## Thinking in binary

One way to think about this is how we can represent a number as a sum of powers of 2.

In decimal, we can easily use the number to describe how it can be shown as the sum of numbers modulo 10 multiplied by a power of 10.


| 4              | 7              | 1              |
|----------------|----------------|----------------|
| 10<sup>2</sup> | 10<sup>1</sup> | 10<sup>0</sup> |
| 100            | 10             | 1              |



471 = 4 \* 10<sup>2</sup> + 7 \* 10<sup>1</sup> + 1 \* 10<sup>0</sup>

    = 4 \* 100 + 7 \* 10 + 1 \* 1
    = 400 + 70 + 1




Or 203:

203 = 2 \* 10<sup>2</sup> + 0 \* 10<sup>1</sup> + 3 \* 10<sup>0</sup>

    = (2 * 100) + (0 * 10) + (3 * 1)
    = 200 + 00 + 3


---


So if we see the binary number 1010, we can convert this to decimal in a similar way.

| 1             | 0             | 1             | 0             |
|---------------|---------------|---------------|---------------|
| 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
| 8             | 4             | 2             | 1             |

Here, we take this same breakdown of the binary `1010` and convert it to decimal.

`1010` => (1 \* 2<sup>3</sup>) + (0 \* 2<sup>2</sup>) + (1 \* 2<sup>1</sup>)+ (0 \* 2<sup>0</sup>)

     => (1 * 8) + (0 * 4) + (1 * 2) + (0 * 1)

     => 8 + 0 + 2 + 0

     => 10

---

## Converting to binary

So say we now want to convert the number 27 to binary.

Let's think about this from largest digit to smallest digit.

First, what is the largest power of two that is less than 27?

| 2<sup>0</sup> | 2<sup>1</sup> | 2<sup>2</sup> | 2<sup>3</sup> | 2<sup>4</sup> | 2<sup>5</sup> |
|---------------|---------------|---------------|---------------|---------------|---------------|
| 1             | 2             | 4             | 8             | 16            | 32            |

So 2<sup>4</sup> (16) is the largest power of 2 less than 27. So the leftmost digit will be in the 5th place (remember it's zero indexed!)

So then we can take out 16 from 27.

27 = 16 + 11

   = 2<sup>4</sup> + 11

We now repeat this process for 11.

Does 11 contain 2<sup>3</sup> (8) i.e. is 11 >= 8? Yes.

So we have a 1 in the 8s digit.

27 = 16 + 8 + 3

   = (1 \* 2<sup>4</sup>) + (1 \* 2<sup>3</sup>) + 3

Does 3 contain 2<sup>2</sup> (4) i.e. is 3 >= 4? No.

Then there is a 0 in the 4s digit.

27 = 16 + 8 + 0 +  3

   = (1 \* 2<sup>4</sup>) + (1 \* 2<sup>3</sup>) + (0 \* 2<sup>2</sup>) + 3


---

Does 3 contain 2<sup>1</sup> (2) i.e. is 3 >= 2? Yes.

Then there is a 1 in the 2s digit.

27 = 16 + 8 + 0 + 2 + 1

   = (1 \* 2<sup>4</sup>) + (1 \* 2<sup>3</sup>) + (0 \* 2<sup>2</sup>) + (1 \* 2<sup>1</sup>) + 1


Does 1 contain 2<sup>0</sup> (1) i.e. is 1 >= 1? Yes.

   Then there is a 1 in the 1s digit.

   27 = 16 + 8 + 0 + 2 + 1

= (1 \* 2<sup>4</sup>) + (1 \* 2<sup>3</sup>) + (0 \* 2<sup>2</sup>) + (1 \* 2<sup>1</sup>) + (1 \* 2<sup>0</sup>)

  From this, we can pull out those leading 1s and 0s to show that

  ```
    27 => 11011
  ```

---

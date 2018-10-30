# Number Theory
## More Information

If you want to learn more about cryptography, here is a site that helps you build up your crypto skills:
https://cryptopals.com/

Here is a link to a talk I gave that is an introduction to the topic of elliptic curve cryptography:
https://www.youtube.com/watch?v=JPTfivFVGe8

## Problems

### Decoder Ring
You want to trade secret messages with your friends. You decide that you are going to shift all of your messages over by a few letters so `A` becomes `F`, `B` becomes `G`, and `Z` becomes `E`.

| plaintext  | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |   
|------------|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| encrypted  | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E |

Write two functions, one to encode and one to decode, that take in the number of letters you are shifting by and the string you are encoding or decoding.

For a more advanced version, try making an [Affine Substitution Cipher](https://en.wikipedia.org/wiki/Affine_cipher).

### Sieve of Eratosthenes

This is a method for finding all primes less than a set number `n`. Starting from 2, you remove all multiples of two up to and including `n`. You move on to the next number that hasn't been removed and repeat the process until you have found all the primes. Since you have removed the multiples of all the smaller primes, if a number has not been removed it must be prime.

![Sieve of Eratosthenes Animation](./Sieve_of_Eratosthenes_animation.gif)

For more information, visit https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes

### Euclidean Algorithm

A quicker way to find the GCD of two numbers than finding their prime factorizations and comparing is to use the Euclidean algorithm.

An introduction to the Euclidean algorithm can be found at http://sites.math.rutgers.edu/~greenfie/gs2004/euclid.html

This explains how it works and provides some links that explain _why_ this works.

Basically, assign `a` and `b` so `a > b`.
Divide `a` by `b` to find the `q` and `r` where

`a = qb + r`
and
`0 <= r < b`

Repeat this process with `b` and `r` as your new `a` and `b`. The process ends when `r = 0` and then your `q` value is the GCD.

Example:
```
88 and 121

  a = q *  b +  r

121 = 1 * 88 + 33
 88 = 2 * 33 + 22
 33 = 1 * 22 + 11
 22 = 2 * 11 +  0
           ^    stop

GCD(121, 88) = 11
```

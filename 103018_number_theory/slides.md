
# Number Theory

---

# What is Number Theory?

Number theory is the study of integers, i.e. whole numbers. Much of the subject is devoted to studying the general properties of integers.

Of particular interest are __prime numbers__, numbers only divisible by themselves and 1.

---

# Modulo

We say that a number `a` is congruent to a number `b` modulo a number `n` if there are some integer `m`, so that `a + mn = b`. Another way of thinking about this is that `a` and `b` have the same **remainder** when divided by `n`.

$$
a \equiv b (\bmod n)
$$


---

# Prime numbers

Why are prime numbers so special? The Fundamental Theorem of Arithmetic says that every number greater than one can be represented as the product of a unique set of prime numbers. This fact, while it may seem dry, is the foundation of much of our modern life.

For the past thirty years, much of our digital security has been built on this foundation.

---

# Greatest common denominator

The GCD of a pair of numbers is the largest number that divides both numbers. So the GCD of 30 and 24 is 6.

How can we figure this out? If we look at the prime factorization of both numbers, we can see that their common factors are a single two and a three.

$$
30 = 2 * 3 * 5
\\
24 = 2 * 2 * 2 * 3 = 2^3 * 3
$$

---

# Greatest common denominator

Two numbers are said to be _relatively prime_ or _coprime_ if their GCD is 1. Another way of saying this is that the largest number that divides both the given numbers is 1. For example, neither 10 nor 21 is prime, but they are coprime.

$$
10 = 2 * 5
\\
21 = 3 * 7
$$

---

# So what?

Imagine you multiply two very large prime numbers - each hundreds of digits long. If I am trying to factorize this number, I am going to have to check every prime number between 1 and the smaller prime find either one by brute force since nothing but 1, the number itself, and these two primes can divide the number.

This is called the **discrete log problem** and is the basis of much of our modern cryptosystems.

---

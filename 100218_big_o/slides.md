class: center, middle

# Big O

---

# What Is This Big O Thing I Keep Hearing About?

Big O is a way to measure how fast a function will run or how much memory it will use.

---

# What Is This Big O Thing I Keep Hearing About?

Big O measures how the space used or length of time will change as the input “grows”.

This can refer to either the **time complexity** or **space complexity** of a particular function.

---

# What Is This Big O Thing I Keep Hearing About?

When we talk about Big O, it tends to be very abstract - we mostly want to know roughly the space used or the time taken as the function inputs grow towards infinity.

---

# How Big Do You Mean?

What we define as the inputs growing depends entirely on the function - if you have a function that takes in arrays and concatenates them, it doesn't matter as much in terms of speed how long any particular array is, just how many total there are. If you are iterating over an array, however, the length of the array will mean running the iteration one more time for each additional element.

---

# What Is Big O?

**Big O** is specifically the **worst-case** scenario in terms of time or space.

**Big Θ** (Big Theta) is the **average** scenario.

**Big Ω** (Big Omega) is the **best-case** scenario.

---

# How Do We Measure Big O?

When we want to measure, these are rough approximations. Does the function take up the same amount of space no matter the input or do you need to hold a changed value? Does every step halve the number of things you have yet to look at? These more abstract things can help you identify Big O in the wild.

---

# Highlights

## O(1) - Constant Time (or Space)

Think something that will always take the same amount of time. This is looking up a value using a key in hashes, accessing an array at a particular index, assigning a variable to a set number or boolean.

## O(n) - Linear Time

These are things where you have to iterate or look at each element of an array or string or whatever it is. Think of mapping an array - you have to look at each element and you are returning a new array of the same length.

---

# Highlights

## O(n^2) - Quadratic Time or
## O(n^c) - Polynomial Time

Think nested loops. If you have an array of length n and you are looping over it inside of another loop, for each element in the array, you are looking at each element again. So inside of a step happens n times, you are doing something n times.

---

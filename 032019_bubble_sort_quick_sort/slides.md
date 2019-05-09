# Sorting Algorithms
## Bubble Sort & Quick Sort

---

## What is a sorting algorithm?
In the most basic terms, a sorting algorithm is a process for putting things in a certain order. The output of running a collection through a sorting algorithm should:
  1. Return a collection in a _non-decreasing order_ (or non-increasing order). This means that each element is no smaller than the previous value (no bigger for non-increasing).
  2. Return a _permutation_ of the original collection; there is a one-to-one mapping from the original collection to the output collection.


## Comparing Functions

Your input will include both the collection and some _comparing_ function. Are you sorting alphabetically? Numerically? Are you sorting by a particular value in a hash or object? These functions take in two values and determine whether they need to be switched or not. See [here](https://ruby-doc.org/core-2.2.0/Array.html#method-i-sort) for Ruby's implementation. Given `a` and `b`:

 -  if the function returns `-1`, `a` is less than `b` and `a` should come first in the result - no swapping needed.

 - if the function returns `1`, `a` is greater than `b` and `b` should come first in the result - swapping is needed.

 - if the function returns `0`, `a` is equivalent to `b` and they can be returned in either order - no swapping needed, but nothing bas about swapping either.

We are not going to spend a lot of time on how to write different types of comparison, we are going to focus on writing the sorting algorithm.


## Bubble Sort

A bubble sort works by trying to find the smallest (or largest) value first, then the next smallest, etc. It does this by running through the collection and each time it compares values, it keeps the smaller one. At the end of the array, this finds the smallest result. Now that you have found the smallest value, you look at the unsorted collection and repeat the process to find the next smallest value.
Despite the name, the start of [this video] (https://www.youtube.com/watch?v=aXXWXz5rF64) provides a nice visual explanation.

There are a lot of nice sorting videos out there, it is worth a look at them!

 - https://www.youtube.com/watch?v=WaNLJf8xzC4
 - https://www.youtube.com/watch?v=lyZQPjUT5B4 (this one has folk dancing!)

## Quick Sort

Quick sort works a bit differently than a bubble sort, but with some similarities. In quick sort, you start by picking a random element - this can be the first, or the last, or anywhere in the middle. This is your pivot. You then compare this pivot to each other ball, moving the smaller values "left" (to the smaller end) and the larger values "right". This pivot is now in its final spot.

Why? Even if the the smaller values are not in the right order, everything that is smaller is now to the "left". Similarly, everything that bigger is to the "right".

Repeat this process to the left and to the right to sort those until you have one or two values, which can be immediately sorted.



## Time Complexity

Bubble Sort has one of the worst time complexities out there. On average and in the worst-case scenario, the time is on the order of `n^2`. In general terms, each of the elements needs to be compared to each other element.

Unlike with bubble sort, though, quick sort does more than find the position of one value. In the comparisons, it has partitioned the collection into values smaller than the pivot, the pivot itself, and values larger than the pivot. In terms of time complexity, having two arrays to sort will be faster than combining those arrays and sorting the result, since each value is now making roughly half as many comparisons, not one fewer.

As a result, the average time of quick sort is `n log(n)`. However, if you are unlucky in choosing pivots and happen to choose the pivots so they are repeatedly close to the end, the partition does less to make smaller collections, so the worst-case is on the order of `n^2` as well.


## Problems

For the sake of these problems, assume you have a function `compare(a, b)` that works like the comparison functions described.

Relationship | Return
-------------|-------
a < b        | -1
a > b        | 1
a = b        | 0



### Bubble Sort

Your function should take in an array and return the non-decreasing array. Use `compare` to determine when values need to be swapped.

### Quick Sort

Same directions as bubble sort with the added advice that it might be useful to write a helper function that does the work of picking the pivot and swapping values accordingly.

class: center, middle

# Recursion

---

# What is recursion?

> In mathematics and computer science, a class of objects or methods exhibit recursive behavior when they can be defined by two properties:
> 1. A simple base case (or cases)—a terminating scenario that does not use recursion to produce an answer
> 2. A set of rules that reduce all other cases toward the base case

Thanks, [Wikipedia](https://en.wikipedia.org/wiki/Recursion).

---

# What?

Imagine you are trying to solve a problem and you realize that having the solution for a "smaller" piece of the problem would help!

In code, we can do this by calling a function inside of its definition.

A recursive function needs at least two cases - one where the function calls itself and one where it does not. A case where the function does not call itself is a _base case_. This is where the function stops calling itself so there won't be an infinite loop. The other type of case, the _recursive case_, is one where the function calls itself in a way that it will eventually lead to the base case. This usually means calling the function with a smaller number or a shorter array - something that, with enough calls, will reach the condition for the base case.

---

# Fibonacci

The Fibonacci sequence where every number is the sum of the previous two, starting with 0 and 1. In order to get the nth value, we need the n-1 and n-2 value.
Those words should 
---

# Fibonacci continued

```ruby
def fib(n)
  if n <= 0
    0
  elsif n == 1
    1
  else
    fib(n - 1) + fib (n - 2)
  end
end
```

---

# Fibonacci continued
![Fibonacci tree](./fib-tree.jpeg)
[Source](https://cdn-images-1.medium.com/max/925/1*svQ784qk1hvBE3iz7VGGgQ.jpeg)


---

# Binary Search Tree

Summing up a binary tree is another example. If we wanted to sum up the tree below, we could think of this from the root as adding the sum of all elements to the left and all of the elements to the right to the value of the root itself.

```
       5
    /     \
   7       9
    \     / \
     8   1   4
    / \   \
   3   4   9
```

---

# Recursion and Big O

In the real world, recursion is often frowned upon for the time it takes or how easily it can lead to a stack overflow. There are some types of search that use it or you may see it in some games to create a game loop.  Just remember that you need to have some idea of how the function is going to be terminated with a base case.

---

class: center, middle
# Question Time!

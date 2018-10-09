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

Imagine you are thinking about a function and you see how you can do a piece and then could use the function on a "smaller" piece - this is when you can think about using recursion.

---

# Fibonacci

The classic example is the Fibonacci sequence where every number is the sum of the previous two. So in order to get the nth value, we need the n-1 and n-2 value. Unless n-1 or n-2 are our base cases of 0 and 1, we can use the function we are writing to generate those values!

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

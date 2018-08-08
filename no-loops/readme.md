# Avoiding loops using recursion

In functional programming, we avoid mutable state, and therefore avoid iterative loops using `for` or `while`.
Instead, we use recursion to break down the problem into smaller ones.

A recursive function has two parts:
- A base case: condition(s) under which the function returns an output without making a recursive call  
- A recursive case: condition(s) under which the function calls itself to return the output

## Exercises

- Iteration vs. recursion (`iterationVsRecursion.js`)
  - [ ] Implement both iterative and recursive versions of functions to compute the factorial of a given number and the Nth number in the Fibonacci sequence
  - [ ] Compare your implementations with those of your partner/group
  - [ ] Discuss with your partner/group: Which version did you find easier to write/read? Why?

- Filter, Map, Reduce (`filterMapReduce.js`)
  - [ ] Run the tests in `filterMapReduce.test.js` with the command `node filterMapReduce.test.js` - tests should be failing
  - [ ] Work through the `TODO`s in `filterMapReduce.js` to write recursive implementations of all three functions
    - To move away from the object-oriented method-calling mindset to a functional mindset, use the helper functions `head`, `tail`, and `count` defined at the top of the file
    - [ ] Run the tests again - most should now be passing
  - [ ] Work through the `TODO`s in `filterMapReduce.test.js` to write applications of these functions that get the remaining tests to pass
  - [ ] Compare your implementations with those of your partner/group and discuss

- [optional] Tail Recursion
  - A tail-recursive function makes its recursive call in "tail position", i.e. as the very last operation in the function. In other words, the calling function does no additional work after the recursive function call is evaluated.
  - [ ] Return to your iterative and recursive implementations in `iterationVsRecursion.js`, and try running both versions with higher and higher input numbers. When does performance become an issue for the recursive implementations?
  - [ ] Implement tail-recursive versions of both functions. Try running the function with Node's tail call optimization enabled, which is available in Node 6 under the "harmony" flag:
    ```
    $ nvm use 6
    $ node --harmony iterationVsRecursion.js
    ```
    Can you get the function to successfully run with inputs that the non-tail-recursive version couldn't handle?
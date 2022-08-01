# Big-O Notation
## So, What is Big O?

- Big O notation is the language we use for talking about how long an algorithm takes to run *(time complexity)* or how much memory is used by an algorithm *(space complexity).* 

- Defined as: *given a function F(n), the T(n) is a Big O of function F(n)*, and we define this as follows: <br>
<p style="text-align:center">
            T(n) =O(F(n))
</p>

- Big O notation can express the best, worst, and average-case running time of an algorithm.

**NB**
- An important thing to note is that the running time when using big O notation does not directly equate to time as we know it (e.g. seconds, milliseconds, microseconds, etc).
- Analysis of running times does not take certain things into account, such as the processor, the language, or the run-time environment. Instead, we can think of time as the number of operations or steps it takes to complete a problem of size n. 
- In other words, big O notation is a way to track how quickly the run-time grows relative to the size of the input.

## Big O Notation Cheat Sheet

![MarineGEO circle logo](/assets/big-o-notation.jpeg "Big-O")
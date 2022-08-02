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

## Time Complexity ...
- The time complexity of the algorithm is the amount of time that an algorithm will take to execute
on a computer system to produce the output. 
- The aim of analyzing the time complexity of the
algorithm is to determine, for a given problem and more than one algorithm, which one of the
algorithms is the most efficient with respect to the time required to execute.

## Rules of the Big O
1. If you have 2 steps in your algorithm you add the steps. eg *Step 1 == O(a) && O(b)* which becomes *O(a+b)*
2. Drop contants. 
3. If you have different inputs then you have different var to represent them. 
    - Big o is an equation of how the runtime changes/scales, so it becomes *O(a***b)*
4. Drop none dominant terms. 

**Reference** ==> [Big O Notation](https://www.youtube.com/watch?v=v4cd1O4zkGw&ab_channel=HackerRank) by HackerRank
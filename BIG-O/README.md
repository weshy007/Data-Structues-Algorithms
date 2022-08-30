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

**Reference** 

==> [Big O Notation](https://www.youtube.com/watch?v=v4cd1O4zkGw&ab_channel=HackerRank) by HackerRank. :point_up_2:

==>[Big O Notation - Full Course
](https://www.youtube.com/watch?v=Mo4vesaut8g&t=199s&ab_channel=freeCodeCamp.org) by freecodecamp.org :point_down:

- You learn and understand how to apply the concepts of Big O Notation to Software Engineering. 
    - Remember, Big-O notation is a way to describe how long an algorithm takes to run or how much memory is used by an algorithm. 
## Orders of Growth in O-Notations
| Step| Growth |
| --- | --- |
| **O(1)** | Constant|
| *O(log n)* | Logarithmic|
| *O(n)* | Linear |
| *O(n log n)*| Linearithmic |
| *O($n^2$)* | Quadratic |
| *O($n^3$)*| Cubic|
| *O($2^n$)*| Exponential|
| *0(n!)* | Factorial|
|||

    
    NB
    - Showing from good to bad.

</br>
<br>

## The 0($n^2$) - Quadratic
![MarineGEO circle logo](/assets/0n2.png "Big-O")

- Iterate through the first for loop and for **each** iteration in the first loop, you iterate in the nested loop.
- Then you console the log of index of i and j

    - Lets call the square() function with 4 as a parameter.
    - The function will have an iteration of 16 times. How?
    - When we start at *i=0*, we go for *j=0*, then *j=1*, *j=2* & *j=3* respectively.
    - Same case goes for *i=1*, we go for *j=1*, then *j=2* & *j=3* respectively. And the function will run for *i=2* & *i=3* where in the end, it forms a square if you draw the indexes.
    - Hense the **O($4^2$)** which comes from **O($n^2$)**
    - Refer to the image below for clearer understanding.

![MarineGEO circle logo](/assets/On2complete.png "Big-O")

<br>
<br>

## The O($n^3$) - Cubic
![MarineGEO circle logo](/assets/On3.png "Big-O")

- Iterate through the first for loop and for **each** iteration in the first loop, you iterate in the nested loop, and for **each** iteration in the 1st nested loop, you iterate in the 2nd loop.

    - If we call the function cube() with 4 as the parameter, we get to console 3 indexes/dimensions. ie i, j and k. Lets take them as columns, rows and height.
    - When we start at *i=0*, we go for *j=0*, then go for *k=0*, *k=1*, *k=2* & *k=3* respectively.
    - We then go for *j=1* then *k=0*, *k=1*, *k=2* and *k=3*. 
        - The reason why we go back to j=1 is because we have not finished iteration in the 1st nested loop.
    - We then go for *j=2* then *k=0*, *k=1*, *k=2* and *k=3* again. This goes on till you finish all the iterations(64).
    - Since we go for n iterations of i, j and k, where we want to get the volume of the cube, we do a mulitiplication of i, j and k.
    - This will be 4x4x4 which is $4^3$. Where we get now **O($n^3$)**
    - Refer to the image below.

![MarineGEO circle logo](/assets/On3complete.png "Big-O")

<br>
<br>

## 0(log n) - Logarithms
### Meaning of Logrithms
Is the power a number has to be raised to get some other number. ***$n^n$=another number***.

- In Computer Science, unless specified otherwise, assume the number to be raised to some power is 2.
- Taking 8 as an example:
    
    $2^?$=8 which can be written as $log{_2}8$=? where 2 is the base number.

![MarineGEO circle logo](/assets/logarithms.png "Big-O")

### O(log n) - recursive
Here is our function

![MarineGEO circle logo](/assets/logn.png "Big-O")

- The functions take the number n(8), then divides it by 2 and calls itself with the result of the division. 
- Not only applicable to recusive applications.

![MarineGEO circle logo](/assets/logncomplete.png "Big-O")

### O(log n) - iterative/ non-recursive

![MarineGEO circle logo](/assets/lognnon.png "Big-O")

- The function iterates on the while loop as long as n(8) is greter than 1. For each iteration of the while loop, n is divided by 2 and reassigned to n.
- In the first iteration, our n == 4, 2nd iteration == 2 and 3rd iteration is == 1.
 
![MarineGEO circle logo](/assets/lognnoncomplete.png "Big-O")

<br>
<br>

## O(log n) What Is Binary Search?
- Also known as half-interval search, logarithmic search, or binary chop, is a search algorithm that finds the position of a target value within a sorted array. Binary search compares the target value to the middle element of the array. 
- We need to undertsand that for this to work, the array must be an ordered array. Both descending and ascending (sorted) arrays will work.
- For the coiding binary search, refer [here](https://youtu.be/Mo4vesaut8g?t=2168)


<br>
<br>


## O(n log n) Explanation
![MarineGEO circle logo](/assets/nlognex.png "Big-O")

- The function take one argument n(4).
    - We then declared a variable y(*Will be used in the for loop so that we can iterate through the original size of n*).
- The while loop iterates though n till n == 1.
- For every iteration in the top level loop, which iterates through n till its 1, n is divided by 2. The value of n is split into two.
- Process time increases linearly with the size of n.

![MarineGEO circle logo](/assets/nlognexcomplete.png "Big-O")


<br>
<br>


## O(2^n) Explanation With Fibonacci

<br>
<br>

## O(n!) Explanation

<br>
<br>

## Space Complexity & Common Mistakes

<br>
<br>


<u><b> INFORMATIVE RESOURSE </b></u>
- Check out this [link](https://www.bigocheatsheet.com/ 'Big-O cheats') for the Big-O cheatsheet.
# Sorting-and-Complexity
This is short presentation is about sorting and complexity as concepts.

## First, complexity.
The complexity of an algorithm is a measure of the amount of time and/or space required by an algorithm for inputs of a given size (n).
### Time complexity
There are a lot of variables that affect the run time of an algorithm, such as:
* The representation of abstract data types (ADTs):
    * ADTs are almost what we call, user-defined data types.
    * The representation of ADTs follows some norms, such as:
        - Non-repetitive: choosing non-repetitive and usable elements.
        - Keep it simple: It's better to have a few simple operations that can be combined in a powerful way, rather than a complex operation.
* The efficiency of a compiler: of course, there are a lot of compilers for different programming languages with different ups and downs.
* The complexity of the algorithm.
* Size of the input.
So how can we find a common ground to calculate the amount of time required for an algorithm to function if there are a lot of variables in this equation?
We can't, but what we can do is calculate the growth of the runtime of a function (And this is a really important idea), let's take the next pseudo-code where we need to calculate the number of elements in a given array:
```
    array = [1, 2, 3, 4, 5, ..., n]
    def elem_num(array):
        num = 0
        for each i in array:
            num++
        return num
```
If we consider that every instruction takes 1 second to be executed (of course it takes much less time), we will need to wait **n** seconds for the results, but as I mentioned above, we can't really calculate the time required so we calculate the growth of the runtime. For our example, if we ignored the declaration and return statement because they take a constant amount of time, we will see that the time takes to finish the process is increasing constantly as we add more inputs, for example, if there are 10 inputs, the time required is 10 units of time, or in other words ``f(n) = n``.

![alt text](https://github.com/MGS15/Sorting-and-Complexity/blob/main/imgs/constant-growth-01.png?raw=true)

### Big-O notation
The result of the function **f** is what we called the **Big-O notation**, and in our example, it is expressed like ``O(n)``, **(Big-O of n)**, and in the previous example, we can say that time complexity of our algorithm is  big-O of n, which means that the amount of time required to finish the function properly (t) is increasing in proportion to the number of inputs (n).
There are a lot of "Big-O notations" the most common ones are:
* **O(n)**: Big-O of n or ``f(n) = n`` as we mentioned above.
* **O(1)**: Big-O of 1 or ``f(n) = a`` where ``a`` is a constant, O(1) says that there is no runtime growth (or complexity growth) of a given algorithm regardless of the input, which means the amount of time required by a function is **a** if the number of inputs **n** is 1 or 10 or 1 million. In complex algorithms, big-O of 1 is usually ignored since it's a constant.

![alt text](https://github.com/MGS15/Sorting-and-Complexity/blob/main/imgs/O(1).png?raw=true)


# RECURSION
#### Self invokation of methods or functions is actually quite useful, so much that it gets it's own name as : *Recursion*

## Recursive Functions
A function definition that calls itself, then this function would be known as a **Recursive Function** 

``` Python
def A():   #Here we have defined the function
    A()     #Here we have called the same function we are defining in the function \
```

* Where a function calls itself directly from within it's body is an example of direct recursion

* Recursion can be indirect as well, if a function calls another function which calls it's caller functions from within it's body

###### Now in the next parts we will be learning how to write recursive functions and implement recursion, but  before that look at the codes below and determin their output carefully

``` Python

def func1():
    print("Hello func2!!")
    func2()
   
def func2():
    print("Yes func1")
    func1()
```
###### In case you were not able to guess, this code will print the lines given below endlessly

``` Python
"Hello func2"
"Yes func1"
"Hello func2"
"Yes func1"
.
.
.
.
```

###### But in case of python this code wouldn't go  on forever as python will report the folloing error

``` Python
RuntimeError : maximum recursion depth exceeded.....
```
## Right / Sensible recursive codes

Conditions
* Must have a *Base Case*, Base case is a case whose result or value in computed without any recursive calling
* Must have a *Recursive Case*, where the function calls itself or recursion comes into action

To understand the above point let us take a look at one example program

``` Python
'''Write a recursive function that computes the sum of numbers 1....n; get the value of last number n from the user'''

def compute():
    if num == 1 :          #BASE CASE for the function
        return 1
    else :                  #RECURSION CASE for the function
        return (num + compute(num-1))

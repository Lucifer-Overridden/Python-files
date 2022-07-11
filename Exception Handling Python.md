# Difference between Syntax error and Exceptions
*Syntax Error :* As the name suggests this error is caused by the wrong syntax in the code. It leds to the temination of the program 

*Exceptions :* Exceptions are raised when the program is syntactically correct but the code resulted in an error. This error does not stop the execution of the program, however it changes the normal flow of program

_NOTE :_ Excception is the base class for all the exceptions in the python and also has a set hierarchy

# Try and Except statement - Catching exceptions

Try and except statements are used to catch and handle exceptions in Python. **Statements that can raise exceptions are kept inside the try clause** and the **statements that handle the exception are written inside the except clause**

**Example :** Let us try to access the array element whose indek is out of bound and handle the corresponding exception

```Python
#Python program to handle simple runtime error 

a = [1,2,3]
try :
  print("Second element = %d" %(a[1]))
  
  #throws error since there are only 3 elements in array
  print("Fourth element = %d" %(a[3]))
  
except:
  print("An error occured")
```
```Python
#OUTPUT
Second element = 2
An error occurred
```

Now in the above example the statements that could have raised error are placed inside the try statement and then the exception is caught by the except statement

### Catching specific Exception

A try statement can have more than one except clause, to specify handlers for different exceptions. It should be noted that at most handler will be executed.

The general syntax for adding specific exceptions are ⏬
```Python
try:
  # statement(s)
except IndexError:
  # statement(s)
except ValueError :
  # statement(s)
```

**Example :** Catching Specific exception in Python

```Python
#program to handle multiple errors with one except statement

def fun(a):
  if a<4 :
    #throws ZeroDivisionError for a = 3
    b = a/ (a - 3)
    
  #thrown NameError if a >= 4
  print("Value of b = ", b)
  
try:
  fun(3)
  fun(5)
  
#note that braces() are necessary here for multiple exceptions

except ZeroDivisionError :
  print(" ZeroDivisionError Occurred and Handled")

except NameError :
  print("NameError Occurred and Handled")
```
```Python
#Output 
ZeroDivisionError Occurred and Handled
```
If you comment on line fun(3),  the output will be

```Python
NameError Occurred and Handled
```
The output above is so because as soon as python tries to access the value of b,NameError occurs

### Try with Else Clause

In python, you can also use the else clause on the try except block which must be present after all the except clauses. The code enters the else block only if the try clause does not raise an exception

**Example :** Try with else clause

```Python
#Program to depict else clause with try-except

#Function which returns a/b

def AbyB(a,b):
  try : 
    c = ((a+b)/(a-b))
  except ZeroDivisionError :
    print("a/b result in 0")
  else :
    print(c)

#Driver program to test above function

AbyB (2.0, 3.0)
AbyB (3.0, 3.0)
```

```Python
#Output
-5.0
a/b result in 0
```

### Finally keyword in Python

python provides a keyword **finally**, which is always executed after the try and except blocks. The final block always executes after the normal termination of the try block or when try block terminates due to some exception

#### SYNTAX
```Python
try: 
  # Some code
  
except:
   #Optional block
   # Handling of exception (if required)
   
else :
  # execute if no exception
  
finally :
  # Some code .....(always executed)
```
#### EXAMPLE
```Python
#Python program to demonstrate finally

#No exception Exception raised in try block
try:
  k = 5//0 #raises divide by 0 exception
  print(k)
  
#Handles zerodivision exception
except ZeroDivisionError:
  print("Can't divide by Zero")
  
finally : 
  # this block is always executed
  #regardless of exception generation
  print('This is always executed')
```
#### OUTPUT
```Python
Can't divide by 0
This is always executed
```
### Raising Exception

The raise statement allows the programmer to force a specific exception to occur. The sole argument in raise indicates the exception to be raised. This must be either an exception instance or an exception class (a class that derives from exceptions)

```Python
#Program to depict raising an exception

try:
  raise NameError("Hi There") #Raise Error
except NameError:
  print("An exception")
  raise #To determine whether the exception was raised or not
```
The output of the above code will simply line printed as "An exception" but a runtime error will also occur in the last sue to the raise statement in the last line.


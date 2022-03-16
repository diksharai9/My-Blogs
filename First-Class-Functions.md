> A programming language is said to have First-class functions when functions in that language are treated like any other variable.

Functions are also called first-class objects, this means that functions should have all the properties which object haves.

**The properties a first-class function have are:**


1. 
A function can be assigned to a variable. Following is the code explaining that.

```
#Defining a function square
def square(num):
    return num*num
#assinging function to a variable
x=square #now x is same as square and we can treat x as a function
print (square)
print(x)
#both print statements will have same results
#calling the functions
print(square(2)) # output-4
print(f(2))#output-4


``` 



2. 
A function can be passed as an argument to other functions.

```
#defining a function
def multiple_of_two(num):
    return 2*num


#defining another function
def my_func(func, a_list_of_integers):

    result=[ ] #creating an empty list which will be used later in function
    for i in a_list_of_integers:

        result.append(func(i))
    return result # each element of list is passed as an argument to "func" function
#and the output of that function is then added to "result"


multiplication = my_func(multiple_of_two, [1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

print(multiplication) #output-[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

``` 

3. A function can be returned from other functions.


```
def greetings(name):
    def greet():
        print("Hi "+msg)
        return
    return greet #returning greet function from greetings function


my_func = greetings("xyz")
my_func() #calling the function


``` 


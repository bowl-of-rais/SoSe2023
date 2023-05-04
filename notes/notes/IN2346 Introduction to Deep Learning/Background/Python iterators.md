
This post is meant for those who are not familiar with the **iterator / generator** functionalities of python, and wish to arrive more prepared to the exercise 03's release.

  
## What is an iterator / generator

An **iterator** is a python object that can be iterated upon, meaning that you can traverse through all the values. A python list (e, g. [1, 2, 3]) could be looked at as an iterator, because we can iterate over it and access the elements inside it. 

A **generator** is a function that we could be used as an iterator. Also, a python class could be a generator, by implementing its corresponding function __iter__().

  
## How to implement an iterator / generator?

```
def regular_foo():  
    indx = 0  
    return_list = []  
    while indx < 10:  
        return_list.append(indx)  
        indx += 1  
      
    return return_list

def myIterartor():  
    indx = 0  
    while indx < 10:  
        yield indx  
        indx += 1  

if __name__ == '__main__': 
      
    # for loop 1  
    for x in regular_foo():  
        print(x)

    # for loop 2 
    for x in myIterartor():  
        print(x) 
```
 
  
##### Distinction between the **return** and the **yield** statements
- regular_foo(): runs the code line-by-line from indx = 0 to return return_list, and finish the **scope** of the function
	- next time regular_foo() is called, the same process happens
	- loop 1:  
		-  run the function and load the list of numbers between 0 and 9 to the **RAM**.  
		-  return that list to the **outer scope** of the main function.  
		-  run the for-loop on the returned list, and print all the numbers within, 1-by-1.

- for my_iterartor(), on the other hand, the process is slightly different: 
-  for loop 2 runs the first iteration.  
-  Enter the function for the first time, and run line-by-line until the **yield** statement.  
- The function's state, including the pointer to the executed line, is saved to the memory.  
-  Return the value of indx (0) to the **outer scope**. Now x == 0.  
- Print the value of x  →  0.  
- Enter the function again, in the next iteration.  
- **The most crucial notion** - we enter my_iterartor() again, but now, in comparison to the regular call of a function, the function state is **relaoded**, and we now stand on the line indx += 1.   
- We start the second iteration of the while loop, and **yield** the value 1.  
- This loop continues, until the while loop within my_iterator() finishes, and the function **returns** and finishes, i.e. it doesn't generate anything else.

What's the main difference here? The regular_foo() loads all the numbers to the RAM, returns it, and then we iterate over the array and print its elements. The iterator, on the other hand, loads each one of the elements at a time, not overloading the RAM. 

Note, that this characteristic of the iterator is important to deep learning, because real-world data could be **super heavy,** for example when we want to train models on 3D data. If we try to load all the dataset to the RAM, with most common setups, the program will just crush. For those who see themselves going into this amazing world, the idea of how to construct a Dataloader is a **corner-stone**.

Will be relevant only after exercise 03 is out:

  
`class Dataset():`  
      
    `def __iter__(self):`  
        `indx = 0`  
        `while indx < 10:`  
            `yield indx`  
            `indx += 1`   
              
          
`if __name__ == '__main__':`  
      
    `dataset = Dataset()`  
    `for x in dataset:`  
        `print(x)`  
  
For a class object to become an iterator / generator, we need to implement its corresponding __iter__() function, so it could be iterated over and generate data. 

**Common mistakes:**

- Use the yield statement within a **nested function:**  
  
`class Dataset():`  
      
    `def __iter__(self):`  
          
        `def nested_function(x)`  
            `yield x`  
              
        `indx = 0`  
        `numbers = []`  
        `while indx < 10:`  
            `numbers.append(nested_function(indx))`  
            `indx += 1`   
              
        `return iter(numbers)`

`if __name__ == '__main__':`  
      
    `dataset = Dataset()`  
    `for x in dataset:`  
        `print(x)`  
  
We've encountered that many of you have implemented their generators in that fashion, sometimes without a return statement. Here, the **yield** statement returns a value from within the scope of nested_function() back to the scope of __iter__(), but not to the main, where the dataset is iterated over. That means that your iterator operates exactly like a regular function, and when it is called in for x in dataset it will run all the lines of code and load everything to the RAM, before x even gets anything.

- For those of you who don't use any **return** statemnet, you return the default value of a python fucntion: None. That's why you guys get errors related to a Nonetype object.

For any questions, let's start a discussion here.
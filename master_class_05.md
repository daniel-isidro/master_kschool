# MASTER CLASS 5: Python Fundamentals

## Custom functions 

Custom functions can be imported as below, where dani library is a .py file

	import dani as dn 

## File operations in python

# curl

Download files from the Internet

## f.read(int)

Every time it gives a different output, as f.read(int) moves the pointer and gives the last "int" characters

## f.seek(0)

Used to move the pointer to the specified position (zero in this case)

## f.tell()

Gives the position of the pointer

## f.close()

Always close files after stopping working with them

## with open () as f

Reommended to use "with": Opening files and closing them when exiting (without the need of f.open() and f.close() )

	with open("Finn.txt") as f:
    		print(f.readlines())

## fw

Delete content and write

	fw=open('newfile.txt', mode='w')

## fa

Append content

	fa=open('newfile.txt', mode='a')


### lists

## extend

Like append but for multiple elements


## reversed(list)

Gives the reversed list but does not modify it

## objects in python

In python everything is an object, functions as well, so functions can be an argument of another function

	def apply_to_list(some_list, some_function):
    		results=[]
    		for value in some_list:
        		results.append(some_function(value))
    		return results

	ints=[1, 2, 3, 4]
	apply_to_list(ints, lambda x:x*2)

Out:
	[2, 4, 6, 8]

Functions can also be part of lists

	def add_one(value):
	    return value+1
	def double_value(value):
	    return 2*value
	def add_three(value):
	    return value+3

	math_ops =[add_one, double_value, add_three]

## map

It iterates over each element of a series

	k=[1,2,3]

	list(map(lambda i:i+1,k))
	
Out:
	[2, 3, 4]


## List comprehensions

	a=[1,2,3,4, 5, 6]

	result2=[val**2 for val in a if val%2]

Out:
	[1, 9, 25]

First the values of the resulting list

	val**2

Then iterates an iterable object

	for val in a

Takes only the values of the initial list that meet the condition

	if val%2	

Other example **(completeley unreadable)**:

	result3=[val**2 if val%2 else 1 for val in a ] #--> changes the place for if condition
	result3

Out:
	[1, 1, 9, 1, 25, 1] 

## zip

“pairs” up the elements of a number of lists, tuples, or other sequences, to create a sequence of tuples

Useful to match two pairs of lists, for example

## enumerate()

Useful for showing index and values

	for counter, val in enumerate(range(10, 20)):
        	print(counter, val)

Also useful especially when constructing a dict

	mydict={}
	for i,pet in enumerate(pets):
		mydict[i]=pet

## Dictionaries

TIP: Use dictionaries as output in functions, as they are self-describing, because those outputs do not depend on position

	import numpy as np
	myarray=np.array([0,1,2,3,4,5,6,7,8,9])
	def describe(myarray):
    		return {"min":myarray.min(),"max":myarray.max(),"mean":myarray.mean()}

	describe(myarray)

Out:
	{'min': 0, 'max': 9, 'mean': 4.5}

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

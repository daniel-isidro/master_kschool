# MASTER CLASS 4: Python Fundamentals

## Jupyter notebooks

Select .py notebook and click on shutdown to kill execution

When in a cell, in blue mode, press "h" for keyboard commands

Execute cell and create one cell below

	ALT + ENTER

With ipython you can see a clear order of the executed cells. In Jupyter notebooks the order is on the left side of the cells and can be confusing
 
When on a command, with SHIFT + TAB (TAB several times), it explains the use of the command

With tuples, if there are lists inside, you can change the values inside the list

You can also create a tuple without parenthesis

	c=(3,4)
	c=3,4

Check if an object is an instance of a particular type

	a={1,2}

	isinstance(a,(int, set)) -> True

	isinstance(a,(int)) -> False

Look all the attributes of an objet

	dir(c)

There are more attributes to an object, hidden, that  not visible with tab

	c='hahaha'
	c.__hash__()
	4870081446263348069

# Referencing an object

	a=6
	b=a
	id(a),id(b)
	(139850300655560,139850300655560)

	c=a.copy()
	c.append(5)
	id(c)
	139850300057928

	a=6
	b=a
	a=7

a points to 7, but b continues to point to 6

## Functions

Print function explanation

	def function(a,b):
		'''This
		is
		the explanation of the function'''
		print(a,b)

	help(function)

Use 'global' in functions to state a global variable (variables are local by default)

## Strings

Strings are immutable, so when doing 

	a='hello'
	id(a)
	138986876786

	a=a+'goodbye'
	
	print(a)
	hellogoodbye

	id(a)
	138977687678

Use .find() instead of .index() bc .find() returns "-1" when the search term is not found, while .index() returns an error if not found



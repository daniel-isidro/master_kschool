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

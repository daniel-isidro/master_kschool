# Introduction to Data Analysis with Python

TIP: Use jupyter notebooks without browser to get used to connect to server clusters remotely by SSH

	$ jupyter notebook --no-browser

TIP: Don't import pandas or numpy without "as pd" or "as np" as it makes functions obscure and more difficult to find to what library they belong

## plt.plot()

Works with lists or numpy arrays

TIP: There are libraries on the Internet that beautify the plt.plot() charts. After tweaking your plots you can save them and later import those settings in your notebooks

TIP: Grids are not recommended to be used when showing plots to the public

## numpy

np.zeros and np.eye are the most used matrices

TIP: don't use np.empty() as it shows random quantities close to 0 but not necessarily 0

## %%timeit

Gives the average time of several runs of the execution of one given cell.

	%%timeit
	[math.sqrt(n) for n in plist]

**WARNING: Always do several runs of something, and never give too many decimals as there always is an error, it doesn't make sense**


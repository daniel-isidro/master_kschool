# Functional Programming - Spark
## Dani Mateos
### Data Scientist, Freelance

### Apache Hadoop (MapReduce)

* Revolutionary: using commodity hardware for big data tasks

* Hadoop: Systems have to endure hard disk failures constantly. Hadoop allows data to be dispersed on many nodes

* **Functional programming** has 4 key elements: ```map```, ```reduce```, ```filter```, ```lambda```

**Mapping**

```map``` is a Higher Order Function (HOF) that takes a function f and a sequence and returns a new sequence formed by applying f to each element in the original sequence.

When using ```map``` to repace lambda functions, regular functions like ```square()``` **must be referred withouth arguments** (without parenthesis):
```python
input_list = [1, 2, 3]

list(map(square, input_list))
```

```map``` is the subsitute of some type of for loops

**Filtering**

```filter``` is the subsitute of other type of ```for``` loops, the transformation is done or not depending of a condition. ```fiter```returns a boolean

**Reducing**

```reduce``` is also applied to a list of elements.  It does not produce a collection but just one element. It makes transformations to the first pair of elements, and puts the transformation into the next element until the end of the list

### 2 factors to prioritize in big data

1) Parallelize as much as possible, distributing the data

2) Reducing computing power

Functions must be commutative and associative to be used in distributed computing

```for``` loops are to be avoided in big data, as they are sequential

### Side note
In Python 2, map and filter returned lists. In Python 3, they return generators, which are lazy collections. They are somewhat similar to files in that **they can be depleted of elements after iterating through them**.

```python
this_map = map(lambda x: (x**2, x, 1), numbers)
list(this_map)
```

Output:
```python
[(144, 12, 1),
 (289, 17, 1),
 (361, 19, 1),
 (324, 18, 1),
 (529, 23, 1),
 (576, 24, 1)]
```

```
list(this_map)
```

Output:
```
[]
```

### Spark

Spark is programmed in Scala. pyspark adds a python layer to the native language. Most of the features of Spark that exist in Scala can be used in python, but not all. Also error messages are based in Scala, so it makes it a mess

To check if Spark is correctly installed, execute ```spark```

**Actions and Transformations**

Transformations produce an RDD. Actions are implemented as methods on an RDD, and return an object of a type that is not an RDD. 

**Persistence**

Spark allows chaching to speed up processes and recover lost data

**rdd**

```groupByKey()``` can only be applied to sets of tuples

**DataFrames in spark**

A DataFrame of 1 column is not the same as the column of the DataFrame

```df.select['id']``` does not equal ```df['id']```

DataFrames in spark are immutable. We need to create new DataFrames with the appropriate columns

**User Defined Functions**

with ```functions.udf``` which returns another function, we can use any function and apply it to the DataFrame columns

**cache**

Useful for freezing the result of an action in a DataFrame when getting random results, for example

```python
land = functions.udf(lambda : random.choice(['gondor', 'rohan']))
df4 = df3.withColumn('land', land())
df4.cache().show()
```

**```select```and ```withColumn```**

```df.witchColumn``` allows to add one column, ```df.select``` allow to add/remove several columns

**pandas and spark DataFrames**

When writing spark DataFrames into CSVs, thes CSV files are in relaity containers of as many CSV files as partitions were in the cluster

it is recommended using spark DataFrames instead of rdd, as their use is similar to pandas

**Packaging python code into .py file scripts**

Useful for not running main function code when imorting python scripts into other projects:

```python
if __name__=='__main__':
```

Useful for running .py pyhton scripts with arguments:

```python
file = sys.argv[1]
out = sys.argv[2]
```

# Functional Programming - Spark
## Dani Mateos, Data Scientist, Freelance
### Apache Hadoop (MapReduce)

* Revolutionary: using commodity hardware for big data tasks

* Hadoop: Systems have to endure hard disk failures constantly. Hadoop allows data to be dispersed on many nodes

* **Functional programming** has 4 key elements: map, reduce, filter, lambdas

**Mapping**

```map``` is a Higher Order Function (HOF) that takes a function f and a sequence and returns a new sequence formed by applying f to each element in the original sequence.

When using ```map``` to repace lambda functions, regular functions like ```square()``` **must be referred withouth arguments** (without parenthesis):
```
input_list = [1, 2, 3]

list(map(square, input_list))
```

```map``` is the subsitute of some type of for loops

**Filtering**

```filter``` is the subsitute of other type of for loops, the transformation is done or not depending of a condition

**Reducing**

```reduce``` is also applied to a list of elements.  It does not produce a collection but just one element. It makes transformations to the first pair of elements, and puts the transformation into the next element until the end of the list

2 factors to prioritize in big data: parallelize as much as possible and reduce computing power

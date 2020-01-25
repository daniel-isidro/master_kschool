# Master class 13

## Introducción a R

## Fátima Sánchez Cabo, CNIC

R is an interpreted language, no need to be compiled

**Strong points**
* Good visualizations with almost no effort
* Interactive, output obtained as you code

**First steps in R**

Always setup first the current working directory:

R Studio > Menu Bar > Session > Set Working Directory > Choose Directory

Instead of using the onsole, write everything on a R script (+ button in the top-left area, or File > New R Script)

To execute commands in the R script:

1. Copy/paste it on the console
2. Go to the end of the code and press CTRL + ENTER
3. Click 'Run'

**Environment** is where the created objects appear

**History** is the list of all commands executed

**UP arrow** in the console for going back in the command history

**Assign values to objects:** precio<-871*1.21

**Objects** can be numbers (double(=float) or integer), characters, logic (TRUE/FALSE), or factors(=categories)

(Objects can also be assigned values in the way v3="Hola", but it's not preferred)

**ESC key** for interrupting the output in the console

**Force using integer numbers**

dado<-c(1L,2L,3L)

**Functions**

function(x)
v.g. length(x)
Functions are also objects and they can be numeric, character or logic types

**Using R script in the CLI**

Rscript xxx.R -parameters

**Using comments in the R script** using '#'

**Object names** are case sensitive

**Precission of R** is 16 digits

**Vectors in R** always in the form c(x,y,z)

**Matrices in R** 

All elements in a matrix need to belong to the same type. 
If they are not, R transform them: numeric into character and logical into numeric

**Data.frames** are the most important objects in R, they are used to combine values of different types. Data.frames have been superseded by **tibble** objects

**Factors** are object types used for categories

v.g. gender<-factor("M","F","F","M")

**Transform character vectors into factor vectors**

v.g. gender<-as.factor(c("M","F","F","M"))

Factors are stored in memory as numbers, in alphabetical order

v.g. as.numeric(gender)
[1] 2 1 1 2

**Data.frames or lists**

When vectors are different in size, we must use lists. Data.frames vectors have to be same size

Lists can have different size and type variables. Data.frames cannot

**Help in R**

? function

v.g. ? rep






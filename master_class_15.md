# Master class 15
## Manejo y limpieza de datos
### Fátima Sánchez-Cabo

**tidyverse**

piping is uded with the symbol `%>%`

**dplyr**

Most simple functions

`filter(obj,) -> rows` filter neeeds a vector of logics, needs a vector of logic with size equal to the number of rows of the data.frame()

`select -> columns`

`mutate -> add/change colums`

v.g. `babies %>% filter( , )`

`summarize(function1, function2, ...)` applies one or several functions to the data.frame or tibble; the output of summarize is one single value per used function

`add_row( )`

`arrange( )`

`top_n( )`

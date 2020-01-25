# Master Class 14

## Importing and collecting data

## Fátima Sánchez Cabo, CNIC

**Loops and if-else conditions**

if(TRUE/FALSE){}

Always write }else{ with no spaces inbetween 

**Easily adding comments**

Menu Bar > Code > Comment/Uncomment code lines

**Forcing taking functions from one specifical package**

base::sample (takes sample function from base package)

**Executing an R script from the top in the console**

source("script_name.r")

**Install packages from CRAN**

Downloads the packed to the computer

install.packages(c( , , , ,))

**Install packages from GitHub**

install_github(c( , , , ,))

**Install packages from local repository**

Menu Bar > Tools > Install Packages > Install from Package Archive File (.tar.gz)

**Tidyverse package**

Essential R package for Data Science

Includes other several packages: ggplot2, dplyr, readr, tidyr, tibble

**Adding columns to Data.Frames**

df <- mutate(object, column_name)

v.g. dat <- mutate(dat, region =  as.factor(region))

Mutate is a dplyr function; no need to add the name of the Data.Frame to the dplyr functions

**Piping in Data.Frames**

dat %>% mutate(pop2=population/10^5)

**Reading files and getting Data.Frames**

CSV: read.delim, read.csv
TXT: read.delim
XLSX: read.xlsx

**Reading files and getting tibbles**

CSV: read_delim, read_csv
TXT: read_delim
XLSX: read_xlsx

**Not all packages use tibbles** 

tibbles can be converted to Data.Frames




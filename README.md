# Assignment-2.3
Answers for Assignment 2.3
1. How to Import SAS XPORT Files into R With The foreign package
Answer: install the sas7bdat package. Load it, and then invoke the read.sas7bdat() function contained within the package and you are good to go!

Note that you can also use the foreign library to load in SAS data in R. In such cases, you’ll start from a SAS Permanent Dataset or a SAS XPORT Format Library with the read.ssd()and read.xport() functions, respectively.

2. How To Import SAS Files into R With The haven Package?
Answer:
Haven is part of the tidyverse.

# The easiest way to get haven is to install the whole tidyverse:
install.packages("tidyverse")

# Alternatively, install just haven:
install.packages("haven")
library(haven)

# SAS
read_sas("mtcars.sas7bdat")
write_sas(mtcars, "mtcars.sas7bdat")

3. How to read Weka Attribute-Relation File Format (ARFF) files in R?
Answer:
Read Data from ARFF Files
Description
Reads data from Weka Attribute-Relation File Format (ARFF) files.
Usage
read.arff(file)
Arguments
file	a character string with the name of the ARFF file to read from, or a connection which will be opened if necessary, and if so closed at the end of the function call.
Value
A data frame containing the data from the ARFF file.

Example:
read.arff(system.file("arff", "contact-lenses.arff",
                      package = "RWeka"))

4. How to read a heavy csv/tsv file using readr package?
Answer:
# Installing
install.packages("readr")
# Loading
library("readr")
Functions for reading delimited files: txt|csv
The function read_delim()[in readr package] is a general function to import a data table into R. Depending on the format of your file, you can also use:

read_csv(): to read a comma (“,”) separated values
read_csv2(): to read a semicolon (“;”) separated values
read_tsv(): to read a tab separated (“\t”) values
The simplified format of these functions are, as follow:
# General function
read_delim(file, delim, col_names = TRUE)
# Read comma (",") separated values
read_csv(file, col_names = TRUE)
# Read semicolon (";") separated values
# (this is common in European countries)
read_csv2(file, col_names = TRUE)
	    
# Read tab separated values
read_tsv(file, col_names = TRUE)

# Read a csv file, named "mtcars.csv" 
my_data <- read_csv("mtcars.csv")

# Read a txt file 
my_data <- read_tsv(file.choose()) 

# MASTER CLASS 3: Data Science at the Command Line

## sort, unique
	
What is the aircraft with the highest number of engines?

	sort -t "^" -k 7,7nr optd_aircraft.csv | head

How many manufacturers are there?

	sort -t "^" -k 2,2 -u optd_aircraft.csv | wc
	Output: 77 (76 manufaturers if we don't count the header)

## cut

Change delimiter in output file from "^" to ","

	cut -d "^" -f 1-3,5 --output-delimiter "," optd_aircraft.csv |head

Command "cut" only works with 1-character delimiters

Delimiter TAB:

	"\t"

## paste

Convert column into line

	paste -s numbers            
	Output: 1	2	3	4	5	6	7	8	9	10

Get file and convert into three columns

	cat numbers | paste - - -
	
	Output:
	1	2	3
	4	5	6
	7	8	9
	10		

Get file and convert into two columns

	cat numbers | paste - -  

	1	2
	3	4
	5	6
	7	8
	9	10

Number CSV file with first column of index

	paste numbers optd_aircraft.csv | head

	1	iata_code^manufacturer^model^iata_group^iata_category^icao_code^nb_engines^aircraft_type
	2	100^Fokker^100^100^2J^F100^2^J
	3	141^BAe^146-100^146^4J^B461^4^J
	4	142^BAe^BAE Systems 146-200 Passenger^146^4J^B462^4^J
	5	143^BAe^146-300^146^4J^B463^4^J
	6	146^BAe^146^^^^^
	7	14F^BAe^146 Freighter (-100/200/300QT & QC)^^^^^
	8	14X^BAe^146 Freighter (-100QT & QC)^14F^4J^B461^4^J
	9	14Y^BAe^146 Freighter (-200QT & QC)^14F^4J^B462^4^J
	10	14Z^BAe^146 Freighter (-300QT & QC)^14F^4J^B463^4^J	

Append two files

	paste optd_aircraft.csv optd_aircraft.csv | head

	iata_code^manufacturer^model^iata_group^iata_category^icao_code^nb_engines^aircraft_typiata_code^manufacturer^model^iata_group^iata_category^icao_code^nb_engines^aircraft_type
	100^Fokker^100^100^2J^F100^2^J	100^Fokker^100^100^2J^F100^2^J
	141^BAe^146-100^146^4J^B461^4^J	141^BAe^146-100^146^4J^B461^4^J
	142^BAe^BAE Systems 146-200 Passenger^146^4J^B462^4^J	142^BAe^BAE Systems 146-200 Passenger^146^4J^B462^4^J
	143^BAe^146-300^146^4J^B463^4^J	143^BAe^146-300^146^4J^B463^4^J
	146^BAe^146^^^^^	146^BAe^146^^^^^
	14F^BAe^146 Freighter (-100/200/300QT & QC)^^^^^	14F^BAe^146 Freighter (-100/200/300QT & QC)^^^^^
	14X^BAe^146 Freighter (-100QT & QC)^14F^4J^B461^4^J	14X^BAe^146 Freighter (-100QT & QC)^14F^4J^B461^4^J
	14Y^BAe^146 Freighter (-200QT & QC)^14F^4J^B462^4^J	14Y^BAe^146 Freighter (-200QT & QC)^14F^4J^B462^4^J
	14Z^BAe^146 Freighter (-300QT & QC)^14F^4J^B463^4^J	14Z^BAe^146 Freighter (-300QT & QC)^14F^4J^B463^4^J

Using "paste" with commands instead of files

	 paste <(cat numbers) <(cat numbers)

	1	1
	2	2
	3	3
	4	4
	5	5
	6	6
	7	7
	8	8
	9	9
	10	10

## tr (translate)

Put headers line into different lines, changing delimiters "^" into "\n" (new line)

	head -1 optd_aircraft.csv | tr "^" "\n"

	iata_code
	manufacturer
	model
	iata_group
	iata_category
	icao_code
	nb_engines
	aircraft_type

Change characters

	echo "master data science" | tr ma AM

	AMster dMtM science

Remove spaces (-s: squeeze)

	echo "master    data    science" | tr -s " "

	master data science

	echo "maaaaaster    data   science" | tr -s " a"

	master data science

Keep certain characters

	echo "maaaaaster    data   science" | tr -cd " a"

        aaaaa    aa   %

Change delimiter "^" into "\t" (tab)

	cat optd_aircraft.csv | tr "^" "\t" | head 

	iata_code	manufacturer	model	iata_group	iata_category	icao_code	nb_engines	aircraft_type
	100	Fokker	100	100	2J	F100	2	J
	141	BAe	146-100	146	4J	B461	4	J
	142	BAe	BAE Systems 146-200 Passenger	146	4J	B462	4	J
	143	BAe	146-300	146	4J	B463	4	J
	146	BAe	146					
	14F	BAe	146 Freighter (-100/200/300QT & QC)					
	14X	BAe	146 Freighter (-100QT & QC)	14F	4J	B461	4	J
	14Y	BAe	146 Freighter (-200QT & QC)	14F	4J	B462	4	J
	14Z	BAe	146 Freighter (-300QT & QC)	14F	4J	B463	4	J

## grep

Find one word in two files at the same time, gives you those line numbers (with -v it gives you the lines that don't contain that word)

	grep -n this Text_example.txt Text_example.txt

	Text_example.txt:2:this line is the 1st lower case line in this file.
	Text_example.txt:6:Two lines above this are empty.
	Text_example.txt:7:And this is the last line.
	Text_example.txt:2:this line is the 1st lower case line in this file.
	Text_example.txt:6:Two lines above this are empty.
	Text_example.txt:7:And this is the last line.

Find how many times the word is contained in the file

	grep -c this Text_example.txt

	3

Show line number and counts times of word

	grep -n -o this Text_example.txt

	2:this
	this
	6:this
	7:this

Show all lines that start by "T"

	grep -n "^T" Finn.txt| less

3:The Project Gutenberg EBook of Adventures of Huckleberry Finn, Complete
6:This eBook is for the use of anyone anywhere at no cost and with almost
11:Title: Adventures of Huckleberry Finn, Complete
91:Testament.--Recovering the Raft.--The Wood--pile.--Pork and Cabbage.
94:Temperance Revival.--The Duke of Bridgewater.--The Troubles of Royalty.
100:Town.--A Lazy Town.--Old Boggs.--Dead.
157:Trouble.
170:The Widows
178:They Tip-toed Along
182:Tom Sawyer’s Band of Robbers  
188:The Robbers Dispersed
206:The Widows
214:They Tip-toed Along
218:Tom Sawyer’s Band of Robber

## sed (stream editor)

It's used for converting one stream into other things 

	echo Sunday | sed s/day/night/

	Sunnight

It stops substituting after the first time

	echo Sunday.day | sed s/day/night/

	Sunnight.day

Make global substitue

	echo Sunday.day | sed s/day/night/g

	Sunnight.night

Make global substitue inside a file

	sed 's/this/WHAAT/g' Text_example.txt

	THIS LINE IS THE 1ST UPPER CASE LINE IN THIS FILE.
	WHAAT line is the 1st lower case line in WHAAT file.
	This Line Has All Its First Character Of The Word With Upper Case.


	seq 5
	1
	2
	3
	4
	5

Delete lines from 2 to 4

	seq 5 | sed '2,4d'
	
	1
	5

Delete lines 2 and 4

	seq 5 | sed '2d;4d'

	1
	3
	5

Delete third line

	seq 10 15 | sed '3d' 

	10
	11
	13
	14
	15

Delete line that contains 14

	seq 10 15 | sed '/14/d'

	10
	11
	12
	13
	15

## Working with compressed files

## zip

	zip file.zip files

	unzip file.zip

	zipinfo file.zip

	zcat file.zip (like cat)

	zless file.zip (like less)

	zgrep "string" file.zip

Piping on compressed files

	unzip -c output.zip optd_aircraft.csv | less | head

## gzip

Used for small files. gzip files contain only one file

Compress files and deletes original files

	gzip optd_aircraft.csv optd_aircraft_4_columns.csv optd_airlines.csv optd_por_public.csv 

	ls

	optd_por_public.csv.gz
	optd_aircraft.csv.gz
	optd_aircraft_4_columns.csv.gz
	optd_airlines.csv.gz

Uncompress all files and delete .gz files

	gunzip *.gz

## bz2

Valid for big files, usually over 128 MB. Used for Hadoop

Compress all files and delete the originals

	bzip2 *.csv

	optd_por_public.csv.bz2
	optd_aircraft.csv.bz2
	optd_aircraft_4_columns.csv.bz2
	optd_airlines.csv.bz2

Other commands

	bzcat
	bzless
	bzgrep
	bunzip2

## tar

Valid for grouping files, not necessarily compressed

Put into compressed zip file

	tar -czvf opentravel.gz.tar *.csv

Decompress zip file

	tar -xzvf ./opentravel.gz.tar	

Put into compress BZ2 file

	tar -cjvf opentravel.bz2.tar opentraveldata

Put into uncompressed tar file for grouping

	tar -cf opentravel.tar opentraveldata

## Shell Script

Let's create a script that reads the header (first line) of a CSV file and outputs each column name with an index 

Find text on terminal history

	CTRL + r

For choosing on what program to execute the script (in this case bash):

	!/bin/bash

To know what program is being used

	which bash

	/bin/bash

Execute script with chmod 777 and "#!bin/bash" on first line

	./csv_number_column.sh

	1	iata_code
	2	manufacturer	
	3	model
	4	iata_group
	5	iata_category
	6	icao_code
	7	nb_engines
	8	aircraft_type
	9	
	10	

Use {} for shell variables

	echo ${VARIABLE}

Final script

	#!/bin/bash
	DELIMITER=$1
	FILE=$2
	NUM_OF_COLUMNS=$(head -1 ${FILE} | tr ${DELIMITER} "\n" | wc -l)
	paste <(seq 1 ${NUM_OF_COLUMNS}) <(head -1 ${FILE} | tr ${DELIMITER} "\n")

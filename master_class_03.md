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

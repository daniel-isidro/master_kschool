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

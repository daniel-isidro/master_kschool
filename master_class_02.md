# Master Class 02: Command Line Basics

## CLI

The name of the current app in execution:

	echo $0
	($ means variable)

Enter bash:

	bash

Exit bash:

	exit

Different shells:

	zsh, shell, bash

What is the shell:

	echo $SHELL
	/bin/bash/ is the default shell in Mojave (zsh in Catalina)

Who am I:

	whoami

What machine is in use:

	cat /etc/os-release (not valid on macOS)

CPU info:

	cat /proc/cpuinfo (not valid on macOS)

Define variable:

	MASTER=Kschool

Show two variables:

	echo $MASTER $SHELL (two parameters)
	Out: Kschool /bin/bash

	echo “$MASTER $SHELL” (one parameter)
	Out: Kschool /bin/bash

	echo ‘$MASTER $SHELL’ (print var names)

	echo `$MASTER` (execute command)
	Out: -bash: Kschool: command not found

	echo $”()” (execute command)
	ex.: echo “$(date)”
	out: Sat Nov 16 10:08:24 CET 2019

Exit line:

	CTRL + C

Clean screen:

	CTRL + L

Next line:

	echo “This is” \

Split lines:
	
	\	next line (what comes after gets shown but not executed)
	$ echo "This is" \
	> "second one"
	Out: This is second one

	echo -e "first line \nsecond line"
	Out: first line 
 	second line

	echo -e “ttt\tt\tnnn”
	\t		tab

Concatenate text files:

	cat textfile1.md textfile2.md textfile3.md

Concatenate all files:

	cat *

Concatenate all files that start with T or end with .txt

	cat T*
	cat *.txt
	cat *.txt*

## PIPING

If you can see text as output of a command, you can use that as an inout of another command

Example:

	head optd_aircraft.csv | tail -5 | wc
 	      5      21     222

Gives the word count of the last 5 lines of the first 10 lines of the CSV file

Example:

	cat -n optd_aircraft.csv | head | tail -5 > 5lines.csv (overwrites lines)

	cat -n optd_aircraft.csv | head | tail -5 >> 5lines.csv (appends lines)

## FIND

	find . -mmin -60 -exec echo "Found it" \;
Finds files/dirs modified in the last 60 minutes and prints “Found it” as many times as files 

	find . -mmin -60 -exec ls -l {} \;
Finds files/dirs modified in the last 60 minutes and executes the command with {} as a placeholder of the filename

	find . -mmin -60 -exec sh -c "ls -l {} | wc" \;
As -exec doesn’t allow piping, sh -c “text” allows piping as it uses a shell

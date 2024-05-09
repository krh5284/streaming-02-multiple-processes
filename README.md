# streaming-02-multiple-processes

> Multiple processes accessing a shared resource concurrently
> Week 2 Streaming Data
> Kellie Bernhardt
> NWMSU

## Overview

This example starts a shared database and multiple processes.

The processes represent multiple users, or locations, or programs 
hitting a shared database at the same time. 

## Prerequisites

1. Git
1. Python 3.7+ (3.11+ preferred)
1. VS Code Editor
1. VS Code Extension: Python (by Microsoft)

## Task 1. Fork 

Fork this repository ("repo") into **your** GitHub account. 

## Task 2. Clone

Clone **your** new GitHub repo down to the Documents folder on your local machine. 

## Task 3. Explore

Explore your new project repo in VS Code on your local machine.

## Task 4. Execute Check Script

Execute 00_check_core.py to generate useful information.

## Task 5. Execute Multiple Processes Project Script

Execute multiple_processes.py using 0 seconds

In this first run, we start 3 processes, 
each inserting 2 records into a shared database 
(for a total of 6 records inserted.)

In each case, the process gets a connection to the database, 
and a cursor to execute SQL statements.
It inserts a record, and exits the database quickly.

In general, we're successful and six new records get inserted. 

## Task 6. Execute Multiple Processes Script with Longer Tasks

For the second run, modify the task duration to make each task take 3 seconds. 
Hint: Look for the TODO.
Run the script again. 
With the longer tasks, we now get into trouble - 
one process will have the database open and be working on it - 
then when another process tries to do the same, it can't and 
we end up with errors. 

## Task 7. Document Results After Each Run

To clear the terminal, in the terminal window, type clear and hit enter or return. 

`clear`

To document results, clear the terminal, run the script, and paste all of the terminal contents into the output file.

Use out0.txt to document the first run. 

Use out3.txt to document the second run.


-----
process_streaming_bernhardt.py takes a CSV from Kaggle (https://www.kaggle.com/datasets/sujithmandala/second-hand-car-price-prediction), streams it, and writes to a .txt file to combine the lessons learned in week 1 and week 2

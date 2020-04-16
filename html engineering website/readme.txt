This program works as a towers of Hanoi solver with 3 specific cases for commandline arguements
if argc ==1 (only towers is enterred) by default the program solves 3 disks from T1 to T2 and exit(0)
if argc==2 (towers #) the program solves n disks from T1 to T2 and exit(0)
if argc==4 (towers # # #) the program solves n disks from T# to T# and exit(0)
if any number is negative, if from/dest is not 1,2 or 3, if from==dest, or if in correct number of arguments enterred:
error is printed to stderr and exit(1)

To answer the questions in part 1.
	1. The first recursive call after towers(5,2,3) will be towers(4,2,1) this is because the first
  	   number gets changed by -1, the middle number stays the same and the last number is spare
   	   which is calculated by spare = 6 -2 -3 = 1.
	2. There will be 4 more recursive calls made
	3. The first move will be moving 1 disk from tower 2 to tower 3 the line: 
  	    2  3 will be printed out to stdout
	4. The second recursive call to towers() will be:
           towers(3,2,3)

Question 2.
	How many moves will be printed to stdout when towers(8,1,2) is called
	The formula is (n = #ofDisks) 
	#ofMoves = 2^n -1 
	which is 2^8 -1 = 256-1 = 255 lines to stdout
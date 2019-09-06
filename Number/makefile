#For this problem, you'll modify the makefile to create a better one.
#
#Add macros for compiler and compiler flags.
#The compiler flags to add are: -c, -Wall, -g, -std=c++11
#Add a macro that defines the object files that should be linked together
#to create the executable.
#Add suffix rule that specifies how to create a .o out of a .C file.
#Modify makefile to use the macros.
#Eliminate unnecessary commands and dependencies. (If the make utility can
#determine a dependence or a command then don't provide it.)
#Use tabs properly or makefile won't work.
#Answer first page of quiz questions using your makefile.
#

CC = g++
CFLAGS = -c -Wall -g -std=c++11
.C.o:
	$(CC) $(CFLAGS) $< -o $@ 
OBJ = makeNumber.o Number.o

makeNumber: $(OBJ)

makeNumber.o: Number.h

Number.o: Number.h

clean:
	rm -f *.o

#Create a makefile that will compile the .C files in the source
#directory and create a sortProg executable.
#
#Add macros for the compiler and the compiler flags.
#The compiler flags to add are: -c, -Wall, -g, -std=c++11, -I ../include
#Add a macro that defines the object files to be linked together
#to create the executable.
#Add suffix rule that specifies how to create a .o out of a .C file.
#You'll need a target for the executable (sortProg), each .o, install, and clean.
#The very first target in the makefile should be for the executable,
#sortProg.
#Create a bin directory that is at the same level as the source and include directories.
#The install command should create the executable and move it to the ../bin directory.
#The clean command should delete the .o files.
#Do not add unnecessary commands and dependences.
#Answer the questions in the third part of quiz.

CC = g++
CFLAGS = -c -Wall -g -std=c++11 -I $(INC)
INC = ../include
OBJ = sortProg.o Sort.o List.o BubbleSort.o MergeSort.o QuickSort.o
.C.o:
	$(CC) $(CFLAGS) $< -o $@

sortProg: $(OBJ)
SortProg.o: sortProg.C $(INC)/Sort.h $(INC)/BubbleSort.h $(INC)/QuickSort.h $(INC)/MergeSort.h $(INC)/List.h 
Sort.o: Sort.C $(INC)/Sort.h
List.o: List.C $(INC)/List.h
BubbleSort.o: BubbleSort.C $(INC)/BubbleSort.h $(INC)/Sort.h
MergeSort.o: MergeSort.C $(INC)/MergeSort.h $(INC)/Sort.h
QuickSort.o: QuickSort.C $(INC)/QuickSort.h $(INC)/Sort.h

install: 
	make sortProg
	mv sortProg ../bin 

clean:
	rm -f *.o

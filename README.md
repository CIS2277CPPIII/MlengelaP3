# Searching an Ordered List

# Turn in requirements: 
1.	10 pts Turn in your development project folder, named LastnameP3, to Brightspace.  Delete the x64/debug and ipch folders and Browse.VC file before zipping the project to upload.   
2.	Your project will have your Driver.cpp, your LastnamePersonGen folder, the Search.h and the Search.cpp, PersonSort.h, and all the files needed for generating Persons, including the Person.h, Date.h, PersonGen.h, two lib files, and the name text files. Some of these can be in your LastnamePersonGen folder.

**For P3, you will need to fix your PersonGen  from P2 if it wasn’t working correctly.**

__For Program 3, your project will contain your Driver.cpp, and the LastnamePersonGen folder at the source code level. Your two new files for this program are Search.h and cpp.  You will also create Driver.cpp and obtain PersonSort.h from Blackboard.  Turn in requirements:  LastnameP3 Project__

**Obtain the file: PersonSort.h from Brightspace.**

Program Specifications: We will be searching through an array of Person objects, trying to find an individual by name.  You are to build three different search functions.  We won’t have the functions in a class; they will just be functions.  Place the prototypes in the Search.h and actual functions in Search.cpp.  Each function requires that the list it is searching be an ordered list (i.e., sorted).  

In order to sort the values, you will use the PersonSort.h and create a sorter object for sorting Person objects.  Follow the directions in the comment at the top of the PersonSort.h to implement this sorter class in your program.

The goal of each of these three search functions is to determine if a Person with the desired name is in the list.  If the Person is in the list, the function returns true and the position (not the array element value) of the Person in the list. 

NOTE: the array indices will be [0] through [total-1], but you’ll be reporting the position in regular counting order, i.e., the first in the list will be in position #1 (array element 0).  If you are looking for “Anna”, and Anna is in element [0], the functions will return 1 for her position.  The position will not be the array element. If the named Person is not in the list, it returns false from the function, and -1 for the position. 

## The function prototypes are:

#### __1)	bool	SequentialSearch(Person folks[], int total, string target, int *position, int *pNumCompares);__

This search begins at the first element in the Person array and checks each Person in sequence for the “target” name.  If it passes the location where the name would be, it doesn’t look any further.  If it finds the target, it stops looking and returns true and the position in the list where the name is located.  It does not check for duplicate names.

NOTE: A comparison is counted anytime you are actually checking to see if a person is the one for which you are looking. Be sure you write the algorithms as specified to ensure you are going to have the right number of compares. 

#### __2) bool BinarySearch(Person folks[], int total, string target, int *position, int *pNumCompares);__

This function implements a loop that begins by setting the first and last indices—the 0th value is the first, and the last is the (total-1) value as “endpoints”. The function then calculates the midpoint element between the “first” and “last” and checks to see if the target is the value at the midpoint of the list.  If the target name is found, the position is returned.  If not, the function changes the appropriate first or last index to reduce the list to either the top half or the bottom half, and checks the midpoint for the search target. 

NOTE: No cheating by checking the 0th and “total-1” values first. 

The search stops when it either finds the target person or when the first and last index can’t be reassigned to new values.

The third search has you call the RunRecursiveSearch. Here is the prototype.

__3) bool RunRecursiveSearch(Person folks[], int total, string target, int *position, int *pNumCompares);__

The RunRecursiveSearch function calls a recursive version of the binary search. Its prototype is:

__bool RecursiveBinarySearch(Person folks[], string target, int first, int last, int *position, int *pNumCompares);__

The recursive function calculates the midpoint value and checks to see if it is the target. If it is, the position is returned. If not, the recursive function determines which section of the list to check again and calls the recursive function again. You will need to include a stopping condition in this function so that your functions aren’t stuck in an infinite recursive call sequence.

Your main function should show your header.  Ask the user to enter a name for an output file that will log the search results, then open it.   Create a new array of 1000 Persons.  Use a new PersonGenerator to fill this array.  Please print out the first 20 Persons’ names to the screen and into the log file so that we have known people in the array.  You then sort your array so that the Person objects are in alphabetical order based on the name.  Your Person class has overloaded operators for this purpose; otherwise, you would not be able to sort Person objects.

The main function then begins a do-while loop that asks the user to enter a name, firstname, and lastname.  Since this is not the format of the list, your function will reconfigure the name entered so it is searchable. Your project  then searches the list for the name using all three search functions.  The main will log the results to the screen and the output file,e including whether the name was found, at what position, and the number of comparisons used to find the target.  If the name was not found, still report the number of comparisons performed in the search.

Continue to allow the user to enter names until the user is finished.  Just add a regular “Do Another?” question

Your program needs to write an output file and screen output, and it needs to contain the following information: 

  <img width="698" height="373" alt="image" src="https://github.com/user-attachments/assets/c787454b-b37c-436c-ac85-9a70b4c8abda" />

NOTE: On the class day before the assignment is due, I’ll provide you with a test data file of 1000 persons, and your program needs to use my file and run the script I provide.  You’ll turn in the script and log file showing the results of the program at that time. 

# Sources:
# Usage: 
# Contributions: 

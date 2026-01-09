# Searching an Ordered List

# Turn in requirements: 
1.	10 pts Turn in your development project folder, named LastnameP3, to Brightspace.  Delete the x64/debug and ipch folders and Browse.VC file before zipping the project to upload.   
2.	Your project will have your Driver.cpp, your LastnamePersonGen folder, the Search.h and the Search.cpp, PersonSort.h, and all the files needed for generating Persons, including the Person.h, Date.h, PersonGen.h, two lib files, and the name text files. Some of these can be in your LastnamePersonGen folder.

**For P3, you will need to fix your PersonGen  from P2 if it wasn’t working correctly.**

**For Program 3, your project will contain your Driver.cpp, and the LastnamePersonGen folder at the source code level. Your two new files for this program are Search.h and cpp.  You will also create Driver.cpp and obtain PersonSort.h from Blackboard.  Turn in requirements:  LastnameP3 Project 

**Obtain the file: PersonSort.h from Brightspace.**

Program Specifications: We will be searching through an array of Person objects, trying to find an individual by name.  You are to build three different search functions.  We won’t have the functions in a class; they will just be functions.  Place the prototypes in the Search.h and actual functions in Search.cpp.  Each function requires that the list it is searching be an ordered list (i.e. sorted).  

In order to sort the values, you will use the PersonSort.h and create a sorter object for sorting Person objects.  Follow the directions in the comment at the top of the PersonSort.h to implement this sorter class in your program.

The goal of each of these three search functions is to determine if a Person with the desired name is in the list.  If the Person is in the list, the function returns true and the position (not the array element value) of the Person in the list. 

NOTE: the array indices will be [0] through [total-1], but you’ll be reporting the position in regular counting order, i.e., the first in the list will be in position #1 (array element 0).  If you are looking for “Anna”, and Anna is in element [0], the functions will return 1, for her position.  The position will not be the array element. If the named Person is not in the list, it returns false from the function, and –1 for the position. 


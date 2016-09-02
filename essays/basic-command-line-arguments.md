---
layout: essay
type: essay
title: Basic Use of Command-Line Arguments
date: 2016-02-14
labels:
  - Software Engineering
  - Learning
---

<img class="ui tiny left circular floated image" src="https://upload.wikimedia.org/wikipedia/commons/6/6f/Octicons-terminal.svg">

Command-line arguments allow you to pass values to a program from the command line, similar to the way in which you would pass values to any function within a program. In the C, C++, and Java programming languages specifically, command-line arguments are passed into the program’s main function if it is defined with the appropriate parameters. Once the arguments are passed, they can be found within the indices of the argv array. In the case of C and C++ argv [0] holds the program’s name, followed by the parsed arguments, while in Java the program’s name is not included in argv.
The arguments are usually passed in by listing them after the name of the program, for example, make hw3. The argument passed to the make program is “hw3”, which in this specific case tells make to check that all the conditions necessary to create the hw3 file exist and, if they do, to then execute all the instructions necessary to create said file.
	Generally, command-line arguments are useful if the chances are good that a user will already know the values that they would like to pass at the time that the program is invoked. For instance, consider a case in which you might be writing a user interface for a bank database. After the program has been invoked, you could print a list of transaction options and prompt the user to enter their choice of action. However, you could also allow users to enter command-line arguments specifying their choice at the time that the program is invoked, a feature that more familiar, repeat users of the program might like to make use of in order to save time.
	The ability to enter command-line arguments often gives the user a little more flexibility in terms of what they want to do with the program. These arguments can allow you to set initial values within a program that differ from the default settings, enable debugging features, or specify certain external files to access. Allowing command-line arguments to be passed can also make it easier for your program to be invoked by other programs. This could be useful in the situation where your program is part of a larger system of programs that work together cohesively, or in the case that your program acts as an extension for an application.
	Depending on how the program is designed, command-line arguments can be used to provide optional functionality, or they can be required for the program to run as intended. I recently made use of two programs for an assignment in ICS 321, Data Storage and Retrieval, one in which command-line arguments were optional, and the other in which they mandatory. 
The first program was called AutoRun, and by default (without command-line arguments) it performed a sequence of hard-coded queries to find matching records in a text file that acted as a database (using comma-separated values). The name of a text file passed as a single optional command-line argument allowed a user to enter a custom sequence of queries to perform, as long as they were specified in the appropriate format within the text file.
The second program was called FileGenerator, and it was designed to generate text file databases of the kind previously mentioned. If it was run without any arguments it would print a message detailing the proper usage of the program, which was to enter the program name followed by command-line arguments specifying the size of file to generate and the name that this file should be given. Upon entering the appropriate arguments¬¬¬¬ the program would generate a text file with the specified name and size.
As you can see, command-line arguments can provide a number of possible benefits. In the end, their usefulness is only limited by your imagination.

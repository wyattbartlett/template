---
layout: project
type: project
image: images/cpp-programming-language-300px.jpg
title: Customer Database Interface in C++
permalink: projects/customer-database-interface-cpp
date: 2016
labels:
  - C++
  - g++
  - SCCS
  - Unix
summary: A command-line interface for a customer database written in C++ for ICS 212, Program Structure.
---

<img class="ui medium right floated rounded image" src="../images/customer-db-interface-c.png">

After creating a mock customer database interface in C for ICS 212, Program Structure, I recreated it in C++. The application still has no GUI, but is designed to be used through the command-line interface (CLI) as before. When the application is started a menu is displayed prompting the user to choose one of several options. Options include:

1. Add Record
2. Modify Record
3. Print Record
4. Print All Records
5. Delete Record
6. Quit

It took about a week to translate this application to C++ and add some extra features. I was once again the sole author of this project, and it was written entirely in C++, following C++ conventions. It was interesting to program in an object-oriented style outside of Java. I would like to build more experience in C++ and become more fluent in the language in the future.

Programming this application gave me a deeper understanding of passing by reference, and how easy it is! The experience also introduced me to overloading an operator, which I had experienced previously but never really recognized. I also became aware of preprocessor directives through this project, and how they can be used in combination with make to create different versions of an application, such as a special version for debugging.
 
Source: <a href="https://github.com/wyattbartlett/customer-database-interface-cpp"><i class="large github icon"></i>Check out my repo on GitHub.</a>

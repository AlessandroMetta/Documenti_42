---
layout: default
title: notes_CPP02
nav_exclude: true
---

# Notes about CPP02 videos

## Function Overloding

Define many function with the same name but with different parameters.
Simply define more function but with different parameter.

## Operator overload

some vocabulary
1 + 1 is INFIX notation, because the plus operator is between the two operands;
+ 1 1 is PREFIX notation, the operator is before the two operands, is also know as FUNCTIONAL notation;
1 1 + is POSTFIX notation, the operator is after the two operands.

In this video we'll understand how overload an operator:
	Class_name	operator+(attributes)
an overload is composed by the keyword operator follow by the operator which we want to overload, and then the attributes.
The operator can be unary, binary and ternary.
An example of binary is the assignment operator, which have on the left the item we're assign to and on the right the item we want to assign. Similarly, the addition operator is binary, we have an operand on the left and the other one right.
An example of unary operator is the pre-incrementation or the post-incrementation (which both did't admit any parameters).
In this case, we use to return a reference of the class in the assignment overload because it can be assign in turn to another value(like: a = b = c =d). After assign it, the instance will be destructed immediately. 
instead, the return of the addition overload is only an instance of the addition, because it will be assign to an value, but it isn't necessary the same of the assignment overload.
In the end, we want to overload the operator << to redirect to the output a specific type, our integer class. This overload is not a member overload, because the << operator is a library define operator, so is not possible to overload it inside a class. the return of the output string like a reference will allow to chain different redirection.

### Rules to follow when writing operator overload (It's easy to do bad with that):
- the overload must be natural, if aa behavior of an operator is strange, that something to avoid at any cost 
- the overload of you operator must be related to the natural semantic of this operator, in sense to not overload operator to another operator or operation that has not sense.
- JUST DON'T DO IT! Use overload only when is necessary, not because you find it cool.

## Canonical form

It's a way to build basic classes to make sure we have a reasonable and identical interface over all our project. From there anyone who read your source code or even yourself wold be sure that there are a certain number of function available in all your classes allowing  for uniform process.
We would consider a class canonical when have at least:
- a default constructor (does not take parameter);
- a copy constructor (take as parameter a reference of an instance of the class we are defining to make a copy of these class);
- an assign operator overload, allowing to make an assignment from an instance of this class (don't confuse the copy constructor with the assignment: with the copy constructor we do have a new instance created, while in the assignment we only have update the current instance) (Sample & operator=(Sample const & instance));
- a destructor. 
it' also very appreciable (not mandatory) to be able to serialize your class into a string, so think about overload the << operator to print directly the value we are interested in.
This four element will allow your class to be called canonical. 
From now on, it's mandatory write you classes in the canonical form! If it's not specified by subject, it will considered mistake.

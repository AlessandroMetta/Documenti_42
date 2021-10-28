---
layout: default
title: notes_CPP02
nav_exclude: true
---

# CPP01
## ex00
The aim of the exercise is to understand the different functions to allocate on the heap not only values, but also classes.

### intra video:  new and delete
```
Sample_class* instance = new Sample_class( /* arguments if needed */ ); (malloc)
delete instance; (free)
```

## ex01
Similarly to the previous, this exercise aims to understand how to allocate arrays of instances.
```
Sample_class* instance = new Sample_class[number_of_element];
delete [] instance;
```

## ex02
The aim of this exercise is to understand how to use pointers and references, a new tool of C++. It’s very similar to pointer, but that can’t be NULL.
```
int value = 1;
void *valuePtr = &value;
void & valueRef = value;
cout << *valuePtr << valueRef;
```
## ex03
The aim of this exercise is to understand when to use the reference and the pointers.

## ex04
The aim of this project is to understand how to use the filestream in C++.
The function to open a file in a read mode  is fstream, while to write is ofstream;
```
while (getline(srcFile, linegetted))
{
	while ((pos = linegetted.find(argv[2])) != std::string::npos)
	{
		linegetted.erase(pos, str1.length());
		linegetted.insert(pos, str2);
	}
	dstFile << linegetted << std::endl;
}
```

## ex05
The aim of this exercise is to learn to use the pointer to members.
### intra video: pointer to members
```
int Sample_class::*ptr_to_value = NULL;
ptr_to_value = &Sample_class::value
// this line of code initializes a pointer on a member attribute of the Sample class to a variable public member of the class.
// If we want to access that value, if it's an instance on the stack instance.
*ptr_to_value = 0;
// this will modify the value pointed by ptr_to_value of the instance
// else if it’s instance on the heap
instancePtr->*ptr_to_value = 0;
// this instead will modify the value pointed by ptr_to_value of the pointed instance

void (Sample::*ft)(void) const;
ft = &Sample::bar;
// in the above two lines, I declare a pointer to member function and the assign the function bar
(instance.*f)();
// in this case I call the function pointed by ft of the stack intanciated instance
(instancePtr->*f)();
// in this case I call the function pointed by ft of the heap intanciated instance
```
## ex06
The aim of this exercise is to understand the usage of the switch case, a new control statement.
```
switch (expression)
{
  case constant1:
     group-of-statements-1;
     break;
  case constant2:
     group-of-statements-2;
     break;
  .
  .
  .
  default:
     default-group-of-statements
}
```
In our case, we need to print all the below information, so we put the default condition at the top and remove from the other cases the break, so it executes all the cases above the input one.


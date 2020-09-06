---
layout: post
title: Array Data Structure
color: rgb(0,0,255) 
tags: [Array Operations, Array Data Structure]
excerpt: An array is a collection of finite number of elements that means the size an array is fixed and should be defined at the time of declaration of an array
author: BBB
---

An array is a collection of finite number of elements that means the size an array is fixed and should be defined at the time of declaration of an array. 

Array is linear, homogeneous and static data structure. The elements of an array can be accessed randomly by specifying its index value. 

Array data structure is used to store elements of basic data type like int, float, double, char etc. 

## Advantages of Array
1. Reduces number of variables and lines of code as we can store the multiple values using single variable name.
2. As Array size need to be defined at the time of declaration of an array variable, there is no chance for memory overflow or memory underflow.
3. Arrays provides the Random access to the elements.
4. Applying a particular opeartion like traversing becomes easy with the help of iterative statement.

## Disadvantages of Array
1. Array size can not be changed as they are of fixed size.
2. Array size should be known at the time of declaration of an array.
3. Declaration of array with more size than the reqirement may lead to wastage of memory. 
4. Insertion and deletion operations are would be costly as the memory locations need tobe managed to store element values. 
5. Usually the Compiler or Interpreter does not verify the array index number at the time of compilation, that leads to run-time error.

## Application of Array
1. Arrays can be used to perform the vector and matrix operations. 
2. Arrays can be used to implement the sorting algorithms like Bubble Sort, Insertion Sort, Merge Sort etc.
3. Arrays can be used to implement other data structure like Stack, Queue, Linked List etc.
4. Arrays can be used to implement the various operating System Algorithms like CPU Scheduling.
5. Arrays can be used to group the elements of basic as well as user-defined data types.

## Types of Array

Depending on the number of dimensions ( Number of subscripts or index ), arrays can be classified as- 
1. One-Dimensional Array
2. Two-Dimensional Array
3. Multi-dimensional Array

### One-Dimensional Array

An array with a single subscript is known as one-dimensional array. One-dimensional array can be used to store the set of values of same data types 
or in other terms we can say that one-dimensional array can be used to store the values of a vector.

#### For Example
Let us define a one-dimensional array named 'A' to store marks of 5 students. 

So here, Size of array is 5 and  Index of First element will be 0.

Note: All code statements included into this blog are written using the of syntax C++ language.

Define or Declare an Array A as,

```A[5] = {60,70,75,85,90} ```

#### Pictorial Representation 
When you create an array variable or object, it will be initialized with the address of first element.
If the memory location assigned to first element is 3050, the memory location address for other elements will be as follows:

| | | | | | |
|-|-|-|-|-|-| 
| Index           |	0	     | 1       |	2      |      3	|      4 |
| Element Value	  | 60    | 70      |	75     |	   85 |     90 |
| Memory Location |	3050 | 3051	| 3052 | 3053 |	3054 |

#### Array Declaration  
```int A[5];```
#### Array Declaration and Initialization into a Single Statement
```int A[5] = {60,70,75,85,90};```
#### Initialization of an individual Element of an Array 
Initialize an individual element by specifying the index value of an element.
Let us define all elements of Array A:

`A[1]=70;`

`A[2]=75;`

`A[3]=85;`

`A[4]=90;`

### Access the element of an array
The individual ement can be accessed by specifying subscript or index value of the element.

For eaxmple, Print 3rd element of an array and its memory location address

`cout <<”A[2]=”<<A[2];`

### Two-Dimensional Array

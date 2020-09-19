---
layout: post
title: Array Operations 
color: rgb(0,0,255) 
tags: [Array, Array Operations]
excerpt: 
author: BBB
---

# Array Operations
Array data structure supports following basic operations - 
1. Traverse
2. Insertion
3. Deletion
4. Search
5. Update


## 1. Traverse 
   In Traversing operation every element of an array will be visited for processing for only once.  
   
**Example**
Given an array arr_A of 5 elements like 10,80,40,70,60, traverse and print the elements of the array.

**Arr_Traverse.cpp** 
```cpp
// Array Traversal Operation - To print all elements of array arr_A
#include <iostream>

using namespace std;

int main()
{
    int arr_A[]={10,80,40,70,60};
    int i;
    cout<<"Elements of Array A are: \n";
    // Traverse an array arr_A for printing all elements 
    for(i=0;i<5;i++)
    {
    cout<<"arr_A["<<i<<"]="<<arr_A[i]<<"\n";
    }
    return 0;
}

```   

**Output**
```
Elements of Array A are:
arr_A[0]=10                                                                           
arr_A[1]=80                                                                                                   
arr_A[2]=40                                                                                                   
arr_A[3]=70                                                                                                   
arr_A[4]=60                                                                                                   
                                                                                                              
                                                                                                              
...Program finished with exit code 0                                                                          
Press ENTER to exit console.  
```

## 2. Insertion 
   Intsertion operation is to insert one or more elements into an array. The element can be inserted at the begining, end or at any given position.
   
**Example**
Given an array arr_A of 5 elements, insert an element into the array at the given position.

**Arr_Insertion.cpp**
``` cpp
//Array Insertion Operation - Insert an element into array at the specific position

#include <iostream>
using namespace std;

int main ()
{
  int arr_A[5] = {10,80,40,50,0}; // Here 0 represents blank element
  int arrSize = 5, curPos = 3;
  int i, insAtIdx, newEleVal, shift;
  cout << "Elements of Array A are: \n";
  for (i = 0; i < arrSize; i++)
    {
      cout << "arr_A[" << i << "]=" << arr_A[i] << "\n";
    }
  cout << "Enter the positon of an element to be inserted: \n";
  cin >> insAtIdx;
  if (curPos < arrSize - 1 && insAtIdx < arrSize-1)
    {
       cout << "Enter value of an element to be inserted: \n";
       cin >> newEleVal;
       //Make the space for new element to be inserted
       //Shift elements forward by one position 
       for (shift = curPos; shift >= insAtIdx; shift--)
         arr_A[shift + 1] = arr_A[shift];
       arr_A[insAtIdx] = newEleVal;
      
       //Reprint the array arr_A after insertion of new element
       cout << "Elements of Array A are: \n";
       for (i = 0; i < 5; i++)
        cout << "arr_A[" << i << "]=" << arr_A[i] << "\n";
    }
  else
    cout << "Position of the element tobe inserted is out of range";

  return 0;
}

```


**Output**
```
Elements of Array A are:                                                                                      
arr_A[0]=10                                                                                                   
arr_A[1]=80                                                                                                   
arr_A[2]=40                                                                                                   
arr_A[3]=50                                                                                                   
arr_A[4]=0                                                                                                    
Enter the positon of an element to be inserted:                                                               
2                                                                                                             
Enter value of an element to be inserted:                                                                     
100                                                                                                           
Elements of Array A are:                                                                                      
arr_A[0]=10                                                                                                   
arr_A[1]=80                                                                                                   
arr_A[2]=100                                                                                                  
arr_A[3]=40                                                                                                   
arr_A[4]=50 
                                                                                                             
                                                                                                              
...Program finished with exit code 0                                                                          
Press ENTER to exit console.             
```


## 3. Deletion 
   Deletion operation refers to removing an element from an array. In order to remove the element from an array you have to reorganize the elements of an array. 

**Example**










## 4. Search
   Searching operation helps to check the existance of a particular element into the array.

**Example** 
Given an array arr_A of 5 elements like 10,80,40,70,60 and element tobe searched, find the first occurance of an elements 
into the array.

**Arr_Search.cpp**
```cpp

// Array Searching Operation - To search for the first occurance of the given element into an array

#include <iostream>

using namespace std;

int main ()
{
  int arr_A[] = { 10, 80, 40, 70, 60 };
  int i, searchEle, Flag = -1;
  cout << "Elements of Array A are: \n";
  for (i = 0; i < 5; i++)
    {
      cout << "arr_A[" << i << "]=" << arr_A[i] << "\n";
    }
  cout << "Enter the element to be searched:";
  cin >> searchEle;
  for (i = 0; i < 5; i++)
    {
      if (arr_A[i] == searchEle )
       {
       Flag=1;
       break;
       }
      else
       {
        Flag = -1;
       }
  }
  if(Flag == 1)
      cout << "Element " << searchEle << " found at index " << i << "\n";
  else
      cout << "SearchEle Not Found in given array\n";
       
return 0;
}
```
**Output**
```
Elements of Array A are:                                                                                      
arr_A[0]=10                                                                                                   
arr_A[1]=80                                                                                                   
arr_A[2]=40                                                                                                   
arr_A[3]=70                                                                                                   
arr_A[4]=60                                                                                                   
Enter the element to be searched:60                                                                           
Element 60 found at index 4                                                                                   
                                                                                                              
                                                                                                              
...Program finished with exit code 0                                                                          
Press ENTER to exit console. 
```


## 5. Update − Updates an element at the given index.
   The Updating operation refers to updating the existing element value from an array at a given index.

**Example**
Given an array arr_A of 5 elements like 10,80,40,70,60 and the values of index and element tobe updated, update element
of the array.

**Arr_Update.cpp**
```cpp
#include <iostream>
using namespace std;

int main ()
{
  int arr_A[] = { 10, 80, 40, 70, 60 };
  int i, updateIdx, newEleVal;
  cout << "Elements of Array A are: \n";
  for (i = 0; i < 5; i++)
    {
      cout << "arr_A[" << i << "]=" << arr_A[i] << "\n";
    }
  cout << "Enter the index of element to be updated:";
  cin >> updateIdx;
  cout << "Enter new value for the element";
  cin >> newEleVal;
  if (updateIdx < 5)
    {
      arr_A[updateIdx] = newEleVal;
      cout << "Array element at index " << updateIdx << " is Updated\n";
      cout << "arr_A[" << updateIdx << "] = " << arr_A[updateIdx];
    }
  else
    cout << " Index out of range \n ";

  return 0;
}
```

**Output**
```
Elements of Array A are:                                                                                      
arr_A[0]=10                                                                                                   
arr_A[1]=80                                                                                                   
arr_A[2]=40                                                                                                   
arr_A[3]=70                                                                                                   
arr_A[4]=60                                                                                                   
Enter the index of element to be updated: 2                                                                   
Enter new value for the element100                                                                            
Array element at index 2 is Updated                                                                           
arr_A[2] = 100                                                                                                
                                                                                                              
...Program finished with exit code 0                                                                          
Press ENTER to exit console. 
```

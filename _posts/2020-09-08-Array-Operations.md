---
layout: post
title: Array Operations 
color: rgb(0,150,255) 
tags: [Array, Array Operations]
excerpt: An array data structure supports Insert, Update, Delete, Search and Traverse operations. 
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
   In Traversing operation every element of an array will be visited only once for processing. 

  **Steps to traverse an array**

   1. Start array traversal from the first element that exists at index 0.
   2. Visit that element that means apply the process/tesk to that element.
   3. Move to next element and repeat steps from step number 2 till the last element.
     
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

  Let us consider an array of size 'n' with 'm' existing elements, where 'm' is always less than or equal to 'n-1' as array index starts from 0.

  **Steps to insert an element at the end of an array**
   1. If the array is empty that means if m=o, insert the elements at the 1st position into the array.
   2. If the array contains m elements and m<=n-2,insert the element at (m+1)th position into the array.
     
  **Steps to insert an element at the begining of an array**
   1. If the array is empty that means if m=0, insert an element at 1st position into the array.
   2. If the array of size 'n' contains 'm' elements, then shift the m elements forward by one position and insert the new element at the 1st position.
   3. If the number of existing elements are equal to the array size that means if n=m, the you can not insert the elements intothe array.

  **Steps to insert an element at the specific position into an array**
   1. Read the index position 'insAtIdx' from the user, where the new element isto be inserted.
   2. If array is not full and if insAtIdx<=n-2, shift the subsequent element upward by one position that means shift the elements from mth position to insAtIdx position.
   3. Insert the new element at the given index position neinsAtIdxwIdx. 

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
  Deletion operation refers to removing an element from an array. You can delete the element from an array by reading its index position or value from the user. 
  
  **Steps to delete the element at given index position**
   1. Read the index position of the element to be deleted.
   2. Return the value of deleted element.
   3. Shift the subsequent elements upward by one position to fill up the array.
   4. Replace the last element by zero.
  
  **Steps to delete the last element of an array**
   1. Return the value of last element that means deleted element.
   2. Replace the last element by zero.
  
  **Steps to delete the specific element from an array**
   1. Read the element tobe deleted from the user.
   2. Search for the first occurance of input element into an array.
   3. Return the value of deleted element.
   4. Shift the subsequent elements upward by one position to fill up the array.   
   5. Replace the last element of array by zero.

**Example**

**Arr_Deletion.cpp**
```cpp
//Array - Delete operation : Delete element from an array that exists at specific position
#include <iostream>
using namespace std;

int main ()
{
  int arr_A[] = { 10, 80, 40, 70, 60 };
  int i, delIdx, arrSize = 5;
  
  //Print element of array 
  cout << "Elements of Array A are: \n";
  for (i = 0; i < 5; i++)
    {
      cout << "arr_A[" << i << "]=" << arr_A[i] << "\n";
    }
    
  //Read index position of an element to be deleted    
  cout << "Enter the index position of an element to be deleted:";
  cin >> delIdx;
  
  //Delete element of array that exist at the given index position 
  if(delIdx >=0 && delIdx < arrSize-1)
     cout << "Element value of deleted element is : " << arr_A[delIdx] << "\n";
  
  //Shift element of array upward by one position to fill up an array
  for (i = delIdx; i < arrSize - 1; i++)
    {
      arr_A[i]=arr_A[i+1];
    }
    
  //Store 0 as the value of last array element
  arr_A[arrSize-1] = 0; 
  
  //Print array after deletion operation
  cout<<"Elements of array after deletion operation : \n";
  for (i = 0; i < arrSize; i++)
    {
      //arr_A[i]=arr_A[i+1];
      cout << "arr_A[" << i << "]=" << arr_A[i] << "\n";
    }
  
return 0;
}
```
**Output**
```cpp
Elements of Array A are:                                                                                      
arr_A[0]=10                                                                                                   
arr_A[1]=80                                                                                                   
arr_A[2]=40                                                                                                   
arr_A[3]=70                                                                                                   
arr_A[4]=60                                                                                                   
Enter the index position of an element to be deleted:0                                                        
Element value of deleted element is : 10                                                                      
Elements of array after deletion operation :                                                                  
arr_A[0]=80                                                                                                   
arr_A[1]=40                                                                                                   
arr_A[2]=70                                                                                                   
arr_A[3]=60                                                                                                   
arr_A[4]=0                                                                                                    
                                                                                                              
                                                                                                              
...Program finished with exit code 0                                                                          
Press ENTER to exit console.                                                                                  
                          
```

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


## 5. Update − Updates an element at the given index
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

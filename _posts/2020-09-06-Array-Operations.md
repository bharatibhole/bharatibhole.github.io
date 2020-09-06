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
   
```cpp
#include <iostream>

using namespace std;

int main()
{
    int arr_A[]={10,80,40,70,60};
    int i;
    cout<<"Elements of Array A are:"
    for(i=0;i<5;i++)
    {
    cout<<"arr_A["<<i<<"]="<<arr_A[i]<<"\n";
    }
    return 0;
}
```   
## 2. Insertion 
   Intsertion operation is to insert one or more elements into an array. The element can be inserted at the begining, end or at any given position.
   

## 3. Deletion 
   Deletion operation refers to removing an element from an array. In order to remove the element from an array you have to reorganize the elements of an array. 

## 4. Search
   Searching operation helps to check the existance of a particular element into the array.
```cpp

#include <iostream>

using namespace std;

int
main ()
{
  int arr_A[] = { 10, 80, 40, 70, 60 };
  int i, searchEle,flag;
  cout << "Elements of Array A are:";
  for(i = 0; i < 5; i++)
    {
      cout << "arr_A[" << i <<"]=" << arr_A[i] << "\n";
    }
  cout << "Enter the element to be searched:";
  cin >> searchEle;
  for(i = 0; i < 5; i++)
    {
    if (arr_A[i] == searchEle)
	   flag = i;
	else
	   flag = -1;
	}
  if(flag >=0)	
    cout << "Element " << searchEle << " found at index " << flag << "\n";
  else
    cout<<"SearchEle Not Found in given array\n";
  return 0;
}
```

## 5. Update − Updates an element at the given index.
   The Updating operation refers to updating the existing element value from an array at a given index.

```cpp
#include <iostream>

using namespace std;

int main ()
{
  int arr_A[] = { 10, 80, 40, 70, 60 };
  int i, updateIdx, newEleVal;
  cout << "Elements of Array A are:";
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
      cout << "arr_A[updateIdx]=" << arr_A[updateIdx];
    }
  else
    cout << "Index out of range\n";

  return 0;
}

```



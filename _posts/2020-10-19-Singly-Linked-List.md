---
layout: post
title: Singly Linked List
color: rgb(0,0,255) 
tags: [Singly Linked List, LL]
excerpt: Linked List is a linear collection of data elements in which linear order is not given by their physical placement in memory. 
author: BBB
---

#Singly Linked List

Linked List is a linear collection of data elements in which linear order is not given by their physical placement in memory. In linked list the elements are represented by a node. Each node consists of the data value and referenceto the next element. The last node contains the reference value NULL.

#Singly Linked List operations
1. Insertion of an element at the end of Singly Linked List
2. Insertion of an element at the begining of Singly Linked List
3. Insertion of an element at a particular position
4. Traverasing the Linked List
5. Reversing the Linked List


##Insertion of an element at the end of Singly Linked List

**SLinkedList.cpp**
```cpp
#include<iostream>
using namespace std;
//Define structure of a Node
struct Node
{
  int ItemValue;
  struct Node *RefToNxtNode;
};
//Define a class for all operations of Linked List
class SinglyLL
{
private:
  Node * headOfLL, *tailOfLL;
public:
  //Define constructor to initialize starting andending point of Linked List
  SinglyLL ()
  {
    headOfLL = NULL;
    tailOfLL = NULL;
  }
  //Define a method to display Menu
  void menu ()
  {
    cout <<
      "\nMenu\n 1. Add Node to the End of LL\n 2. Traverse LL\n 9. Exit\n";
  }
  //Define a method to insert an element atthe endof the Linked List 
  void addNodeToEndOfLL (int eleValue_in)
  {
    Node *tempNode = new Node;
    tempNode->ItemValue = eleValue_in;
    tempNode->RefToNxtNode = NULL;
    if (headOfLL == NULL)	//LL is empty
      {
	headOfLL = tempNode;
	tailOfLL = tempNode;
      }
    else
      {				//if LL is not empty then add ele to the end of list
	tailOfLL->RefToNxtNode = tempNode;
	tailOfLL = tempNode;
      }
  }
  //Define a method to traverse a Linked List
  void traverse ()
  {

    Node *NodePtr;
    NodePtr = headOfLL;
    cout << "\nThe elements of Linked List are" << endl;
    while (NodePtr != NULL)
      {
	cout << NodePtr->ItemValue<<" -> ";	//Print the item value of element
	NodePtr = NodePtr->RefToNxtNode;	//Goto next element
      }

  }
};				//End class

int main()
{
  int eleValue, urChoice;
  SinglyLL obj1;		// Object of LL class
  while (1)
    {
      obj1.menu();
      cout << "Enter Your Choice : ";
      cin >> urChoice;
      switch (urChoice)
	{
	case 1:
	  cout<< "Enter Element Value to be added into LL: \n";
	  cin >> eleValue;
	  obj1.addNodeToEndOfLL(eleValue);
	  break;

	case 2:
      obj1.traverse ();
	  break;
	case 9:
	  cout<<"Program Terminated by You";
	  exit (0);
	}
    }
return 0;
}
```
**Output**
```cpp
Menu
 1. Add Node to the End of LL
 2. Traverse LL
 9. Exit
Enter Your Choice : 1
Enter Element Value to be added into LL: 
10

Menu
 1. Add Node to the End of LL
 2. Traverse LL
 9. Exit
Enter Your Choice : 2

The elements of Linked List are
10 -> 
Menu
 1. Add Node to the End of LL
 2. Traverse LL
 9. Exit
Enter Your Choice : 9
Program Terminated by You

...Program finished with exit code 0                                                                     
Press ENTER to exit console. 
```
---
layout: post
title: Doubly Linked List
color: rgb(0,200,255)
tags: [Programming,Linked List, Doubly Linked List]
excerpt: The Doubly Linked List is a Linked List that can be traversed in both Forward and Backward Direction.
anchor: BBB
---

# Doubly Linked List

The Doubly Linked List is a Linked List that can be traversed in both Forward and Backward Direction. Doubly Linked List is also referred as Two-Way Linked List.

# Doubly Linked List operations:

The Doubly Linked List supports the following operations:

Insertion of an element at the end of Doubly Linked List
2. Insertion of an element at the begining of Doubly Linked List
3. Insertion of an element at a particular position in Doubly Linked Lsit
4. Traverasing the Doubly Linked List
5. Reversing the Doubly Linked List

## 1. Insertion of an element at the end of Doubly Linked List and Traversal of Doubly Lined List

**DLinkedList.cpp**

```cpp
#include <iostream>
using namespace std;
struct Node
{
    struct Node *prev;
    int info;
    struct Node *next;
};

class DLL
{
 private: 
 Node *head, *tail;
 public:
 DLL()
 {head=NULL; tail=NULL;}
 
 void addNode(int data)
 {
     Node *temp =new Node;
     temp->prev=NULL;
     temp->next=NULL;
     temp->info=data;
     if(head==NULL)
     { head=temp;tail=temp;  }
     else
     {
         temp->prev=tail;
         tail->next=temp;
         tail=temp;
     }
 }
 
 void traverse()
 {
  Node *ptr;
  //Forward Traversing
  ptr=head;
  cout<<"The elements of DLL are: \n";
  while(ptr!=NULL)
  {
      cout<<ptr->info<<" -> ";
      ptr=ptr->next;
  }
     
 }
 void addNodeBeg(int data)
 {
     Node *temp =new Node;
     temp->prev=NULL;
     temp->next=NULL;
     temp->info=data;
     if(head==NULL)
     { head=temp;tail=temp;  }
     else
     {
         temp->next=head;
         head=temp;
     }
 }
 void addNodeSpec(int loc, int data1)
 {
     Node *temp =new Node;
     Node *ptr,*succesor;
     temp->prev=NULL;
     temp->next=NULL;
     temp->info=data1;
     ptr=head;
     while(ptr->next!=NULL && ptr->info!=loc)
     {
      ptr=ptr->next;   
     }     
     if(ptr->next==NULL && ptr->info!=loc)
        {
            cout<<"Value cant be inserted as"<<loc << " not found in DLL\n";
            exit(0);
        }
        if(ptr->next!=NULL)
        {
            succesor =ptr->next;
            temp->next =succesor;
            ptr->next=temp;
            temp->prev=ptr;
        }    
         
     else
        {
           temp->next=NULL;
           temp->prev=ptr;
             ptr->next=temp;
             tail=temp;
        }
     
 }
 
};
int main()
{
  DLL obj1;
  int i,data,loc,data1;
  for(i=0;i<5;i++)
  {
  cout<<"Enter data value of node";
  cin>>data;
  obj1.addNodeBeg(data);
  }
  obj1.traverse();
  cout<<"\nEnter the value of node after which you want to add new element:\n";
  cin>>loc;
  cout<<"Enter Value tobe added:\n";
  cin>>data1;
  obj1.addNodeSpec(loc,data1);
  obj1.traverse();
}
```

**Output**
```cpp
Enter data value of node10
Enter data value of node20
Enter data value of node30
Enter data value of node40
Enter data value of node50
The elements of DLL are: 
50 -> 40 -> 30 -> 20 -> 10 -> 
Enter the value of node after which you want to add new element:
30
Enter Value tobe added:
35
The elements of DLL are: 
50 -> 40 -> 30 -> 35 -> 20 -> 10 -> 
```


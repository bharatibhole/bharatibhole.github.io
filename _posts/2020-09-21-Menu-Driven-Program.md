---
layout: post
title: Menu Driven Program
tags: [Programming, Menu Driven Program]
feature-img: "/assets/img/wordcloudbutterfly.jpg"
excerpt: Menu Driven Program helps user to select and execute a particular operation out of multiple operations.
author: BBB
---

# Menu Driven Program

Menu Driven Program helps user to select and execute a particular operation out of multiple operations. 

**Example**

Write a Menu Driven program to perform the Matrix addition, Multiplication and Transpose Operations.

**arrayOper.cpp**

```cpp
#include <iostream>
using namespace std;
int a[2][2]={{1,2},{3,4}};
int b[2][2]={{10,20},{30,40}};
int c[2][2]={{0,0},{0,0}};

void menu();
void perform(int choice);
void transpose();
void addition();
void multiplication();
void displayRes();

void menu()
{
    cout<<"Menu\n";
    cout<<"1. Matrix Addition\n";
    cout<<"2. Matrix Multiplication\n";
    cout<<"3. Matrix Transpose \n";
    cout<<"4. Exit\n";
}

void perform(int choice)
{
    switch (choice)
    { 
    case 1:  
          addition();
          cout<<"Addition of matrices is: \n"; 
          displayRes();
          break; 
    case 2:
          multiplication();
          cout<<"Multiplication of matrices is: \n"; 
          displayRes();  
          break;
    case 3:
          transpose();
          cout<<"Transpose of matrix is: \n";
          displayRes(); 
          break; 
    case 4:
          cout<<"Program terminated \n";exit(0);
    default:
          cout<<"Wrong choice";break;
    } 
}

void transpose()
{
    int i,j;
    for(i=0;i<2;i++)
       {
        for(j=0;j<2;j++)
           {
            c[i][j]=a[j][i];         
           }
       }
}
void addition()
{
        int i,j;
    for(i=0;i<2;i++)
       {
        for(j=0;j<2;j++)
           {
            c[i][j]=a[i][j]+b[i][j];         
           }
       }
}
void multiplication()
{
    
        int i,j,k;
    for(i=0;i<2;i++)
       {
        for(j=0;j<2;j++)
           {  c[i][j]=0; 
      
            for(k=0;k<2;k++)
            c[i][j]=c[i][j]+a[i][k]*b[k][j];         
           }
       }

}
void displayRes()
{
int i,j;
for(i=0;i<2;i++)
       {
        for(j=0;j<2;j++)
           {
            cout<< c[i][j] <<"  ";   
           }
        cout<<"\n";   
       }
}

int main()
{
    int choice=0;
    do
    {
    menu();
    cout<<"Enter Your choice: ";
    cin>>choice;
    perform(choice);
    }while(choice<6);
return 0;    
}    
```

**Output**

```cpp
Menu
1. Matrix Addition
2. Matrix Multiplication
3. Matrix Transpose 
4. Exit
Enter Your choice: 1
Addition of matrices is: 
11  22  
33  44  
Menu
1. Matrix Addition
2. Matrix Multiplication
3. Matrix Transpose 
4. Exit
Enter Your choice: 2
Multiplication of matrices is: 
70  100  
150  220  
Menu
1. Matrix Addition
2. Matrix Multiplication
3. Matrix Transpose 
4. Exit
Enter Your choice: 3
Transpose of matrix is: 
1  3  
2  4  
Menu
1. Matrix Addition
2. Matrix Multiplication
3. Matrix Transpose 
4. Exit
Enter Your choice: 4
Program terminated 
```


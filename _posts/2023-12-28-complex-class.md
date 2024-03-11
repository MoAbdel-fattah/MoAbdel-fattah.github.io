---
layout: post
title: Complex Class
date: 2023-12-28 00:00 +0000
categories: [C++,OOP]
tags: [c++,oop]
---
# Introduction
In this  post, I will explain the basic concepts of Object-Oriented Programming (OOP) in C++ using a simple example of a class that represents complex numbsers. OOP is a programming paradigm that uses objects to model real-world problems. Objects are instances of classes that contain both data and functions.

### OOP has many advantages over procedural programming, such as:
- OOP is faster and easier to execute
- OOP provides a clear structure for the programs
- OOP helps to keep the C++ code DRY "Don't Repeat Yourself", and makes the code easier to maintain, modify and debug
- OOP makes it possible to create full reusable applications with less code and shorter development time
### The main concepts of OOP are:
- Class and Object: A class is a user-defined data type that has data members and member functions, which define the properties and behavior of the objects in that class. An object is an instance of a class that has its own values for the data members and can access the member functions.
- Encapsulation: Encapsulation is the process of binding together the data and the functions that manipulate them in a class, and hiding the implementation details from the outside world. Encapsulation is achieved by using access specifiers such as public and private, which determine the visibility of the data members and member functions.
- Operator Overloading: Operator overloading is a form of polymorphism that allows a user-defined operator to work with different types of operands. Operator overloading is achieved by defining a special function that has the keyword operator followed by the operator symbol.

## The code for the class Complex is as follows:
```c++
#include<iostream> 
using namespace std; 
class Complex {
int real , img ;
public: // declare the public section of the class
Complex(); // declare a default constructor
Complex(int, int); // declare a parameterized constructor
void Display(); // declare a member function named Display to print the complex number
Complex operator+(Complex &); 
// declare an operator overloading function for the + operator
//without this function if we add two complex number we will get error
};
Complex::Complex(){ // define the default constructor
    real=0; // initialize the real part to 0
    img=0; // initialize the imaginary part to 0
}
Complex::Complex(int r,int i) // define the parameterized constructor
{
    real=r; // assign the real part to the first parameter
    img=i; // assign the imaginary part to the second parameter
}
void Complex::Display() // define the Display function
{    
//we but if here because if we make i value (imaginary number) nagitve the output will be +- and that a logic error
char ch; 
if(img>=0) 
// check if the imaginary part is non-negative
//notice! for char we use '' not "" 
 ch='+'; 
else 
 ch='-';
 //if we print the value will appear -- not fix this error use abs() function to get absluote value
cout<<real<<ch<<abs(img)<<"i"<<endl; // print the complex number in the form of real+imgi using the cout object
}
Complex Complex::operator+(Complex &c) 
// define the operator overloading function for the + operator
{
Complex temp; 
// declare a temporary object of the class Complex
temp.real=real+c.real; 
// add the real parts of the current object and the parameter object and assign it to the real part of the temp object
temp.img=img+c.img; 
// add the imaginary parts of the current object and the parameter object and assign it to the imaginary part of the temp object
return temp; 
// return the temp object as the result of the addition
}
int main() {
    Complex c1(5,10);
    Complex c2(6,12); 
    Complex c3; 
    c3=c1+c2;
    c1.Display(); 
    c2.Display();
    cout<<"The addation of pervious complex number : \n" ; 
    c3.Display(); 
    return 0; // return 0 to indicate successful execution
}
```

### The OOP concepts that are used in this code are:
- Class and Object: The class Complex is a user-defined data type that has two data members (real and img) and four member functions (Complex, Display, and operator+). The objects c1, c2, and c3 are instances of the class Complex that have their own values for the data members and can access the member functions using the dot operator (.). For example, the following code creates an object of the class Complex named c1 and initializes it with 5 and 10 using the parameterized constructor:
```c++
Complex c1(5,10);
```
- Encapsulation: The data members real and img are private, which means they can only be accessed by the member functions of the class Complex. The member functions are public, which means they can be accessed by any code that has access to the objects of the class Complex. This way, the data is protected from being modified by external code and the integrity of the object is maintained. For example, the following code prints the complex number in the form of real+imgi using the cout object, but it does not directly access the data members of the object:
```c
c1.Display();
```
- Operator Overloading: The operator+ function is an example of operator overloading that allows the addition of two complex numbers using the + operator. The function takes a reference to another object of the class Complex as a parameter and returns a new object of the class Complex as the result. The function is defined using the keyword operator followed by the operator symbol (+). For example, the following code adds the c1 and c2 objects using the operator overloading function and assigns the result to the c3 object:
```c
c3=c1+c2;
```
# Conclusion
I have explained the basic concepts of OOP in C++ using a simple example of a class that represents complex numbers. I have also explained the code line by line and the OOP concepts that are used in the code. I hope this post was helpful and informative.Thank you for reading!
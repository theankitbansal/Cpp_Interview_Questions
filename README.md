# Cpp_Interview_Questions
Questions asked in interviews.

1. What are the different data types present in C++?

The 4 data types in C++ are given below:

Primitive Datatype(basic datatype). Example- char, short, int, float, long, double, bool, etc.
Derived datatype. Example- array, pointer, etc.
Enumeration. Example- enum
User-defined data types. Example- structure, class, etc.

2. What is the difference between C and C++?

The main difference between C and C++ are provided in the table below:

![Screenshot (961)](https://user-images.githubusercontent.com/81725794/181152964-e84c451a-647e-4453-bb66-e39f24a82a41.png)

3. What are class and object in C++?

A class is a user-defined data type that has data members and member functions. Data members are the data variables and member functions are the functions that are used to perform operations on these variables.

An object is an instance of a class. Since a class is a user-defined data type so an object can also be called a variable of that data type.

A class is defined as-

class A{
private:
 int data;
public:
 void fun(){

 }
};

![image](https://user-images.githubusercontent.com/81725794/181153000-6b12ac87-b1aa-4584-9fc0-59e0725064c4.png)

For example, the following is a class car that can have properties like name, color, etc. and they can have methods like speed().

4. What is the difference between struct and class?

In C++ a structure is the same as a class except for a few differences like security. The difference between struct and class are given below:
![Screenshot (962)](https://user-images.githubusercontent.com/81725794/181153189-7a545532-4c50-49ad-b7ed-1024654becbe.png)

5. What is operator overloading?

Operator Overloading is a very essential element to perform the operations on user-defined data types. By operator overloading we can modify the default meaning to the operators like +, -, *, /, <=, etc. 

For example -

The following code is for adding two complex number using operator overloading-

class complex{
private:
 float r, i;
public:
 complex(float r, float i){
  this->r=r;
  this->i=i;
 }
 complex(){}
 void displaydata(){
  cout<<”real part = “<<r<<endl;
  cout<<”imaginary part = “<<i<<endl;
 }
 complex operator+(complex c){
  return complex(r+c.r, i+c.i);
 }
};
int main(){
complex a(2,3);
complex b(3,4);
complex c=a+b;
c.displaydata();
return 0;
}

6. What is polymorphism in C++?

Polymorphism in simple means having many forms. Its behavior is different in different situations. And this occurs when we have multiple classes that are related to each other by inheritance.

For example, think of a base class called a car that has a method called car brand(). Derived classes of cars could be Mercedes, BMW, Audi - And they also have their own implementation of a cars

The two types of polymorphism in c++ are:

Compile Time Polymorphism
Runtime Polymorphism

![image](https://user-images.githubusercontent.com/81725794/181153251-e0934956-df93-48cf-927b-a5541a77591c.png)

7. Explain constructor in C++

The constructor is a member function that is executed automatically whenever an object is created. Constructors have the same name as the class of which they are members so that compiler knows that the member function is a constructor. And no return type is used for constructors.

Example:

class A{
 private:
  int val;
 public:
  A(int x){             //one argument constructor
   val=x;
  }
  A(){                    //zero argument constructor
  }
}
int main(){
 A a(3);     

 return 0;
}

8. Tell me about virtual function

Virtual function is a member function in the base class that you redefine in a derived class. A virtual function is declared using the virtual keyword. When the function is made virtual, C++ determines which function is to be invoked at the runtime based on the type of the object pointed by the base class pointer.

9. Compare compile time polymorphism and Runtime polymorphism

The main difference between compile-time and runtime polymorphism is provided below:

![Screenshot (963)](https://user-images.githubusercontent.com/81725794/181153435-9af9df17-f72d-49e0-b25f-19f48d32707d.png)

10. What do you know about friend class and friend function?

A friend class can access private, protected, and public members of other classes in which it is declared as friends.

Like friend class, friend function can also access private, protected, and public members. But, Friend functions are not member functions.

For example -

class A{
 private:
  int data_a;
 public:
  A(int x){
   data_a=x;
  }
  friend int fun(A, B);
}
class B{
 private:
  int data_b;
 public:
  A(int x){
   data_b=x;
  }
  friend int fun(A, B);
}
int fun(A a, B b){
 return a.data_a+b.data_b;
}
int main(){
 A a(10);
 B b(20);
 cout<<fun(a,b)<<endl;
 return 0;
}
Here we can access the private data of class A and class B.

11. What are the C++ access specifiers?

In C++ there are the following access specifiers:

Public: All data members and member functions are accessible outside the class.

Protected: All data members and member functions are accessible inside the class and to the derived class.

Private: All data members and member functions are not accessible outside the class.

12. Define inline function

If a function is inline, the compiler places a copy of the code of that function at each point where the function is called at compile time. One of the important advantages of using an inline function is that it eliminates the function calling overhead of a traditional function.

13. What is a reference in C++?

A reference is like a pointer. It is another name of an already existing variable. Once a reference name is initialized with a variable, that variable can be accessed by the variable name or reference name both.

For example-

int x=10;
int &ref=x;           //reference variable

If we change the value of ref it will be reflected in x. Once a reference variable is initialized it cannot refer to any other variable. We can declare an array of pointers but an array of references is not possible.

14. What do you mean by abstraction in C++?

Abstraction is the process of showing the essential details to the user and hiding the details which we don’t want to show to the user or hiding the details which are irrelevant to a particular user.

15. Is deconstructor overloading possible? If yes then explain and if no then why?

No destructor overloading is not possible. Destructors take no arguments, so there’s only one way to destroy an object. That’s the reason destructor overloading is not possible.

16. What do you mean by call by value and call by reference?


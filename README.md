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

8. Tell me abo




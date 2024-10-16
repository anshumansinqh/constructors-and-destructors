# Constructors & Destructors

## Contents
- [Aim](#Aim)
- [Software Used](#Software-used)
- [Theory](#Theory)
  * [Purpose of Constructors](#purpose-of-constructors)
  * [Types of Constructors](#types-of-constructors)
  * [Default Constructor](#default-constructor)
  * [Parameterized Constructor](#parameterized-constructor)
  * [Copy Constructor](#copy-constructor)
  * [Constructor Overloading](#constructor-overloading)
  * [Destructors](#destructors)
- [Algorithms](#Algorithms)
- [Conclusion](#Conclusion)
  
## Aim 
To study Constructors

## Software Used 
VS Code

## Theory

Constructors are special member functions of a class that are automatically invoked when an object of that class is created. They play a crucial role in initializing objects, ensuring that they are set up correctly before they are used. 

### 1. Purpose of Constructors
The primary purpose of a constructor is to initialize an object. When a new object is created, the constructor ensures that the object's member variables are set to appropriate values (either default values or ones provided by the user).

#### Characteristics of Constructors:
- **Same name as the class:** Constructors always have the same name as the class they belong to.
- **No return type:** Unlike regular member functions, constructors do not have a return type, not even `void`.

### 2. Types of Constructors

#### 2.1 Default Constructor
A default constructor is one that takes no parameters. If you do not provide any constructor in your class, the compiler automatically generates a default constructor that initializes the object with default values. However, if any other constructor is defined, the compiler will not provide a default one.

```cpp
class MyClass {
public:
    MyClass() { // Default constructor
        // Initialization code
    }
};
```

### 2.2 Parameterized Constructor
A parameterized constructor takes arguments to initialize the object with specific values provided by the user. This allows the initialization process to be more flexible.

```cpp
class MyClass {
private:
    int x;
public:
    MyClass(int a) { // Parameterized constructor
        x = a;
    }
};
```
### 2.3 Copy Constructor
A copy constructor creates a new object as a copy of an existing object. The compiler provides a default copy constructor, but you can write your own for deep copies.
```cpp
class MyClass {
private:
    int* ptr;
public:
    MyClass(int a) { 
        ptr = new int(a); // Allocating memory
    }

    // Copy constructor
    MyClass(const MyClass &obj) {
        ptr = new int(*obj.ptr); // Deep copy
    }
};
```
### 3. Constructor Overloading
You can define multiple constructors in a class with different parameter lists. This is known as constructor overloading, providing flexibility in object initialization.
```cpp
class MyClass {
public:
    MyClass() { // Default constructor
        // Initialization
    }

    MyClass(int a) { // Parameterized constructor
        // Initialization
    }

    MyClass(int a, int b) { // Another parameterized constructor
        // Initialization
    }
};
```
### 5. Destructors
A destructor is a special member function called when an object is destroyed. It frees resources acquired during the object's lifetime.
```cpp
class MyClass {
public:
    ~MyClass() { // Destructor
        // Code to release resources
    }
};
```
## Conclusion 
In this experiment we learnt how to use constructors and destructors in cpp.



# PPP

---



# Chapter 0 : Notes to the Reader

## 0.1 The structure of this book

- Part I “The basics”

- Part II “Input and Output”

- Part III “Data and Algorithms”

- Part IV “Broadening the View”

- Appendices provide useful informations.

### 0.1.1 General approach

- go back to read.
- don’t take “in one sitting”
- Think by oneself.
- don’t underestimate a simple statement like “This is often useful”
- It’s not perfect tools offered.

### 0.1.2 Drills, exercises, etc.

Two levels of programming practice:

- Drills: A drill is a very simple exercise, you haven’t done the drills, you have not done the book.
- Exercises: Initiative and imagination.

### 0.1.3 What comes after this book?

- you will not be an expert.
- parallel with a real project.
- should learn another programming language.

## 0.2 A philosophy of teaching and learning

UNREAD

## 0.3 Programming and computer science

UNREAD

## 0.4 Creativity and problem solving

UNREAD

## 0.5 Request for feedback

UNREAD

## 0.6 References

UNREAD

---



# Chapter 1: Computer, People, and Programing

UNREAD



---



# Part I  The Basics

# Chapter 2, Hello, World

## 2.1 Programs

Different Thinking between Human and Machine.

## 2.2 The classic first program

```c++
#include "std_lib_facilities.h"
int main()
{
  cout<<"Hello, World!\n";
  return 0;
}
```
| # | | note |
| --- | ---- | :-- |
| String  | "  " | |
| Newline | \n | |
| Standard output stream | Cout | “see-out”, **c**haracter **out**put stream |
| Comment | // | “slash” |
| Make file available | #include |  |
| header or a header file | .h | A header contains definitions of terms |
| start executing program | Main |  |
| Output operator | << | |

- code is for reading — do all you can to make it readable.

- Every C++ program must have a **main** function.
- A function has four parts

| function 4 parts | eg   |
| ---------------- | ---- |
| Return type      | int  |
| Name             | main |
| parameter        | ()   |
| function body    | {}   |

- Main() is called by "the system", we won't use that return value. However on some system (notably Unix/Linux) it can be used to check the program terminated successfully.

## Compilation

- C++ is a compiled language.
- *compiler* translate human-readable to machine can understand.
- What you read and write is called *source code* or *program text*, and what the computer executes is called *executable, object code*, or *machine code*.

| *                    |                           |
| -------------------- | ------------------------- |
| C++ source code file | .cpp  .h                  |
| object code file     | .obj (windows)  .o (Unix) |

> C++ source code -->  C++ compiler  -->  Object code

- Put a semicolon after every expression that doesn’t end with a right curly brace (}).”



## 2.4 Linking

- A program usually consists of several separate parts, often developed by different people. These separate parts (sometimes called translation units) must be compiled and the resulting object code files must be linked together to form an executable program. The program that links such parts together is called a *linker*.

>File1.cpp  -->  C++ compiler  -->  File1.obj
>
>File1.obj  +  ostream.obj --> Linker  --> hello_world.exe

- Object code and executables are not portable among systems.
- Errors found by the compiler are called **compile-time errors**, errors found by the linker are called **link-time errors**, and errors not found until the program is run are called **run-time errors** or **logic errors**.

## 2.5 Programming environments

- Put our source text into the computer and to edit it.
  1. Command-line	// compile and link commands yourself.
  2. IDE // interactive (integrated) development environment

## Drill

- compile and link hello_world.cpp file



# Chapter 3: Objects, Types, and Values

## 3.1 Input

- An **object** is a region of memory with a *type* that specifies what kind of information can be placed in it.

- A named object is called a **variable**

```c++
cout<<"Please enter your first name (followed by 'enter'):\n";	//Such a message is typically called a 'prompt'

string first_name; // first_name is a variable of type string. //This sets aside an area of memory for holding a 'string' of characters and gives it the name 'first_name'.
```

- A statement that introduces a new name into a program and sets aside memory for a variable is called a *definition*.

```c++
cin>> first_name;		//read characters into first_name
```

- **cin** refers to the standard input stream ("see-in" for "char-acter input") defined in the standard library.
- **>>** operator ("get form") specifies where that input goes.

- **cout<<"xxx"<<"xxx";**  combined those tow output operations into a single statement.

```c++
cout<<"first_name"<<"is"<<first_name;
//"first_name" gives us the ten characters
// first_name  gives us the value of the variable first_name.
```

## 3.2 Variables

- The "places" in which we store data are called **objects**. To access an object we need a **name**. A named object is called a **variable** and has a specific **type**.

- The data items we put into variables are called **values**

| Types  | Means                  | e.g.       |
| ------ | ---------------------- | ---------- |
| int    | integers               | 55         |
| double | floating-point numbers | 2.5        |
| char   | individual characters  | '.'        |
| string | character strings      | "Chenlola" |
| boll   | Logical variables      | true       |



## 3.3 Input and type

| Operation |            |
| --------- | ---------- |
| >>        | "Get from" |

```c++
cin>>first_name;
cin>>age;
// type in: Carlos 22  the >> operator will read Carlos into first_name, 22 into age.
```

- by convention, reading of strings is terminated by what is called *whitespace*, that is, space, newline, and tab characters. Otherwise, whitespace by default is ignored by >>. 

```c++
$              22 chenlola				//white space before is ignored.
$ your name is : 22 
$ your age is : 0
```

- A **string** read using **>>** is (by default) terminated by whitespace;



## 3.4 Operations and operators

| *                     | bool | char | int  | double | string |
| --------------------- | ---- | ---- | ---- | ------ | ------ |
| assignment            | =    | =    | =    | =      | =      |
| addition              |      |      | +    | +      | +      |
| concatenation         |      |      |      |        | +      |
| Subtraction           |      |      | -    | -      |        |
| Multiplication        |      |      | *    | *      |        |
| Division              |      |      | /    | /      |        |
| Remainder(modulo)     |      |      | %    |        |        |
| increment by 1        |      |      | ++   | ++     |        |
| decrement by 1        |      |      | --   | --     |        |
| increment by n        |      |      | +=n  | -=n    |        |
| add to end            |      |      |      |        | +=     |
| decrement by n        |      |      | -=n  | -=n    |        |
| Multiply and assign   |      |      | *=   | *=     |        |
| divide and sssign     |      |      | /=   | /=     |        |
| remainder and assign  |      |      | %=   |        |        |
| Read from s into x    | s>>x | s>>x | s>>x | s>>x   | s>>x   |
| Write x to s          | s<<x | s<<x | s<<x | s<<x   | s<<x   |
| Equals                | ==   | ==   | ==   | ==     | ==     |
| not equal             | !=   | !=   | !=   | !=     | !=     |
| greater than          | >    | >    | >    | >      | >      |
| greater than or equal | >=   | >=   | >=   | >=     | >=     |
| Less than             | <    | <    | <    | <      | <      |
| less than or equal    | <=   | <=   | <=   | <=     | <=     |

> A blank square indicates that an operation is not directly availablefor a type 

Two string compare is the first letter of Alphabetically-Comaring.

`"azzz" > "zaaa"`  :  `True`

## 3.5 Assignment and initialization

- `=` is assignment operator.

- Initialization

- Assignment


## 3.6 Composite assignment operators

```C++
++number
number = number + 1
a += 5
b -= 2
c *= 4
d /= 3
```

## 3.7

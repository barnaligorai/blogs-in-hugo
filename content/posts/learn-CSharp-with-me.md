---
title: "Learn C# With Me"
date: 2022-10-07T10:42:46+05:30
draft: true
tags: 
  - tech
---

### C# and .NET
  
  C# is a programming language, while .NET is a framework. It consists of a run-time environment (CLR) and a class library that we use for building applications.

### CLR
  
  C# compiler compiles the code to Intermediate Language(IL) code. IL code is platform independent like Byte code(Java). To run C# program on a different computer with different hardware architecture and operating system, we need CLR. CLR compiles the IL code into the native machine code for the computer on which it is running. This process is called Just-In-Time(JIT).


### Architecture of .NET Applications
  - Class :
    - An application in C# consists of building blocks called *classes*.
    - A class consists of *attributes* and *methods*.
  - Namespace :
    A *namespace* is a container for related classes.
  - Assembly :
    - An *assembly* is a container for related namespaces.
    - An assembly is a file (EXE / DLL) that contains one or more namespaces and classes.
    - An *EXE* file represents a program that can be executed.
    - A *DLL* is a file that includes code that can be reused accross different programs.
    

### Getting Started

  - Download the '.NET SDK'
  - Create a new console app and goto app directory
  ```sh
   dotnet new console -o app
   cd app
  ```
  - Build the app
  ```sh
  dotnet build
  ```
  - Write your program in Program.cs
  ```cs
  Console.WriteLine("Hello, World!");
  ```
  - Run your program
  ```sh
  dotnet run
  ```


### Types

*Value* types and *Reference* types are the two main categories of C# types.
  - A variable of a value type contains an instance of the type. 
  - A variable of a reference type contains a reference to an instance of the type.
    - Value Type : primitive types, custom structures
    - Reference Type : Array, String, custom classes

Then there is also premitive and non-primitive types.
  - Primitive : byte, short, int, long, char, float, double, bool
  - Non-Primitive : class, struct, array, string, enum


### Expressions And Statements

  #### Operator :
  Expressions are constructed from operands and operators.

  C# provides operators to perform arithmetic, logical, bitwise, shift operations, equality and order comparisons.

  Examples of operators include + , - , * , /, % etc.
  Examples of operands include literals, fields, local variables,and expressions.
  
  - When an expression contains multiple operators, the precedence of the operators controls the order in which the individual operators are evaluated.
    - For example : 
      x + y * z + a, first multiplies y by z and then adds the result to x and then adds to a

  - Except for the assignment and null-coalescing operators, all binary operators are left-associative, meaning that operations are performed from left to right.
    - For example :
      x + y + z is evaluated as (x + y) + z .
  
  - The assignment operators, the null-coalescing '??' and '??=' operators, and the conditional operator '?:' are right-associative, meaning that operations are performed from right to left.
    - For example : 
      x = y = z is evaluated as x = (y = z) .
  
  - Precedenceand associativity can becontrolled using parentheses.   
    - For example : 
     (x + y) * z, first adds x and y and then multiplies the result by z .

  #### Statement :

  - if statement :
  ```cs
  int number = 5;
  if (number == 5) { 
    Console.WriteLine("Number is equal to 5");
  }
  else if (number < 5) {
    Console.WriteLine("Number is lesser than 5");
  }
  else {
    Console.WriteLine("Number is greater than 5");
  }
  ```
  - switch statement :
  ```cs
  int number = 5;
  switch (number)
  {
    case 5: 
      Console.WriteLine("Number is 5");
      break;
    default:
      Console.WriteLine("Number is not 5");
      break;
  }
  ```

  #### Iteration Statements

  - while loop :
  ```cs
  int number = 0;
  while(number < 5) {
    Console.WriteLine(number++);
  }
  ```
  - do-while loop :
  ```cs
  int number = 0;
  do {
    Console.WriteLine(number++);
  } while(number < 5);
  ```

  - for loop :
  ```cs
  for (int number = 0; number < 5; number++)
  {
    Console.WriteLine(number);
  }
  ```

  - foreach :
  ```cs
  string name = "Roshan";
  foreach (var character in name)
  {
    Console.WriteLine(character);
  }
  ```

  - random :
   ```cs
   var random = new Random();
  for (int index = 0; index < 5; index++)
  {
    Console.WriteLine((char)('a' + random.Next(0, 26)));
  }
  ```


### Array

C# supports :
  - Single-dimensional array
  - Multi-dimensional arrays 
    - Rectangular array
    - Jagged array

```cs
int[] a1 = new int[10]; // single dimensional
int[,] a2 = new int[10, 5]; // two dimensional
int[,,] a3 = new int[10, 5, 2]; // three dimensional 
```
```cs
int[,] rectangularArray = new int[3, 4]; // rectangular

int[][] jaggedArray = new int[3][]; // jagged
jaggedArray[0] = new int[10];
jaggedArray[1] = new int[5];
jaggedArray[2] = new int[20];
```

Array methods :
  - Length
  - IndexOf
  - Clear
  - Sort
  - Reverse
  - Copy
```cs
int[] numbers = new int[] {10,30,25};
Console.WriteLine(numbers.Length); // 3

Console.WriteLine(Array.IndexOf(numbers, 30)); // 1

// clears 1 value in number from index 0
Array.Clear(numbers, 0, 1);
Console.WriteLine(numbers[0]); // 0

// sorts in ascending order and modifies the original array
Array.Sort(numbers);

// reverses numbers and modifies the original array
Array.Reverse(numbers);

int[] another = new int[3];
// Copies 3 values of numbers in another
Array.Copy(numbers, another, 3);
```

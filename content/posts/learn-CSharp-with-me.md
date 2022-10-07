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

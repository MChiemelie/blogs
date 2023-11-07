---
title: "JavaScript: Demystifying Key Features and Characteristics"
seoTitle: "JavaScript: Demystifying Key Features and Characteristics"
seoDescription: "In this article, we take a deep dive into the technicalities and principles of JavaScript. This article discusses the key characteristics of JavaScript."
datePublished: Tue Nov 07 2023 12:16:18 GMT+0000 (Coordinated Universal Time)
cuid: clooap4js000509jr4u8t9zj2
slug: javascript-deep-dive
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699358960392/3e56dd08-fc0c-4ef2-bf38-7804b82b898b.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1699359220250/66d72ac1-6f18-4cc5-bbf8-0358735dea3f.png
tags: javascript, deep-dive, intermediate-javascript

---

It's important for developers and programmers working with JavaScript to understand the inner workings of the language. Every programming language operates uniquely. The structure and level of abstraction in a programming language influence how it gets processed and converted into machine code, how it's executed, and where it can be used.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699219142966/d72b4c31-829c-4127-83c1-c03ebbf8cb76.jpeg align="center")

JavaScript is often described as ***a high-level, single-threaded, garbage-collected, interpreted, or just-in-time compiled, prototype-based, multi-paradigm, dynamic language with a non-blocking event loop***. We will discuss each of these characteristics of JavaScript with practical examples.

## High-Level Language

As a high-level programming language, JavaScript code is more readable and comprehendible to humans than machine binary code which is written in `1s` and `0s`.

It provides higher ***abstraction*** from the computer hardware and operating system. As a developer, you don't have to interact and worry about memory management, memory addresses, registers, and call stacks.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699207070431/c05b7004-db6a-45d5-ac21-ff4afad906cd.webp align="center")

Its primary emphasis is enhancing usability rather than striving for optimal program efficiency.

## Single-Threaded Language

A thread is an independent unit capable of executing code. JavaScript was designed as a single-threaded language, meaning it operates with only one such unit for executing code. It executes tasks sequentially, one at a time.

In the browser, the main thread is used by the browser to handle user events such as clicking, rendering, and painting the display and to run the majority of code that runs on a typical website.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697737678387/6884746d-4aa4-49d5-85ef-38aa19fe5086.png align="center")

Due to JavaScript using one thread to perform one task at a time, this can cause slow and low-performance issues.

Modern JavaScript offers ways to create additional threads, each executing independently while communicating with one another using web workers. Slow, complex, and long-running processes complex can be taken off from the main thread which increases the performance.

## Garbage-collected

JavaScript manages memory through ***garbage collection*** - the automatic process of freeing up memory that the program no longer uses.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697750298405/046e5b94-22aa-44b7-85e0-0d3133e46e9a.webp align="center")

Because JavaScript is interpreted and a high-level language, it does not enjoy direct access to the computer’s memory. Instead, it relies on the browser’s memory management system to allocate and deallocate memory.

It uses a method called “***mark-and-sweep***” to identify objects in memory that are no longer needed by “marking” them and then “sweeping” them away.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699217222648/3760852b-8970-465a-961e-42ed56931b54.jpeg align="center")

JavaScript creates variables, arrays, functions, and objects in memory as it runs. However, it still uses the stack and the heap to store data. The below table shows how data is saved in both the stack and heap.

|  | Stack | Heap |
| --- | --- | --- |
| **Primitive vs Non Primitive** | Holds primitive values and references | Holds non-Primitive values |
| **Data Types** | Stores strings, numbers, booleans, undefined, and null | Stores objects and functions |
| **Size** | Size is known at compile time | Size is known at runtime |
| **Memory Allocation** | **Static Memory Allocation:** The engine allocates a fixed amount of memory for these values | **Dynamic Memory Allocation:** The engine allocates memory as needed. |

## Interpreted language / Just-In-Time Complied

Interpreting JavaScript code involves a multi-step process that transforms human-readable code into machine-executable instructions. JavaScript is typically not compiled directly into machine code but rather interpreted by a JavaScript engine, which executes the code line by line. Here's an expository explanation of how this interpretation process works and how it eventually reaches machine code:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697750697966/acebd0c1-f2c1-4cca-8b44-2e08f2f4b9fd.webp align="center")

1. The source code is first broken down into smaller units called tokens. These tokens represent keywords, identifiers, operators, and other language elements.
    
    Once tokenized, the JavaScript engine constructs an Abstract Syntax Tree (AST). The AST is a hierarchical representation of the code's structure, showing how different parts of the code relate to each other.
    
2. The JavaScript engine parses the AST to determine the syntactical correctness of the code. It checks if the code adheres to the rules and grammar of the JavaScript language. If there are syntax errors, the engine will report them at this stage.
    
3. Before the code starts running, the JavaScript engine creates an execution context. This context includes a global context and can have multiple local contexts, each associated with a specific function or block of code. These contexts manage variable scopes and function calls.
    

JavaScript was not initially designed as a compiled language, but modern browser engines like the V8 engine and other browser engines compile JavaScript to gain additional capabilities and improve performance.

## Prototype-Based Language

JavaScript uses a prototype-based inheritance model. This means that instead of classes, objects are created directly from other objects, serving as prototypes.  
*Everything* in Javascript is an object, and each object holds a link to its prototype. This creates a prototype chain where objects can *inherit* values and behaviours from other objects. This unique approach allows for flexible and dynamic object creation.

```javascript
// Creating a constructor function
function Person(name, age) {
  this.name = name;
  this.age = age;
}

// Adding a method to the Person prototype
Person.prototype.sayHello = function() {
  console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
};

// Creating instances of the Person object
const person1 = new Person('Alice', 30);
const person2 = new Person('Bob', 25);

// Calling the sayHello method on the instances
person1.sayHello(); // Output: Hello, my name is Alice and I am 30 years old.
person2.sayHello(); // Output: Hello, my name is Bob and I am 25 years old.
```

## Multi-Paradigm Language

JavaScript is a multi-paradigm language that supports various programming styles like procedural, object-oriented, and functional programming. This flexibility empowers developers to select the most suitable approach for a particular task, making JavaScript well-suited for various applications.

Procedural programming is focused on giving explicit instructions to the computer, often using loops and conditional statements.

```javascript
// Procedural approach to find the sum of an array
function sumArray(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
}

const numbers = [1, 2, 3, 4, 5];
console.log("Sum of the array:", sumArray(numbers));
```

Functional programming emphasizes the use of pure functions and avoiding mutable states.

```javascript
// Functional approach to find the sum of an array using reduce()
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
console.log("Sum of the array:", sum);
```

JavaScript supports object-oriented programming. This paradigm of programming is based on creating and working with objects and classes.

```javascript
// Object-Oriented Programming in JavaScript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}

const person1 = new Person("Alice", 30);
person1.sayHello();
```

## Dynamic Typed Language

JavaScript is a dynamically typed language, which means that variable types are determined at runtime rather than at compile time.

```javascript
let name = "Josephine"; // this is a declared a string
let age = 22; // this is a declared a number
let married = true; // this is a declared a boolean
let friends = ["Promise", "Mercy", "Dorcas", "Victoria"] // this is a declared an array
```

This dynamic nature provides flexibility but can potentially lead to runtime errors if not carefully managed.

```javascript
let a = 5; // decalared as a number
let b = "10"; // decalared as a string
let result = a + b; // JavaScript performs type coercion and treats 'a' as a string, resulting in "510"

console.log(result); // Outputs "510"
```

## Non-Blocking Event Loop

JavaScript was designed as a single-threaded language, meaning it has only one main thread of execution. However, JavaScript incorporates a non-blocking event loop mechanism that allows for asynchronous programming. This event loop allows JavaScript to handle tasks such as I/O operations, network requests, and timers without blocking the main thread, which would otherwise make applications unresponsive.

```javascript
const button = document.getElementById("myButton");

button.addEventListener("click", function () {
  console.log("Button clicked");
});

console.log("Event listener registered");
```

In the below code, an event listener is registered for a button-click event. "Event listener registered" will be logged immediately, and when the button is clicked, "Button clicked" will be logged. JavaScript's event loop handles event-driven programming by waiting for and responding to events.

### Conclusion

In this blog post, we've explored the key concepts that define JavaScript as a high-level, single-threaded, garbage-collected, interpreted (or just-in-time compiled), prototype-based, multi-paradigm, dynamic language with a non-blocking event loop. Understanding these concepts is essential for any developer looking to harness the full power of JavaScript in web development. JavaScript's unique combination of features and paradigms makes it a versatile and indispensable tool for creating dynamic and interactive web applications.

If you found this blog post helpful, please consider sharing it with others who might benefit. You can also follow me for more content on Javascript, React.js, Next.js and other web development topics.

To sponsor my work, please visit: [**Chiemelie's Sponsor Page**](https://chiemelie.hashnode.dev/sponsor) and explore the various sponsorship options.

Connect with me on [**X (Twitter)**](https://twitter.com/ChiemelieJM), [**LinkedIn**](https://www.linkedin.com/in/melikamchiemelie/), and [**GitHub**](https://github.com/MChiemelie).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697702819130/c72d4abf-3dd1-44f3-9607-d69dc5e697e5.png align="center")

.
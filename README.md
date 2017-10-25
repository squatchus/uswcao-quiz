# uswcao-quiz
This repository contains set of questions for a self-check based on the book "Using Swift with Cocoa and Objective-C (Swift 3 beta)".

## Table of Contents
* [Getting Started](../master/README.md#getting-started)
* [- Basic Setup](../master/README.md#basic-setup)
* [- Understanding the Swift Import Process](../master/README.md#simple-values)
* [Interoperability](../master/README.md#interoperability)
* [- Initialization](../master/README.md#initialization)

## Getting Started

### Basic Setup

1. What is the minimum deployment target for an app made with Swift 3.0/Xcode 8?
   <details> 
   <summary>Answer:</summary>
  
   iOS 7 or OS X 10.9. Setting an earlier deployment target results in a build failure.
   </details>
2. Does Swift executables built from the command line have the runtime statically linked?
   <details> 
   <summary>Answer:</summary>
  
   No, if you plan to ship a Swift executable built from the command line, you'll need to ship the Swift dynamic libraries as well.
   </details>

### Understanding the Swift Import Process

3. Which Objective-C frameworks and C libraries can be imported into Swift and how?
   <details> 
   <summary>Answer:</summary>
  
   Any framework or library that supports _modules_ can be imported. This includes all of the Objective-C system frameworks. It can be imported simply by adding import statement to top of the file:
   ```Swift
   import Foundation
   ```
   </details>
4. How to import C++ code into Swift?
   <details> 
   <summary>Answer:</summary>
  
   It isn't possible to import C++ code directly into Swift. Instead you need to create an Objective-C or C wrapper for C++ code.
   </details>

## Interoperability

### Initialization

5. Let's say you have an Objective-C class **Person** with initializer listed in a code below. This class imported into Swift code. How do you instantiate this **Person** in Swift?
   ```Objective-C
   - (instancetype)initWithName:(NSString *)name age:(NSInteger)age;
   ```
   <details> 
   <summary>Answer:</summary>
  
   ```Swift
   let bob: Person = Person(name: "Bob Novado", age: 40)
   // or you can omit the type and let Swift to infer it
   let bob = Person(name: "Bob Novado", age: 40)    
   ```
   </details>
6. How does Objective-C class factory methods imported into Swift?
   <details> 
   <summary>Answer:</summary>
  
   They imported as convinience initializers, like:
   ```Swift
   let color = UIColor(red: 0.5, green: 0.5, blue: 0.5, alpha: 0.5)
   // instead of [UIColor colorWithRed:0.5 green:0.5 blue:0.5 alpha:0.5]
   ```
   </details>

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

<details> 
  <summary>1. What is the minimum deployment target for an app made with Swift 3.0/Xcode 8?</summary>
  
  iOS 7 or OS X 10.9. Setting an earlier deployment target results in a build failure.
</details>

<details> 
  <summary>2. Does Swift executables built from the command line have the runtime statically linked?</summary>
  
  No, if you plan to ship a Swift executable built from the command line, you'll need to ship the Swift dynamic libraries as well.
</details>

### Understanding the Swift Import Process

<details> 
  <summary>3. Which Objective-C frameworks and C libraries can be imported into Swift and how?</summary>
  
  Any framework or library that supports _modules_ can be imported. This includes all of the Objective-C system frameworks. It can be imported simply by adding import statement to top of the file:
```Swift
import Foundation
```
</details>

<details> 
  <summary>4. How to import C++ code into Swift?</summary>
  
  It isn't possible to import C++ code directly into Swift. Instead you need to create an Objective-C or C wrapper for C++ code.
</details>

## Interoperability

### Initialization

<details> 
  <summary>5. Let's say you have an Objective-C class **Person** with initializer listed in a code below. This class imported into Swift code. How do you instantiate this **Person** in Swift?
```Objective-C
- (instancetype)initWithName:(NSString *)name age:(NSInteger)age;
```
  </summary>
  
```Swift
let bob: Person = Person(name: "Bob Novado", age: 40)
```
</details>

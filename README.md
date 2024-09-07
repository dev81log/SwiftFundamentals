# Swift Fundamentals

A comprehensive guide to getting started with the Swift programming language. This resource provides a detailed introduction to the fundamentals of Swift, covering basic syntax, key concepts, and practical examples to help beginners understand and start coding in Swift effectively.

# Swift Introduction Guide

## 1. Introduction to Swift

Swift is a powerful and intuitive programming language developed by Apple to create apps for iOS, macOS, watchOS, and tvOS. It combines simplicity and efficiency, making it ideal for beginners and experienced developers alike.

### 1.1 First Steps: Variables and Constants

In Swift, you can store values using variables and constants. Variables are defined with the `var` keyword and can have their values changed throughout the program. Constants are defined with the `let` keyword and cannot be changed after they are defined.

```swift
var myVariable = 42
myVariable = 50
let myConstant = 42
```

## 2. Data Types in Swift

Swift is a strongly typed language, meaning that each variable or constant must have a specific data type, such as `Int` for integers, `Double` for decimal numbers, `Bool` for boolean values, and `String` for text.

### 2.1 Data Type Examples

```swift
let name: String = "Lucas"
let age: Int = 25
let weight: Double = 1.70
let isStudent: Bool = true
```

### 2.2 Challenge: Converting Data Types

#### Challenge 1:
Create a program to convert a `String` in the format `"true"` to a Boolean value (`Bool`).

```swift
let booleanString = "true"
let booleanConverted = Bool(booleanString)
print(booleanConverted) // Output: true
```

#### Challenge 2:
Convert a decimal number (`Double`) to an integer (`Int`).

```swift
let decimalNumber: Double = 20.1
let integerNumber: Int = Int(decimalNumber)
print(integerNumber) // Output: 20
```

## 3. Operators in Swift

Operators are used to perform operations on variables and constants. Swift offers a variety of operators, including arithmetic, comparison, and logical.

### 3.1 Arithmetic and Logical Operators

```swift
var x = 10
x += 1 // x is now 11
x -= 1 // x is now 10
x *= 2 // x is now 20
x /= 2 // x is now 10

let y = 10
let isEqual = y == 10 // true
let isGreaterThan = y > 5 // true
let isTrue = true
let isFalse = false

isTrue && isFalse // false
isTrue || isFalse // true
!isTrue // false
```

### 3.2 Challenge: Working with Logical Operators

1. Compare the equality of two `Strings`.
2. Check if a person can drive based on their age.
3. Invert the logic to check if the person CANNOT drive.
4. Check if the person is a driver OR is 17 years old or older.
5. Check if the person is a driver AND over 30 years old.

```swift
let stringA = "Lucas"
let stringB = "Lucas"
let isEqual = stringA == stringB
print(isEqual) // true

let age = 18
let canDrive = age >= 18
print(canDrive) // true

let cannotDrive = age < 18
print(cannotDrive) // false

let isDriver = true
let isAdult = age >= 17
let canDriveOrIsAdult = isDriver || isAdult
print(canDriveOrIsAdult) // true

let isOlderDriver = isDriver && age > 30
print(isOlderDriver) // false
```

## 4. Flow Control

Swift allows you to control the flow of execution of your program using conditionals and loops.

### 4.1 Conditionals: `if`, `else`, `switch`

```swift
let temperature = 30

if temperature > 25 {
  print("It's hot outside!")
} else {
  print("It's cold outside!")
}

let dayOfWeek = "Monday"

switch dayOfWeek {
case "Monday":
  print("Start of the week.")
case "Friday":
  print("End of the week.")
default:
  print("Another day of the week.")
}
```

### 4.2 Loops: `for`, `while`

```swift
for i in 1...5 {
  print(i)
}

var counter = 5
while counter > 0 {
  print(counter)
  counter -= 1
}
```

### 4.3 Challenge: Applying Flow Control

Create a loop that counts from 1 to 10 and, for each number, check if it's even or odd.

```swift
for i in 1...10 {
  if i % 2 == 0 {
    print("\(i) is even")
  } else {
    print("\(i) is odd")
  }
}
```

## 5. Functions and Scope

Functions are blocks of code that perform specific tasks. In Swift, you can declare and use functions to organize and reuse your code.

### 5.1 Function Declaration and Usage

```swift
func greet(name: String) -> String {
  return "Hello, \(name)!"
}

let greeting = greet(name: "Lucas")
print(greeting) // Output: Hello, Lucas!
```

### 5.2 Variable Scope

Variables declared inside a function are local and cannot be accessed outside of it.

```swift
func calculateSum(a: Int, b: Int) -> Int {
  let sum = a + b
  return sum
}

let result = calculateSum(a: 5, b: 10)
print(result) // Output: 15
```

### 5.3 Challenge: Creating Custom Functions

Create a function that takes a number as a parameter and returns whether it's even or odd.

```swift
func isEven(number: Int) -> Bool {
  return number % 2 == 0
}

let number = 4
let result = isEven(number: number)
print(result) // Output: true
```

## 6. Collections in Swift

Swift offers three main types of collections: Arrays, Dictionaries, and Sets.

### 6.1 Arrays

```swift
var fruits = ["Apple", "Banana", "Orange"]
fruits.append("Mango")
print(fruits) // Output: ["Apple", "Banana", "Orange", "Mango"]
```

### 6.2 Dictionaries

```swift
var carPrices = ["Toyota": 20000, "BMW": 35000, "Audi": 40000]
carPrices["Mercedes"] = 45000
print(carPrices) // Output: ["Toyota": 20000, "BMW": 35000, "Audi": 40000, "Mercedes": 45000]
```

### 6.3 Sets

```swift
var uniqueNumbers: Set = [1, 2, 3, 4, 5]
uniqueNumbers.insert(6)
print(uniqueNumbers) // Output: [1, 2, 3, 4, 5, 6]
```

### 6.4 Challenge: Collection Manipulation

1. Create an array of integers and sum all the elements.
2. Create a dictionary to store names and ages, and then find the age of a specific name.

```swift
let numbers = [1, 2, 3, 4, 5]
let sum = numbers.reduce(0, +)
print(sum) // Output: 15

let people = ["Lucas": 25, "Mariana": 30, "Pedro": 22]
if let age = people["Mariana"] {
  print(age) // Output: 30
}
```

## 8. Optionals

Optionals in Swift are used to represent values that may be absent. An optional is a variable that can hold either a value or `nil`.

### 8.1 Declaring Optionals

```swift
var optionalString: String? = "Hello"
```

### 8.2 Unwrapping Optionals

To access the value of an optional, you can "unwrap" it using `if let` or `guard let`.

```swift
if let unwrappedString = optionalString {
  print(unwrappedString) // Output: Hello
} else {
  print("optionalString is nil")
}
```

Another way is to use the `!` operator, but this should be done with caution as it can cause errors if the optional is `nil`.

```swift
print(optionalString!) // Force Unwrapping (Use with Caution)
```

## 9. Classes and Inheritance

Swift also supports object-oriented programming with classes. Classes, unlike structs, support inheritance.

### 9.1 Declaring Classes

```swift
class Animal {
  var name: String

  init(name: String) {
    self.name = name
  }

  func makeSound() -> String {
    return "Some sound"
  }
}

let dog = Animal(name: "Dog")
print(dog.name) // Output: Dog
```

### 9.2 Inheritance

A class can inherit properties and methods from another class.

```swift
class Dog: Animal {
  override func makeSound() -> String {
    return "Woof"
  }
}

let dog = Dog(name: "Dog")
print(dog.makeSound()) // Output: Woof
```

## 10. Protocols

Protocols in Swift define a "contract" or set of methods and properties that a class or struct must implement.

### 10.1 Declaring Protocols

```swift
protocol Greetable {
  func greet() -> String
}

class Person: Greetable {
  var name: String

  init(name: String) {
    self.name = name
  }

  func greet() -> String {
    return "Hello, \(name)"
  }
}

let person = Person(name: "Lucas")
print(person.greet()) // Output: Hello, Lucas
```

## 11. Enumerations (Enums)

Enums in Swift are types that allow you to work with values defined in a closed set.

### 11.1 Declaring Enums

```swift
enum Direction {
  case north
  case south
  case east
  case west
}

var direction = Direction.north
direction = .east
```

### 11.2 Enums with Associated Values

Enums can also store associated values.

```swift
enum Barcode {
  case upc(Int, Int, Int, Int)
  case qrCode(String)
}

var productBarcode = Barcode.upc(8, 85909, 51226, 3)
productBarcode = .qrCode("ABCDEFGHIJKLMNOP")
```

## 12. Extensions

Extensions allow you to add new functionality to an existing type, such as a struct, class, or primitive type, without the need to modify the original code.

### 12.1 Creating an Extension

```swift
extension String {
  func reversed() -> String {
    return String(self.reversed())
  }
}

let greeting = "Hello"
print(greeting.reversed()) // Output: "olleH"
```

## 13. Conclusion

In this guide, we covered the basics and advanced concepts of Swift, including variables, constants, data types, operators, flow control, functions, collections, structs, optionals, classes, inheritance, protocols, enums, and extensions. With this knowledge, you are well-equipped to continue exploring Swift and develop robust apps for the Apple platform.

### Next Steps in Learning Swift

- Explore iOS frameworks like UIKit and SwiftUI.
- Learn about object-oriented programming in Swift.
- Create practical projects to solidify your learning.

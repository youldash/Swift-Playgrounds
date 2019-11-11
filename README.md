# Swift Playgrounds
 Supplementary material for the Designing and Developing iOS Apps Course on KKUx.

Brought to you by:
<div align="center"><img src="https://raw.github.com/youldash/https://github.com/youldash/Swift-Playgrounds/master/misc/kkux.png" width="50%" /></div>

[![Twitter Follow](https://img.shields.io/twitter/follow/youldash.svg?style=social?style=plastic)](https://twitter.com/youldash)
[![Twitter Follow](https://img.shields.io/twitter/follow/kkuxedu.svg?style=social?style=plastic)](https://twitter.com/kkuxedu)
[![Twitter Follow](https://img.shields.io/twitter/follow/IAU_CCSIT.svg?style=social?style=plastic)](https://twitter.com/IAU_CCSIT)

## Swift 5 Comprehensive Cheat Sheet and Quick Reference

This part of the course is designed to assist you in getting up-to-speed with Swift. More importantly, we believe that it is vita for you (*i.e.* if you are a complete beginner to Swift) to develop an understanding of the selected topics, and gain an insight into the core fundamentals of the language using the various code segments enlisted herein.

### How to use This Reference

As you go through each topic you will see that they are published in a specific order, starting with **Language Basics**, **Strings**, ..., and so forth. To gain maximum benefit (especially if you are a complete newbie to Swift) we encourage you to go though each listing (*i.e.* the code segments) under each topic and try to type the code rather than copying and pasting each code block [using the latest release of Xcode in the App Store](https://itunes.apple.com/au/app/xcode/id497799835?mt=12).

In Xcode there is a superb feature called **Playgrounds**. A playground, in simple terms, is an designated area where people (normally kids) can play. in Xcode, playgrounds look similar to the following screenshot:

![Screenshot](https://raw.github.com/youldash/Swift-Playgrounds/master/misc/cheatsheet.png)

Because the topics covered herein concentrate on the basic elements of the language itself, building an app (or Xcode project if you will) within each topic isn't very practical. As such, we will rely on playgrounds as a suitable means to explore the various features of Swift.

### Learning Outcomes

By the end of this part you will be able to:

* Develop an understanding of the important key-elements in Swift (which are not limited to the ideas covered herein).
* Distinguish between Swift and other Object-oriented programming languages like Java, and Objective-C (which predated Swift as the preferred language of choice for iOS app development).
* Explore Swift Playgrounds and explore their hidden gyms.
* Start building blocks of code in your iOS apps, with confidence!

## Outline

* [Section 1: Language Basics](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#language-basics).
* [Section 2: Strings](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#strings).
* [Section 3: Basic Control Structures](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#basic-control-structures).
* [Section 4: Tuples](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#tuples).
* [Section 5: Arrays](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#arrays).
* [Section 6: Dictionaries](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#dictionaries).
* [Section 7: Sets](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#sets).
* [Section 8: Optionals](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#optionals).
* [Section 9: Implicitly Unwrapped Optionals](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#implicitly-unwrapped-optionals).
* [Section 10: Enumerations](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#enumerations-aka-enums).
* [Section 11: Switch](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#switch).
* [Section 12: Functions](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#functionsmethods).
* [Section 13: Closures](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#closures).
* [Section 14: Classes and Protocols](https://github.com/youldash/Swift-Playgrounds/tree/master/cheatsheet#classes-and-protocols).

> Code listings were last checked using Xcode 9.4.1 (9F2000) on June 26, 2018.

### Language Basics

#### Listing 1.1

``` Swift
/*
 In Swift, you can use the underscore as a thousands separator.
 */
let trillion = 1_000_000_000_000 // i.e. a million million (1,000,000,000,000 or 10^2).
```

#### Listing 1.2

``` Swift
/// Variables can be updated.
var variableNumber: Int = 1
variableNumber = variableNumber + 1

/// Constants cannot be updated.
let constNumber: Int = 1
// constNumber = constNumber + 1 <- error!

/// Inferred type.
let inferredInt = 1
```

#### Listing 1.3

``` Swift
/// Swift types.
let int: Int = 20
let double: Double = 3.5
let float: Float = 4.5
let bool: Bool = false
var str: String = "Hello, Swift!"
```

#### Listing 1.4

``` Swift
/// Explicit type conversion.
let pi = 3.1415
let multiplier = 2
let twoPi = pi * Double(multiplier)
```

### Strings

#### Listing 2.1

``` Swift
var 🤓 = "Geek"
var 👨🏼‍💼 = "فلان"
var combinedString = "\(🤓) says مرحباً to \(👨🏼‍💼)!"
var tipString = "2499"
var tipInt = Int(tipString) // Casting.
```

#### Listing 2.2

``` Swift
tipString = "24.99"
var tipDouble = Double(tipString)
```

#### Listing 2.3

``` Swift
/// String API.
var string: String! = "Hello, Swift!"
string = string.lowercased(); print(string)

/* You can check any optional type using an if statement. */
if string != nil {
    string = string.lowercased(); print(string)
}
```

#### Listing 2.4

``` Swift
/// String API.
var greeting: String = "hello, world".capitalized
var alternateGreeting = greeting

alternateGreeting += " and beyond!"
print(alternateGreeting)

greeting.append(Character("!"))
print(greeting + "\n")
```

### Basic Control Structures

#### Listing 3.1

``` Swift
for _ in 1..<3 {
    // Loops with index taking values 1,2.
}

for _ in 1...3 {
    // Loops with index taking values 1,2,3.
}

for _ in stride(from: 10, through: 20, by: 2) {
    // Loops from 10 to 20 (inclusive) in steps of 2.
}
```

#### Listing 3.2

``` Swift
var index = 0
while index < 5 {
    // Loops 5 times.
    index += 1 // ++
}

index = 0
repeat { // Loops 5 times.
    
    index += 1 // ++
} while index < 5
```

#### Listing 3.3

``` Swift
/// if/else.
let temperature = 45
if temperature > 60 {
    print("It's hot!")
} else if temperature > 40 {
    print("It's warm.")
} else {
    print("It's chilly.")
}
```

#### Listing 3.4

``` Swift
/// Control Flow.
var condition = true
if condition {
    // ...
    
} else { /* ... */ }

srandomdev() // Seed the random number generator.

// Omits upper value, use ... to include.
for _ in 0..<2 {
    print("\(arc4random())")
}
```

#### Listing 3.5

``` Swift
for i: Int in 0..<3 { print("i = \(i)") }

for j in 0..<3 { // Uses fast enumeration.
    
    print("j = \(j)")
}
```

### Tuples

#### Listing 4.1

``` Swift
let tuple = (1, 3, 5) // Inferred type (Int, Int, Int).
let tuple2 = (1, 5.0) // Inferred type (Int, Double).
let tuple3: (Double, Double) = (5, 6)

/// Indexing a tuple.
print(tuple.0)
print(tuple.1)
print(tuple.2)
```

#### Listing 4.2

``` Swift
/// A tuple with named elements.
let product = (id: 24, name: "Swift Book")
print(product.name)
```

#### Listing 4.3

``` Swift
/// Decomposing a tuple.
let (x, y, z) = tuple
print("\(x), \(y), \(z)") // "1, 3, 5."
```

#### Listing 4.4

``` Swift
/*
 Tuples are a grouping of multiple values into a single type.
 Unlike classes and structs, however,
 you can create a tuple without explicitly defining the type.
 */
var address = (742, "Salam St.")
print(address.0)
print(address.1)

/* You can update the components of a tuple via the index notation, as follows: */
address.0 = 744
```

#### Listing 4.5

``` Swift
// Using a type annotation.
var address1: (Int, String) = (50, "Peace Rd.")

// By explicit creation of a Double.
var address2 = (Double(50), "Peace Rd.")

// By using a double literal value.
var address3 = (50.0, "Peace Rd.")
```

#### Listing 4.6

``` Swift
/* You can also deconstruct tuples into their individual elements. */
let (house, street) = address
print("House: " + String(house)) // Using string interpolation.
print("Street: " + street  + "\n")

/* Another way to work with tuples is to name their elements. */
var address4 = (number: 50, street: "Peace Rd.")
print("I live at \(address4.number), \(address4.street)")
```

### Arrays

#### Listing 5.1

``` Swift
/// Empty array creation.
let emptyAr1 = [String]()
let emptyAr2 = Array<String>()
let emptyAr3: [String] = []

/// A constant array with inferred type.
let animals = ["cat", "dog", "chicken"]
// animals.append("cow") <- error!
// animals[2] = "fish" <- error!
```

#### Listing 5.2

``` Swift
/// A variable array with explicit type.
var mutableAnimals: [String] = ["cat", "dog", "chicken"]
mutableAnimals.append("cow")
mutableAnimals[2] = "fish"
```

#### Listing 5.3

``` Swift
/// Iteration.
for animal in animals { print(animal) }
```

#### Listing 5.4

``` Swift
/// Array API.
animals[0]                      // "cat."
animals[1..<3]                  // "dog", "chicken" "3."
animals.count                   // 3.
animals.contains("cat")         // true.
mutableAnimals.remove(at: 0)    // "cat."
```

#### Listing 5.5

``` Swift
/// Functional API.
animals.map { $0.uppercased() }         // "CAT", "DOG", ...
animals.filter { $0.hasPrefix("c") }    // true.
animals.sorted { $0 < $1 }              // false.
```

#### Listing 5.6

``` Swift
/// Bridged NSArray API.
let nsArray = animals as NSArray
nsArray.object(at: 2) // "chicken."
```

#### Listing 5.7

``` Swift
/// Arrays (Quick Examples).
var array1 = [1, 2, 3, 4, 5]
print(array1[2]); print()

var person1 = "فلان"
var person2 = "علان"
var array2: [String] = [person1, person2]

/* Adds (appends) a new element at the end of the array. */
array2.append("وليد")

/* You can even extend an array by adding a sequence to it, such as a range. */
//array1.extend(7...10)

for person in array2 {
    print("person: \(person)")
}

var waleed = array2[2]
```

### Dictionaries

#### Listing 6.1

``` Swift
/// Empty dictionary creation.
let emptyDict1 = [Int:String]()
let emptyDict2 = Dictionary<Int, String>()
let emptyDict3: [Int:String] = [:]
```

#### Listing 6.2

``` Swift
/// A constant dictionary with inferred type.
let numbers = [1 : "One", 2 : "Two"]
// numbers[4] = "Four" <- error!

/// A variable dictionary with explicit type.
var students: [String: String] = ["123": "Amal",
                                  "456": "Ahmed",
                                  "789": "Fahad"]
```

#### Listing 6.3

``` Swift
/// Unwrapping.
if let student = students["789"] {
    print("Student is \(student)")
}
```

#### Listing 6.4

``` Swift
/// Dictionary API.
students["789"]                     // "Fahad."
students["789"] = "Sarah"           // "Sarah."
students["1"]                       // "nil."
students.count                      // "3."
students.removeValue(forKey: "456") // Delete "Ahmed" OR students[456] = nil.

/// Dictionary values are returned as optionals.
students["789"]!.hasPrefix("s")     // true.
```

#### Listing 6.5

``` Swift
/// Iteration.
for (key, value) in students {
    print("Student[\(key)], : \(value)")
}
```

### Sets

#### Listing 7.1

``` Swift
//var setA = Set<Int>()
var setA: Set = [1, 2, 3]
setA.insert(1)
print(setA)

setA.remove(1)
print(setA)

var setB: Set = [2, 4, 6]
print(setA.intersection(setB))
```

### Optionals

#### Listing 8.1

``` Swift
/// An optional variable.
var maybeString: String?    // Defaults to nil.
maybeString = nil           // Can be assigned a nil.
maybeString = "fish"        // Can be assigned a value.
```

#### Listing 8.2

``` Swift
/// Unwrapping an optional.
if let unwrappedString = maybeString {
    // "unwrappedString" is a String rather than an optional String.
    print(unwrappedString.hasPrefix("f")) // true.
} else {
    print("maybeString is nil.")
}
```

#### Listing 8.3

``` Swift
/// Forced unwrapping - fails at runtime if the optional is nil.
if maybeString!.hasPrefix("f") {
    print("maybeString starts with 'f'")
}
```

#### Listing 8.4

``` Swift
/*
 Optional chaining, returning an optional with the result of hasPrefix,
 which is then unwrapped.
 */
if let hasPrefix = maybeString?.hasPrefix("f") {
    if hasPrefix {
        print("maybeString starts with 'f'")
    }
}
```

#### Listing 8.5

``` Swift
/// Unwrapping of multiple optionals.
let strOne: String? = "256"
let digitOne: Int? = Int(strOne!) // Swift 1.x used "strOne.toInt()."
let strTwo: String? = "123"
let digitTwo: Int? = Int(strTwo!) // Swift 1.x used "strOne.toInt()."
```

#### Listing 8.6

``` Swift
/// NSString API.
let strThree: NSString = "123"
let one23: Int = Int(strThree.intValue)
```

#### Listing 8.7

``` Swift
/// Optional chaining.
var optionalPi: Double? = nil /*Using forced unwrapping.*/
optionalPi = 3.14159

print("Force unwrapped! \(optionalPi!)" + "\n")
```

#### Listing 8.8

``` Swift
if let definiteDouble = optionalPi {
    definiteDouble
}

if let digitOne = digitOne, let digitTwo = digitTwo {
    /*
     Notice that digitOne and digitTwo are local constants of type Int
     that 'shadow' the constants of type Int? that were initialized earlier.
     */
    print(digitOne + digitTwo)
}
```

#### Listing 8.9

``` Swift
/// Optional unwrapping with conditions.
if let digitOne = digitOne,
    let digitTwo = digitTwo,
    digitTwo != 5 {
    
    print(digitOne + digitTwo)
}
```

#### Listing 8.10

``` Swift
/// "nil" coalescing.
var anOptional: Int?
var coalesced = anOptional ?? 3 // "nil" value coalesced to 3.
```

### Implicitly Unwrapped Optionals

#### Listing 9.1

``` Swift
/// An implicitly unwrapped optional variable.
var optionalString: String!
optionalString = nil
optionalString = "fish"
```

#### Listing 9.2

``` Swift
/// Methods invoked directly, failing at runtime if the optional is nil.
if optionalString.hasPrefix("f") {
    print("maybeString starts with 'f'")
} else {
    print("maybeString does not start with an 'f'")
}
```

### Enumerations (*a.k.a.* Enums)

#### Listing 10.1

``` Swift
/// Enum declaration.
enum Direction { case North, South, East, West }

/// Assignment.
var direction = Direction.North
direction = .South // Enum type inferred.
```

#### Listing 10.2

``` Swift
/// Switching on enums.
switch direction {
case .North:
    print("Going North.")
default:
    print("Going someplace else!")
}
```

#### Listing 10.3

``` Swift
/// Advanced enumerations - using generics.
enum Result<T> {
    case Failure
    // Enumeration member with associated value.
    case Success(T)
}

/// Creating an instance - where the type T is an Int.
var result = Result.Success(22)
```

#### Listing 10.4

``` Swift
/// Switching and extracting the associated value.
switch result {
    case .Failure:
        print("Operation failed.")
    case .Success(let value):
        print("Operation returned value \(value).")
}
```

#### Listing 10.5

``` Swift
/// Assignment (using data types.)
enum EdgeType: Int {
    case directed = 1
    case undirected = 2
}
var type = EdgeType.undirected
```

### Switch

#### Listing 11.1

``` Swift
enum Bit { case Zero, One }
let bit = Bit.Zero
```

#### Listing 11.2

``` Swift
/// A simple switch statement on an enum.
switch bit {
case .Zero:
    print("zero")
case .One:
    print("one")
}
```

#### Listing 11.3

``` Swift
/// Interval matching.
let time = 45
switch time {
case 0..<60:
    print("A few seconds ago.")
case 60..<(60 * 4):
    print("A few minutes ago.")
default: // Default required in order.
    print("Ages ago!") // To be exhaustive
}
```

#### Listing 11.4

``` Swift
/// Tuples and value bindings.
let boardLocation = (2, 5)
switch boardLocation {
    
case (3, 4), (3, 3), (4, 3), (4, 4):
    print("Central location.")
    
case (let x, let y):
    print("(\(x), \(y)) is not in the center.")
    
} /* Note: switch cases must be exhaustive and cover all possible cases. */
```

### Functions/Methods

#### Listing 12.1

``` Swift
/// A simple function.
func display(message: String) {
    print(message)
}
display(message: "Hello, Swift!")
```

#### Listing 12.2

``` Swift
/// A function that returns a value.
func multiply(arg1: Double, arg2: Double) -> Double {
    return arg1 * arg2
}
let val = multiply(arg1: 20.0, arg2: 35.2)
```

#### Listing 12.3

``` Swift
/// Another example.
///
/// - Parameters:
///   - s1: 1st parameter.
///   - s2: 2nmd parameter.
///   - joiner: 3rd parameter.
/// - Returns: A joined string,
func join(string s1: String,
          toString s2: String,
          withJoiner joiner: String) -> String {
    return s1 + joiner + s2
}
join(string: "Hello", toString: "Swift!", withJoiner: ", ")
```

#### Listing 12.4

``` Swift
/// Our three parameters now have these external and local names:
///
///  - external message, local: message.
///  - external: withPrefix, local: prefix.
///  - external: andSuffix, local: suffix.
func logMessage(message:String,
                withPrefix prefix: NSString,
                andSuffix suffix: NSString) {
    print("\(prefix)-\(message)-\(suffix)")
}
logMessage(message: "QWERTY", withPrefix: "***", andSuffix: "$$$")
```

#### Listing 12.5

``` Swift
/// in-out parameters.
///
/// - Parameter number: A parameter.
func square(_ number: inout Double) {
    number *= number
}
var number = 4.0
square(&number) // number = 16.
```

#### Listing 12.6

``` Swift
/// Function types.
let myFunc: (Double, Double) -> Double = multiply
```

#### Listing 12.7

``` Swift
/// A generic function.
func areEqual<T: Equatable>(op1: T, op2: T) -> Bool {
    return op1 == op2
}
```

### Closures

#### Listing 13.1

``` Swift
let degrees = ["Bachelor", "Master", "PhD"]

degrees.sorted {
    (one: String, two: String) -> Bool in
    return one > two
}
```

#### Listing 13.2

``` Swift
/// Inferred argument type.
degrees.sorted {
    (one, two) -> Bool in
    return one > two
}
```

#### Listing 13.3

``` Swift
/// Inferred return type.
degrees.sorted {
    (one, two) in
    return one > two
}
```

#### Listing 13.4

``` Swift
/// No brackets around parameters.
degrees.sorted {
    one, two in
    return one > two
}
```

#### Listing 13.5

``` Swift
/// No return keyword.
degrees.sorted {
    one, two in
    one > two
}
```

#### Listing 13.6

``` Swift
/// Shorthand arguments.
degrees.sorted { $0 > $1 }

/// Trailing closure.
degrees.sorted() { $0 > $1 }
degrees.sorted { $0 > $1 }
```

### Classes and Protocols

#### Listing 14.1

``` Swift
/// Base class implementation.
public class BaseClass {
    
    /// Private constant property.
    private let id: Int
    
    init(id: Int) { self.id = id }
}
```

#### Listing 14.2

``` Swift
/// Protocols.
protocol NamedType {
    
    /// A property with a getter.
    var name: String { get }
}

/// Class implementation.
class Student: BaseClass, NamedType {
    
    /// Variable with public getter and private setter.
    private(set) var name: String
    
    /// Implicit internal property.
    var size: Double = 45.0
    
    /// Public constant property.
    public let fullName: String
    
    /// All properties initialized before base init invoked.
    ///
    /// - Parameters:
    ///   - id: Student id.
    ///   - name: Student name.
    ///   - fullName: Student full name.
    init(id: Int, name: String, fullName: String) {
        
        self.name = name
        self.fullName = fullName
        
        // "super" initializer invoked.
        super.init(id: id)
        
        /* Functions on self can now be called. */
    }
}
```

#### Listing 14.3

``` Swift
/// Creating an instance.
var student = Student(id: 140101, name: "Foo", fullName: "Foo, son of Foo")
```

#### Listing 14.4

``` Swift
/// Another abstract (base) class.
class AbstractClass { /* ... */ }

/// Protocols.
protocol OptionalProtocol1 {}
protocol OptionalProtocol2 {

    /// Tells whether an object is updated or not.
    var updated: Bool? { get set }

    /// Sample function with parameters.
    ///
    /// - Parameters:
    ///   - a: A variable.
    ///   - b: Another variable.
    func addUp(_ a: Float, b: Float) -> Double
}
```

#### Listing 14.5

``` Swift
/// Subclass implementation.
class MySubclass : AbstractClass, OptionalProtocol1, OptionalProtocol2 {

    /* Property declarations. */
    var myProperty: String
    var myOptionalProperty: String?
    // More properties...

    /// Tells whether an object is uppdated or not.
    var updated: Bool? = false

    /// Only need override if subclassing.
    override init()  {
        myProperty = "Foo"
    }

    /* Functions. */

    /// A function dubbed "compute()."
    ///
    /// - Returns: An integer.
    func compute() -> Int { return 0 }

    func compute(a: Int) -> Int {
        return a
    }

    func compute(a: Int, b: Int) -> Int {
        return a + b
    }

    func compute(a: Int, and b: Int) -> Int {
        return a + b
    }
    
    /// Sample function with parameters.
    ///
    /// - Parameters:
    ///   - a: A variable.
    ///   - b: Another variable.
    /// - Returns: A boolean value.
    func addUp(_ a: Float, b: Float) -> Double {
        return Double(a * b)
    }
}

/// Creating an instance.
var a = MySubclass()
a.myProperty
a.compute()
a.compute(a: 1)
a.compute(a: 2, b:3)
a.compute(a: 2, and: 3)

let b = a.compute(a: 2, and: 3) as Int
print("2 + 3 = \(b)")
```

## Sample Code

Completed Xcode Playground for this exercise can be found in ZIP format (archived):

* [CheatSheet.playground.zip](https://github.com/youldash/Swift-Playgrounds/blob/master/CheatSheet.playground.zip).

## Trademark

, Mac, macOS, iOS, and Xcode, are trademarks of Apple, Inc.

## Sponsors

<div align="center">
	<table border="0">
		<tr>
			<td align="center"><img src="https://raw.github.com/youldash/Swift-Playgrounds/master/misc/kkulogo.png" width="25%" /></td>
			<td align="center"><img src="https://raw.github.com/youldash/Swift-Playgrounds/master/misc/IAU.jpg" width="100%" /></td>
		</tr>
	</table>
</div>

This repo was made possible, thanks to:
- [King Khalid University](http://www.kku.edu.sa/en/).
- [College of Computer Science and Information Technology](https://www.iau.edu.sa/en/colleges/college-of-computer-science-and-information-technology) of Imam Abdulrahman Bin Faisal University.

## License

By using this site, you agree to the **Terms of Use** that are defined in [LICENSE](https://github.com/youldash/Swift-Playgrounds/blob/master/LICENSE).

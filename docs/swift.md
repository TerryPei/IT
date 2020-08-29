# Swift 5.

## Basic 

### Value
The value of a constant can’t be changed once it’s set, whereas a variable can be set to a different value in the future.
```swift
let maxNumberOfLoginAttempts = 10
var currentLoginAttempt = 0
var x = 0.0, y = 0.0, z = 0.0
```

### Type annotation


```swift
var welcomeMessage: String
welcomeMessage = "Hello"
```

```swift
var red, green, blue: Double
```

### Naming constants and variables

```swift
let π = 3.1415953
let str = "Terry Pei"
let 🐶🐮 = "dogcow"
```


```swift
let languageName = "Swift"
languageName = "Swift++"
// This is a compile-time error: languageName cannot be changed.

var friendlyWelcome = "Hello!"
friendlyWelcome = "Bonjour!"
// friendlyWelcome is now "Bonjour!"
```

### Print
```swift
print("FriendlyWelcome is \(friendlyWelcome)")
```

### Int, Double, String
```swift

```
```swift
let paddedDouble = 000123.456
let oneMillion = 1_000_000
let justOverOneMillion = 1_000_000.000_000_1
```

### Tuples
Tuples group multiple values into a single compound value. The values within a tuple can be of any type and don’t have to be of the same type as each other.
```swift
let http404Error = (404, "Not Found")
// http404Error is of type (Int, String)

print("The status code is \(http404Error.0)")
// Prints "The status code is 404"
print("The status message is \(http404Error.1)")
// Prints "The status message is Not Found"

let (statusCode, statusMessage) = http404Error
```

```swift
let http200Status = (statusCode: 200, description: "OK")

print("The status code is \(http200Status.statusCode)")
// Prints "The status code is 200"
print("The status message is \(http200Status.description)")
// Prints "The status message is OK"
```
## Optionals
value + nil, need unwrap.
nil is not a pointer in swift
```swift
var serverResponseCode: Int? = 404
// serverResponseCode contains an actual Int value of 404
serverResponseCode = nil
// serverResponseCode now contains no value

var surveyAnswer: String?
// surveyAnswer is automatically set to nil
```
Forced Unwrapping

```swift
if value != nil {
    print("value contains some value.")
}
```
Optional Binding
 use optional binding to find out whether an optional contains a value, and if so, to make that value available as a temporary constant or variable.

```swift
if let actualNumber = Int(possibleNumber) {
    print("The string \"\(possibleNumber)\" has an integer value of \(actualNumber)")
} else {
    print("The string \"\(possibleNumber)\" could not be converted to an integer")
}

if let firstNumber = Int("4"), let secondNumber = Int("42"), firstNumber < secondNumber && secondNumber < 100 {
    print("\(firstNumber) < \(secondNumber) < 100")
}
// Prints "4 < 42 < 100"
```
Implicitly Unwrapped Optionals
    sure always have a value. 
    `String!` rather than `String?`
    The following example shows the difference in behavior between an optional string and an implicitly unwrapped optional string when accessing their wrapped value as an explicit String:

```swift
let possibleString: String? = "An optional string."
let forcedString: String = possibleString! // requires an exclamation point

let assumedString: String! = "An implicitly unwrapped optional string."
let implicitString: String = assumedString // no need for an exclamation point
```

```swift
let optionalString = assumedString
// The type of optionalString is "String?" and assumedString isn't force-unwrapped.
```

## Error Handling
A function indicates that it can throw an error by including the throws keyword in its declaration.
```swift
func canThrowAnError() throw {
    // this function may or may not throw an error
}

do {
    try canThrowAnError()
    // no error was thrown
} catch {
    // an error was thrown
}
```
In the following example, the makeASandwich() function will throw an error if no clean dishes are available or if any ingredients are missing. Because makeASandwich() can throw an error, the function call is wrapped in a try expression. By wrapping the function call in a do statement, any errors that are thrown will be propagated to the provided catch clauses.
```swift
func makeASandwich() throws {
    // ...
}

do {
    try makeASandwich()
    eatASandwich()
} catch SandwichError.outOfCleanDishes {
    washDishes()
} catch SandwichError.missingIngredients(let ingredients) {
    buyGroceries(ingredients)
}
```
## Assertions and Preconditions
If the Boolean condition in the assertion or precondition evaluates to true, code execution continues as usual. If the condition evaluates to false, the current state of the program is invalid; code execution ends, and your app is terminated.

Debugging with Assertions
```swift
let age = -3
assert(age >= 0, "A person's age can't be less than zero.")
// This assertion fails because -3 is not >= 0.
```
If the code already checks the condition, you use the assertionFailure(_:file:line:) function to indicate that an assertion has failed. For example:

```swift
if age > 10 {
    print("You can ride the roller-coaster or the ferris wheel.")
} else if age >= 0 {
    print("You can ride the ferris wheel.")
} else {
    assertionFailure("A person's age can't be less than zero.")
}
```
Enforcing Preconditions
```swift

```
```swift

```
```swift

```
```swift

```
```swift

```

# Learning-swift
## Sub heading
Just a sample repo for learning the basic the basics of markdown.

more text with two line breaks between.

- first time
- second time 
- third time
    - indented  
        1. inner number

[This is the hyperlink](http://www.github.com)

This paragraph has some `varible` inline code.

```html
<p>A paragraph example</p>
```

```swift
let terry: String
```

```python
import numpy as np
```

![alt text](http://picsum.photos/200/200)

Some paragrph with text

> blockquote text below the paragraph

| heading | header | head |
| --- | --- | --- |
| content | more content | Text |
| more | more | more |

This is being created on a **Wednesday** ~~Saturday~~.


## Test4




---
layout: post
title: 100 Days of SwiftUI - Day 5
date: 2019-09-27
author: Chuck Underwood
categories: 100-Days-of-SwiftUI
---

## Day 5
### 100 Days of SwiftUI

I learned two new things about functions today during Day 5 of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui).

Variadic functions allow for mutliple parameters to be used in a function without predetermining the number of parameters.  For example ```print()``` can take any number of parameters and will print all of the inputs.

I also learned about inout parameters.  Declaring a function parameter as inout makes the functions capable of modifying the passed in parameter outside the scope of the function. We write the functions as follows:

```swift
func doubleInPlace(number: inout Int) {
    number *= 2
}
```

To use this function when calling we need to explicitly indicate that we know the parameter is changing by prepending an '&' infront of the parameter. To use this we need to declare a variable not a constant.

```swift
var num = 10 
doubleInPlace(number: &num)
```

I believe that it would better to return the value but I will look for a good reason to use this type of syntax.
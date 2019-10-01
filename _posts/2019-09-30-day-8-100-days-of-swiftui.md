---
layout: post
title: 100 Days of SwiftUI - Day 8
date: 2019-09-30
author: Chuck Underwood
categories: 100-Days-of-SwiftUI
---

## Day 8
### 100 Days of SwiftUI

All about structs today.  I actually watched all of the videos for today and tomorrow because I was learning with each video.  Tomorrow I will rewatch all of the videos for structs and take all of the tests.

When you want to change a property inside a method, you need to mark it using the mutating keyword.

```swift
struct Contact {
    var email: String

    mutating func updateEmail(new: String) {
        email = newEmail
    }
}
```

Property Observers are also a helpful aspect of structs that let you run code before or after a property changes.

```swift
struct Balance {
    var account: String
    var balance: Int
    var amount: Int {
        didSet {
            print("\(account) now has a \(balance).")
        }
    }
}
```

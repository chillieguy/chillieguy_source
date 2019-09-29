---
layout: post
title: 100 Days of SwiftUI - Day 4
date: 2019-09-26
author: Chuck Underwood
categories: 100-Days-of-SwiftUI
---

## Day 4
### 100 Days of SwiftUI

Finished up Day 4.  All of about loops.

Learned how to label an outside loop so we can exit nested loops at the level that we choose.

```swift
outerLoop: for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print ("\(i) * \(j) is \(product)")
    }
}
```

We can then set a condition in the inner loop to break out of both loops.

```swift
outerLoop: for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print ("\(i) * \(j) is \(product)")

        if product == 73 {
            print("It's Sheldon's favorite number!")
            break outerLoop
        }
    }
}
```

If we did not break out of "outerloop", the inner loop would break and the outer loop would continue to run.
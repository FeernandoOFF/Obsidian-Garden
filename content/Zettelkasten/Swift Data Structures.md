---
draft: false
title: Swift Structures
publishDate: 28-10-2022
lang: en
tags:
- core-topics/tech/languages/swift
---

# Swift Structures


## Arrays 
A bunch of items separated by commas and you can access a value from his Index

**Declaration:** 
```swift
let eggTimes = [5,8,12]
```

Type: `[Int]` - This way we can type a variable
Literal: `[]`

## Sets
A _set_ stores distinct values of the same type in a collection with no defined ordering. You can use a set instead of an array when the order of items isn’t important, or when you need to ensure that an item only appears once.

```swift
var letters = Set<Character>()
```

## Dictionaries
Key-value pair  and you can access his value with the key in brackets

 **Declaration:** 
```swift
let eggTimes : [String:Int ]= ["Soft":5,"Medium":8,"Hard":12]

eggTimes["Soft"] //5
```




## References
[Collection types](https://docs.swift.org/swift-book/LanguageGuide/CollectionTypes.html)

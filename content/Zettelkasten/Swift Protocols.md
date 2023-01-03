---
draft: false
title: Swift Protocols
type: note
publishDate: 04-11-2022
fc-calendar: Obsidian Calendar
fc-date: 04-Nov-2022
fc-category: Note
lang: en
tags:
- PreMoc/swift
---

# Swift Protocols

## Definition
A _protocol_ defines a blueprint of methods, properties, and other requirements

- Data type that allows you to **define methods** of structs and classes, it is handy when you want different **classes** or **structs** to share a logic without using inherence from other class like in this example: 
- ![[Pasted image 20221102230018.png|300]]
- By using it as a type in a function parameter we make sure that the parameter we are sending have the implementation of certain method


## Declaration
```swift
protocol CanDelete {
	let mustHave: String
	func delete()
}
```
### Implementation
```swift
struct SomeStructure: OneProtocol, SecondProtocol {}

class SomeClass: SuperClass, OneProtocol,SecondProtocol{}
```

 You can also [[Swift Extensions#Extensions and Protocols| Set a default behaviour]] with Extensions! so you don't have to set a function every time 


## References

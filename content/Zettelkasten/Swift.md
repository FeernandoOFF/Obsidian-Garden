---
draft: false
title: "Swift"
publishDate: 12-10-2022
lang: en
tags:
- core-topics/tech/languages
- todo
- PreMoc
---



# Swift

## What is Swift?
Swift is **the language** created by Apple ...

[[Swift UI]]

## Why swift?
To develop to the [[Zettelkasten/Apple Ecosystem]]

## Basics
- Naming conventions 
	- camelCasing
	- kebab-casing
	- snake_case
- Comments (`//`)
	- `CMD + /`
	- `/* multiline comment */`
- Playgrounds
	- File -> new -> Playground
		- Blank
		- Single View
		- Map
		- Game
- Print
	- Interpolation `"STRING..\(Code..) Continues"`
- Variables
	- `var` -> regular variable
	- `let` -> Constant variable




## [[Swift Data Types]]
The swift Data types are the **primitive values** and the framework that you will use to create your apps

## [[Zettelkasten/Swift Data Structures|Data Structures]]

A data structure is a **specialized** format for **organizing**, processing, retrieving and storing data. There are several basic and advanced types of data structures, all designed to arrange data to suit a specific purpose. Data structures make it easy for users to access and work with the data they need in appropriate ways.

## Operators
`a...b` All including the highest
`a..<b` But no B
`..b` Up to B

```swift
object.value! //Will stop execution if property not found
```


## Functions
Syntax: 
```swift
 func nameOfFunction(parameterName: DataType,secondParameter:DataType)
 {
		//
 }
```

Call: 
```swift
	nameOfFunction(parameterName: Value)
```


#### Returning values

```swift
func getData() -> Bool {
	let res = fetchData()
	if(res) {return true}
	return false
}
```

#### External parameter names

> [!NOTE] You can disable parameter names!
> By calling the external parameter `_` It wont require any name!

The external parameter names are useful whenever you want to call a function/method form outside without calling from the internal name

```swift
 func nameOfFunction(pa parameterName: DataType)-> DataType
 {
		//
 }

nameOfFunction(pa: 'Hola')
```
**Without parameter name:**

```swift
 func nameOfFunction(_ parameterName: DataType)
 {
		//
 }

nameOfFunction('Hola')
```


--- 



## Conditionals
```swift
if(){
	//
}if else{
	//
}else{
 //
}
```


```swift
switch var{
	case "value":
		//
	case "z":
		//
	default:
		//
}
```







---- 

## Structures
Help us to create custom `Data-Types` - Kind of [[Javascript Classes]]

```swift
struct Person {
	// Property
	let name = "Fernando"
	let age = 19

	// Constructor
	init(){
	}

	// Method
	mutating func greetings(){
	}
}

```
#### Characteristics
- **Mutating** value is necessary as it **removes the object** and creates another one with the updated values 
- Struct is **passed via value**, so if
```swift
let enemy1 = Enemy(health:100)//struct Enemy {}
let enemy2 = enemy1
enemy1.health = 50
print(enemy2.health ) //100
```


## Classes

> [!NOTE] Convention
> The name of the file matches the name of the class

The main **difference** between classes and **structs** is that classes **can extend** from other clases

- Override
- **super**
```swift
class Enemy {
	var health = 200
	var attackStrenght = 10
	var position = [0,0]
	var name = "Enemy"

	func move(){
		position[0] = position[0] + 1
	}
	func attack(){
		print("enemy attacks \(attackStrenght) damage ")
	}
}


class Dragon: Enemy {
	 override func move(){
		 print("The dragon flyes")
	 }

	func talk(){
			let name = super.name
			print("\(name) the dragon says: ----")
	 }
}
```

All the objects come from the **NSObject** class

> [!NOTE] Note
> **NS** comes from NeXSTEP - company that Steve Jobs founded when kicked out of Apple






## Structs vs Classes

> [!NOTE] When use each?
> Start by **using structs** and if you need to work with **objetive-c** or **inherence**, use classes

Structs are not able to inherit 
Similarities:
- Blueprint
- Group (attributes and behaviour) 
- Initialisers

Structs comes with **built-in init() function** and classes need to provide an **init()** function

> [!attention]
> **Classes** are passed by **reference** while **Structs** are passed by **value**


## Extra
[[Swift Cheatsheet]]

UiKit -> Framework (UiKit includes Foundation) 
Foundation

If a method is **expecting a property of instance** you can pass directly the **dot property** `.red`



- SF Symbols


- [[Swift UITextField]]

- [[Swift Protocols]]
- [[Swift Delegate Pattern]]
- [[Swift Networking]]
- [[Swift Extensions]]
- [[Swift CoreLocation]]
- [[Swift Loops]]

- Navigation Stack - AKA Back button
	- Editor
		- Embed In
			- Navigation stack

- Swift Anonymous function
- check in the range of numbers `300...332`
- Computed property
	- Stored properties

```swift
struct Struct {
	let id:Int
	let temp:String
//computed
	var conditionalProperty:String {
		//...value based on other properties
	}
}
```

- UpdateUI with completion handler
- DispatchQueue 

Array methods
- Map
- Reduce
- Filter

## References
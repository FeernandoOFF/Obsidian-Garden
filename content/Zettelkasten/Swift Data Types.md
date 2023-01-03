---
draft: false
title: Swift Data Types
publishDate: 28-10-2022
lang: en
tags:
- core-topics/tech/languages/swift
---


## Nil

## Data Types


> [!NOTE] Data types in swift
> Swift supports **Six data types** which are [[#Int]],[[#String]],[[#Float]],[[#Double]],[[#Bool]] and [[#Character]]

 
#### Type **Inference** (AKA "Swift knows")

Is not necessary to explicitly tell the variable which type is going to hold **if** you **assign a value** when you **create** it.
```swift
var currentNumber = 0 //currentNumber:Int
```



## Int
The **Integer** type represent **complete numbers** which can be 1,2,3... and it **can't** hold **decimal point**

```swift
var number:Number = 1
```

#### Methods

| Method | Syntax |
| ------ | ------ |
| Random | Int.**random(in:1..5)**|



## String
The **String** or  **[[unicode]] string**  type represents a  collection of [[#Character|Characters]] and it's declared  **Only** with **double quotes**

```swift
var string: String = "Hello world" 
```

#### String Interpolation
You can **insert variables** into a string with `\(var..)`

```swift
let name = "Rosa"
let personalizedGreeting = "Welcome, \(name)!"// personalizedGreeting == "Welcome, Rosa!"
```

#### Multiline
A multiline string can be made with three quotation marks (`"""`)
```swift
let banner = """
					 ^
	Watch Up |
		"""
```

#### Methods

| Method | Syntax |
| ------ | ------ |
| Count  | "string"**.count**       |



## Float
This type **can** hold **decimal point** values

> [!NOTE] Note
> This type is useful with **Progress bars** 
> `Float(current)/Float(total)`

```swift
let progress: Float = 0.5
```




## Double
The same as [[#Float]] but with **more** memory allocated to decimal points

## Bool
This is type can hold **two** values (`true` or `false`)

```swift
var isOpen:Bool = false
```


## Character
## Optionals
An optional data type can be defined by adding `?` to the data type of your variable - this means that the variable can be `nil` (Empty)

```swift
var hardness : String?
```

#### Ways to work with Optional values
1. Force Unwrap
	1. `OptionalValue!`
2. checkWith if 
	1. `if optionalValue != nil {...}`
3. Optional binding
```swift
if let safeOptional = optionalValue {
	 //safeOptional is now a unwrapped value!
}
```

1. nil coalescing operator 
	1. `optional ?? defaultValue`
2. Optional chaining
	1. `optional?.property || optional?.method()`





## References


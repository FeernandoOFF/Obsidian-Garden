---
draft: false
title: Swift extensions
type: note
publishDate: 07-11-2022
fc-calendar: Obsidian Calendar
fc-date: 07-Nov-2022
fc-category: Note
lang: en
tags:
- PreMoc/swift
---

# Swift extensions

What if you'd like that the **Int**  dataType had a `fromString` or **custom** methods. Well, **you can do that with swift extensions!** - You can also extend elements from **UIKit**
```swift
extension Double {
	func round(to places:Int){
		
	}
}
```



## Extensions and Protocols

You can also set **default behaviour** for **[[Swift Protocols|Protocols]]** so they have a default implementation

```swift
protocol canFly {
	fly()
}

extension canFly {
	func fly(){
		print("The object takes off into the air")
	}
}
```

## Using extensions to refactor 
We can use **extensions** to refactor different things with different **concerns** for example in our viewController we have a pice of code that handles the [[Swift UITextField|UITextFieldDelegate]] methods and also our custom `WeatherManagerDelegate`, so in this case we can use extensions to **refactor those concerns** into **different blocks** of code

```swift 
extension ViewController:UITextFieldDelegate {
	textFieldShouldReturn(){...}
	textFieldDidEndEditing(){...}
}
```

## References

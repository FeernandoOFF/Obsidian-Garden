---
draft: false
title: Swift UI
type: note
publishDate: 16-11-2022
fc-calendar: Obsidian Calendar
fc-date: 16-Nov-2022
fc-category: Note
lang: en
tags:
- PreMoc/swift
---

# Swift UI

## What is?
Declarative IOS development

Features
 - Drag and drop
 - Stacks VHZ
 - Highly reusable - [[Components]] - Right click extract
 
Inspiration from web 
Project Catalyst - Multiplatform

- Modifier library (object library tab)

#### Tips
- Wrap in Stack `cmnd + click`


### Views and Stacks
SwiftUI provides a View which is like the [[HTML#Divs]] and the stacks are like applying [[Flexbox#Flex-Direction]] property.
##### Syntax 
```swift
struct ContentView: View {
	var body: some View {
		ZStack {
			//back
			Color(.darkGray).ignoresSafeArea()
			//front
			VStack{
				//top
					Image("name-in-assets").clipShape(Circle())
				//bottom
			}
			HStack{
				//left
					View {
						Text("Hi")
					}
				//right
			}
		}
	}
}
```



### Components - Subviews
Extract in Subview

Create file for component. `create file -> swiftUI` 
- Create your component
Preview your solo component 
`.previewLayout(.sizeThatFits)`

##### Syntax
```swift
struct InfoView :View{
	let text:String
	var body: some View {
		
	}
}
```



## State
The [[Swift#Structures]] are inmutable by default and the way to mutate them is by adding the **mutating** prefix to his method, but this means that the whole object has to be deleted and re-created. Well... `@State` is a new keyword that lets swift update a value without recreating the object

## Styling
### Images
- Resizable - Stretches all the way
- ignoresafeArea
- aspectRatio(1,contentMode:xxx)

## References

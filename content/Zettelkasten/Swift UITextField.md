---
draft: false
title: Swift UITextField
type: note
publishDate: 04-11-2022
fc-calendar: Obsidian Calendar
fc-date: 04-Nov-2022
fc-category: Note
lang: en
tags:
- PreMoc/swift
---

# Swift UITextField

Complex because of keyboard handling
[[Swift Delegate Pattern]]

- UITextField
	- Automatic Appearance
	- Customise keyboard
		- **Text Input Traits**
		- Capitalisation
		- Return Key
		- Keyboard type
	- `UITextLabel`.**text**
	- Manage text return events
		- ViewController **extends** from **UiTextFieldDelegate**
		- The delegate has many functions to hook into various moment of the search
```swift
class IndexViewController: UIViewController, UITextFieldDelegate{
	@IBOutlet weak var textField:UITextField!
	
	override func viewDidLoad(){
		super.viewDidLoad()
		// comunicate text field with the keyboard
		textField.delegate = self
	}

	//Functioncalled on enter
	func textFieldShouldReturn(text)->Bool{
		print(textField.text)
		textField.endEditing(true)
		return true
	}
// 
func textFieldDidEndEditing(text){
	textField.text = ""
}
}
```


## References

---
draft: false
title: Swift Delegate Pattern
type: note
publishDate: 04-11-2022
fc-calendar: Obsidian Calendar
fc-date: 04-Nov-2022
fc-category: Note
lang: en
tags:
- PreMoc/swift
---

# Swift Delegate Pattern

![[Design Pattern#What is a Design Pattern?]]



- [[Swift Protocols]] - Required methods
- Perfect for Packages
- It makes sure that whatever method you're passing has a method and that allows you to switch whatever ViewController
![[Pasted image 20221104200810.png|500]]

> Every class that says that it can deal with x should be able to implement this method - Kind of a  [[JS Callbacks]]


## Example
EmergencyCallHandler receives a notification and he has to send somebody who **must have completed** the Advanced Life Support Course (Protocol) - So whenever the Emergency call should be able to say RCP and whoever is at the other line **has to understand certain concepts** such as **RCP**

![[Pasted image 20221104201617.png|500]]
## References

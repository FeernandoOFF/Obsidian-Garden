---
draft: false
title: Swift Networking
type: note
publishDate: 04-11-2022
fc-calendar: Obsidian Calendar
fc-date: 04-Nov-2022
fc-category: Note
lang: en
tags:
- PreMoc/swift
---

# Swift Networking

## Create Fetch
1. Create URL
	1. `URL(string)`
2. Create URLSession
	1. `session = URLSession(configuration: .default)`
3. Give the session a task
	1. `task = session.dataTask(with:url, completionHandler)`
4. Start the task
	1. `task.resume()`

## JSON Decoding

JSON ("JavaScript Object notation") which is protocol from the Web world where is important to send and receive data.

`Data`

- Type `Decodable`
- `JSONDecoder()`
- decoder.decode(`struct.self`,from`Data`)
- try catch  / Do - Try - Catch `error`

## References

---
draft: false
title: Swift Cheatsheet
publishDate: 28-10-2022
lang: en
tags:
- core-topics/tech/apple
- core-topics/tech/cheat-sheet
---

# Swift Cheatsheet
This is a [[cheatsheet]] which contains things that are useful but a little tricky to remind

## Timer
```swift
timer = Timer.scheduledTimer(timeInterval: 1, target: **self**, selector: **#selector**(updateTimer), userInfo: **nil**, repeats: **true**)
```

## Play an audio
```swift
import AVFoundation


let url = Bundle.main.url(forResource: "alarm_sound", withExtension: "mp3")
  
player = try! AVAudioPlayer(contentsOf: url!) 
player.play()
```

## String format
```swift
String(format: "%.2f", 100.23234123421) //100.23
```

## References

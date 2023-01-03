---
draft: false
title: React ContextAPI
type: note
publishDate: 08-11-2022
fc-calendar: Obsidian Calendar
fc-date: 08-Nov-2022
fc-category: Note
lang: en
tags:
- PreMoc/React
---

# React ContextAPI

## What is ContextAPI?
It provides an easier way to pass state between components, in a react app the **data is passed top-down** via props. But sometimes we require an easier way to access data from grand-grand-grand child to the root, and that's what the context API provide to us.

- Is considered a **global store** for data


> [!warning] Before you use it
> Before implementing the ContextAPI you can use [[component composition]] which is an easier way to archive a similar result


## Syntax

####  Create Context
```js
//Default value
const ThemeContext = React.createContext('light');
```

####  Available for the wrapped components

```js
return (
	      <ThemeContext.Provider value="dark">        
		      <YourApp.. />
	      </ThemeContext.Provider>
      )
```

#### Consume the data
- Function Components
```js
const state = useContext(ThemeContext)
```


- Class Components
```js
<MyContext.Consumer>
  {value => /* render something based on the context value */}
</MyContext.Consumer>
```

## References

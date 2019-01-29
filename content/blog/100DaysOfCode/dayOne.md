---
title: Day One - 100DaysOfCode
date: '2019-01-28T00:00:03.284Z'
---

Today I found out a better way to write an array function with the help of **reducer** in javaScript.  
I learnt this by an online course on egghead
[Reduce Data with Javascript Array#reduce](https://egghead.io/courses/reduce-data-with-javascript-array-reduce)
Thanks [@mykola](https://twitter.com/mykola) for the helpful instructions.

Get the sum of an array:

```jsx
var data = [15, 3, 20]

var reducer = function(accumulator, item) {
  return accumulator + item
}

var initialValue = 0

var total = data.reduce(reducer, initialValue)
```

Reduce an Array into a Single Object:

```js
var votes = [
  'angular',
  'angular',
  'react',
  'react',
  'react',
  'angular',
  'ember',
  'react',
  'vanilla',
]

var initialValue = {}

var reducer = function(tally, vote) {
  if (!tally[vote]) {
    tally[vote] = 1
  } else {
    tally[vote] = tally[vote] + 1
  }

  return tally
}

var result = votes.reduce(reducer, initialValue)
```

Use the Optional Reduce Arguments:

```jsx
function reducer(accumulator, value, index, array) {
  var intermediaryValue = accumulator + value

  if (index === array.length - 1) {
    return intermediaryValue / array.length
  }

  return intermediaryValue
}

var data = [1, 2, 3, 3, 4, 5, 3, 1]
var mean = data.reduce(reducer, 0)
```

Looks neat, right?

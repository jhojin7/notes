---
planned: 9~10
covered: 11
---
# ablestudy 2022-02-17
- text string -> `.parse()` -> JSON objects
- JSON objects -> `.stringify()` -> text string

## Code
```js
jsonText = '{"name":"authorname","email":"author@gmail.com", "nationality": "KR"}'

// string to object
console.log(typeof jsonText) // string
const jsonObject = JSON.parse(jsonText)
console.log(typeof jsonObject) // object

// object to string
jsonStr = JSON.stringify(jsonObject)
console.log(jsonStr, typeof jsonStr)
// {"name":"authorname","email":"author@gmail.com","nationality":"KR"} string

str = `${jsonObject.name} ${jsonObject.email} ${jsonObject.nationality}`
console.log(str) // authorname author@gmail.com KR
```
https://replit.com/@jhojin7/DarkFilthyExtraction

## Resources
- MDN docs JSON object https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/JSON
---
planned: 11-12
covered: 12-15
---
# ablestudy 2022-02-18
- js에서 html 페이지에 element추가하려면 document.createElement()
- document.createTextNode(text): text를 새로운 노드로 만들어둠.
- element.appendChild(elem): elem을 다른 element에 붙임. 
- 

## Code
```js
console.log(books[0].comments.length)
// print all comments
for (let comment of books[0].comments){
    console.log(comment.id,":", comment.text)
}
// comment winners
console.log(books[0].comwinner.join(", "))

// create sample li
let li = document.createElement("li")
let liTxtNode = document.createTextNode("aa")
li.appendChild(liTxtNode)
// append to div
let bookList = document.getElementById('bookList')
bookList.appendChild(li)
```

```js
let books = [{
    "isbn":"11111",
    "author": {
        "name":"authorname",
        "email":"author@gmail.com"
    },
    "editor": {
        "name":"editorname",
        "email":"editor@gmail.com"
    },
    "title":"abcde",
    "category": [
        "nonfiction","it","politics"
    ],
    "comments":[
        {"id":"aaa", "text":"helloworld aaa"},
        {"id":"bbb", "text":"helloworld bbb"},
        {"id":"ccc", "text":"helloworld ccc"},
        {"id":"ddd", "text":"helloworld ddd"},
        {"id":"eee", "text":"helloworld eee"}
    ],
    "comwinner":["aaa","ccc","eee"]
}]

// after window is loaded 
window.onload = () => {
    // when button is clicked
    document.getElementById('btn').addEventListener('click', function() {
        // unordered list under bookList div
        let bookList = document.getElementById('bookList')
        let ul = document.createElement("ul")
        bookList.appendChild(ul) 

        // for all comments, li element and append to list
        for (let comment of books[0].comments){
            console.log(comment)
            let commLi = document.createElement("li")
            let commText = document.createTextNode(
                comment.id+": "+comment.text)
            commLi.appendChild(commText)
            // bookList.appendChild(commLi)
            ul.appendChild(commLi)
        }
        // bookListWinner
        document.getElementById('bookListWinner').innerText
             = books[0].comwinner.join(",")

        // print ul content in console
        console.log(bookList.innerHTML)
    })
}
```
https://replit.com/@jhojin7/DarkFilthyExtraction

## Resources
- MDN docs DOM: https://developer.mozilla.org/ko/docs/Web/API/Document_Object_Model/Introduction
---
planned: 6~8
covered: 8~10
---
# ablestudy 2022-02-16
- `window.onload`event
	- 윈도우의 `load`이벤트가 불러지면 실행된다.
- `for (let ... in ...)`
- `for (let ... of ...)`
	- 파이썬이랑은 조금 틀린듯.
- `val += '${book["category"][i]} <br>';` 
	- 이게 왜 안되는지 모르겠음. 아마 repl 환경이 구형 환경이라 그런가?
	- ...라고 생각했는데, `${book["category"][i]}` 처럼 backtick으로 해야됨. (자료 두번째 링크 참고)

## Code
```js
const book = {
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
    ]
}

console.log(book["author"].name)
console.log(book["isbn"]) // book.isbn

window.onload = () => {
    console.log("onload")
    let val = "";
    // let val = book.category[0];
    // document.getElementById("aaa").innerText = val;
	
	for (let i = 0; i < book.category.length; i++){
		// val += book["category"][i];
		val += `${book["category"][i]} <br>`; // ``````
	}
		
    //     val += '${book["category"][i]} <br>';//????
    // }
    
    // for (let i in book.category)
    //     val += book.category[i] + "<br>";

    // for (let cat of book.category)
    //     val += cat + "<br>";

    document.getElementById("aaa").innerHTML = val; 
}
```

## Resources
- MDN docs .onload: https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/onload
- MDN docs  template literals: https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Template_literals#expression_interpolation%ED%91%9C%ED%98%84%EC%8B%9D_%EC%82%BD%EC%9E%85%EB%B2%95
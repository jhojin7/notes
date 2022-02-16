# ablestudy 2022-02-15
```
오늘진도: 1~5
나간진도: 1~7
```

- 선행학습
	- JSON
	- AJAX
	- JS, jQuery
	- DOM (HTML??)
	- 필요하다함.
	- 자바쪽은 안해봐서 미리 좀 봐둬야 할듯함. 
	- json 다루는데 java 없어도 그냥 텍스트 긁어와서 쓰면 되는거 아닌가 싶긴한데 일단 수업 들어보고 생각해보기로...

- Setup
	- eclipse
	- notepad++ -> vscode 쓸 예정.
	- python + sqlite3 ->설치됨.
	- bootstrap
	- 브라우저

- 공공데이터 쓰는 흐름
	- data.go.kr 같은데 들어가서 쓸 데이터 찾기
		- (활용신청을 먼저 하고 사용 승인이 나야지 쓸수있음.)
	- OpenAPI 미리보기 가능함.
		- request parameter 바꿔가면서 미리보기 가능
	- xml이나 json으로 받아서 jsp로 넘김.

- json
	- `{"key": "value", "key": "value"}` 형식
	- 객체들의 배열도 가능
	
- js 코드 https://leetcode.com/playground/TM6CnKNp
	- leetcode playground embed
	
```js

// JSON 

jss = {
    "group1": {
        "name":"honggildong",
        "age":20,
        "nationality":"KR",
        "hobby":"movie",
        "company":{
            "cname":"xx",
            "cphone":"xx",
        }
    }
}

person = [
    {"name":"aaaa", "age":"20", "nationality": "kr"},
    {"name":"bbbb", "age":"30", "nationality": "jp"},
    {"name":"cccc", "age":"40", "nationality": "us"}
]

console.log(typeof person[1]) //object
console.log(person[0].name) // aaaa

console.log(...person); //전개연산자 (spread operator)

console.log({...person}) //__proto__ array
console.log([...person]) // object
    {
      '0': { name: 'aaaa', age: '20', nationality: 'kr' },
      '1': { name: 'bbbb', age: '30', nationality: 'jp' },
      '2': { name: 'cccc', age: '40', nationality: 'us' }
    }
    [
      { name: 'aaaa', age: '20', nationality: 'kr' },
      { name: 'bbbb', age: '30', nationality: 'jp' },
      { name: 'cccc', age: '40', nationality: 'us' }
    ]

for (let i of person)
    console.log(i.name, i.age, i.nationality);

```

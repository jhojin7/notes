---
planned: 19-21
covered: 19-21
---
# ablestudy 2022-02-22
### JSON 데이터를 긁어와서 HTML로 표시
- head에 jQuery, Ajax, Bootstrap script랑 링크 추가하기.

### Bootstrap
- class만 설정하면 JS로 접근하여 편집이 가능하게 가능하게 함.
- html head에 bootstrap끼리 version 값이 일치해야지 제대로 나옴. 
- table class 설명
	- `table-dark`: dark background table
	- `table-stiped`: table with different color every other row
	- `table-hover`: changes color when hovering with mouse
	- `thead-dark`: dark background for thead only
	- https://getbootstrap.com/docs/4.1/content/tables/

### VSCode
### 브라우저로 볼 때 내용이 안 나올때 해결방법
강의에서 추가하라는 플래그를 추가 한 바로가기를 만들어서 쓰자.
 - 내가 사용하는 폴더에서 `빈공간 우클릭 -> 새로 만들기 -> 바로가기` 선택
 - '항목 위치 입력' 칸에 `"C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" --disable-web-security --user-data-dir="c:\msedge"` 입력 하고 '다음' 선택.
 (아마 edge는 기본 설치 프로그램이라 대부분 저대로 쓰면 될듯함.)
 - 파일 이름은 `msedge.exe`로 두고 '마침' 선택 

## Code
- Repo: https://github.com/jhojin7/ablestudy-public-api
- HTML: https://github.com/jhojin7/ablestudy-public-api/blob/master/index.html
- JS: https://github.com/jhojin7/ablestudy-public-api/blob/master/script.js
- Java 코드: https://github.com/jhojin7/ablestudy-public-api/blob/master/ApiExplorer.java

## Resources
- 플래그랑 같이 바로가기 만들기(크롬기준): https://alfilatov.com/posts/run-chrome-without-cors/
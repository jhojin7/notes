# Python
이런저런 잡다한 것들 모음. 쉽지만 까먹은 내용들도 여기에 정리

## String 관련
- string append `str.append(str)`


## datetime 관련
- datetime 스트링 포매팅할때 {0:%a}하면 0번째에 있는 time 클래스의 %a데이터를 출력함.
	`{0:%Y}-{0:%m}-{0:%d} {0:%a} #####".format(today)` 
	-> 2022-01-08 Sat
- 오늘날짜 구하려면 `date.today()`

## math 관련
- 소수 number를 digit만큼 남겨서 출력 `round(number, digit)`
- 소수 내림 `math.floor(number)'

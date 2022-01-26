# Python
## [[Anvil]]

## 잡동사니
이런저런 잡다한 것들 모음. 쉽지만 까먹은 내용들도 여기에 정리 (최신껄 위로)
- 콘솔 지우기 `os.system('cls')` (리눅스는 clear)

### String 관련
- string append `str.append(str)`

### datetime 관련
- datetime 스트링 포매팅할때 {0:%a}하면 0번째에 있는 time 클래스의 %a데이터를 출력함.
	`{0:%Y}-{0:%m}-{0:%d} {0:%a} #####".format(today)` 
	-> 2022-01-08 Sat
- 오늘날짜 구하려면 `date.today()`

### math 관련
- 소수 number를 digit만큼 남겨서 출력 `round(number, digit)`
- 소수 내림 `math.floor(number)`


### 파일 IO
```python
with open("fname",'w',encoding="utf-8") as f:
    f.write('')
	f.close()
#### 열고 닫기
f = open("file.txt",'w')
f.close()
#### 읽고 쓰기
f.read()
f.readline()
f.readlines()
f.write(str)
```
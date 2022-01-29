# vscode에서 raspberry-pi랑 연결하기
## Purpose
- 요근래 이것저것 끄적여보면서 vscode를 메인 에디터로 쓰게됨.
- 집에서 쓰다말다 뒹굴거리는 라즈베리파이(산딸기) 굴려보려고 다시 헤드리스로 연결 후 셋업함.
- 지금까진 WSL데비안에서 ssh로 들어가서 사용함. 이젠 vscode에서 사용하려고 함. 

## VScode Side
- `ctrl+shift+p` 누르고 terminal with profile 검색해서 나오는 걸 선택하기. 
- 본인이 사용할 쉘 선택. (raspbian 기준 초기설정을 안건드렸다면 bash)
- 밑에 새로운 창이 뜨고 새로운 쉘이 켜질 것. 
	- 터미널창 상단바에 (or 여러 쉘이 열려있다면 오른쪽에) 보이는 "bash"를 우클릭 해서 ''터미널을 편집기 영역으로 이동" 시켜줄 것.
- ~~`sudo apt-get update` `sudo apt-get update` 해주기.~~
- `sudo apt install code` 입력하면 리눅스에서 vscode설치됨 (데비안 기준)


# 라즈베리파이에 있는 로컬 코드를 vscode로 편집하기
- `ctrl+o` 파일열기
- 파일 directory 입력 + enter
- 열림..
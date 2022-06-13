# WSL2

## 현재 설치된 WSL들 확인하기
```cmd
>wsl -l -v
  NAME      STATE           VERSION
* Ubuntu    Running         1
```

## WSL1에서 WSL2로 변환하기
```
wsl --set-version Ubuntu 2
```
https://docs.microsoft.com/ko-kr/windows/wsl/install

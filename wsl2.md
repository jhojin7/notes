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

## WSL환경에서 node.js 설치하기
1. `sudo apt-get install curl`
2. 설치. `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash` 
3. `nvm --version` or `command -v nvm` or `nvm ls`
4. Install nodejs lts `nvm install --lts` 
5. check with `npm --version`

https://docs.microsoft.com/ko-kr/windows/dev-environment/javascript/nodejs-on-wsl

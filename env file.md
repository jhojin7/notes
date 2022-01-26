# `.env` File
- 환경변수 (enviornment variables) 저장하는 파일.
- 프로젝트 root directory에 저장.
- API key들이나 민감한 정보들을 따로 빼두고 gitignore하는 방향으로 사용.

- 공식 문서 예시
```
# Development settings
DOMAIN=example.org
ADMIN_EMAIL=admin@${DOMAIN}
ROOT_URL=${DOMAIN}/app
```

## Python setup
1. 설치 `pip install python-dotenv`
2. 불러오기 `load_dotenv()`, `var=os.getenv('VAR1')`
3. 

## Resources
- 공식 docs. 정리잘되있음. https://pypi.org/project/python-dotenv/

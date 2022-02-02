# `.env` File
- 환경변수 (enviornment variables) 저장하는 파일.
- 프로젝트 root directory에 저장.
- API key들이나 민감한 정보들을 따로 빼두고 gitignore하는 방향으로 사용.

## Installation, import
```
pip install python-dotenv
import os
```
- `.env` file setup. (Must be in the same directory)
```
# Development settings
DOMAIN=example.org
ADMIN_EMAIL=admin@${DOMAIN}
ROOT_URL=${DOMAIN}/app
VAR=foo
```

## Load all variables
```
from dotenv import load-dotenv
os.getenv('VAR') #os.environ('VAR')
```

## Load variables selectively
```
from dotenv import dotenv_values
config = dotenv_values('.env')
# config = {
#  "VAR": "foo"
#  }
```

## Resources
- 공식 docs. 정리잘되있음. https://pypi.org/project/python-dotenv/

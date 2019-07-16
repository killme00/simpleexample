# Python

## 명령어

### module 업데이트
```
C:\Python\v3_6_8\python -m pip install --upgrade pip
C:\Python\v3_6_8\python -m pip install --upgrade virtualenv
```

### virtualenv 생성
```
C:\Python\v3_6_8\Scripts\virtualenv.exe -p C:\Python\v3_6_8\python.exe C:\Users\kimbaek\.virtualenvs\flask_venv
```

### vscode 의 settings.json
```
{
    "python.pythonPath": "C:\\Python\\v3_6_8\\python.exe",
    "files.autoGuessEncoding": true,
    "python.linting.pylintEnabled": true,
    "python.linting.enabled": true,
    "terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe",
    "terminal.integrated.shellArgs.windows": [
        "/K",
        "SET Path=C:\\Users\\kimbaek\\.virtualenvs\\pytest_venv\\Scripts & C:\\Users\\kimbaek\\.virtualenvs\\pytest_venv\\Scripts\\activate.bat"
    ],
    "python.testing.pytestArgs": [
        "."
    ],
    "python.testing.unittestEnabled": false,
    "python.testing.nosetestsEnabled": false,
    "python.testing.pytestEnabled": true
}
```

## Articles
[Flask Vue.js Integration Tutorial](https://dev.to/michaelbukachi/flask-vue-js-integration-tutorial-2g90)

[2018 파이썬 개발자 설문조사 결과 알아보기](https://tariat.tistory.com/597)

[Pipenv: Python Development Workflow for Humans](https://github.com/pypa/pipenv)

## Anaconda 4.5.12 설치 시 SSLError 우회 대응
- installed conda 4.5.11 -> Anaconda3-5.3.1-Windows-x86_64.exe
- installed with openssl __conda install openssl__
- Added openssl to PATH
- Updated conda __conda update conda__
- Updated everything else __conda update --all__

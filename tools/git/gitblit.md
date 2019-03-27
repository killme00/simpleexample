# gitblit

[Windows 에서 git 서버 구축하기(Gitblit + Jetty)](https://www.lesstif.com/pages/viewpage.action?pageId=26084460)

## 시작
```
C:\bin\gitblit\gitblit.cmd
```

## 종료
```
C:\bin\gitblit\gitblit-stop.cmd
```

## gitblit

## 계정 - 기본값
admin / admin

[gitblit setting](http://gitblit.com/setup_go.html)

#### installService.cmd 수정
```
--StartParams="--storePassword;death100;--baseFolder;%CD%\data" ^
```

### jvm.dll 경로 지정
gitblitw.exe 을 실행하여 [Java] 탭의 'Java Virtual Machine' 경로를 변경

#### installService.cmd 실행하여 서비스 등록

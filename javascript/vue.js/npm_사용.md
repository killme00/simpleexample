# npm 사용

## npm 사용 시 에러가 날 때 조치
[출처 : npm ERR! Error: EPERM: operation not permitted, rename](https://stackoverflow.com/questions/39293636/npm-err-error-eperm-operation-not-permitted-rename)

- clean cache with
```
npm cache clean --force
```


- install the latest version of npm globally as admin:
```
npm install -g npm@latest --force
```

- clean cache with
```
npm cache clean --force
```

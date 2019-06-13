# yarn

[출처 : yarn - npm보다 빠른 노드 패키지 설치](https://eveript.tistory.com/entry/yarn-npm%EB%B3%B4%EB%8B%A4-%EB%B9%A0%EB%A5%B8-%EB%85%B8%EB%93%9C-%ED%8C%A8%ED%82%A4%EC%A7%80-%EC%84%A4%EC%B9%98)

## yarn 기본 사용법

### yarn 설치
```
$ npm install -g yarn
```

### package.json 설치
```
npm init
```
===>
```
yarn init
```

### package.json 안의 모든 패키지 설치
```
npm install
```
===>
```
yarn install
```

### 패키지 설치 후 package.json 의 dependencies 에 기록
```
npm install --save [패키지]
```
===>
```
yarn add [패키지]
```

### 패키지 설치 후 package.json 의 devDependencies 에 기록
```
npm install --save-dev [패키지]
```
===>
```
yarn add -D [패키지]
```

### 패키지 삭제 후 package.json 의 dependencies 수정
```
npm uninstall --save [패키지]
```
===>
```
yarn remove [패키지]
```

### 패키지 삭제 후 package.json 의 devDependencies 수정
```
npm uninstall --save-dev [패키지]
```
===>
```
yarn remove -D [패키지]
```

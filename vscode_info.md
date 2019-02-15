# Visual Studio Code

## 문제점

### 4k 모니터에서 색에 붉은 톤으로 나타남

#### electron 버전 확인
F1 > developer tools : console 탭에서 다음 입력
```
> process.versions.electron
```
출처 : [Provide a way to inspect what version of electron vscode is using](https://github.com/Microsoft/vscode/issues/49644)

#### Disable GPU rendering
[How can I disable GPU rendering in Visual Studio Code](https://stackoverflow.com/questions/29966747/how-can-i-disable-gpu-rendering-in-visual-studio-code/30007549)

#### visual studio code 실행 시 옵셥 추가
**하드웨어 가속 disable**
```
code.exe --disable-gpu
```

##### electron 기반인 chrome 에서의 처리
설정
```
chrome://settings
```
에서 **고급**을 선택
```
시스템 > 가능한 경우 하드웨어 가속 사용
```
선택 해제

# simpleexample

## Quick setup -- if you've done this kind of thing before
```
https://github.com/killme00/simpleexample.git
```

## create a new repository on the command line
```
echo "# simpleexample" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/killme00/simpleexample.git
git push -u origin master
```

## 설치된 윈도우 제품키 프로그램 없이 알아보기
```
https://nightly.tistory.com/99
```

## dcevm hotswap 설정

I have configured hot swap agent for multi module project. In Web project i have added hotswap-agent.properties file. In hotswap-agent.properties file added path to the service projects target directory like this

extraClasspath=D:/Sample/serviceproject/target/classes

and now it is reloading files from above mentioned directory.

[dcevm hotswap](https://stackoverflow.com/questions/32425303/hot-swap-agent-configuration-for-multi-module-project)

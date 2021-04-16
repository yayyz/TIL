# travis-ci 
github고 연동 가능한 CI/CD 툴 


## configuarion tester
yaml 기반이기 때문에 -> 대체로 여기서 확인하면 됨
http://www.yamllint.com

yaml config 에서 제공하는 tester도 있다. 아직 사용해보진 않았다!
참고: https://stackoverflow.com/questions/50551277/could-not-parse-travis-yml

## build stages + deploy to multiple envrionment! 
기존에 사용하고있는 travis-ci 파일에서는 그냥 develop 환경 기준으로 배포를 사용하고있었음. 
운영환경에 이제 배포할 준비를 해야하는데, travis-ci에섣 가능할까? -> 가능하다!
conditioanl build 라는 config를 사용하면 된다 

```yml 
- stage: deploy dev
      if: branch = develop
- stage: deploy release 
      if: branch = master
```
이런식으로 사용하면 된다. stage 옆의 값들은 그냥 빌드에 대한 naming이다. 동작과는 전혀 상관없느 내용!
if: branch = [빌드 하고자 하는 브랜치] 로 설정하고 하위에 각 환경에 따른 설정들으 추가해주면 된다. 


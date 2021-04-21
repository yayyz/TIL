# javascript 

## Object Deconstructing 
```javascript 
const { resolve } = require('bluebird') 
```
- 이런 코드가있을때, { } 가 의미하는것은 무엇일까? 
- 이것은 `Object Deconstructing`이라는 것! ES2015 규격이라고 한다. 
- bluebird 라는 모듈안에서 resolve 만을 사용하겠다! 라는 의미라고 보면 된다

예시 (stackoverflow 출처: https://stackoverflow.com/questions/33798717/javascript-es6-const-with-curly-braces) 
```javascript
const name = app.name;
const version = app.version;
const type = app.type;

// as this
const { name, version, type } = app;
```

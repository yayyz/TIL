# RESTful 

## curl to REST
- -u option을 REST로 하면? 
- 헤더 값으로 "Authorization", value 로는 "Basic [인코딩된값]" 
- 인코딩은 Base64로 

```kotlin
webClient.get().uri { uriBuilder ->
            uriBuilder
                .scheme("http")
                .host("host")
                .port("port")
                .path("path")
                .build()
        }.header("Authorization", "Basic [인코딩된값]")
            .exchange().block()
```

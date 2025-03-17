### Feign Request Interceptor Config
```
@Configuration
@Slf4j
public class FeignConfig {
    @Bean
    public Encoder feignEncoder() {
        return new SpringEncoder(() -> new HttpMessageConverters(new MappingJackson2HttpMessageConverter()));
    }

    @Bean
    public RequestInterceptor requestInterceptor() {
        return requestTemplate -> {
            log.info("Request URL: {}", requestTemplate.url());
            log.info("Request Method: {}", requestTemplate.method());
            if (requestTemplate.body() != null) {
                log.info("Request Body: {}", new String(requestTemplate.body()));
            }
            log.info("Request Headers: {}", requestTemplate.headers());
        };
    }
}
```

```

@FeignClient(name = "communicator-email",
        url = "${email.communicator.endpoint}",
        configuration = FeignConfig.class)
public interface CommunicatorClient {
...
}

```

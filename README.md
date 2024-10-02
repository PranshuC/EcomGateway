# ECommerce Project - API Gateway + Load Balancer

### Backend Project: Spring Cloud - Api G/W, Lb, Logging & Monitoring [07-03-24]
1. Create the Project - boilerplate code
2. application.properties : spring.cloud.gateway.routes
3. spring-boot-starter-actuator dependency for monitoring
http://127.0.0.1:4040/actuator/health - Health Check URL (IDE has feature too)

Map like structure in application.properties for passing routing info of services <br>
/products/ => EcomProductService <br>
/payments/ => EcomPaymentService <br>
/users/ => EcomUserService

For Authentication, API Gateway has to rely on User Service

http://127.0.0.1:4040/actuator/ : many endpoints available for metrics, threadump, config, scheduledtasks etc. <br>
Can integrate with 3rd party monitoring tools like Prometheus, Grafana, New Relic.

References : <br>
https://www.baeldung.com/spring-cloud-gateway-oauth2 <br>
https://en.wikipedia.org/wiki/Token_bucket <br>
https://www.baeldung.com/spring-cloud-gateway-rate-limit-by-client-ip <br>
https://mvnrepository.com/artifact/io.micrometer/micrometer-registry-prometheus/1.12.3 <br>
https://www.baeldung.com/spring-boot-self-hosted-monitoring <br>
https://docs.spring.io/spring-framework/reference/web/webmvc/mvc-servlet.html 
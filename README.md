# booking-business-cloud-native-service

The booking-business-cloud-native-service is the application that consumes the microservices that are already started up 
(Room and Guests cloud native). In order to do that, we will need to use "RestTemplate" like displayed below


@Configuration
@PropertySource("classpath:config/config.properties")
public class RestTemplateConfig {

    @LoadBalanced
    @Bean
    public RestTemplate getRestTemplate(){
        return new RestTemplate();
    }
}


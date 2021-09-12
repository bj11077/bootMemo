## CORS정리

    @RestController
    
    @CrossOrigin(origins = "http://localhost:18080")
    @GetMapping("/hello")
    public String hello(){
        return "hello";
    }
    
    해당코드와같이 CrossOrigin을 설정해줘야 hello라는 정보를 18080에서 요청해서가져올수잇음
    
    
    
## 전역설정

    @Configuration
    public class WebConfig implements WebMvcConfigurer {

    @Override
    public void addCorsMappings(CorsRegistry registry) {
        registry.addMapping("/**").allowedOrigins("http://localhost:18080");
    }
    }

해당 클래스처럼 설정파일을만들어서 addCorsMappings만 오버라이드 ( 다른설정들은 그냥사용하면서 이거만바꾸는것)

## CORS정리

    @RestController
    
    @CrossOrigin(origins = "http://localhost:18080")
    @GetMapping("/hello")
    public String hello(){
        return "hello";
    }
    
    해당코드와같이 CrossOrigin을 설정해줘야 hello라는 정보를 18080에서 요청해서가져올수잇음

Passo 1: Configuração da API com um Controller
Crie ou verifique se já possui uma API funcional com Spring Boot.
Certifique-se de que existe pelo menos um Controller na API, com alguns métodos para serem documentados.
Exemplo de um Controller simples:


@RestController
@RequestMapping("/api")
public class ExampleController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, World!";
    }

    @GetMapping("/greet/{name}")
    public String greet(@PathVariable String name) {
        return "Hello, " + name + "!";
    }
}


Passo 2: Adicionar a dependência Springdoc no pom.xml
Abra o arquivo pom.xml do seu projeto.
Adicione a dependência da Springdoc:

<dependency>
    <groupId>org.springdoc</groupId>
    <artifactId>springdoc-openapi-ui</artifactId>
    <version>1.6.15</version>
</dependency>

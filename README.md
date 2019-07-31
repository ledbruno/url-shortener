# url-shortener Spring Boot

### Descrição
Este projeto contém endpoints que fazem o encurtamento de uma varíavel e possibilitam o redirecionamento para a URL original.
Uma URL é mantida por um determinado tempo, até expirar. Implementado com Spring Boot. 

### Requisitos
* [Java 8+](https://www.java.com)
* [Apache Maven](https://maven.apache.org)
* [Docker](https://docker.com) (opcional)

### Build

No diretório do projeto, executar:

```
$ mvn clean install
``` 

### Configuração

O tempo default de expiração de uma URL encurtada é de **60** segundos. 
Para definir outro valor, informar a propriedade `expirationTimeMillis`.

Ex: `-DexpirationTimeMillis=120000` (2 minutos)

### Utilização

No diretório do projeto, executar:

```
$ mvn spring-boot:run -Dspring-boot.run.jvmArguments="-DexpirationTimeMillis=60000"
``` 

### Testes

* Acessar via browser: [http://localhost:8080/index.html](http://localhost:8080/index.html)

* Para encurtar uma url, utilizar o comando abaixo:

```
$ curl -v -X POST http://localhost:8080/create-url?url=http://www.google.com
``` 

* Para ser redirecionado a URL original, utilizar o comando abaixo:

```
$ curl -v -L -X GET http://localhost:8080/4170157c
```

### Referência:

[https://github.com/ledbruno/desafios/tree/master/1%20-%20Easy/Encurtador%20de%20URL](https://github.com/ledbruno/desafios/tree/master/1%20-%20Easy/Encurtador%20de%20URL)
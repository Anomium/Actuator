# Actuator


## ¿Que es?

_Spring Boot Actuator es una librería que nos proporciona herramientas de monitorización y administración de nuestra API REST de una manera bastante sencilla._

## ¿Para que sirve?

_Lo que hace es organizar una serie de endpoints REST, a través de un proyecto complementario de una aplicación web, dónde podemos acceder a diferente información de monitorización para revisar el estado de nuestra API REST en muchos ámbitos diferentes._

### Instalación 🔧

_Para incluir dentro de nuestra API REST esta librería, tan solo tenemos que añadir esta dependencia maven starter:_
```
<dependency>
   <groupId>org.springframework.boot</groupId>
   <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```
_Una vez incluida la dependencia se habilitan varios endpoints de actuator, para activar mas incluimos las siguientes líneas en el yml_
```
management:  
  endpoints:
    web:
      exposure:
        include: "*"
```

_Si queremos, podemos hacer que cada actuator nos muestre una información más detallada que la que muestra por defecto._
_Por ejemplo, el actuator health, por defecto, solo muestra si la aplicación está levantada o no. Para ver más información sobre la misma, debemos establecer la siguiente propiedad:_
```
management:
  endpoint:
    shutdown:
      enabled: true
    health:
      show-details: always
```
## Versionado 📌
Actuator [Versiones](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-actuator)
## Autor
**Andrés Villanueva** - [Fuente](https://openwebinars.net/blog/como-anadir-spring-boot-actuator-tu-proyecto/)

# Herramientas de desarrollo
El software de ALA fue desarrollado con varias herramientas. Una de las principales es [Grails](https://grails.org/), un marco de trabajo para desarrollo de aplicaciones en la Web basado en el lenguaje de programación [Groovy](https://groovy-lang.org/) y que se ejecuta en la [máquina virtual de Java (JVM)](https://en.wikipedia.org/wiki/Java_virtual_machine). Fue construído sobre otro marco de trabajo llamado [Spring Boot](https://spring.io/projects/spring-boot).

A continuación, se presenta el proceso de instalación de Grails mediante SDKMAN!, en el sistema operativo Ubuntu 18.04.3 LTS.

## Instalación de Grails y herramientas asociadas mediante SDKMAN!
El [Software Development Kit Manager (SDKMAN!)](https://sdkman.io/) permite instalar y administrar varias herramientas de desarrollo (ej. Java, Groovy) desde la línea de comandos en sistemas Unix. Entre sus ventajas, está la capacidad de mantener varias versiones de la misma herramienta.

### Instalación de SDKMAN!
Las instrucciones detalladas pueden consultarse en [https://sdkman.io/install](https://sdkman.io/install). 

Desde una terminal del sistema operativo, deben ejecutarse los comandos:
```
$ cd
$ curl -s https://get.sdkman.io | bash
$ source "$HOME/.sdkman/bin/sdkman-init.sh"
```

Para verificar la versión instalada:
```
$ sdk version
```

Las herramientas instaladas mediante SDKMAN! quedan almacenadas en el directorio ~/.sdkman/candidates/

### Instalación de Java
### Instalación de Gradle
### Instalación de Grails

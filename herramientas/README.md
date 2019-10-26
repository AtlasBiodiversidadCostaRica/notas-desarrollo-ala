# Herramientas de desarrollo
El software de ALA fue desarrollado con varias herramientas. Una de las principales es [Grails](https://grails.org/), un marco de trabajo para desarrollo de aplicaciones en la Web basado en el lenguaje de programación [Groovy](https://groovy-lang.org/) y que se ejecuta en la [máquina virtual de Java (JVM)](https://en.wikipedia.org/wiki/Java_virtual_machine). Fue construído sobre otro marco de trabajo llamado [Spring Boot](https://spring.io/projects/spring-boot).

A continuación, se presenta el proceso de instalación de Grails, mediante SDKMAN!, en el sistema operativo Ubuntu 18.04.3 LTS.

## Instalación de Grails y herramientas asociadas mediante SDKMAN!
El [Software Development Kit Manager (SDKMAN!)](https://sdkman.io/) permite instalar y administrar varias herramientas de desarrollo (ej. Java, Groovy) desde la línea de comandos en sistemas Unix. Entre sus ventajas, está la capacidad de mantener varias versiones de la misma herramienta.

### Instalación de SDKMAN!
Las instrucciones detalladas pueden consultarse en [https://sdkman.io/install](https://sdkman.io/install). 

Desde una terminal del sistema operativo, deben ejecutarse los siguientes comandos.

Instalación de zip:
```
$ sudo apt install zip -y
```

Instalación de SDKMAN!:
```
$ cd
$ curl -s https://get.sdkman.io | bash
$ source "$HOME/.sdkman/bin/sdkman-init.sh"
```

Para verificar la versión instalada:
```
$ sdk version
```
En octubre de 2019, la versión de SDKMAN! es 5.7.3+337

**Notas sobre el uso de SDKMAN!:**

Hay una guía detallada en [https://sdkman.io/usage](https://sdkman.io/usage). Se resumen a continuación algunos de los principales comandos.

```
$ sdk help                   # Obtención de ayuda
$ sdk version                # Versión instalada de SDKMAN!
$ sdk selfupdate [force]     # Instala una nueva versión de SDKMAN!. [force] fuerza la reinstalación aún si no hay una nueva versión disponible.
$ sdk install java           # Instalación de la última versión estable de un SDK
$ sdk install scala 2.12.1   # Instalación de una versión específica de un SDK
$ sdk uninstall scala 2.11.6 # Desinstalación de una versión específica de un SDK
$ sdk list                   # Lista de versiones disponibles de todos los SDK
$ sdk list groovy            # Lista de versiones disponibles de un SDK
$ sdk use scala 2.12.1       # Selección de una versión para uso en la terminal actual
$ sdk default scala 2.11.6   # Selección de una versión por defecto
$ sdk current java           # Versión en uso de un SDK
$ sdk upgrade                # Lista de versiones a las que pueden actualizarse todos los SDK
$ sdk upgrade springboot     # Lista de versiones a las que puede actualizarse un SDK
```

Las herramientas instaladas mediante SDKMAN! quedan almacenadas en el directorio:
```
~/.sdkman/candidates/
```

### Instalación de Java
### Instalación de Gradle
### Instalación de Grails

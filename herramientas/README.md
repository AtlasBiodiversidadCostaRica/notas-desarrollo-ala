# Herramientas de desarrollo
El software de ALA fue desarrollado con varias herramientas. Una de las principales es [Grails](https://grails.org/), un marco de trabajo para desarrollo de aplicaciones en la Web basado en el lenguaje de programación [Groovy](https://groovy-lang.org/) y que se ejecuta en la [Máquina Virtual de Java (JVM)](https://en.wikipedia.org/wiki/Java_virtual_machine). Fue construído sobre otro marco de trabajo llamado [Spring Boot](https://spring.io/projects/spring-boot).

A continuación, se presenta el proceso de instalación de Grails, mediante SDKMAN!, en el sistema operativo [Ubuntu 18.04.3 LTS (Bionic Beaver)](http://releases.ubuntu.com/18.04/).

## Instalación de Grails y SDK asociados mediante SDKMAN!
El [Software Development Kit Manager (SDKMAN!)](https://sdkman.io/) permite instalar y administrar varios SDK (Software Development Kit), tales como Java, Groovy, Grails y otros, desde la línea de comandos de sistemas Unix. Entre sus ventajas, está la capacidad de mantener varias versiones del mismo SDK.

### Instalación de SDKMAN!
Las instrucciones detalladas pueden consultarse en [https://sdkman.io/install](https://sdkman.io/install). Se resumen aquí los principales pasos.

Instalación del paquete zip (es necesaria para el siguiente paso):
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

### Notas sobre el uso y configuración de SDKMAN!

Hay una guía detallada en [https://sdkman.io/usage](https://sdkman.io/usage). Se resumen a continuación algunos de los principales comandos.

```
$ sdk help                   # Obtención de ayuda
$ sdk version                # Versión instalada de SDKMAN!
$ sdk selfupdate [force]     # Instala una nueva versión de SDKMAN!. [force] fuerza la reinstalación aún si no hay una nueva versión disponible.
$ sdk install java           # Instalación de la última versión estable de un SDK
$ sdk install scala 2.12.1   # Instalación de una versión específica de un SDK
$ sdk uninstall scala 2.11.6 # Desinstalación de una versión específica de un SDK
$ sdk list                   # Lista de todos los SDK disponibles para instalar
$ sdk list groovy            # Lista de versiones disponibles de un SDK
$ sdk use scala 2.12.1       # Selección de una versión para uso en la terminal actual
$ sdk default scala 2.11.6   # Selección de una versión por defecto
$ sdk current java           # Versión en uso de un SDK
$ sdk upgrade                # Lista de versiones a las que pueden actualizarse todos los SDK
$ sdk upgrade springboot     # Lista de versiones a las que puede actualizarse un SDK
```

Los SDK instalados quedan almacenados en el directorio:
```
~/.sdkman/candidates/
```

El archivo de configuración está ubicado en ```~/.sdkman/etc/config```. El siguiente es un ejemplo de su contenido:
```
sdkman_auto_answer=false
sdkman_auto_selfupdate=false
sdkman_insecure_ssl=false
sdkman_curl_connect_timeout=7
sdkman_curl_max_time=10
sdkman_beta_channel=false
sdkman_debug_mode=false
sdkman_colour_enable=true
```

### Instalación de Java
### Instalación de Gradle
### Instalación de Grails

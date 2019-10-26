# Herramientas de desarrollo
El software de ALA fue desarrollado con varias herramientas. Una de las principales es [Grails](https://grails.org/), un marco de trabajo para desarrollo de aplicaciones en la Web basado en el lenguaje de programación [Groovy](https://groovy-lang.org/) y que se ejecuta en la [Máquina Virtual de Java (JVM)](https://en.wikipedia.org/wiki/Java_virtual_machine). Fue construído sobre otro marco de trabajo llamado [Spring Boot](https://spring.io/projects/spring-boot).

A continuación, se presenta el proceso de instalación de Grails, mediante SDKMAN!, en el sistema operativo [Ubuntu 18.04.3 LTS (Bionic Beaver)](http://releases.ubuntu.com/18.04/).

## Instalación de Grails y SDK asociados mediante SDKMAN!
El [Software Development Kit Manager (SDKMAN!)](https://sdkman.io/) permite instalar y administrar varios SDK (Software Development Kit), tales como Java, Groovy, Grails y otros, desde la línea de comandos de sistemas Unix. Entre sus ventajas, está la capacidad de mantener varias versiones del mismo SDK.

Para instalar Grails mediante SDKMAN!, deben instalarse antes el Java Development Kit y el sistema Maven para automatización de construcción de código abierto.

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

Hay una guía detallada en [https://sdkman.io/usage](https://sdkman.io/usage). Se ejemplifican a continuación algunos de los principales comandos.

```
$ sdk help                   # Ayuda
$ sdk version                # Versión instalada de SDKMAN!
$ sdk selfupdate [force]     # Instalación de una nueva versión de SDKMAN!. [force] fuerza la reinstalación aún si no hay una nueva versión disponible.
$ sdk install java           # Instalación de la última versión estable de un SDK
$ sdk install scala 2.12.1   # Instalación de una versión específica de un SDK
$ sdk uninstall scala 2.11.6 # Desinstalación de una versión específica de un SDK
$ sdk list                   # Listado de todos los SDK disponibles para instalar
$ sdk list groovy            # Listado de versiones disponibles de un SDK
$ sdk use scala 2.12.1       # Selección de una versión para uso en la terminal actual
$ sdk default scala 2.11.6   # Selección de una versión por defecto
$ sdk current java           # Versión en uso de un SDK
$ sdk upgrade                # Listado de versiones a las que pueden actualizarse todos los SDK
$ sdk upgrade springboot     # Listado de versiones a las que puede actualizarse un SDK
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

### Instalación de Java Development Kit (JDK)
El [Java Development Kit (JDK)](https://www.oracle.com/technetwork/java/) es una implementación de la plataforma [Java](https://www.oracle.com/java/) que incluye una JVM y otros recursos para el desarrollo de aplicaciones. La edición que se incluye en SDKMAN! es [Java Platform, Standard Edition (Java SE)](https://www.oracle.com/technetwork/java/javase/overview/).

Para instalar el JDK, debe ejecutarse el comando:
```
# Versión probada para el desarrollo con los módulos de ALA, en octubre 2019
$ sdk install java 8.0.232-zulu
```

Puede comprobarse la instalación con el comando:
```
$ java -version
openjdk version "1.8.0_232"
OpenJDK Runtime Environment (Zulu 8.42.0.21-CA-linux64) (build 1.8.0_232-b18)
OpenJDK 64-Bit Server VM (Zulu 8.42.0.21-CA-linux64) (build 25.232-b18, mixed mode)
```

### Instalación de Gradle
[Gradle](https://gradle.org/) es un sistema de automatización de construcción de código abierto basado en el lenguaje Groovy. Es utilizado por Grails.

Para instalar Gradle:
```
# Versión probada para el desarrollo con los módulos de ALA, en octubre 2019
$ sdk install gradle 3.4.1
```

Puede comprobarse la instalación con el comando:
```
$ gradle -v
------------------------------------------------------------
Gradle 3.4.1
------------------------------------------------------------
```

### Instalación de Grails
Se instala con el comando:
```
# Versión probada para el desarrollo con los módulos de ALA, en octubre 2019
$ sdk install grails 3.2.11
```
**NOTA:** En el caso del software de ALA, la versión de Grails puede verse en los archivos ```application.properties``` o ```gradle.properties```. Por ejemplo en:

[https://github.com/AtlasOfLivingAustralia/bie-index/blob/master/gradle.properties](https://github.com/AtlasOfLivingAustralia/bie-index/blob/master/gradle.properties)

[https://github.com/AtlasOfLivingAustralia/ala-bie/blob/master/gradle.properties](https://github.com/AtlasOfLivingAustralia/ala-bie/blob/master/gradle.properties)

Puede comprobarse la instalación con el comando:
```
$ grails -v
| Grails Version: 3.2.11
| Groovy Version: 2.4.11
| JVM Version: 1.8.0_232
```

# Maven

![Maven](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/maven.png?token=AIOFQT67HF2M57M44OJCVHC5SDRF2 "Logo de Maven")

Maven es un software de administración y herramienta de comprensión basada en el concepto de Project Object Model (POM) el cual puede administrar la creación de un proyecto, los reportes y documentación desde una pieza central de información.

## Archivos POM

![POM](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Project-Object-Model.jpg?token=AIOFQT4MGPVPWWDN5NDSCUK5SDQUS "Archivos POM")

Son archivos XML que contienen información acerca del proyecto y detalles de configuración usados por Maven para construir el proyecto (ubicación de códigos fuente, dependencias del proyecto, etc.). El archivo debe de ser llamado `pom.xml` y estar ubicado en la carpeta raíz del proyecto. Cuando se ejecuta una tarea u objetivo, Maven lee el POM, obtiene la información necesaria de la configuración y entonces ejecuta el objetivo.

## ¿Qué querían los creadores de Maven?

- Una manera estandar para construir proyectos.
- Una definición clara sobre que consisten los proyectos.
- Una manera fácil de publicar información acerca de los proyectos y compartir los `.jar` a través de multiples proyectos.

El resultado es una herramienta capaz de administrar cualquier proyecto basado en Java, con la intención el trabajo diario de los desarrolladores en Java más fácil y ayudar de manera general con la comprensión de cualquier proyecto basado en Java.

## Objetivos de Maven

- Hacer el proceso de construcción sencillo.
- Proveer una construcción uniforme de sistemas.
- Proveer información de calidad acerca del proyecto.
- Proveer lineamientos para mejorar las prácticas de desarrollo.
- Permitir la migración transparente a nuevas características.

## Instalar Maven

En tu línea de comandos ingresa el siguiente comando:

    $ sudo apt install maven

Para revisar la versión que tienes usa `mvn -v`

## Hola mundo con IntelliJ y Maven

El primer paso es abrir nuestro IDE IntelliJ y crear un nuevo proyecto.

![IDE](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso1.png?token=AIOFQT4T2TU72XSGINMWU3C5SGUDU "Nuevo proyecto")

En la parte izquierda se encuentra un panel donde podemos seleccionar el tipo del proyecto, en este caso vamos a seleccionar la opción `Maven`. Podemos escoger la versión del JDK y abajo nos aparece una opción para crear el proyecto en base en un arquetipo, que son plantillas de proyectos que ya han sido creadas. Seleccionamos `maven-archetype-quickstart` para empezar con nuestro "Hola Mundo".

![Proyecto](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso2.png?token=AIOFQT5LZDN5YFNOL2UNE2K5SGUYO "Arquetipo")

Asignamos los nombres de los paquetes.

![Paquetes](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso3.png?token=AIOFQT2IT2M74AHS7PEOWKS5SGVB4 "Identificadores")

Escogemos el directorio donde se encuentra Maven, en este caso si no aparece nada, podemos instalarlo con el comando que se mostró en un apartado anterior. Para este ejemplo se está usando la versión 3.6.0.

![Versión](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso4.png?token=AIOFQT6UQCFWLSPP6GWJSEC5SGVJK "Versión de Maven")

Asignamos el nombre del proyecto, por defecto tendrá el mismo nombre del `ArtifactId` que asignamos con anterioridad.

![Nombre](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso5.png?token=AIOFQTZSGGLBFUY5XCFJZPC5SGVO2 "Nombre del proyecto")

Cuando se abre nuestro proyecto nos aparecerá un mensaje preguntando si queremos activar las importaciones automáticas, podemos hacerlo para que cada vez que añadamos una dependencia a nuestro archivo POM se agreguen de manera automática.

![Import](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso6.png?token=AIOFQT26UGA5YTNDIRGK2HS5SGVXC "Auto import")

El primero archivo que vemos al abrir nuestro proyecto por primera vez es nuestro POM, podemos ver todos los datos que ingresamos al momento de crear el proyecto.

    <?xml version="1.0" encoding="UTF-8"?>

    <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
      <modelVersion>4.0.0</modelVersion>

      <groupId>MavenHolaMundo</groupId>
      <artifactId>mhm</artifactId>
      <version>1.0-SNAPSHOT</version>

      <name>mhm</name>
      <!-- FIXME change it to the project's website -->
      <url>http://www.example.com</url>

      <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <maven.compiler.source>1.7</maven.compiler.source>
        <maven.compiler.target>1.7</maven.compiler.target>
      </properties>
    </project>
    
 Podemos ver el nombre del esquema, su ubicacón y su versión, al igual que el identificador de grupo y artefacto.
 
     <plugin>
              <artifactId>maven-clean-plugin</artifactId>
              <version>3.1.0</version>
            </plugin>
            <!-- default lifecycle, jar packaging: see https://maven.apache.org/ref/current/maven-core/default-bindings.html#Plugin_bindings_for_jar_packaging -->
            <plugin>
              <artifactId>maven-resources-plugin</artifactId>
              <version>3.0.2</version>
            </plugin>
            <plugin>
              <artifactId>maven-compiler-plugin</artifactId>
              <version>3.8.0</version>
            </plugin>
            
También se encuentran los plugins necesarios para cumplir los objetivos de Maven.

En la ventana de nuestro proyecto podemos ver que se encuentran todas las carpetas y archivos, como podemos observar, además de nuestro programa se encuentra una carpeta dedicada a las pruebas.

![Navegador](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso7.png?token=AIOFQT6T5VZHXYGKNNC33YK5SGWUO "Main y test")

En la ventana de Maven podemos ver todos los objetivos que tiene el proyecto al igual que los plugins que estamos utilizando, podemos ejecutar cada objetivo de manera individual.

![Maven](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso8.png?token=AIOFQTYZSRG3UQ3WSGOH2GC5SGW4S "Objetivos y plugins")

Al momento de seleccionar y ejecutar un objetivos nos desplegará toda la infomación de los procesos que se están realizando, en este ejemplo se seleccionó `build`.

![Build](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso9.png?token=AIOFQTYPMBRZWLWRJRYCWK25SGXJC "Objetivo build")

Así se ven los códigos de nuestra aplicación y su prueba.

    package MavenHolaMundo;

    public class App 
    {
        public static void main( String[] args )
        {
            System.out.println( "Hello World!" );
        }
    }
    
    package MavenHolaMundo;
    import static org.junit.Assert.assertTrue;
    import org.junit.Test;


    public class AppTest 
    {
        @Test
        public void shouldAnswerWithTrue()
        {
            assertTrue( true );
        }
    }
    
Resultados obtenidos después de correrlos:

![Main](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso10.png?token=AIOFQT63LFRPUDV3QDEGOFS5SGX2Q "App")
![Test](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso11.png?token=AIOFQT2FNITQBXLD6RKHVCS5SGX3E "Test")

## Trabajando con multimodulos

Los proyectos multimódulo(o proyectos aggregator) recogen todos los módulos disponibles para ser ejecutados y los ordena para hacer un build de cada uno, cabe notar que cada módulo cuenta con su propio `POM`.

Para crear un nuevo módulo en IntelliJ hacemos lo siguiente: 

`File -> New -> Module...`

De la misma manera que creamos un nuevo proyecto, nos aparecerá una ventana donde podemos seleccionar el tipo de módulo, en este caso seleccionamos Maven, el `JDK`, y un arquetipo si así lo queremos.

![Módulo](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso12.png?token=AIOFQT5FCGTIE7EIKDUOCES5SG5M6 "Creación de un módulo")

En la siguiente ventana podemos seleccionar si queremos añadirlo como un módulo de otro proyecto y asignarle un padre, asi como indicar un id de artefacto, en este caso escogemos nuestro proyecto `Hola mundo`.

![Padre](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso13.png?token=AIOFQT2U6BU5HDLII272RAK5SG5YM "Padre y módulo")

Escogemos entre los proyectos existentes:

![Añadir](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso14.png?token=AIOFQT5JSDYE5VHIG7KMEIC5SG54S "Selección de proyectos")

Asignamos el nombre al módulo y también podemos ver la ubicación de los contenidos.

![Ubicación](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso15.png?token=AIOFQT7WTXKA4JHIAYTVJNS5SG6B6 "Nombre y contenido")

Después de crear el nuevo módulo podemos observar que en nuestro proyecto principal se añadió una nueva carpeta del nuevo módulo. 

![hijo](https://raw.githubusercontent.com/AlfonsoLVG/POO/master/Maven/Imagenes/Paso16.png?token=AIOFQTZMEG3RO2IWC5TJCTC5SG6GQ "Proyecto hijo") 

    <?xml version="1.0" encoding="UTF-8"?>
    <project xmlns="http://maven.apache.org/POM/4.0.0"
             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
        <parent>
            <artifactId>mhm</artifactId>
            <groupId>MavenHolaMundo</groupId>
            <version>1.0-SNAPSHOT</version>
        </parent>
        <modelVersion>4.0.0</modelVersion>
        <artifactId>mhijo</artifactId>
    </project>
    
Así se ve el archivo POM del nuevo módulo y podemos observar la información sobre su padre.

    <groupId>MavenHolaMundo</groupId>
    <artifactId>mhm</artifactId>
    <packaging>pom</packaging>
    <version>1.0-SNAPSHOT</version>
    <modules>
        <module>mhijo</module>
    </modules>
    
Como hemos añadido un nuevo módulo así se ve ahora el POM del proyecto padre.



#### Links 
https://howtodoinjava.com/maven/maven-pom-files/

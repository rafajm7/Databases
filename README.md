# Bases de datos SQL y NoSQL
El objetivo de este repositorio es resolver una serie de ejercicios en cinco bases de datos distintas para que se puedan observar las diferencias entre ellas y sirva como referencia para obtener ejemplos de cómo traducir consultas de unas bases de datos a otras.

Las bases de datos que se han usado son:

* MySQL: base de datos relacional.
* MongoDB: base de datos basada en documentos.
* HBase: base de datos columnar.
* Neo4j: base de datos basada en grafos.
* Redis: base de datos de tipo clave-valor.

Para cada una de las bases de datos anteriores, se seguirá la siguiente estrategia:

1. Los datos que se usarán son unos ficheros .csv que contienen información sobre la web de StackOverflow en español. Estos se dividen en posts (preguntas o respuestas), usuarios, comentarios, votos y tags. Estos ficheros están en la carpeta principal del proyecto.
2. Antes de pasar a la realización de los ejercicios, debemos leer estos datos y conformar las estructuras que se consideren necesarias dependiendo de la base de datos en la que estemos.
3. Una vez leídos los datos, se realizarán una serie de consultas sobre los mismos, y podremos ver cómo cada base de datos es capaz de resolverlas de manera distinta.

### Instrucciones de instalación y ejecución

Cada carpeta correspondiente a una base de datos distinta contiene un fichero docker-compose.yml. Este fichero se ejecuta con el comando:
```shell
sudo docker-compose up
```
El cometido de este fichero es crear un contenedor en el que instalamos la base de datos. Esta es una forma rápida y sencilla de trabajar con las bases de datos, ya que no tienes que instalarlas explícitamente en tu sistema, sino que únicamente tienes que ejecutar el contenedor.

Una vez lo ejecutamos, se abre automáticamente un Jupyter Notebook que contiene todo el código. Dentro de ese notebook, y con la base de datos ya instalada, hemos utilizado una serie de APIs que tiene cada una de ellas para poder ejecutarlas en Python.

Los datos están disponibles en la web ![http://neuromancer.inf.um.es:8080/es.stackoverflow/](http://neuromancer.inf.um.es:8080/es.stackoverflow/), pero el código de cada uno de los notebooks se encarga de descargar los ficheros .csv y añadirlos a la carpeta principal del proyecto.

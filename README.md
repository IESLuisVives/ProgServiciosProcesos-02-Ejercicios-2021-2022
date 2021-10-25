# Programación de Servicios y Procesos - 02 - Ejercicios - 2021-2022
Programación de Servicios y Procesos - 02 Programación Multihilo. 2DAM. Ejercicios realizados por el alumnado. Curso 2021-2022


![imagen](https://antarestrade.world/wp-content/uploads/2020/08/Blockcain-Seo.png)

## ¿Cómo Colaborar?
Estos ejercicios están resueltos por el alumnado y están basados en la relación de la [Unidad 2: Programación Multihilo](https://github.com/joseluisgs/ProgServiciosProcesos-02-2021-2022).

Para subir tu ejercicio a GitHub, **POR FAVOR SIGUE ESTAS NORMAS**:

- Hazte un fork de este repositorio
- Trabaja con GitFlow
- Crea una reama feature con tu Iniciales y apellido y el nombre del problema realizado por el profesor, por ejemplo: /feature/JLGonzalez/cajas-executor
- Crea un directorio dentro del directorio del problema del repositorio con tu Iniciales y Apellido, por ejemplo cajas-executor/JLGonzalez. 
- Copia tu proyecto de IntellIJ creado y gestionado con Maven a tu directorio creado. Debes tener en cuenta que el gitignore de ese proyecto debe evitar subir el directorio /out y /target de Intellij.
- Cierra la Feature siguiendo el flujo de GitFlow, fusionando los cambios a Develop, pero no borres esa rama por si la vuelves a necesitar.
- Confirma los cambios y sube los cambios a tu repositorio GitHub.
- Hazme un pull request para que acepte los cambios y explícame dichos cambios en la rama **Develop** en tu commit.
- Aplica las acciones oportunas para tener todo sincronizado.
- **SI NO SE SIGUEN ESTAS NORMAS SE TE INVALIDARÁ EN PULL REQUEST. PIENSA QUE ES POR EL BIEN DE TODOS/AS Y TU EJERCICIO CONSTARÁ COMO NO ENTREGADO.**
- **ESTE REPOSITORIO SIRVE PARA TENER DISTINTOS PUNTOS DE VISTA, PUEDEN QUE FALLEN SI LOS PRUEBAS O QUE UN ERROR PERJUDIQUE A OTROS FICHEROS.** Te aconsejo que los pruebes en un proyecto vació con la estructuras de directorios propuesta, llamándolo main.ts y usando el módulo que necesite para que no arrastre errores a otros ficheros o problemas. Cualquier duda usa Discord o pregunta en clase.

!!! FIN !!! 😀 🤝

## Problemas

### Cajas y Colas. Multihilo con Executer
Nos van a contratar para simular el sistema de atención al cliente en un supermercado, para eso queremos obtener los tiempos de ejecución en determinadas situaciones. Vamos a crear una aplicación llamada super.jar, donde la llamaremos con los parámetros nº de cajas y número de clientes. Por ejemplo java -jar super.ja3 3 21


Gestionaremos con un Pool de Hilos Workers que serán nuestras cajas disponibles. Tendremos una COLA de objetos del tipo Clientes que a su vez tiene un Carro con un máximo de 1 a 30 Productos. Cada Producto tiene asociado un tiempo de procesamiento en la caja de 1 a 5 segundos.

Programa este ejemplo usando programación concurrente. Echa un ojo al tiempo que se tardaría y compáralo con el mismo ejemplo usando programación secuencial. Lo ideal es que crees antes todos los datos y hagas dos métodos (para que trabajen con los mismos datos de número de productos 
y tiempos de productos) y los ejecutes en dos métodos, uno secuencia y otro concurrente. Repite varias veces.

Pista: Debéis tener Caja ,Clientes que es una Cola, El Cliente, El Cliente tiene un Carro y el Carro está compuesto de Productos

Entrega 14/10/2021

### Procesando RSS con asíncronía.
Vamos a realizar un Parser XML asíncrono, usando a librería que prefieras.
Lanzaremos tres trabajos asíncronos de manera asíncrona leyendo estos RSS del El País:
- Últimas Noticias: http://ep00.epimg.net/rss/tags/ultimas_noticias.xml
- Tecnología: https://feeds.elpais.com/mrss-s/pages/ep/site/elpais.com/section/tecnologia/portada
- Ciencia: https://feeds.elpais.com/mrss-s/pages/ep/site/elpais.com/section/ciencia/portada

Una vez terminen los tres, irás mostrando su resultado por pantalla. Es importante que midas el tiempo que tarda cada uno, y el tiempo total de la aplicación, ¿Con cuál casa o se corresponde? ¿Y si lo comparas con su ejecución secuencial?

Entrega 21/10/2021

### Cajas Productor Consumidor.
Vamos a realizar un simulacro de nuestras cajas de supermercado con la filosofía del productor consumidor.
Tendremos dos Productores de Clientes que producirán Clientes en tiempos aleatorios entre 500 y 1000ms de forma aleatoria. Los asignarán a la cola, siempre que haya espacio disponible. 
Tendremos 3 cajeras/os que procesan los clientes. El tiempo del procesamiento de cada cliente viene dado al procesar su carro y procesar la pila de productos que tienen entre 1 y 10, de forma aleatoria. Cada producto tiene un tiempo entre 100 y 500ms de forma aleatoria.
Nuestra cola de clientes, tiene un tamaño máximo de 10. No se puede producir más, si está llena ni consumir de ella cuando esté vacía.
Cada productor producirá 15 clientes cada uno de ellos.
El programa terminará cuando se haya procesado todos los carros. Se debe mostrar cuantos carros ha procesado cada cajera.

Una vez te funcione, intenta generalizar el programa para que funcione con N Productores, M Cajeras/as, Cola de Tamaño J, Carros con Pila de Tamaño T.

Usa Workers en donde creas que es posible


Entrega 02/11/2021


## Autor

Codificado con :sparkling_heart: por [José Luis González Sánchez](https://twitter.com/joseluisgonsan)

[![Twitter](https://img.shields.io/twitter/follow/joseluisgonsan?style=social)](https://twitter.com/joseluisgonsan)
[![GitHub](https://img.shields.io/github/followers/joseluisgs?style=social)](https://github.com/joseluisgs)

### Contacto
<p>
  Cualquier cosa que necesites házmelo saber por si puedo ayudarte 💬.
</p>
<p>
    <a href="https://twitter.com/joseluisgonsan" target="_blank">
        <img src="https://i.imgur.com/U4Uiaef.png" 
    height="30">
    </a> &nbsp;&nbsp;
    <a href="https://github.com/joseluisgs" target="_blank">
        <img src="https://cdn.iconscout.com/icon/free/png-256/github-153-675523.png" 
    height="30">
    </a> &nbsp;&nbsp;
    <a href="https://www.linkedin.com/in/joseluisgonsan" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/768px-LinkedIn_logo_initials.png" 
    height="30">
    </a>  &nbsp;&nbsp;
    <a href="https://joseluisgs.github.io/" target="_blank">
        <img src="https://joseluisgs.github.io/favicon.png" 
    height="30">
    </a>
</p>

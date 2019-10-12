# MCOC-Proyecto2
repositorio destinado a la entrega 4 del ramo MCOC

Introduccion

Introducción
En esta entrega del proyecto 2 (individual) se va a implementar y validar un código que busca simular el transporte de sedimentos en el fondo de un a corriente de agua, mediante un método Lagrangiano, que sigue a cada partícula individualmente. Se evaluó el comportamiento de múltiples números de partículas:2,5,10 y20. Por otro lado , se busca observar cómo influyen las decisiones del algoritmo de implementación y los métodos de input-output en el rendimiento del programa.
Esto anterior se conoce como complejidad computacional debido a que son una serie de raciocinios que debe llevar a cabo el algoritmo que pueden hacer más o menos eficiente el código. 
 
Objetivos
 
Se busca poder entender con más detalle el comportamiento de un número creciente de partículas sedimentarias que son arrastradas por la corriente de un cauce de agua. Para ello es necesario diseñar un modelo computacional que, en base a propiedades físicas y mecánicas conocidas, pueda modelar el movimiento de múltiples sedimentos que son arrastrados. Se busca por otro lado entender la influencia del uso de algoritmos matemáticos-computacionales en el modelamiento del fenómeno de arrastre de sedimentos, entre ellos algoritmos de complejidad computacional y métodos input-output.
 
 
 
Resultados para una partícula
 
 Para el estudio del comportamiento de una partícula transportada por un fluido se usaron los siguientes datos y supuestos:
 
 La partícula transportada corresponde a una grano de arena.
La forma de la partícula es considerada esférica.
El comportamiento se estudia mediante relaciones Euler-Lagrange

Datos usados:

diámetro de partícula = 1 mm
densidad de partícula = 155 kg/m^3
coeficiente Drag para partícula esférica = 0,47

El desplazamiento en x de la partícula según la velocidad a la que se mueve se muestra en el siguiente gráfico, donde el eje "x" representa el desplazamiento y el eje "y" la velocidad en determinado instante.

Grafico:

![65996866-a65a9300-e46e-11e9-945e-d2ca47f3125f](https://user-images.githubusercontent.com/53713567/66690292-98262700-ec65-11e9-921e-71e33bc9da6e.png)

Discusion de resultados:

Características del computador:

Marca: hp
Procesador: intel core i5
Memoria instalada: 6gb
Tipo de sistema operativo:  sistema operativo de 64 bits
Edicion de windows: windows 7  professional

En lo siguiente se busca ver como responde el computador a la modelación de 4 números de partículas distintos. Es de esperar que a medida de que se incrementa el numero de particulas simuladas, el computador tarde más en modelar, debido a que el número de pasos del algoritmo va creciendo con el número de partículas. Para obtener un tiempo representativo y no depender de otros procesos que pueda estar llevando a cabo el ordenador, se corrió el programa 3 veces con cada numero de particulas, obteniendo de esta forma un promedio de tiempo representativo.

Tiempo por cada nro de partículas:

1)  1 partícula: 2,3 seg
2) 2 partículas: 10,1 seg
3) 5 partículas: 17,1 seg
4) 10 partículas: 27,7 seg
5) 20 partículas: 109,9 seg

Gráficos:

2 partículas:
![2 particulas](https://user-images.githubusercontent.com/53713567/66690672-023fcb80-ec68-11e9-81d0-5a9c8ecbd13b.jpeg)


5 partículas:
![5 particulas](https://user-images.githubusercontent.com/53713567/66690681-1683c880-ec68-11e9-9dab-bacd53969330.jpeg)


10 partículas:
![10 partículas](https://user-images.githubusercontent.com/53713567/66690693-23082100-ec68-11e9-9677-80aa26833888.jpeg)


20 partículas:
![20 partículas](https://user-images.githubusercontent.com/53713567/66690697-2dc2b600-ec68-11e9-9c94-c19db6f95e12.jpeg)

Como se dijo anteriormente, los sedimentos en el fondo del cauce de agua son arrastrados debido a la velocidad del agua. La trayectoria de cada partícula va a depender de propiedades físicas de cada partícula como densidad, su geometría y textura superficial. Para efectos de esta modelación, se asume que todas las partículas son del mismo tamaño y forma, esférica perfecta, calculandose el drag de cada una de la misma forma. Al ir incrementando el numero de particulas, aumenta la posibilidad de que las partículas puedan chocar entre ellas, lo que altera su trayectoria. El total transcurrido que modela el código confeccionado es de  0,5 segundos para así poder obtener el máximo detalle de un periodo acotado de tiempo. El choque entre partículas está definido en el código como una fuerza k_penal, la que representa la  reacción en una partícula debido al choque sufrido con otra con un determinada inercia.

Con respecto a las modificaciones que se podrían llevar a cabo en el código para optimizarlo y de esta forma reducir el tiempo que tarda en correrlo,  se podría implementar otro método de integración de variables. En la tercera entrega se utilizó el método  de Euler para integrar las variables. en el caso de esta entrega, se implementó un metodo de integración llamado odeint. Cuando se analiza el rendimiento de un código, se debe tener en cuenta el largo de los ciclos de iteraciones que el sistema lleva a cabo. Mientras más largos sean los ciclos, logicamente más tardará el computador en procesarlos, por ende más se demorará el código. Es por esto que si se busca optimizar el código, se deberá optar por un método integrador de variables que minimice el largo de los ciclos iterativos. Una alternativa a lo anterior sería aumentar el número de supuestos y restricciones del problema, lo que no necesariamente seria eficiente, debido a que se puede caer en un sesgo y de esta forma perder exactitud en cuanto a la predicción de resultados.

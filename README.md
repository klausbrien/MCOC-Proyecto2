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
Datos usados
diámetro de partícula = 1 mm
densidad de partícula = 155 kg/m^3
coeficiente Drag para partícula esférica = 0,47
El desplazamiento en x de la partícula según la velocidad a la que se mueve se muestra en el siguiente gráfico, donde el eje "x" representa el desplazamiento y el eje "y" la velocidad en determinado instante.


# Práctica 4

## Integrantes

- Dante Mejía Silva
- Atzin Morales Alejandre

## Introducción

En los procesos automatizados, la repetición de tareas es un aspecto esencial para garantizar la eficiencia y precisión. Para lograr esto, el ciclo *For* es una de las estructuras de control más utilizadas en programación. Este ciclo permite ejecutar una serie de instrucciones un número determinado de veces, lo que resulta especialmente útil en entornos donde se realizan operaciones repetitivas, como en la automatización industrial, la robótica o el control de dispositivos.

El ciclo *For* proporciona una forma sencilla y eficiente de iterar sobre un conjunto de acciones, lo que permite ahorrar tiempo y recursos al evitar la necesidad de escribir múltiples bloques de código para cada repetición. En lugar de realizar una tarea manualmente una y otra vez, el ciclo permite definir la cantidad de veces que se desea repetir, garantizando uniformidad y exactitud en cada iteración.

Por ejemplo, en un sistema de apilamiento automatizado, como el apilamiento de fusibles o piezas, el ciclo *For* puede utilizarse para mover un brazo robótico repetidamente a diferentes posiciones, ajustando ligeramente las coordenadas para apilar elementos uno sobre otro. Esto no solo reduce el margen de error, sino que también optimiza el tiempo de ejecución de la tarea.

## Instrucciones
En primer lugar se realizó el código de manera simulada mediante un ciclo *For*, cabe destacar la falta de la pinza en el brazo por lo que únicamente se corroboró la correcta trayectoria de agarre del fusible y la correcta repetición.
```
Function main
Integer i
For i = 0 To 3
	Home
	Go primero
	
	Go segundo
	
	Go primero
	Home
	Go tercero +Z(i * 13)
	
	Home
Next

Fend
```
![image](https://github.com/user-attachments/assets/a711b197-e597-416f-a4a4-fb908df00d05)





## Conclusiones

***Atzin Morales Alejandre:*** 


***Dante Mejía Silva:*** 

## Referencias Bibliográficas 

[1] 	EpsonCompany, «Especialistas en automatización industrial». 2024, https://www.epson.es/es_ES/robots

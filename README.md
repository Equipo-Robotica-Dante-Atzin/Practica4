# Práctica 4

## Integrantes

- Dante Mejía Silva
- Atzin Morales Alejandre

## Introducción

En los procesos automatizados, la repetición de tareas es un aspecto esencial para garantizar la eficiencia y precisión. Para lograr esto, el ciclo *For* es una de las estructuras de control más utilizadas en programación. Este ciclo permite ejecutar una serie de instrucciones un número determinado de veces, lo que resulta especialmente útil en entornos donde se realizan operaciones repetitivas, como en la automatización industrial, la robótica o el control de dispositivos.

El ciclo *For* proporciona una forma sencilla y eficiente de iterar sobre un conjunto de acciones, lo que permite ahorrar tiempo y recursos al evitar la necesidad de escribir múltiples bloques de código para cada repetición. En lugar de realizar una tarea manualmente una y otra vez, el ciclo permite definir la cantidad de veces que se desea repetir, garantizando uniformidad y exactitud en cada iteración.

Por ejemplo, en un sistema de apilamiento automatizado, como el apilamiento de fusibles o piezas, el ciclo *For* puede utilizarse para mover un brazo robótico repetidamente a diferentes posiciones, ajustando ligeramente las coordenadas para apilar elementos uno sobre otro. Esto no solo reduce el margen de error, sino que también optimiza el tiempo de ejecución de la tarea.

## Instrucciones
En primer lugar se realizó el código de manera simulada mediante un ciclo *For*, cabe destacar la falta de la pinza en el brazo por lo que únicamente se corroboró la correcta trayectoria de agarre del fusible y su perfecta repetición.
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

Una vez comprobado el primer código se procedió a desarrollar otro código que implementará y tomara en cuenta la pinza del brazo robótico.
```
Function main
Integer i
For i = 0 To 3
	Home
	Go primero
	On 2
	Go segundo
	Off 2
	Go primero
	Home
	Go tercero +Z(i * 13)
	On 2
	Home
Next
Fend
```
El objetivo de esta práctica es controlar un sistema robótico o automatizado que apile cuatro fusibles de forma precisa. El robot se moverá a diferentes posiciones y alturas, colocando cada fusible en una capa encima del anterior.

Una vez iniciado el ciclo de ejecución del código:

   - El brazo robótico se moverá a la posición inicial (**Home**), luego se dirigirá donde se encuentra el primer fusible desde la posición definida como **primero**, activará el pin para recoger el fusible (**On 2**), y bajara en z durante la posición **segundo**, donde agarrará el fusible cerrando la pinza (**Off 2**).
     
   - Después de colocar el fusible en su posición utilizando **tercero + Z(i * 13)**, el brazo volverá a **Home** y repetirá el proceso para el siguiente fusible, ajustando la altura en el eje Z por cada fusible adicional.
   
   - Esto significa que en la primera iteración, el fusible se coloca en el nivel base, y en las siguientes iteraciones, la altura aumenta en 13 milimetros para apilar el fusible encima del anterior.
     
   ![Imagen de WhatsApp 2024-09-28 a las 18 31 35_9f18c53b](https://github.com/user-attachments/assets/5dc43714-e933-4ccb-9923-79a027c9f9bb)

   - El ciclo se repetirá cuatro veces hasta que todos los fusibles estén apilados.
     
     ![Imagen de WhatsApp 2024-09-28 a las 18 31 35_65da979d](https://github.com/user-attachments/assets/284372df-3a79-49aa-b589-7b3820d97a27)

   - Una vez completado, el brazo volverá a **Home**, indicando que el proceso de apilamiento ha finalizado.

## Conclusiones

***Atzin Morales Alejandre:*** 

La práctica permitió comprender sobre el uso de los ciclos **For** en la programación de sistemas robóticos, como en este caso, permitiendo la repetición de movimientos necesarios para apilar los fusibles de manera automatizada mediante el brazo robótico. A través de la implementación del ciclo que ajustaba las posiciones del brazo robótico y la pinza en cada iteración, se logró implementar el incremento progresivo de la altura en el eje Z.

La implementación del ciclo no solo optimizó la ejecución de las tareas repetitivas, sino que también minimizó posibles errores al mantener una uniformidad en cada operación del ciclo. La simulación inicial permitió verificar la precisión en las trayectorias del brazo y que la lógica del código fuera la correcta, esto para evitar errores en la implementación física.

Por último, el uso del ciclo **For** demostró ser una herramienta eficaz para la automatización de procesos repetitivos, siendo viable en tareas industriales que requieren de precisión, como en este caso el apilamiento de piezas.



***Dante Mejía Silva:*** 

Esta práctica nos ha permitido entender de manera profunda cómo el uso del ciclo `For` puede optimizar tareas repetitivas en un entorno automatizado, como el apilamiento de fusibles. Mediante la implementación de este ciclo, se logra que el sistema robótico ejecute de manera precisa y eficiente una serie de movimientos controlados, evitando la duplicación de código y asegurando la exactitud en cada operación. El robot ajusta la altura del apilamiento en cada iteración, permitiendo que cada fusible se coloque de manera uniforme uno sobre otro.

La automatización de este proceso no solo minimiza el riesgo de errores humanos, sino que también mejora significativamente la productividad. Este enfoque modular en la programación facilita la adaptación del código a distintos escenarios, permitiendo ajustar parámetros como la cantidad de fusibles o la altura de apilamiento sin necesidad de reestructurar el programa completo.

En conclusión, esta práctica nos demostró la importancia de utilizar estructuras de control como el ciclo `For` en la automatización de tareas repetitivas, lo que no solo ahorra tiempo y esfuerzo, sino que también garantiza precisión y eficiencia en el proceso. Esto es fundamental en cualquier entorno industrial, donde la optimización de recursos y la calidad en la ejecución son esenciales para el éxito del sistema.

## Referencias Bibliográficas 

[1] 	EpsonCompany, «Especialistas en automatización industrial». 2024, https://www.epson.es/es_ES/robots

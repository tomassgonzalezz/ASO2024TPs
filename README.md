1-a ¿Qué se puede notar con respecto al tiempo de ejecución? ¿Es
predecible?

Los tiempos de ejecución difieren entre utilizar hilos y no utilizarlos. Con hilos, las tareas pueden ejecutarse simultáneamente, lo que resulta en un tiempo total de ejecución más corto en comparación con la ejecución secuencial sin hilos. En promedio, en 10 ejecuciones, los tiempos fueron de aproximadamente 4.0262633 segundos con hilos
5.1820766 segundos sin hilos.

La diferencia de tiempo se debe a que, con hilos, mientras una tarea está en espera, otras tareas pueden continuar ejecutándose.

1-b Comparar con un campañero el tiempo de ejecución. ¿Son iguales?
Comparando con otro estudiante, sus tiempos fueron: alrededor de 4.07101 segundos con hilos 5.17174 segundos sin hilos. Estos tiempos validan la ventaja de utilizar hilos para tareas que pueden ejecutarse en paralelo, lo que lleva a una menor duración total del proceso.

1-c-Ejecutar el archivo suma_rasta.py unas 10 veces, luego descomentar(borrar el #) las líneas 11,12,19 y 20 guardarlo y ejecutarlo otras 10veces. ¿Qué pasó? ¿Por qué?
Cuando ejecuté el archivo suma_rasta.py unas 10 veces, todo parecía estar bien. Pero luego me pidieron que descomentara esas líneas específicas en el código y lo ejecutara otras 10 veces más.

Después de hacer eso, noté que el tiempo que tomaba completar el programa era más largo. ¿Por qué? Bueno, resulta que cuando descomenté esas líneas, agregué dos bucles adicionales que no estaban haciendo nada útil, solo estaban pasando el tiempo con un pequeño retraso.

Estos bucles estaban dentro de las funciones sumador y restador, y cada uno se ejecutaba mil veces. Aunque cada iteración de estos bucles no hacía nada relevante, sumaba tiempo total de ejecución del programa.

Entonces, en resumen, el tiempo de ejecución aumentó porque añadí estas iteraciones adicionales. Ahora, respecto al cambio en el valor final, ocurrió debido a este tiempo adicional de ejecución. Al introducir los bucles adicionales, aumenté el tiempo en el que acumulador estaba siendo modificado. Esto significaba que entre cada incremento y decremento de acumulador, había mil iteraciones adicionales que estaban ocurriendo. Durante este tiempo, el valor de acumulador estaba siendo afectado por la lógica dentro de esos bucles adicionales, lo que resultó en un valor final diferente al que obtendría sin ellos.

2-a.
puzzle resuelto

explicacion de cambio de turno
-un cambio de turno lo puse antes de salir de la zona critica. Lo hice asi para que cuando un hilo come una hamburguesa deba pasar al otro turno para que pueda entrar en la seccion critica y comer una hamburguesa.
-si no quedan hamburguesas entra al else, alli pongo el cambio de turno y paso al turno siguiente para que no se quede en un bucle infinito mirando la bandeja vacia

![WhatsApp Image 2024-06-07 at 1 16 08 PM](https://github.com/tomassgonzalezz/ASO2024TPs/assets/167874265/3a290b0b-c7b1-4af6-a1fc-a960d60b7459)


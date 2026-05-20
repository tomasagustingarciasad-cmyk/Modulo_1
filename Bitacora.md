# Bitacora TyHM García Tomás
### 4 de marzo de 2026: Inicio de Clases y Comienzo del Proyecto

- El profesor indico la clase de github, indicando su funcionamiento y solicitando que hagamos un repositorio
donde colocar todas las entregas los chicos de mecatrónica. 
- Como primera tarea se nos indico analizar un CPU con el que el profesor contaba. Lo desarmamos y observamos sus 
componerntes, para posteriormente debatir que sistema operativo podría ser compatible para utilizarlo como servidor.
- Por último, se nos solicitó realizar bobinas enrrollando cable, y presentarlo la siguiente semana.

-------------------------------------------
### 11 de marzo de 2026: Comprobacion de Bobinas y Continuación del Servidor

  Esta clase nos dividimos en dos grupos, los cuales tuvieron diferentes tareas.
 -  La primera de las tareas consistió en realizar la medición de todas las bobinas realizadas por los diferentes estudiantes
  y anotar en el repositorio un cuadro con los nombres de los participantes del grupo, el valor objetivo de inductancia en mH,
  y el valor que obtuvo experimentalmente. En mi caso realicé un informe sobre la eleccion de los parametros de la inductancia.
  - La segunda de las tareas consistió en continuar con el análisis del servidor, y su instalacion en la computadora de la que se disponia
  (No hago mas aclaraciones sobre esta seccion debido a que pase toda la tarde con lo de las bobinas)
- Por último, en esta clase se nos solicitó realizar un capacitor, haciendo uso de metodos caseros.
En este caso, como es casi imposible conocer los valores del dielectrico, se realizo sin ninguna consigna de valor objetivo

-------------------------------------------
### 18 de marzo de 2026: Comprobacion de los capacitores, análisis de frecuencias, log en servidor, etc.

 En esta clase volvimos a dividirnos, realizando diferentes tareas cada grupo.
 - Una de las tareas consitió en realizar el loggeo de cada uno de los participantes en el servidor que se había instalado la semana anterior.
 - Otro grupo estuvo encargado de desarmar unos auriculares que nos fue provisto por el profesor con el objetivo de obtener su sistema de carga.
 - Otro de los grupos tuvo el objetivo de aplicar la recepción de señales mediante el SDR receiver, haciendo uso de la aplicacion rx.kiwisdr.com.
 - El siguiente grupo estuvo encargado de visualizar y anotar señales obtenidas mediante la pagina https://www.qrz.com/db/LU8MIL. Respecto a esta actividad,
 en el repositorio se encuentran los valores obtenidos el limitado tiempo en el que estuvo abocado a esta tarea. El archivo en cuestion se llama Valores_Obtenidos_18-3

Esta misma clase, el profesor nos enseño diferentes aplicaciones para trackear la posicion de aviones, como la pagina https://www.flightradar24.com/,
la app para seguir la posicion de la ISS como "ISS Detector", o la aplicacion que se puede utilizar para observar una simulacion del cielo nocturno en 3D llamada Stellarium.
Por ultimo, cuando quedabamos pocos ya, el profesor nos mostro algunos comandos útiles en linux mediante el servidor que teníamos, como por ejemplo cal, man cal, mail perfil, etc.

Como actividades para realizar, nos quedo intentar fotografiar la ISS con nuestros telefonos, en la siguiente clase intentar fotografiarla con la cámara
que se encontraba en el aula de la maestria en logistica, 

-------------------------------------------
### 25 de marzo de 2026: Comprobacion de los capacitores, análisis de frecuencias, log en servidor, etc.

En esta clase volvimos a separarnos en grupo. 
- Un grupo pequeño tuvo que quedar en el aula escuchando la explicación del profe sobre como elaborar el informe informe.
- Otro grupo tuvo que estar monitoreando 2 frecuencias durante 2 horas anotando todo lo que escuchaba y de que tan lejos venían las señales.
- Otro grupo tuvo la tarea de ver tutoriales sobre como fotografiar la Luna con la camara que se nos prestó. Y cuando oscureció debía que fotografiar la Luna y
  los satelites de Júpiter.
- Y por último respecto a las actividades correspondientes a este día, se nos indico que todos individualmente
  debiamos escribir un informe que nos sirva como machete sobre la metodología Scrum. Este informe se encuentra en el repositorio con el nombre de informe_metodologias.pdf

-------------------------------------------

8 de abril de 2026 Herramientas de Validación y Hardware

Empezamos a trabajar con hardware real. Recibimos las instrucciones para construir un dipolo para 163 MHz 
(con una longitud total de 92 cm) y una antena radial de 13 cm. El profe nos desafió a usar esa antena radial 
corta para intentar escuchar algo en los 22.116 MHz de la misión ARTEMIS, aunque sabemos que será difícil por 
la diferencia de longitud de onda.

También aprendimos a usar el NanoVNA. Entendí que para no quemar el RTL-SDR, el conector de la antena tiene que 
tener una impedancia cercana a los 50 ohms. Aprendimos a diferenciar los puertos del VNA: el CH0 (S11) para ver 
qué tanto transmite o refleja la antena (midiendo el ROE/SWR) y el CH1 (S21) para ver lo que recibe. Además, 
empezamos a chusmear el software RTL1090 para ver si captamos aviones en 1090 MHz.

-------------------------------------------

10 de abril de 2026: Análisis de Telemetría Fotográfica

Enfoque en parte óptica. Un grupo de alumnos investigó cómo usar archivos para leer la información EXIF de las 
fotos, como ExifViewer. El objetivo fue extraer valores críticos como la apertura (f), la exposición y la apertura 
de la toma para poder replicar esas mismas condiciones en otras cámaras y así estandarizar nuestras capturas de 
la ISS.

-------------------------------------------

12 de abril de 2026

Nos dividimos en dos grupos. Unos obtuvieron los valores del exif y otros (donde yo estaba) modelamos una antena 
radial con suelo artificial para los 22,116MHz en MMana Gal.

-------------------------------------------

15 de abril de 2026: Teoría de Ondas y Montaje de Campo

Estudiamos el batido de ondas sumando dos señales sinusoidales, algo fundamental para entender cómo el SDR 
baja las frecuencias altas (down converter). El profe nos pasó unos scripts en R para analizar esto 
matemáticamente.
En la parte mecánica, decidimos que vamos a usar una montura ecuatorial para el seguimiento, similar a cómo 
se hace en los polos, y configuraremos el tipo de montura en el Gpredict. También definimos que usaremos 
bandas para los motores en lugar de engranajes y que no debemos pasar los 5V para proteger el Arduino. Al 
final de la clase, fuimos afuera y montamos una antena de hilo largo en el mástil de la bandera para 
monitorear entre 7 MHz y 28 MHz.

-------------------------------------------

16 de abril de 2026: Cambio de Software

Debido a que el SDR# se puso muy inestable en Windows 10 y 11, decidimos migrar a SDR++ (o RTLSDR++), 
que anda muchísimo mejor según los reportes y lo que nos comentó el equipo.

-------------------------------------------

22 de abril de 2026

Hoy trabajamos a fondo en la integración: intentamos que el Gpredict controle los motores a través del Arduino. 
También vimos la antena circular (Magnetic Loop) del laboratorio y exploramos Xnec2c como alternativa para 
modelar.
Lo más importante fue la simulación en MMANA-GAL para la frecuencia de 144.400 MHz. Probamos varias 
configuraciones (Dipolo, Moxon, Yagi, etc.) a nivel de piso. Hicimos las comparaciones finales y los 
resultados fueron: nuestra Yagi de 3 elementos dio una ganancia de 7,83 dB, superando los 5,43 dB de la Moxon. 
Con esto, concluimos que la Yagi será nuestra antena definitiva para construir.

-------------------------------------------

29 de abril de 2026

Finalmente, y tras analizar las opciones con los chicos, nos quedamos con la antena Moxon para el prototipo 
final. Aunque la Yagi nos daba un poco más de ganancia teórica en las simulaciones, decidimos priorizar la 
compacidad y la robustez de la Moxon para integrarla mejor al soporte motorizado.

Además del análisis bibliográfico, hoy calculamos las dimensiones físicas exactas para un 
prototipo de antena Moxon sintonizada a los 145 MHz. Utilizamos un calculador técnico considerando un 
conductor de 1 mm de diámetro, obteniendo los siguientes parámetros para el diseño:
  .Ancho (A): 748.8mm.
  .Excitado (B): 108.0mm.
  .Separación de puntas (C): 25.8mm.
  .Longitud total del excitador (Lexc): 964.7mm.
  .Longitud total del reflector (Lref): 1031.9mm.
Con un fondo total de solo 275.4mm, esta antena es extremadamente eficiente para su tamaño.
Hicimos esta elección para asegurar que el sistema de seguimiento controlado por Arduino pueda mover la 
estructura sin problemas de inercia excesiva, manteniendo la seguridad de los 5V para no quemar nada.

Además, completamos el análisis del material de la cátedra sobre batido de ondas en R, lo que nos da el 
sustento teórico para procesar la señal que recibamos con esta nueva antena en SDR++.

Tambien hicimos un ensayo de soldadura con cautín.
-------------------------------------------

6 de mayo de 2026

Cerraron la facultad por zonda. El profe nos compartió un link para ideas de antena moxon.


-------------------------------------------

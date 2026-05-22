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
### 25 de marzo de 2026: Monitoreo de Frecuencias, Fotografía,etc.

En esta clase volvimos a separarnos en grupo. 
- Un grupo pequeño tuvo que quedar en el aula escuchando la explicación del profe sobre como elaborar el informe informe.
- Otro grupo tuvo que estar monitoreando 2 frecuencias durante 2 horas anotando todo lo que escuchaba y de que tan lejos venían las señales.
- Otro grupo tuvo la tarea de ver tutoriales sobre como fotografiar la Luna con la camara que se nos prestó. Y cuando oscureció debía que fotografiar la Luna y
  los satelites de Júpiter.
- Y por último respecto a las actividades correspondientes a este día, se nos indico que todos individualmente
  debiamos escribir un informe que nos sirva como machete sobre la metodología Scrum. Este informe se encuentra en el repositorio con el nombre de informe_metodologias.pdf

-------------------------------------------
### 1 de abril de 2026: Comprobacion de los capacitores, análisis de frecuencias, log en servidor, etc.

En esta clase se realizaron diversas tareas. 
- Se inicio con el estudio del funcionamiento del programa gpredict, y como se podría conectar éste a un rotor para poder apuntar su posicion al satelite.
- Probamos la aplicación Zello, hicimos llamadas entre nosotros y creamos grupos para comprobar su utilidad y funcionamiento.
- Un grupo subio al techo con el objetivo de tener mejor señal para poder sintonizar una frecuencia específica hablada en clase mediante el uso de un handie.
- Realizamos una investigación sobre la correcta configuración de la cámara Nikon Coolpix L840. La principal fuente de información fue https://www.manual.ar/nikon/coolpix-l840/manual?p=23. Un resumen de algunas cosas que vimos en la investigacion se encuentra en el archivo Investigacion_uso_nikonCoolpix_L840

-------------------------------------------
### 8 de abril de 2026: 

 Esta clase tambien se nos presentó el principio de funcionamiento de las antenas, junto con muchos modelos de antena, tal como la dipolo, paragua, moxon, etc. 
- Se nos presento un software que se utiliza para el diseño de las antenas y se puede observar su alcance y direccion, abocando un grupo al diseño de diversas antenas para su posterior comparacion en la siguiente clase.
-  Tambien se nos presento el dispositivo Nano VNA, donde tambien se nos explico parte de su funcionamiento.

Debido a la cantidad presentes ese día, no hizo falta realizar grupos muy aislados entre sí, por lo que todos trabajamos dentro de todo en conjunto ese día. 
Entre las principales tareas realizadas (Ademas de las mecionadas previamente) destacan:
- Seguimiento del despegue de ARTEMIS
- Recepción y escucha de distintos puntos de radio haciendo uso de la antena dipolo provista por el profesor.

-------------------------------------------
### 15 de abril de 2026: 
El día de hoy se comenzo extrayendo la informacion y metadatos de las imagenes obtenidas en la clase anterior. Se generó un archivo con esa información, el cual se encuentra publicado en el repositorio https://github.com/tomasagustingarciasad-cmyk/Entrega. 

Ademas de eso, estudiamos y trajamos con el batido de ondas sumando dos señales sinusoidales, algo fundamental para entender cómo el SDR 
baja las frecuencias altas (down converter).

El profe nos pasó unos scripts en R para analizar esto matemáticamente.
Tambien decidimos la utilización de una montura ecuatorial para poder seguir a un satélite como si estuvieramos en el polo. Para poder trabajar con el sistema de seguimiento se le debe indicar a gpredict el tipo de montura a utilizar.

Se converso de la posibilidad de realizar el movimiento del sistema mecanico con una transmision mediante bandas en lugar de engranajes. 
Otro tema importante conversado es que al utilizar tensiones mayores que las propias de arduino para poder manejar los motores, deberemos tener cuidado en las conexiones realizadas.

Mientras la mayor parte de los grupos se trabajo en cuestiones de decisiones, teoricas y de software en la oficina de la maestria en logistica, el grupo al que yo pertenecía se encargó de montar una antena de hilo largo en el mastil de la bandera, lo que nos permitió salir al final de la clase y monitorear frecuencias entre 7 MHz y 28 MHz. Al realizar este monitoreo logramos escuchar una señal de radio de Chile, otros paises los cuales no logramos identificar pero que por el acento parecía ser Cuba o cercano, y logramos sintonizar una señal en la cual se lograba escuchar musica que parecía ser japonesa.


-------------------------------------------
### 22 de abril de 2026: 

-------------------------------------------
### 29 de abril de 2026: 

-------------------------------------------
### 6 de mayo de 2026: 

-------------------------------------------
### 13 de mayo de 2026: 


-------------------------------------------
### 20 de mayo de 2026: Descarga de software, diseño de sistema mecanico, extraccion de informacion gpredict, construccion antena y diseño y construccion de sistema electronico

En la clase de hoy se trabajo de muchas formas diferentes en paralelo, por lo que se realizaron muchos grupos diferentes.

- En mi caso, yo trabajé en un grupo cuya tarea fue la descarga e instalación de dos software diferentes. Lo primero que se descargó fue el software ngrok, la cual es una herramienta que crea un túnel seguro entre un entorno de desarrollo local e internet. Esto queremos hacerlo debido a que la red local será generada por SDR Phantom, el cual es un software WebSDR gratuito y de código abierto que permite compartir y acceder a receptores de Radio Definida por Software (SDR). Al realizar esta tarea presentamos el problema de que el dispositivo en el cual debiamos descargarlo no contaba con los requerimientos de harware suficientes para lograr compilar el programa descargado, razon por la cual se trababa y dejaba de funcionar en medio de la compilación. Para poder sortear este inconveniente realizamos la instalacion y compilacion en otro dispositivo y luego transferimos entre los dispositivos el programa ya compilado. Aún no sabemos si esta solución fue la apropiada, por lo que realizaremos las pruebas pertinentes la siguiente semana.
- Tambien hubo un grupo que se encontró avocado a la fabricación de la antena moxon que utilizaremos para las conexiones.
- Otro equipo realizó el diseño y modelado del sistema mecanico que se utilizará para realizar el seguimiento del satelite.
- Otro grupo se encargó del diseño y fabricación del sistema electronico para el control del motor que movilizará el sistema mecánico
- Por último, hubo otro equipo encargado de la extraccion de los parametros proveidos por el software gpredict. Dichos parametros seran los que se utilicen como setpoint para la determinacion del movimiento del sistema mecanico. 


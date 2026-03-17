# Sistemas Operativos como Gestores de Unidades de Concurrencia

Una forma útil de entender los sistemas operativos es interpretarlos como **gestores de unidades de concurrencia sobre recursos computacionales**.

Un sistema computacional posee recursos físicos fundamentales:

- CPU  
- memoria  
- almacenamiento  
- dispositivos de entrada/salida  

El sistema operativo introduce una **capa de abstracción** que permite que múltiples entidades computacionales utilicen estos recursos de forma concurrente.

De forma conceptual:

Hardware → Sistema Operativo → Unidades de concurrencia → Programas

En este sentido, el sistema operativo cumple dos funciones fundamentales:

- **Gestión de recursos**
- **Coordinación de concurrencia**

---

# Unidades de concurrencia

Las **unidades de concurrencia** son las entidades que el sistema planifica y ejecuta sobre el hardware.

Cada modelo de sistema computacional define una **unidad fundamental distinta**. Ejemplos comunes incluyen:

- procesos  
- threads  
- actores  
- eventos  
- tareas ligeras  

La elección de esta unidad determina la estructura del modelo de ejecución, así como las estrategias de comunicación, sincronización y planificación utilizadas por el sistema.

---

# El espacio de modelos de sistemas operativos

Podemos interpretar la teoría de sistemas operativos como el estudio del **espacio de modelos posibles para coordinar unidades de concurrencia sobre recursos computacionales**.

Cada modelo puede caracterizarse mediante cuatro componentes principales:

- **unidad de concurrencia**
- **modelo de memoria**
- **mecanismo de comunicación**
- **estrategia de scheduling**

Desde esta perspectiva, distintas arquitecturas de sistemas pueden entenderse como **puntos dentro de un espacio más amplio de modelos de concurrencia**.

---

# Modelos principales

## Modelo basado en procesos

En este modelo, la unidad fundamental de concurrencia es el **proceso**.

Un proceso es una instancia de un programa en ejecución que posee:

- espacio de memoria propio  
- recursos propios  
- estado de ejecución  

Características principales:

- fuerte aislamiento entre unidades  
- comunicación mediante mecanismos de **IPC (Inter-Process Communication)**  
- mayor costo de creación y cambio de contexto  

Este fue el modelo dominante en los primeros sistemas multitarea, especialmente en sistemas Unix.

---

## Modelo basado en threads

En este modelo, la unidad fundamental de concurrencia es el **thread**.

Un thread representa un flujo de ejecución dentro de un proceso.

Características principales:

- múltiples threads pueden existir dentro de un mismo proceso  
- los threads comparten el espacio de memoria del proceso  
- menor costo de creación y cambio de contexto que los procesos  

En este modelo, el sistema operativo planifica **threads** directamente sobre la CPU.

---

## Modelo híbrido proceso–thread

Este modelo separa dos responsabilidades fundamentales:

Proceso → aislamiento de recursos  
Thread → unidad de ejecución

El proceso actúa como **contenedor de recursos**, mientras que los threads representan **flujos de ejecución concurrentes dentro de ese contenedor**.

Este es el modelo dominante en la mayoría de sistemas operativos modernos.

---

## Modelo de actores

En el modelo de actores, la unidad fundamental de concurrencia es el **actor**.

Cada actor:

- mantiene su propio estado interno  
- procesa mensajes  
- se comunica exclusivamente mediante **paso de mensajes**

No existe memoria compartida directa entre actores.

Este modelo es particularmente adecuado para sistemas altamente concurrentes y distribuidos.

---

## Modelo dirigido por eventos

En este modelo, la ejecución se organiza alrededor de **eventos** o **callbacks**.

El sistema mantiene un **event loop** que procesa eventos de manera secuencial.

Características principales:

- muy eficiente para aplicaciones intensivas en entrada/salida  
- evita el uso masivo de threads  
- reduce ciertos problemas de sincronización  

Este enfoque es común en servidores y sistemas orientados a I/O intensivo.

---

## Modelo de tareas ligeras (user-space scheduling)

En este modelo, la unidad fundamental de concurrencia es una **tarea ligera gestionada en espacio de usuario**.

El runtime del lenguaje implementa su propio scheduler sobre un conjunto reducido de threads del sistema operativo.

Características principales:

- permite manejar miles o incluso millones de tareas concurrentes  
- el scheduling se realiza parcialmente en espacio de usuario  
- reduce significativamente el costo de creación de unidades de ejecución  

Este modelo aparece en varios runtimes modernos de lenguajes concurrentes.

---

# Invariantes estructurales

A pesar de las diferencias entre modelos, todos los sistemas de concurrencia comparten ciertos elementos estructurales.

Un sistema de concurrencia siempre incluye:

- **un conjunto de unidades de ejecución**
- **estado local asociado a cada unidad**
- **mecanismos de comunicación**
- **un scheduler que coordina la ejecución**

Estos componentes constituyen **invariantes estructurales** dentro del espacio de modelos de sistemas concurrentes.

---

# Conclusión

Desde esta perspectiva, los sistemas operativos pueden entenderse como una instancia particular dentro de un espacio más amplio de **modelos de coordinación de computación concurrente**.

La diferencia entre arquitecturas de sistemas radica principalmente en:

- qué entidad se define como **unidad fundamental de concurrencia**
- cómo se organiza la **comunicación entre unidades**
- qué estrategia utiliza el sistema para **planificar su ejecución**

Estudiar estos modelos como parte de un **espacio de configuraciones posibles** permite comparar arquitecturas, comprender sus compromisos de diseño y explorar nuevas formas de estructurar sistemas concurrentes.

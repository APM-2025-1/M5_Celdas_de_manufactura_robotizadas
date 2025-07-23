<div align="center">
<picture>
    <source srcset="https://imgur.com/5bYAzsb.png" media="(prefers-color-scheme: dark)">
    <source srcset="https://imgur.com/Os03JoE.png" media="(prefers-color-scheme: light)">
    <img src="https://imgur.com/Os03JoE.png" alt="Escudo UNAL" width="350px">
</picture>

<h3>AUTOMATIZACIÓN DE PROCESOS DE MANUFACTURA</h3>

<h1>Módulo 5 - Celdas de manufactura robotizadas</h1>

<h2>Mep Mep Raideres</h2>

<h5>Joan Sebastian Arcila Cardozo<br>
    Juan Sebastian Daleman Martinez<br>
    Daniel Santiago Muñoz Bernal<br>
    Maria Alejandra Pérez Petro<br>
    Emma Carolina Sarmiento Cabarcas</h5>

<h6>Universidad Nacional de Colombia<br>
    Facultad de Ingeniería<br>
    Departamento de Ingeniería Mecánica y Mecatrónica<br>
    Bogotá, Colombia<br>
    2025</h6>
</div>


<details>
    <summary>🗂️ Tabla de Contenido</summary>

<!-- TOC -->
- [1. 🤖 Celda Robótica de Inflado de Llantas](#1--celda-robótica-de-inflado-de-llantas)
  - [1.1. 🦾 Manipuladores Robóticos](#11--manipuladores-robóticos)
    - [1.1.1. Cálculos estimados del *Takt time*:](#111-cálculos-estimados-del-takt-time)
  - [1.2. 🛻 Elementos de Transporte y Posicionamiento](#12--elementos-de-transporte-y-posicionamiento)
  - [1.3. 🧰 Herramientas y Sensores](#13--herramientas-y-sensores)
  - [1.4. 🦺 Seguridad](#14--seguridad)

</details>


# 1. 🤖 Celda Robótica de Inflado de Llantas
Un paso crucial en el ensamble de nuestras patinetas es el proceso de inflado de llantas. Las llantas se reciben desinfladas por varias razones de seguridad y logística: evitar rupturas durante el transporte, optimizar el espacio de almacenamiento, y permitir una calibración precisa de la presión según las especificaciones del manual. Actualmente, el proceso de inflar es realizado por un operario, pero hemos identificado que un sistema robotizado podría ejecutar esta tarea de manera más eficiente y precisa.

Especificamente, se desea diseñar una celda róbotica para el proceso de inflado y calibración de la **Llanta 145/70-6**, una de nuestras referencias clave. A continuación se describe la configuración de la celda róbotica diseñada.


## 1.1. 🦾 Manipuladores Robóticos

**Robots Industriales (2 unidades):**

* **Robot 1 – Alimentación y desalimentación:**

  * Consiste de un X-arm 6, permite la orientación de la llanta para dejar la boquilla en la ubicación necesaria.
  * Toma llantas desinfladas desde el área de entrega de llantas.
  * Entrega llantas infladas a la cinta transportadora.
  * Equipado con un gripper magnetico para ajustarse facilmente a todos los tipos de llanta.

* **Robot 2 – Inflado:**

  * Consiste de un X-arm 5, similar tamaño del X-arm 6.
  * Posiciona la herramienta de inflado en la válvula.
  * Mantiene la boquilla en posición durante el proceso de inflado.
  * Integra herramienta neumática con acople automático y sensor de presión.
  
### 1.1.1. Cálculos estimados del *Takt time*:

* **Alimentación:** ≈ 4 segundos
* **Inflado:** ≈ 20 segundos
* **Desalimentación:** ≈ 4 segundos

> Al ser un proceso realizado por dos robots de manera paralela, los tiempos de alimentación y desalimentación no agregan tiempo al proceso. El **tiempo crítico** es de **20 segundos**, determinado por el proceso de inflado de la llanta.

## 1.2. 🛻 Elementos de Transporte y Posicionamiento

* **Cinta transportadora:**

  * Mueve las llantas desinfladas hacia la celda y las infladas hacia la salida.
  * Sincronizada con el ciclo de los robots.

* **Fixtures de sujeción:**

  * Mantienen la llanta estable y correctamente orientada durante el inflado.
  * Compatibles con el sistema de sujeción del robot y alineados con la válvula.

---

## 1.3. 🧰 Herramientas y Sensores

* **Herramienta de inflado:**

  * Acople neumático automático.
  * Capaz de inflar a diferentes presiones según referencia.

* **Sensor de presión:**

  * Monitorea la presión interna de la llanta en tiempo real.
  * Sensor-transductor digital con salida 0-10V conectado al controlador del robot.
    

* **X-arm Gripper:**
  
  * Servo gripper compatible con el controlador de los X-arm.
  * Masa de 1.1 Kg

* **Gripper magnético:**
  
  * referencia MHM-32TFD1-M9NLS.
  * Para montaje de costado con 3m de cable.
  * Control compatible con el controlador del robot
  
* **Sensor de posición de vávula:**

  * Verifica que la válvula esté correctamente orientada antes del acople.
  * Sensor mecánico tipo final de carrera palpador.

---

## 1.4. 🦺 Seguridad
Análisis de los 10 posibles peligros al trabajar con una celda robótica
1. Atrapamiento de persona entre el robot y la estructura fija
2. Golpe por movimiento inesperado del robot
3. Pinchazo o corte por el inflador o boquilla
4. Explosión de la llanta por sobrepresión
5. Descarga eléctrica por mal aislamiento
6. Caída de la llanta durante la manipulación
7. Falla del gripper o sujeción de la llanta
8. Acceso no autorizado durante operación
9. Fuga de aire comprimido
10. Caída por tropiezos

* **Cercas de Seguridad:**
  Estructuras físicas que delimitan el perímetro de la celda, evitan el acceso no autorizado y protegen contra movimientos inesperados del robot o posibles fallos durante el inflado.

* **Barrera láser:**
  Detectan la presencia humana dentro de la celda. Su activación detiene automáticamente los movimientos robóticos.

* **Botones de emergencia:**
  Distribuidos estratégicamente alrededor de la celda para permitir una detención inmediata del proceso en caso de incidente.

* **Sensor de presión:**
  Para evitar sobrellenado de las llantas, de esta manera evitando explosiones.






<div align="center">
<picture>
    <source srcset="https://imgur.com/5bYAzsb.png" media="(prefers-color-scheme: dark)">
    <source srcset="https://imgur.com/Os03JoE.png" media="(prefers-color-scheme: light)">
    <img src="https://imgur.com/Os03JoE.png" alt="Escudo UNAL" width="350px">
</picture>

<h3>AUTOMATIZACIÓN DE PROCESOS DE MANUFACTURA</h3>

<h1>Módulo 5 - Celdas de manufactura robotizadas</h1>

<h2>Mep Mep Raideres</h2>

<h5>Joan Sebastian Arcila <br>
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

- [Celda Robótica de Llenado de Llantas](#celda-robótica-de-llenado-de-llantas)
    - [Configuración con Dos Robots](#configuración-con-dos-robots)
    - [Cálculos estimados del *Takt time*:](#cálculos-estimados-del-takt-time)
  - [Celda Robótica de Inflado de Llantas](#celda-robótica-de-inflado-de-llantas)
    - [1. Manipuladores Robóticos](#1-manipuladores-robóticos)
    - [2. Elementos de Transporte y Posicionamiento](#2-elementos-de-transporte-y-posicionamiento)
    - [3. Herramientas y Sensores](#3-herramientas-y-sensores)
    - [4. Seguridad](#4-seguridad)

</details>




# Celda Robótica de Llenado de Llantas
Un paso crucial en el ensamble de nuestras patinetas es el proceso de llenado de llantas. Las llantas se reciben desinfladas por varias razones de seguridad y logística: evitar rupturas durante el transporte, optimizar el espacio de almacenamiento, y permitir una calibración precisa de la presión según las especificaciones del manual. Actualmente, el llenado y calibración es realizado por un operario, pero hemos identificado que un sistema robotizado podría ejecutar esta tarea de manera más eficiente y precisa.

Especificamente, se desea diseñar una celda róbotica para el porceso de llenado y calibración de la **Llanta 145/70-6**, una de nuestras referencias clave. La configuración exacta de esta celda, incluyendo el número de robots, dependerá del método final de alimentación del material, el cual aún está bajo evaluación.

Consideramos dos posibles escenarios para la automatización:

### Configuración con Dos Robots

Si optamos por una solución con dos robots, el proceso se distribuirá de la siguiente manera:

* **Robot 1 (Manipulación de Material):** Se encargaría de la **toma inicial de las llantas desinfladas** de la estación de alimentación de la celda.
* **Robot 2 (Llenado y Calibración):** Equipado con un **sistema de aire comprimido** y **sensores de presión**, este robot realizaría la tarea principal de **llenado y calibración de la llanta**.
* **Robot 1 (Desalimentación):** Una vez que la llanta esté correctamente inflada, el primer robot volvería a intervenir para realizar la **desalimentación** de la llanta llena, trasladándola a la siguiente fase del proceso de ensamble.


### Cálculos estimados del *Takt time*:

* **Alimentación:** ≈ 4 segundos
* **Llenado:** ≈ 20 segundos
* **Desalimentación:** ≈ 4 segundos

> Al ser un proceso realizado por dos robots de manera paralela, los tiempos de alimentación y desalimentación no agregan tiempo al proceso. El **tiempo crítico** es de **20 segundos**, determinado por el proceso de llenado de la llanta.



## Celda Robótica de Inflado de Llantas

### 1. Manipuladores Robóticos

**Robots Industriales (2 unidades):**

* **Robot 1 – Alimentación y desalimentación:**

  * Toma llantas desinfladas desde la cinta transportadora.
  * Entrega llantas infladas al área de salida.
  * Equipado con pinza adaptable a llantas de diferentes tamaños.

* **Robot 2 – Inflado:**

  * Posiciona la herramienta de inflado en la válvula.
  * Mantiene la llanta en posición durante el proceso.
  * Integra herramienta neumática con acople automático y sensor de presión.

### 2. Elementos de Transporte y Posicionamiento

* **Cinta transportadora:**

  * Mueve las llantas desinfladas hacia la celda y las infladas hacia la salida.
  * Sincronizada con el ciclo de los robots.

* **Fixtures de sujeción:**

  * Mantienen la llanta estable y correctamente orientada durante el inflado.
  * Compatibles con el sistema de sujeción del robot y alineados con la válvula.

---

### 3. Herramientas y Sensores

* **Herramienta de inflado:**

  * Acople neumático automático.
  * Capaz de inflar a diferentes presiones según referencia.

* **Sensor de presión:**

  * Monitorea la presión interna de la llanta en tiempo real.
  * Envía señal de corte al alcanzar la presión objetivo.

* **Sensor de posición de vávula:**

  * Verifica que la válvula esté correctamente orientada antes del acople.
  * Puede ser óptico o mecánico.

---

### 4. Seguridad

* **Cercas de Seguridad:**
  Estructuras físicas que delimitan el perímetro de la celda, evitan el acceso no autorizado y protegen contra movimientos inesperados del robot o posibles fallos durante el inflado.

* **Cortinas de luz o escáner láser:**
  Detectan la presencia humana dentro de la celda. Su activación detiene automáticamente los movimientos robóticos.

* **Botones de emergencia:**
  Distribuidos estratégicamente alrededor de la celda para permitir una detención inmediata del proceso en caso de incidente.






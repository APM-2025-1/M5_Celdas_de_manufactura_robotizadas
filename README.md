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

- [Celda Robótica de Inflado de Llantas](#celda-robótica-de-inflado-de-llantas)
  - [1. Manipuladores Robóticos](#1-manipuladores-robóticos)
    - [Cálculos estimados del *Takt time*:](#cálculos-estimados-del-takt-time)
  - [2. Elementos de Transporte y Posicionamiento](#2-elementos-de-transporte-y-posicionamiento)
  - [3. Herramientas y Sensores](#3-herramientas-y-sensores)
  - [4. Seguridad](#4-seguridad)

</details>


# Celda Robótica de Inflado de Llantas
Un paso crucial en el ensamble de nuestras patinetas es el proceso de inflado de llantas. Las llantas se reciben desinfladas por varias razones de seguridad y logística: evitar rupturas durante el transporte, optimizar el espacio de almacenamiento, y permitir una calibración precisa de la presión según las especificaciones del manual. Actualmente, el proceso de inflar es realizado por un operario, pero hemos identificado que un sistema robotizado podría ejecutar esta tarea de manera más eficiente y precisa.

Especificamente, se desea diseñar una celda róbotica para el proceso de inflado y calibración de la **Llanta 145/70-6**, una de nuestras referencias clave. A continuación se describe la configuración de la celda róbotica diseñada.


## 1. Manipuladores Robóticos

**Robots Industriales (2 unidades):**

* **Robot 1 – Alimentación y desalimentación:**

  * Toma llantas desinfladas desde la cinta transportadora.
  * Entrega llantas infladas al área de salida.
  * Equipado con pinza adaptable a llantas de diferentes tamaños.

* **Robot 2 – Inflado:**

  * Posiciona la herramienta de inflado en la válvula.
  * Mantiene la llanta en posición durante el proceso.
  * Integra herramienta neumática con acople automático y sensor de presión.
  
### Cálculos estimados del *Takt time*:

* **Alimentación:** ≈ 4 segundos
* **Inflado:** ≈ 20 segundos
* **Desalimentación:** ≈ 4 segundos

> Al ser un proceso realizado por dos robots de manera paralela, los tiempos de alimentación y desalimentación no agregan tiempo al proceso. El **tiempo crítico** es de **20 segundos**, determinado por el proceso de inflado de la llanta.

## 2. Elementos de Transporte y Posicionamiento

* **Cinta transportadora:**

  * Mueve las llantas desinfladas hacia la celda y las infladas hacia la salida.
  * Sincronizada con el ciclo de los robots.

* **Fixtures de sujeción:**

  * Mantienen la llanta estable y correctamente orientada durante el inflado.
  * Compatibles con el sistema de sujeción del robot y alineados con la válvula.

---

## 3. Herramientas y Sensores

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

## 4. Seguridad

* **Cercas de Seguridad:**
  Estructuras físicas que delimitan el perímetro de la celda, evitan el acceso no autorizado y protegen contra movimientos inesperados del robot o posibles fallos durante el inflado.

* **Cortinas de luz o escáner láser:**
  Detectan la presencia humana dentro de la celda. Su activación detiene automáticamente los movimientos robóticos.

* **Botones de emergencia:**
  Distribuidos estratégicamente alrededor de la celda para permitir una detención inmediata del proceso en caso de incidente.






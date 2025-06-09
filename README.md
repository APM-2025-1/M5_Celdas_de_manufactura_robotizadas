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

<!-- TOC -->
- [](#)



</details>



# Modulo de celda robotica 

Uno de los procesos necesarios para el ensamble de nuestras patinetas es la estación de llenado de llantas. Las llantas son enviadas sin aire, principalmente por motivos de seguridad, ya que podrían romperse si se envían infladas. Además, las llantas infladas ocupan más espacio durante el transporte. Otro factor importante que requiere que las llantas se envíen desinfladas es la necesidad de calibrarlas con la presión específica estipulada en el manual. Este proceso lo realiza un operario pero considermoas que un robot será capaz de realizarlo.

Una de las referencias que utilizamos de llantas en nuestras scooters es la **Llanta 145/70-6**. La celda contaría con un método de alimentación aún en proceso de selección. Dependiendo de eso, se utilizaría **uno o dos robots** para la celda.

En el caso de utilizar **dos robots**, el proceso se dividiría así:

* Un robot realizaría la **toma del material de alimentación de la celda** (llantas desinfladas).
* Otro robot, con un **sistema de aire comprimido** y **sensores de presión**, realizaría la **acción de llenado y calibración**.
* Finalmente, el robot de alimentación realizaría el proceso de **desalimentación** (llanta llena).

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






# Simulacion_CafeteriaPDP
# ☕ Cafetería Concurrente Distribuida

Simulación del funcionamiento de una cafetería mediante **programación concurrente y distribuida en Java**, desarrollada en **NetBeans** como parte de la asignatura **Paradigmas de Programación (PECL – Enero 2026)**.

---

## 🧩 Descripción general

El proyecto modela una **cafetería virtual** con múltiples actores y zonas de actividad:

### **Actores (hilos)**
- **Clientes (C-XXXX):** acuden al parque, entran en la cafetería, compran, pagan y consumen.
- **Vendedores (V-XXXX):** transportan productos desde la despensa al mostrador.
- **Cocineros (B-XXXX):** preparan productos en la cocina y los guardan en la despensa.

### **Zonas de actividad**
- Parque  
- Cocina  
- Despensa  
- Mostrador  
- Caja  
- Área de consumición  
- Sala de descanso  

Cada actor se comporta de forma concurrente y respeta los límites de aforo y tiempos definidos en el enunciado.  
Los recursos compartidos (productos, recaudación, archivo de log, etc.) se gestionan mediante **mecanismos de sincronización**.

---

## 🧠 Objetivos del proyecto

1. Modelar el comportamiento concurrente de los actores.  
2. Gestionar correctamente los recursos y zonas compartidas mediante sincronización.  
3. Registrar la evolución del sistema en un fichero de log con marca temporal.  
4. Desarrollar una **interfaz gráfica (Swing)** que muestre el estado del sistema.  
5. Ampliar el sistema con un **módulo distribuido (RMI o Sockets)** para consultas remotas.

---


## 🧱 Estructura del proyecto

(((Esta imagen es temporal))))
<img width="855" height="677" alt="image" src="https://github.com/user-attachments/assets/ef218a44-faa3-46e3-bfa0-14a7d7787a84" />


---

## 🧮 Recursos y sincronización

Los recursos críticos como el **aforo**, las **unidades de productos** y la **recaudación** se controlan mediante:

- `Semaphore` → para limitar acceso a zonas.  
- `ReentrantLock` → para proteger recursos compartidos.  
- `AtomicInteger` → para contadores concurrentes.  
- `wait()` / `notifyAll()` → para pausas y reanudaciones del sistema.

---

## 🧾 Registro de eventos

Cada evento del sistema se almacena en `logs/evolucion_cafeteria.txt` con la siguiente estructura:


El log es un **recurso compartido sincronizado** accesible por todos los hilos.

---

## 🎨 Interfaz gráfica

- Muestra en tiempo real:
  - Número de clientes en cada zona.
  - Unidades de café y rosquillas en despensa y mostrador.
  - Recaudación total.
- Incluye un botón **Pausar/Reanudar** que detiene o continúa la simulación.
- Usa componentes **Swing** (`JFrame`, `JButton`, `JLabel`, `Timer`).

---

## 🌐 Parte distribuida (RMI o Sockets)

La segunda parte del proyecto amplía la simulación con un **cliente remoto** que:
- Consulta el número de actores en cada zona.
- Muestra el estado actualizado cada segundo.
- Permite pausar y reanudar la ejecución del servidor.

---

## ⚙️ Tecnologías utilizadas

- **Java 17+**
- **NetBeans IDE**
- **Programación Concurrente**
- **Programación Distribuida (RMI / Sockets)**
- **Swing (Interfaz gráfica)**
- **Git / GitHub**

---

## 🧑‍💻 Autores

- Abel Burdet
- Cristian Jimenez Lago 

Grado en Ingeniería en Sistemas de Información  
Convocatoria Ordinaria – Enero 2026

---

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

## ⚙️ Tecnologías utilizadas

- **Java 17+**
- **NetBeans IDE**
- **Programación Concurrente**
- **Programación Distribuida (RMI / Sockets)**
- **Swing (Interfaz gráfica)**
- **Git / GitHub**

---

## 🧱 Estructura del proyecto

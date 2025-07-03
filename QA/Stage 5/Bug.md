# 🐞 ¿Qué es un BUG en QA o Testing?

En **QA (Quality Assurance)** o **Testing**, un **bug** es un **error, defecto o falla** en una aplicación o sistema que causa que este no se comporte como se espera, ya sea funcional o visualmente, respecto a los requerimientos definidos.

---

## 📌 Conceptos Clave

### 🔍 **Definición Formal**

Un **bug** es una discrepancia entre el comportamiento esperado y el comportamiento real del sistema, ya sea en tiempo de ejecución, interfaz, lógica, flujo o interacción.

### ⚠️ **Sinónimos comunes**

- Defecto (_defect_)
    
- Error (_error_)
    
- Fallo (_fault_)
    
- Incidencia (_issue_)
    
- Anomalía (_anomaly_)
    

---

## 🎯 ¿Qué puede causar un bug?

- Malentendidos o ambigüedades en los **requisitos**.
    
- **Errores humanos** en el código fuente.
    
- Fallas en la **lógica del sistema**.
    
- Cambios no comunicados o mal implementados.
    
- Problemas de **integración** entre sistemas o módulos.
    
- Inconsistencias en entornos (desarrollo vs producción).
    

---

## 🧠 Tipos de Bugs más comunes

|Tipo|Descripción|
|---|---|
|**Funcional**|Comportamiento incorrecto respecto a lo esperado.|
|**UI/UX**|Errores visuales, de diseño, alineación o accesibilidad.|
|**De rendimiento**|El sistema es lento, consume muchos recursos o falla bajo carga.|
|**De seguridad**|Fallas que comprometen la integridad, confidencialidad o disponibilidad.|
|**De compatibilidad**|Inconsistencias entre navegadores, dispositivos o sistemas operativos.|
|**De regresión**|Funcionalidades que fallan tras una nueva actualización.|
|**De lógica**|Algoritmos incorrectos o cálculos erróneos.|
|**De datos**|Ingresos, cálculos o visualizaciones incorrectas de la información.|

---

## 🛠️ Ciclo de vida de un Bug

1. **Detección:** Descubierto por QA, desarrolladores o usuarios.
    
2. **Reporte:** Se documenta con pasos para reproducir, evidencias y contexto.
    
3. **Asignación:** Se asigna al responsable (dev, equipo técnico).
    
4. **Corrección:** El error es solucionado por el equipo de desarrollo.
    
5. **Verificación:** QA verifica que el bug fue resuelto y no generó efectos secundarios.
    
6. **Cierre:** Si pasa la verificación, el bug se da por cerrado.
    

---

## 🧾 Buen reporte de bug (Bug Report)

Un buen **reporte de bug** debe contener:

- **Título claro y descriptivo.**
    
- **Prioridad/severidad.**
    
- **Pasos para reproducir.**
    
- **Resultado esperado vs resultado actual.**
    
- **Entorno de pruebas (versión, navegador, dispositivo, etc).**
    
- **Evidencia:** capturas de pantalla, logs o video.
    
- **Estado del bug:** nuevo, asignado, en progreso, resuelto, cerrado, etc.
    

---

## 🏷️ Severidad vs Prioridad

|Concepto|Definición|Ejemplo|
|---|---|---|
|**Severidad**|Qué tan grave es el impacto del bug.|El sistema se cae (Alta).|
|**Prioridad**|Qué tan urgente es su corrección.|Error de UI en producción (Alta prioridad aunque baja severidad).|

---

## 🧩 Relación con QA

- **QA no introduce bugs, los identifica y reporta.**
    
- El objetivo de QA es garantizar que los errores se detecten **antes de llegar al usuario final**.
    
- Un equipo de QA efectivo aporta información clave para mejorar la **calidad del producto y la experiencia del usuario**.

---
↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
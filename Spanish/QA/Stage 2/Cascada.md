# 🧱 Metodología Tradicional Cascada

La **metodología en Cascada** es un modelo de desarrollo de software **secuencial y lineal**, en el que el progreso fluye hacia abajo, como una cascada, a través de diferentes fases del ciclo de vida del desarrollo.

## 📌 Conceptos Clave

- **Linealidad:** Las fases se ejecutan en orden secuencial y no se regresa a etapas anteriores una vez completadas.
    
- **Documentación extensiva:** Cada fase genera documentación detallada que sirve de guía para la siguiente.
    
- **Entrega al final:** El producto completo se entrega una vez finalizadas todas las fases.
    

---

## 🛠️ Fases Principales

1. ### **Recolección de Requisitos**
    
    - Identificación y documentación de todas las necesidades del cliente.
        
    - Punto clave: los requisitos deben ser **claros, completos y estables**.
        
2. ### **Análisis del Sistema**
    
    - Traducción de requisitos en especificaciones técnicas.
        
    - Se define **qué se va a construir** desde un punto de vista técnico.
        
3. ### **Diseño del Sistema**
    
    - Arquitectura, interfaces, modelos de datos y componentes.
        
    - Incluye diseño lógico y físico.
        
4. ### **Implementación (Desarrollo)**
    
    - Codificación del sistema conforme al diseño aprobado.
        
    - Se realizan pruebas unitarias.
        
5. ### **Pruebas**
    
    - Verificación de que el sistema cumple con los requisitos definidos.
        
    - Incluye pruebas de integración, sistema y aceptación.
        
6. ### **Despliegue**
    
    - Instalación del sistema en el entorno productivo.
        
    - Entrenamiento al usuario final.
        
7. ### **Mantenimiento**
    
    - Corrección de errores, mejoras y adaptaciones.
        
    - No se prevé una iteración formal; los cambios suelen implicar nuevos proyectos.
        

---

## ✅ Ventajas

- Proceso bien estructurado y fácil de gestionar.
    
- Alta predictibilidad de tiempos y costos.
    
- Ideal para proyectos con requisitos bien definidos desde el inicio.
    

---

## ⚠️ Desventajas

- Baja flexibilidad frente a cambios.
    
- Riesgo de malinterpretar requisitos si no se comprenden bien desde el inicio.
    
- Feedback del cliente hasta fases muy avanzadas.
    

---

## 🧩 Casos de Uso Típicos

- Proyectos con requisitos estables y bien comprendidos.
    
- Entornos regulados donde se requiere documentación formal (e.g., aeronáutica, defensa, gobierno).
    
- Proyectos de infraestructura o sistemas embebidos.
    

---

## 🔁 Comparación con Metodologías Ágiles

|Aspecto|Cascada|Ágil|
|---|---|---|
|Enfoque|Secuencial|Iterativo e incremental|
|Cambio de requisitos|Difícil de manejar|Aceptado y bienvenido|
|Entrega|Al final del proyecto|Frecuente y continua|
|Participación cliente|Mínima|Activa y constante|

---

## Ventajas vs Desventajas de Cascada en QA

### ✅ **Ventajas para QA**

- **Claridad en los requisitos desde el inicio**
    
    - QA puede diseñar casos de prueba basados en requisitos estables y bien documentados.
        
- **Documentación detallada**
    
    - La planificación de pruebas se facilita con la existencia de especificaciones claras, diagramas y planes formales.
        
- **Fase de pruebas dedicada**
    
    - QA tiene una fase específica y definida para ejecutar pruebas, lo que permite enfocarse completamente en la validación.
        
- **Facilidad para trazabilidad**
    
    - Al tener entregables por fase, es más fácil rastrear defectos hasta su origen (especificación, diseño o desarrollo).
        

---

### ⚠️ **Desventajas para QA**

- **Detección tardía de errores**
    
    - Al no haber validaciones continuas, los bugs se encuentran en etapas finales, lo que eleva el costo de corrección.
        
- **Poca retroalimentación temprana**
    
    - QA no participa activamente durante las fases iniciales, lo que reduce su capacidad de influir en decisiones clave.
        
- **Cambios de requisitos complejos**
    
    - Si los requisitos cambian durante el desarrollo, las pruebas previamente diseñadas pueden volverse obsoletas o incorrectas.
        
- **Riesgo de pruebas apresuradas**
    
    - Si el desarrollo se retrasa, la fase de pruebas suele ser comprimida para cumplir con la fecha de entrega.
        
- **No fomenta automatización temprana**
    
    - Dado que el desarrollo se completa antes de la fase de pruebas, es menos viable implementar automatización desde el principio.
        

---
↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
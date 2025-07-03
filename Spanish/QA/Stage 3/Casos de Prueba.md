## ✅ ¿Qué es un caso de pruebas?

Los _test cases_ o casos de prueba son un conjunto de acciones ejecutadas para verificar una característica o funcionalidad de una aplicación.  
Son escritos por los QAs con el fin de documentar su trabajo y exponer qué se probó y cómo.

Cada caso de prueba contiene un conjunto de pasos y un resultado esperado que sirven para comprobar la calidad de una funcionalidad.


## 🎯 Escenario de prueba

A diferencia del caso de prueba, un escenario de prueba es mucho más acotado.  
Son muy útiles cuando contamos con poco tiempo para testear, cuando la aplicación cambia mucho en poco tiempo, o cuando el equipo ya es maduro y conoce los flujos de la aplicación.

Estos tienen mucho menor nivel de detalle que un caso de prueba, lo cual hace que su mantenimiento sea más rápido.

Identificación de Escenarios

- **Flujos principales (“happy path”)**: los estados más comunes y críticos para el usuario.
    
- **Escenarios alternativos y de error**: validaciones de datos obligatorios, condiciones límite, rechazo de permisos, timeouts.
    
- **Casos fronterizos**: valores máximos y mínimos, formatos atípicos, combinación de campos.
    
![[Escenario.png]]


---
# ✅ Casos positivos y negativos

En el diseño de pruebas, es importante considerar tanto los casos que **confirman el comportamiento esperado** como aquellos que prueban la **resiliencia del sistema ante datos erróneos**.


## 🟢 Positivos

Probar que cada requerimiento del sistema **cumpla con lo que verdaderamente debe hacer**.

Ejemplo:

> Se prueba el formulario “Agregar producto” ingresando datos válidos:
> 
> - **Nombre:** “Mouse inalámbrico”
>     
> - **Precio:** “50000”
>     
> - Se espera que el botón **Guardar** registre el producto correctamente.
>     

---

## 🔴 Negativos

Salir del camino normal de la aplicación y **verificar cómo se comporta el sistema al ingresar datos incorrectos**.

Ejemplo:

> - Dejar el campo **Nombre** vacío.
>     
> - Ingresar texto en el campo **Precio** (por ejemplo, “cincuenta mil”).
>     
> - Se espera que el sistema **muestre errores** y **no permita guardar**.

---
# 🗓️ 1. Planificación

## 🧭 Estrategia de Pruebas

Una buena estrategia de pruebas define el **qué**, **cómo**, **cuándo** y **quién**:

### 🎯 Objetivos de calidad

- ✅ Alinearse con los criterios de éxito del proyecto (ej. “0 defectos críticos en producción” o “tiempo de respuesta < 200 ms”).
    
- ⚖️ Equilibrar tiempo, coste y alcance: decidir qué áreas necesitan mayor cobertura y cuáles pueden testearse más superficialmente.
    

### 🧪 Tipología de pruebas

- 🔹 **Funcionales**: unitarias, integración, sistema, aceptación.
    
- 🔸 **No funcionales**: rendimiento, seguridad, usabilidad, accesibilidad.
    
- 🔍 **Exploratorias y ad-hoc**: detectar escenarios no previstos.
    

### 📊 Enfoque de priorización

- 🔥 **Basado en riesgos**: enfocar esfuerzo en módulos críticos (pagos, login, datos sensibles).
    
- 🧩 **Cobertura de requisitos**: asegurar que todas las historias de usuario están cubiertas.
    
- 🧬 **Cobertura de código**: usar métricas de líneas/ramas sin sacrificar relevancia de pruebas.
    

### 👥 Asignación de recursos

- 🧑‍💻 Quienes diseñan, automatizan, ejecutan, revisan defectos y validan correcciones.
    

### 📆 Calendario

- ⏩ Fases de prueba solapadas con desarrollo (Shift-Left).
    
- 📦 Pruebas de sistema y E2E justo antes de cada demo o release candidate.
    

---

## ⏱️ Estimación de Esfuerzo

### 🧮 Técnicas

- 🃏 **Planning Poker / Wideband Delphi**: estimación por puntos o tiempo.
    
- 📚 **Analogía histórica**: comparación con proyectos anteriores.
    

### 📌 Factores clave

- 🔢 Número y complejidad de historias de usuario.
    
- 🤖 Nivel de automatización existente.
    
- 🧪 Datos y entornos necesarios.
    
- 🔗 Dependencias externas y disponibilidad de entornos.
    

---

## 🧷 Matriz de Trazabilidad

La matriz de trazabilidad garantiza que **cada requisito** tenga al menos un caso de prueba y que **cada caso de prueba** se relacione con uno o más requisitos.

|📄 ID Requisito|📋 Descripción|🧪 ID Caso de Prueba|🧬 Tipo de Prueba|📊 Estado|
|---|---|---|---|---|
|RQ-001|Login con usuario válido|TC-001|Unitario, E2E|✅ Aprobado|
|RQ-002|Error si credenciales inválidas|TC-002|Unitario, UI|⏳ En curso|
|RQ-010|Exportar reporte en PDF|TC-010|Integración|💤 Pendiente|

### 📈 Uso

- 🔎 Detectar requerimientos no probados o tests sin requisitos.
    
- 📢 Facilitar auditorías y comunicación con stakeholders.



---
# ✏️2. Diseño y Preparación

# 🧾 Plantilla de Test Cases

Esta plantilla sirve como guía para diseñar y documentar casos de prueba de manera manual. Es especialmente útil cuando no se utilizan herramientas automatizadas para registrar los test cases.

---

## 📋 Estructura de la plantilla

- **ID**: Identificador del caso de prueba
    
- **Título**: Objetivo del test (Qué se desea probar)
    
- **Descripción**: Breve explicación de lo que se va a probar
    
- **Precondiciones**: Requisitos previos necesarios para ejecutar el test case (datos, entorno, usuario logueado, etc.)
    
- **Datos de prueba**: Querys, credenciales, archivos u otros datos necesarios
    
- **Pasos**: Lista paso a paso sobre cómo ejecutar la prueba
    
- **Resultado esperado**: Comportamiento esperado del sistema si la prueba se ejecuta correctamente
    
- **Pass / Fail**: Estado del caso de prueba (si pasó o falló)
    
- **Prioridad**: Crítica, Alta, Media o Baja
    
- **Etiquetas**: Tags que faciliten la búsqueda o clasificación del caso
    
- **Evidencias**: Capturas de pantalla, gifs, videos u otros recursos visuales que evidencien la ejecución
    
- **Diseñado por**: Nombre de la persona que creó el caso
    
- **Ejecutado por**: Nombre de quien ejecutó la prueba
    
- **Fecha de ejecución**: Fecha en la que se corrió la prueba
    
- **Comentarios**: En caso de fallo, una descripción breve explicando el motivo y el ID del bug reportado
    

## 🧠 Nota útil

Muchas herramientas de gestión de pruebas (como TestRail, Zephyr o Xray) ya incluyen campos similares de forma automática.  
Sin embargo, esta plantilla es muy práctica para:

- Documentar pruebas en etapas tempranas de proyectos
    
- Compartir test cases por correo o archivos simples
    
- Hacer seguimiento manual en hojas de cálculo

---

# 🧠 Técnicas de Diseño

## 🧩 Técnicas de diseño

- 🎯 **Partición de equivalencia**: agrupar datos en clases válidas / no válidas.
    
- 🔄 **Análisis de valores límite**: probar justo dentro y fuera de rangos.
    
- 🗂️ **Tablas de decisión**: combinar múltiples condiciones y acciones esperadas.
    

---

# 🧪 Datos de Prueba y Entorno

## 🧬 Datos de prueba

- 🧻 **Sintéticos vs. enmascarados**: usar datos ficticios o clonar y anonimizar producción.
    
- 📈 **Volúmenes**: para pruebas de carga o stress, definir tamaños y patrones de acceso.
    
- 🔁 **Reutilización**: mantener sets de datos modulares y versionados.
    

## 🏗️ Entorno de pruebas

- 🧪 **Staging**: réplica lo más fiel posible a producción (BD, microservicios, config).
    
- 🧱 **Sandbox/QA**: entornos aislados para pruebas exploratorias o desarrollo temprano.
    
- 🛠️ **Control de versiones de entorno**: Infra as Code (Terraform, Ansible) para reproducibilidad.
    

---

# 🚀 3. Ejecución

## 🧾 Registro de Resultados

- Documentar: 📅 fecha, ⏰ hora, 🔖 versión de la app, 🏞️ entorno, 📄 nombre del caso, ✅ resultado.
    
- Adjuntar **evidencias**: 📸 capturas, 🧾 logs, 🔍 trazas backend, 🧬 respuestas de API.
    

## 🐞 Gestión de Incidencias

### 📌 Defect Tracking

- 🧩 Crear ticket con ID único, descripción clara, pasos para reproducir y severidad.
    
- 🧑‍💻 Asignar responsable de corrección y priorización.
    

### 🔁 Ciclo de vida del defecto

1. 🆕 **Nuevo** → 2. 🧾 **Asignado** → 3. 🔨 **En progreso** → 4. ✅ **Resuelto** → 5. 🔍 **Verificado** → 6. 📁 **Cerrado**
    

- ✏️ Actualizar comentarios (quién probó, evidencia de validación, etc.)
    

## 🔧 Herramientas de Seguimiento

- 🗃️ **Jira**: historias y tickets; flujos personalizables.
    
- 🧪 **TestRail / Zephyr**: planes, suites, ejecuciones, reportes.
    
- 🔗 **Integraciones CI/CD**: conectar resultados de test automáticos a tickets.
    

---

# 📊 4. Reporte y Seguimiento

## 📈 Métricas Clave

- 🐞 **Tasa de defectos**: (Abiertos / Reportados) × 100%
    
- 📋 **Cobertura de pruebas**:
    
    - 📄 **Requisitos**: % con al menos un test
        
    - 🧬 **Código**: % líneas o ramas cubiertas
        
- ⏱️ **MTTR**: tiempo medio de resolución verificada
    
- 📦 **Defect Density**: defectos por módulo o KLOC
    
- 🔁 **Pasos por defecto**: fallos consecutivos, flaky tests
    

## 🧾 Test Summary Report

1. 🌐 **Visión general**: alcance, tipo de pruebas, versiones.
    
2. 📊 **Resumen ejecución**: planificados vs ejecutados, éxito, fallo, pendientes.
    
3. 🐞 **Defectos**: totales, abiertos, críticos, bloqueantes.
    
4. ⚠️ **Riesgos y bloqueos**: baja cobertura, alta falla.
    
5. 💡 **Recomendaciones**: acciones urgentes, mantenimiento.
    

---

# ✅ 5. Cierre

## 🧠 Lecciones Aprendidas

- Reunión retrospectiva de testing:
    
    - ❓ ¿Qué faltó probar o qué datos faltaron?
        
    - 📊 ¿Qué flujos mostraron más defectos?
        
    - 🛠️ ¿Dónde hubo pérdida de tiempo por entornos o flaky tests?
        
- 📝 Documentar mejoras: actualizar trazabilidad, datos, scripts.
    

## 📋 Checklist de Entrega

- ✅ Casos críticos ejecutados y validados.
    
- 🐛 Defectos críticos resueltos y cerrados.
    
- 🧽 Datos y entornos en estado estable o desmantelados.
    
- 📄 Test Summary Report aprobado por stakeholders.
    
- 🗂️ Artefactos archivados y versionados (evidencias, scripts, informes).

---

↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
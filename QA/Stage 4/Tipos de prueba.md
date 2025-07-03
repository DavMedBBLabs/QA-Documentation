# 🧪 Tipos de Pruebas de Software

## 1. 🧩 Pruebas Funcionales

Validan **qué** hace el sistema, asegurando que cada funcionalidad cumple con los requisitos.

### 1.1 🔥 Smoke Testing

- ✅ **Objetivo:** Verificar rápidamente que las funcionalidades críticas están disponibles tras una compilación o despliegue.
    
- 📏 **Alcance:** Conjunto muy reducido de casos de prueba, cubriendo flujos críticos.
    
- 🚨 **Criterio de Éxito:** Si alguno falla, se detienen las pruebas.
    
- 🔁 **Frecuencia:** En cada build del CI.
    

### 1.2 🛠️ Sanity Testing

- ✅ **Objetivo:** Comprobar que una corrección puntual funciona correctamente.
    
- 📏 **Alcance:** Área limitada (módulo o bug fix).
    
- 🎯 **Criterio de Éxito:** Validar corrección sin profundizar en alternativos.
    
- 🔁 **Frecuencia:** Tras hotfixes o correcciones menores.
    

### 1.3 🧭 Pruebas Exploratorias

- ✅ **Objetivo:** Descubrir errores inesperados mediante exploración libre.
    
- 🧾 **Características:**
    
    - 🎯 **Charters** (objetivos por sesión).
        
    - ⏱️ **Time-boxing** de 30–90 minutos.
        
    - 📝 Documentación en tiempo real.
        
- 🧠 **Beneficio:** Detectar bugs que escapan a pruebas automatizadas.
    

### 1.4 📋 Pruebas Basadas en Requerimientos

- ✅ **Objetivo:** Validar que cada requisito esté cubierto por al menos una prueba.
    
- 🛠️ **Método:**
    
    1. 🔍 Extraer criterios de aceptación.
        
    2. 🧩 Mapear en matriz de trazabilidad.
        
    3. ✍️ Diseñar pruebas para flujos primarios y alternativos.
        
- 📊 **Métrica:** 100 % de requisitos cubiertos.
    

---

## 2. ⚙️ Pruebas No Funcionales

Validan **cómo** se comporta el sistema bajo condiciones específicas.

### 2.1 🚀 Rendimiento

- 🧪 **Load Testing:** Simular carga esperada, medir rendimiento.
    
- 📈 **Stress Testing:** Incrementar carga hasta provocar fallos.
    
- ⏳ **Soak Testing:** Carga prolongada para detectar degradación.
    

> 📊 **Métricas:** SLAs, tiempos de respuesta, uso de recursos.

### 2.2 🔐 Seguridad

- ✅ **Objetivo:** Detectar vulnerabilidades de seguridad.
    
- 📚 **OWASP Top 10:**
    
    - 💥 Inyecciones
        
    - 🔓 Autenticación rota
        
    - 🧾 Exposición de datos sensibles
        
    - 📦 XXE
        
    - 🚫 Control de acceso incorrecto
        
- 🔍 **Tipos de prueba:**
    
    - 🧬 SAST (estático)
        
    - 🌐 DAST (dinámico)
        
    - 🕵️‍♂️ Pentesting (manual y auto)
        
- ✅ **Criterio de Éxito:** 0 hallazgos críticos, mitigación para altos/medios.
    

### 2.3 👩‍💻 Usabilidad y Accesibilidad

- 🧪 **Usabilidad:**
    
    - ⏱️ Tiempo/tasa de éxito en tareas clave.
        
    - 📋 Encuestas SUS.
        
- ♿ **Accesibilidad:**
    
    - ✅ WCAG 2.1 AA: contraste, navegación, semántica.
        
    - 🧰 Herramientas: axe, Lighthouse + pruebas con usuarios reales.
        
- 📊 **Criterios:** ≥ 90 % de reglas WCAG pasadas, sin bloqueos.
    

---

## 3. 🤖 Pruebas Automatizadas vs Manuales

### 3.1 ⚙️ Cuándo Automatizar

- ✅ Funcionalidad estable.
    
- 🔁 Alta frecuencia de ejecución.
    
- ⏳ Alto esfuerzo manual.
    
- 📈 Alto ROI.
    

### 3.2 👨‍🔬 Cuándo Ejecutar Manual

- 🧭 Exploratorias o ad-hoc.
    
- 👁️‍🗨️ Validaciones visuales complejas.
    
- 🧷 Casos únicos con bajo valor de repetición.
    

---

## 4. 🧱 Diseño de Scripts y Frameworks

### 4.1 🧩 Page Object Model (POM)

- 📚 **Definición:** Modelo de página como clase con métodos encapsulados.
    
- ✅ **Ventajas:** Centraliza lógica UI, simplifica mantenimiento.
    
- 🛠️ **Práctica:** Métodos atómicos y claros.
    

### 4.2 🧮 Data-Driven Testing

- 📚 **Definición:** Separación entre lógica y datos de prueba.
    
- ✅ **Ventajas:** Reutilización y ampliación sencilla.
    
- 🧾 **Práctica:** Archivos estructurados (CSV, JSON) con valores esperados.
    

### 4.3 🔑 Keyword-Driven / Hybrid

- 📚 **Definición:** Palabras clave describen acciones ("Click", "Verify", etc).
    
- ✅ **Ventajas:** Permite a no-devs escribir escenarios.
    
- 📦 Aísla implementación técnica.
    

---

## 5. 🧰 Complementos Clave para Estrategia QA

- 🔄 **Flaky Tests:** Retries, timeouts dinámicos, diagnóstico de causa raíz.
    
- 🔗 **CI/CD:** Integración de pruebas en pipelines.
    
- 📊 **Reportes:** Allure, HTML reports, dashboards de métricas.
    
- 🧹 **Mantenimiento:** Refactorización y limpieza de casos obsoletos.

---

↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
# 🧪 Estrategia de Testing: Niveles, Prácticas y Herramientas

Para asegurar una estrategia de calidad integral, es fundamental entender cada nivel de testing en profundidad y cómo se interrelacionan. A continuación encontrarás una descripción detallada de cada nivel, sus objetivos, prácticas recomendadas, herramientas típicas y aspectos adicionales que completan el panorama.

---

## 1. Testing Unitario (Unit Testing)

### 🎯 Objetivo

Verificar el correcto comportamiento de la unidad de código más pequeña —funciones, métodos o clases— de forma aislada.

### 🔍 Aspectos clave

- **Aislamiento de componentes**
    
    - Uso de _mocks_, _stubs_ y _fakes_ para simular dependencias externas.
        
    - Inyección de dependencias para facilitar el reemplazo de componentes reales.
        
- **Diseño de pruebas**
    
    - Casos centrados en lógica de negocio, condiciones de frontera y manejo de errores.
        
    - Uso de TDD para guiar el diseño y asegurar cobertura desde el inicio.
        
- **Métricas y prácticas**
    
    - Cobertura de ramas y condiciones críticas.
        
    - Pruebas independientes y rápidas.
        
- **Herramientas habituales**
    
    - **Java**: JUnit, TestNG
        
    - **.NET**: NUnit, xUnit
        
    - **Python**: pytest, unittest
        
    - **JavaScript**: Jest, Mocha
        

---

## 2. Testing de Integración (Integration Testing)

### 🎯 Objetivo

Comprobar que varios componentes o módulos interactúan correctamente entre sí.

### 2.1 Estrategias de Integración

- **Top-Down**
    
    - Se prueban módulos de alto nivel usando _stubs_ para los inferiores.
        
- **Bottom-Up**
    
    - Se prueban primero los componentes de bajo nivel usando _drivers_.
        
- **Sandwich (Híbrido)**
    
    - Combinación de ambos enfoques para detectar errores en capas intermedias.
        

### 2.2 Ámbitos de Integración

- **APIs Web**
    
    - Validar contratos REST, gRPC o colas.
        
    - Herramientas: Postman, RestAssured, pytest + requests.
        
- **Bases de datos**
    
    - Verificar operaciones CRUD e integridad.
        
    - Uso de bases in-memory (H2, SQLite), Docker o DBUnit.
        

### 2.3 Buenas Prácticas

- Entornos dedicados con datos controlados.
    
- Restauración del estado entre pruebas.
    
- Registro de transacciones y tiempos de respuesta.
    

---

## 3. Testing de Sistema (System Testing)

### 🎯 Objetivo

Validar el sistema completo en un entorno que replica producción.

### 3.1 Testing End-to-End (E2E)

- Simulación de flujos reales de usuario.
    
- Enfoque en flujos críticos como login, compra o pagos.
    
- Herramientas: Selenium, Cypress, Playwright, TestCafe.
    

### 3.2 Pruebas de Regresión

- Verificar que no se rompa funcionalidad existente.
    
- Ejecutar continuamente o antes de releases.
    

### 3.3 Alineación con Performance y Seguridad

- Pruebas de carga ligeras y análisis DAST en entorno de sistema.
    

---

## 4. Testing de Aceptación (Acceptance Testing)

### 🎯 Objetivo

Confirmar que el software satisface los criterios del negocio o cliente.

### 4.1 Criterios de Aceptación

- Definidos junto al Product Owner durante la refinación.
    
- Claros, medibles y verificables.
    

### 4.2 UAT vs BDD

- **UAT (User Acceptance Testing)**
    
    - Ejecutado por usuarios finales.
        
    - Manual o semiautomatizado, centrado en workflows reales.
        
- **BDD (Behavior-Driven Development)**
    
    - Escenarios escritos en lenguaje natural (Gherkin).
        
    - Herramientas: Cucumber, SpecFlow, Behave.
        
    - Promueve colaboración QA-dev-negocio.
        

---

## 5. Temas Complementarios para una Cobertura Integral

### 5.1 Test Pyramid (Pirámide de Testing)

- Base: tests unitarios
    
- Medio: integración
    
- Tope: E2E
    
- Optimiza feedback y costos.
    

### 5.2 Contract Testing

- Validar contratos entre servicios (consumer-driven contracts).
    
- Herramientas: Pact, Spring Cloud Contract.
    

### 5.3 Service Virtualization

- Emular servicios externos aún no disponibles.
    
- Herramientas: WireMock, Mountebank.
    

### 5.4 Gestión de Entornos y Datos de Prueba

- IaC para reproducibilidad.
    
- Enmascaramiento y generación de datos realistas.
    

### 5.5 Medición y Métricas por Nivel

|Nivel|Métricas sugeridas|
|---|---|
|Unit Testing|Cobertura de ramas, tiempo promedio de ejecución|
|Integration|Tasa de fallos, tiempo de despliegue|
|System|Tiempo total E2E, flaky test rate|
|Acceptance|% de historias aceptadas sin retrabajo|

### 5.6 Entry/Exit Criteria

- Definir umbrales por nivel (ej. ≥80 % cobertura para unit tests antes de integración).
    

### 5.7 Automatización vs. Manual

- Unit y integración: alta automatización.
    
- E2E y aceptación: combinación manual/automático.
    

### 5.8 Roles y Responsabilidades

|Rol|Enfoque principal|
|---|---|
|**Desarrolladores**|Unit tests, contract tests|
|**QA Engineers**|Integración, sistema, aceptación|
|**Product Owners/Usuarios**|Validación UAT y criterios de negocio|

### 5.9 Ciclo de Feedback y Mejora Continua

- Usar dashboards de resultados para retroalimentar y ajustar prioridades.
    

---

## ✅ Conclusión

Comprender cada nivel de testing, sus objetivos, buenas prácticas y herramientas permite construir una estrategia sólida y escalable. Sumando aspectos como contract testing, métricas, virtualización de servicios y gestión de entornos, podrás elevar la calidad de producto y maximizar eficiencia.

---

↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
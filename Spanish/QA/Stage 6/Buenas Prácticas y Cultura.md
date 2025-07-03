# 🧭 1. Shift-Left y Shift-Right Testing

## 🔄 1.1 Shift-Left Testing

Implica adelantar actividades de calidad y prueba hacia fases tempranas del ciclo de vida del desarrollo.

- **🧩 Revisiones de requisitos y diseño**: Involucrar a testers desde la definición de user stories para clarificar criterios de aceptación y detectar ambigüedades.
    
- **⚙️ Pruebas unitarias y de integración en CI**: Ejecutar automáticamente suites de pruebas al hacer commit para recibir feedback inmediato.
    
- **🧠 Análisis estático y code reviews**: Complementar el testing dinámico con herramientas de análisis de calidad de código y sesiones de revisión cruzada.
    

## 🚀 1.2 Shift-Right Testing

Se refiere a extender la validación hacia entornos de producción y post-despliegue.

- **📦 Canary releases y deployment progresivo**: Desplegar cambios a un subconjunto reducido de usuarios para detectar problemas antes de un rollout completo.
    
- **📊 Monitoreo y observabilidad**: Recoger métricas de rendimiento, errores y uso en tiempo real (logs, trazas, métricas de negocio) y alimentar ciclos de mejora.
    
- **🧪 Pruebas en producción**: Validar hipótesis de usabilidad o rendimiento con pruebas A/B y _feature flags_ controlados.
    

---

# 🌀 2. Testing en Agile y DevOps

## 🧷 2.1 Integración continua de testing

- Los pipelines de CI actúan como guardias de calidad, ejecutando pruebas unitarias, de integración y revisiones de seguridad en cada paso del _merge request_.
    
- Los resultados deben ser accesibles y legibles, con reportes automáticos y notificaciones para todo el equipo.
    

## 🚚 2.2 Entrega Continua y despliegue

- Incorporar suites de pruebas end-to-end y de regresión en el pipeline de CD, garantizando que cada despliegue a staging o producción cumple criterios mínimos de salud.
    
- Automatizar _rollback_ en caso de falla de smoke tests o umbrales de error en producción.
    

## 🗓️ 2.3 Cadencia de sprints y testing iterativo

- Planificar actividades de prueba como historias de usuario con estimación de esfuerzo y criterios de aceptación claros.
    
- Revisar en cada sprint demo los resultados de pruebas y debatir ajustes de alcance o criterios de calidad.
    

## 💾 2.4 Quality as Code

- Versionar configuraciones de pruebas, scripts y entornos con el mismo rigor que el código de producción.
    
- Gestionar infraestructuras de test (contenedores, datos) como código mediante herramientas IaC.
    

---

# 🤝 3. Colaboración Multidisciplinaria

## 👥 3.1 QA, Desarrollo y Product trabajando en tándem

- **🧠 Planning conjunto**: QA participa en refinement y planning para clarificar requisitos y definir casos de prueba desde el inicio.
    
- **👨‍🔬 Paired testing y mob testing**: Sesiones en las que testers y desarrolladores colaboran explorando funcionalidades y validando flujos críticos.
    
- **📣 Daily stand-ups compartidos**: Compartir bloqueos y hallazgos de pruebas junto con progresos de desarrollo, evitando silos de información.
    

## 📢 3.2 Comunicación y transparencia

- Mantener tableros visibles (por ejemplo en Jira o tableros físicos) con el estado de casos, defectos y métricas de calidad.
    
- Definir canales claros (Slack, Teams) para reporte inmediato de fallos en entornos de test o producción.
    

## 🛡️ 3.3 Propiedad colectiva de la calidad

- Fomentar la idea de que “la calidad es responsabilidad de todos”: no delegar el testing únicamente a QA, sino integrar pruebas y validación en el día a día de cada rol.
    
- Reconocer y celebrar cuando se previenen defectos en fases tempranas o cuando se mejora la cobertura y estabilidad.
    

---

# 🔁 4. Cultura de Mejora Continua

## 🧩 4.1 Retrospectivas de calidad

- Dedicar espacio en las retrospectivas para discutir incidentes de testing, defectos críticos y oportunidades de automatización.
    
- Generar acciones concretas: mejorar datos de prueba, optimizar pipelines o introducir nuevas métricas.
    

## 📚 4.2 Formación y conocimiento compartido

- Organizar workshops internos sobre nuevas herramientas, patrones de diseño de pruebas o metodologías (BDD, contract testing).
    
- Documentar buenas prácticas y aprendizajes en un repositorio accesible al equipo.
    

## 📈 4.3 Medición y métricas saludables

- Más allá de la cobertura de código o el número de pruebas, medir el tiempo hasta la detección de defectos, tasa de _flaky tests_ y tiempo de recuperación tras un fallo.
    
- Usar dashboards de calidad en tiempo real como palanca para la toma de decisiones.
    

---

# 📌 5. Temas Adicionales Importantes

## 🔗 5.1 Testing de APIs y contract testing

- Validar contratos de servicios mediante esquemas o herramientas de _pact testing_, garantizando que cambios en un microservicio no rompan consumidores.
    

## ♿ 5.2 Pruebas de accesibilidad integradas

- Incluir _checks_ automáticos de WCAG en pipelines y auditorías manuales con usuarios para detectar barreras de uso.
    

## 🧪 5.3 Gestión de datos de prueba

- Diseñar estrategias de generación y mascarado de datos reales para acercar entornos de test a producción sin comprometer la privacidad.
    

## 🔍 5.4 Estrategias de mitigación de tests inestables

- Identificar y aislar _flakiness_, aplicar _retries_ inteligentes y revisar las causas raíz para mantener la confianza en la suite.

---


↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
## 🎯 Técnicas de Priorización de Casos de Prueba

La priorización de casos de prueba es esencial cuando hay limitaciones de tiempo, recursos o cuando se busca maximizar la cobertura con el menor esfuerzo. Estas son las técnicas más comúnmente utilizadas y avaladas por la industria y estándares como **ISTQB**, **IEEE 829** y prácticas descritas en cursos como el de **ISTQB Foundation Level**:

### 1. **Risk-Based Testing (Pruebas Basadas en Riesgo)**

- **Descripción**: Se asigna prioridad según el nivel de riesgo del módulo o funcionalidad. Esto incluye el impacto potencial de una falla y la probabilidad de que ocurra.
    
- **Cuándo usar**: En sistemas críticos (banca, salud, aeronáutica).
    
- **Beneficio**: Se enfocan esfuerzos en los componentes con mayor impacto de negocio.
    

### 2. **Business Priority (Priorización por Valor de Negocio)**

- **Descripción**: Se priorizan los casos con mayor impacto en la experiencia del usuario o funciones clave del negocio.
    
- **Cuándo usar**: En productos orientados al cliente final o en MVPs.
    
- **Beneficio**: Maximiza la cobertura de funcionalidades clave.
    

### 3. **Test Case Execution History**

- **Descripción**: Se basa en el historial de ejecución anterior. Casos que han fallado frecuentemente se priorizan.
    
- **Cuándo usar**: En proyectos en mantenimiento o con regresiones frecuentes.
    
- **Beneficio**: Prevención efectiva de fallas conocidas.
    

### 4. **Requirement Volatility**

- **Descripción**: Casos relacionados con requisitos que cambian con frecuencia reciben prioridad.
    
- **Cuándo usar**: En entornos ágiles donde los requerimientos cambian seguido.
    
- **Beneficio**: Mayor alineación con cambios recientes.
    

### 5. **Customer-Reported Issues**

- **Descripción**: Casos relacionados con defectos reportados por clientes.
    
- **Cuándo usar**: En productos en producción.
    
- **Beneficio**: Aumento directo en satisfacción del cliente.
    

### 6. **Code Complexity (complejidad del código)**

- **Descripción**: Módulos complejos (por métricas como McCabe o Halstead) tienen más posibilidad de defectos.
    
- **Cuándo usar**: En validaciones técnicas profundas.
    
- **Beneficio**: Mejora la estabilidad técnica del sistema.

---

↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
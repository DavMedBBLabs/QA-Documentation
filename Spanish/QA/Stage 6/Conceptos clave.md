## 🧠 Análisis de Riesgos

El análisis de riesgos en pruebas de software es el proceso sistemático de identificar, evaluar y priorizar los riesgos potenciales que pueden afectar el sistema bajo prueba.

### 🔹 Componentes clave

- **Identificación de riesgos**: Determinar qué puede fallar en el software (funcionalidades críticas, componentes complejos, integraciones)
    
- **Evaluación de probabilidad**: Qué tan probable es que ocurra cada riesgo
    
- **Evaluación de impacto**: Qué tan grave sería el impacto si el riesgo se materializa
    
- **Priorización**: Combinando probabilidad e impacto para determinar qué áreas requieren más atención en las pruebas
    

### 📊 Ejemplo práctico

En un sistema bancario, transferir dinero tiene alto riesgo (alto impacto si falla), mientras que cambiar el color de un botón tiene bajo riesgo.

## 🔍 Partición de Equivalencia

Es una técnica de diseño de casos de prueba que divide el dominio de entrada en clases o particiones donde se espera que el software se comporte de manera similar.

### 🔹 Principio fundamental

Si el software funciona correctamente para un valor representativo de una partición, debería funcionar para todos los valores de esa partición.

### 🔹 Tipos de particiones

- **Particiones válidas**: Datos de entrada que el sistema debería aceptar y procesar correctamente
    
- **Particiones inválidas**: Datos que el sistema debería rechazar o manejar como errores
    

### 📊 Ejemplo práctico

Para un campo "edad" que acepta valores de 18 a 65:

- **Partición válida**: 18-65 años (probar con 25, 40, 60)
    
- **Particiones inválidas**:
    
    - Menores de 18 (probar con 10, 17)
        
    - Mayores de 65 (probar con 70, 100)
        
    - Valores no numéricos (letras, símbolos)
        

## 📏 Criterios de Cobertura

Son métricas que determinan qué tan exhaustivamente se ha probado el software, estableciendo objetivos medibles para las pruebas.

### 🔹 Tipos principales

#### ✅ Cobertura de Código

- **Cobertura de sentencias**: Porcentaje de líneas de código ejecutadas
    
- **Cobertura de ramas**: Porcentaje de decisiones verdadero/falso probadas
    
- **Cobertura de condiciones**: Evaluación de cada condición booleana
    
- **Cobertura de caminos**: Diferentes rutas de ejecución probadas
    

#### ✅ Cobertura Funcional

- **Cobertura de requisitos**: Porcentaje de requisitos verificados
    
- **Cobertura de casos de uso**: Escenarios de usuario probados
    
- **Cobertura de interfaces**: APIs y puntos de integración verificados
    

### 📊 Ejemplo de cobertura de ramas

```
if (edad >= 18 && saldo > 100) {
    aprobarPrestamo();
} else {
    rechazarPrestamo();
}
```

Para 100% de cobertura de ramas necesitas:

- Caso 1: edad ≥ 18 Y saldo > 100 (rama verdadera)
    
- Caso 2: edad < 18 O saldo ≤ 100 (rama falsa)
    

## 🔗 Integración de los Tres Conceptos

### 🔹 Flujo de trabajo típico

1. **Análisis de riesgos** → Identifica áreas críticas
    
2. **Partición de equivalencia** → Reduce espacio de prueba
    
3. **Criterios de cobertura** → Mide el nivel de exhaustividad
    

### 📊 Ejemplo integrado

**Sistema de e-commerce**  
**Análisis de riesgos**: El proceso de pago es crítico (alto impacto)  
**Partición de equivalencia**:

- Tarjetas válidas vs inválidas
    
- Montos dentro del límite vs excedidos  
    **Criterios de cobertura**: Asegurar 90% de cobertura de código en el módulo de pago
    

## 🚀 Por qué son Esenciales

Dado que es imposible probar exhaustivamente, estos enfoques permiten:

- ✅ **Optimizar recursos limitados** de testing
    
- ✅ **Maximizar la detección de defectos** con menos pruebas
    
- ✅ **Proporcionar confianza medible** en la calidad
    
- ✅ **Justificar decisiones** sobre cuándo es suficiente el testing

---
## **CI - Continuous Integration (Integración Continua)**

### **Definición**

La Integración Continua es una práctica de desarrollo donde los desarrolladores integran su código en un repositorio compartido de manera frecuente (varias veces al día), y cada integración se verifica automáticamente mediante la construcción del proyecto y la ejecución de pruebas automatizadas.

### **Componentes clave de CI**:

**1. Integración frecuente**

- Los desarrolladores suben código al repositorio principal múltiples veces al día
- Se evita el "integration hell" (infierno de integración)

**2. Construcción automatizada**

- Cada commit dispara automáticamente el proceso de build
- Compilación, empaquetado y verificación de dependencias

**3. Pruebas automatizadas**

- Ejecución automática de unit tests, integration tests
- Feedback inmediato sobre la calidad del código

**4. Feedback rápido**

- Notificaciones inmediatas si algo falla
- Los problemas se detectan y resuelven rápidamente

### **Ejemplo de flujo CI**:
	Developer commits code → 
	GitHub/GitLab triggers CI pipeline → 
	Build project → 
	Run automated tests → 
	Report results (pass/fail) → 
	Notify team

### **Herramientas CI populares**:

- Jenkins
- GitHub Actions
- GitLab CI
- Azure DevOps
- CircleCI

## **CD - Continuous Delivery/Deployment (Entrega/Despliegue Continuo)**

Aquí hay **dos conceptos diferentes** que comparten las siglas CD:

### **Continuous Delivery (Entrega Continua)**

**Definición**: Extensión de CI donde el código que pasa todas las pruebas se prepara automáticamente para ser liberado a producción, pero el despliegue final requiere aprobación manual.

**Características**:

- El código está **siempre listo** para ser desplegado
- Automatización hasta el punto de despliegue
- **Decisión humana** para el release final
- Reducción de riesgos en releases

### **Continuous Deployment (Despliegue Continuo)**

**Definición**: Nivel más avanzado donde cada cambio que pasa todas las etapas de la pipeline se despliega **automáticamente** a producción sin intervención humana.

**Características**:

- **Automatización completa** hasta producción
- **Sin intervención manual** para deployments
- Requiere alta confianza en pruebas automatizadas
- Feedback directo desde usuarios reales

## **Diferencias Clave entre CI y CD**

|Aspecto|CI|Continuous Delivery|Continuous Deployment|
|---|---|---|---|
|**Objetivo**|Integrar código frecuentemente|Preparar releases|Desplegar automáticamente|
|**Automatización**|Build + Tests|Hasta pre-producción|Hasta producción|
|**Intervención humana**|Mínima|Aprobación para release|Ninguna|
|**Frecuencia**|Múltiples veces/día|Según necesidad|Cada commit válido|

## **Pipeline Completo CI/CD**

### **Etapas típicas**:
	1. CODE COMMIT (Developer)
	   ↓
	2. CI PIPELINE
	   • Build/Compile
	   • Unit Tests
	   • Static Code Analysis
	   • Security Scans
	   ↓
	3. CD PIPELINE - CONTINUOUS DELIVERY
	   • Integration Tests
	   • Deploy to Staging
	   • Acceptance Tests
	   • Performance Tests
	   • [MANUAL APPROVAL]
	   ↓
	4. CD PIPELINE - CONTINUOUS DEPLOYMENT
	   • Deploy to Production
	   • Smoke Tests
	   • Monitoring/Alerts

## **Beneficios de CI/CD**

### **CI Benefits**:

- **Detección temprana** de bugs
- **Reducción de conflictos** de integración
- **Mejor calidad** de código
- **Feedback rápido** al equipo

### **CD Benefits**:

- **Releases más frecuentes** y confiables
- **Menor riesgo** en deployments
- **Time-to-market** reducido
- **Mayor satisfacción** del cliente

## **Ejemplo Práctico**

**Escenario**: Aplicación web de e-commerce

**CI**:

- Developer hace commit → Jenkins ejecuta tests → Si pasan, código se integra
- Si fallan → Notificación al developer para fix

**Continuous Delivery**:

- Código integrado → Deploy automático a staging → Tests de aceptación → **Espera aprobación manual** → Deploy a producción

**Continuous Deployment**:

- Código integrado → Deploy automático a staging → Tests pasan → **Deploy automático a producción** → Monitoreo

## **Implementación Gradual**

La mayoría de organizaciones siguen esta progresión:

1. **Primero CI** - Establecer integración continua sólida
2. **Luego Continuous Delivery** - Automatizar hasta staging
3. **Finalmente Continuous Deployment** - Solo cuando hay alta confianza

CI/CD transforma el desarrollo de software de un proceso manual y propenso a errores en un flujo automatizado, confiable y eficiente.


---

## **Code Review (Revisión de Código)**

### **Definición**

Es el proceso sistemático donde otros desarrolladores examinan el código escrito por un compañero antes de que se integre al repositorio principal, buscando errores, mejoras y verificando que cumple con los estándares del equipo.

### **Proceso típico**:

1. **Developer A** escribe código y crea un Pull Request (PR) / Merge Request (MR)
2. **Developer B y C** son asignados como revisores
3. **Revisores** examinan el código línea por línea
4. **Comentarios y sugerencias** se agregan al PR
5. **Developer A** hace correcciones basadas en feedback
6. **Aprobación final** y merge al branch principal

### **Qué se revisa**:

- **Funcionalidad**: ¿El código hace lo que debe hacer?
- **Legibilidad**: ¿Es fácil de entender?
- **Estándares**: ¿Sigue las convenciones del equipo?
- **Seguridad**: ¿Hay vulnerabilidades potenciales?
- **Performance**: ¿Es eficiente?
- **Tests**: ¿Están incluidas las pruebas necesarias?

### **Ejemplo de comentario en code review**:
	// Código original
	if (user.age > 18 && user.status == "active") {
	    processUser(user);
	}
	
	// Comentario del revisor:
	// "Considera usar === en lugar de == para comparación estricta
	// y extraer esta condición a una función con nombre descriptivo"
	
	// Código mejorado
	if (isEligibleUser(user)) {
	    processUser(user);
	}
	
	function isEligibleUser(user) {
	    return user.age > 18 && user.status === "active";
	}
## **Pair Programming (Programación en Parejas)**

### **Definición**

Es una práctica donde dos desarrolladores trabajan juntos en el mismo código, en tiempo real, compartiendo una sola estación de trabajo.

### **Roles en Pair Programming**:

**Driver (Conductor)**:

- Escribe el código activamente
- Se enfoca en la implementación táctica
- Controla el teclado y mouse

**Navigator (Navegador)**:

- Revisa el código en tiempo real
- Piensa estratégicamente sobre el diseño
- Sugiere mejoras y detecta errores
- Considera el panorama general

### **Rotación de roles**:

Los desarrolladores intercambian roles cada 15-30 minutos para mantener ambos comprometidos.

### **Ejemplo de sesión**:
	Navigator: "¿Qué pasa si userId es null aquí?"
	Driver: "Tienes razón, debería validar eso primero"
	Navigator: "También considera usar un guard clause para hacer el código más legible"
	Driver: "Buena idea, lo refactorizo"
### **Variantes modernas**:

- **Remote Pair Programming**: Usando herramientas como VS Code Live Share
- **Mob Programming**: Más de 2 personas trabajando juntas

## **Análisis Estático de Código**

### **Definición**

Es el proceso automatizado de analizar el código fuente sin ejecutarlo, utilizando herramientas que detectan problemas potenciales, vulnerabilidades, violaciones de estilo y complejidad excesiva.

### **Tipos de análisis**:

**1. Análisis de Calidad**:

- Complejidad ciclomática
- Duplicación de código
- Métricas de mantenibilidad

**2. Análisis de Seguridad**:

- Vulnerabilidades conocidas (OWASP Top 10)
- Inyección SQL, XSS
- Gestión insegura de credenciales

**3. Análisis de Estilo**:

- Convenciones de nomenclatura
- Formato y indentación
- Longitud de funciones y clases

**4. Análisis de Bugs**:

- Null pointer exceptions
- Dead code (código inalcanzable)
- Condiciones siempre verdaderas/falsas

### **Herramientas populares**:

**Multiplataforma**:

- SonarQube/SonarCloud
- CodeClimate
- Checkmarx (seguridad)

**Por lenguaje**:

- **JavaScript**: ESLint, JSHint
- **Python**: Pylint, Flake8, Bandit
- **Java**: SpotBugs, PMD, Checkstyle
- **C#**: Roslyn Analyzers, FxCop

### **Ejemplo de reporte**:
	Issues encontradas:
	🔴 HIGH: Potential SQL Injection in line 45
	🟡 MEDIUM: Function 'processData' has cyclomatic complexity of 15 (max: 10)
	🔵 LOW: Variable 'temp_var' doesn't follow naming convention
	ℹ️  INFO: Unused import 'pandas' in line 3
## **Comparación de las Tres Prácticas**

| Aspecto                    | Code Review         | Pair Programming        | Análisis Estático     |
| -------------------------- | ------------------- | ----------------------- | --------------------- |
| **Timing**                 | Después de escribir | Durante escritura       | Continuo/Automatizado |
| **Humano vs Automatizado** | Humano              | Humano                  | Automatizado          |
| **Cobertura**              | Contextual y lógica | Diseño y implementación | Patrones y reglas     |
| **Feedback**               | Asíncrono           | Inmediato               | Inmediato             |
| **Costo**                  | Medio               | Alto                    | Bajo                  |

## **Cuándo Usar Cada Una**

### **Code Review** - Úsalo cuando:

- Necesitas perspectiva externa sobre el diseño
- Quieres validar lógica de negocio compleja
- El equipo está distribuido geográficamente
- Quieres documentar decisiones de diseño

### **Pair Programming** - Úsalo cuando:

- Trabajas en funcionalidades críticas o complejas
- Necesitas transferir conocimiento rápidamente
- Quieres resolver problemas difíciles colaborativamente
- El equipo es nuevo o está aprendiendo tecnologías

### **Análisis Estático** - Úsalo cuando:

- Quieres detectar problemas básicos automáticamente
- Necesitas hacer cumplir estándares de código consistentemente
- Quieres integrar verificaciones en CI/CD
- Buscas detectar vulnerabilidades de seguridad

## **Integración Óptima**

### **Flujo recomendado**:
	1. DESARROLLO
	   • Pair Programming (para código complejo)
	   • Análisis Estático (en IDE en tiempo real)
	
	2. PRE-COMMIT
	   • Análisis Estático (git hooks)
	   • Formateo automático
	
	3. POST-COMMIT
	   • Code Review (Pull Request)
	   • Análisis Estático (CI pipeline)
	
	4. CONTINUOUS
	   • Análisis Estático (scheduled scans)
	   • Métricas de calidad (dashboards)

### **Beneficios combinados**:

- **Análisis Estático** atrapa errores obvios automáticamente
- **Pair Programming** mejora el diseño durante la escritura
- **Code Review** valida lógica y arquitectura con perspectiva fresca

Estas tres prácticas se complementan perfectamente: el análisis estático maneja la detección automatizada de problemas comunes, el pair programming mejora la calidad durante la creación, y el code review proporciona la validación humana final con perspectiva externa.


---
## Stub

|Idea clave|“Contesta, pero no opina”.|
|---|---|
|**Qué hace**|Devuelve respuestas predeterminadas a las llamadas que reciba. No contiene lógica real ni validaciones.|
|**Cuándo usarlo**|Cuando el código necesita datos para avanzar (p. ej. un repositorio que siempre devuelve una lista fija).|
|**Ejemplo**|Un `UserRepositoryStub` cuya función `findById()` devuelve siempre el mismo usuario JSON sin consultar BD.|

En resumen, el stub **alimenta** al SUT (System Under Test) con datos controlados, pero no comprueba nada por sí mismo. [martinfowler.com](https://martinfowler.com/articles/mocksArentStubs.html?utm_source=chatgpt.com)

## Fake

|Idea clave|“Funciona, pero es más simple”.|
|---|---|
|**Qué hace**|Implementa la funcionalidad real, pero con atajos aptos para pruebas. Suele ser rápido e in-memory.|
|**Cuándo usarlo**|Cuando quieres probar más que puro _happy path_ y el real es costoso o imposible (p. ej. un e-mail server falso).|
|**Ejemplo**|Una base de datos embebida H2 o SQLite que sustituye a PostgreSQL solo durante tests; o un servicio de pagos que solo “marca” transacciones como aprobadas.|

Los fakes permiten pruebas más cercanas a la realidad sin las penalizaciones de rendimiento o dependencias externas. [stackoverflow.com](https://stackoverflow.com/questions/346372/whats-the-difference-between-faking-mocking-and-stubbing?utm_source=chatgpt.com)

## Mock

| Idea clave        | “Estoy aquí para vigilar”.                                                                                                                                                                        |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Qué hace**      | Registra las interacciones del SUT y permite **verificarlas**. Antes del test declaras expectativas (cuántas veces, con qué argumentos). Al final, el propio mock decide si el test pasa o falla. |
| **Cuándo usarlo** | Cuando la lógica que pruebas es “orientada a mensajes” y lo importante es que cierta colaboración suceda (p. ej. que se envíe un correo o se dispare un evento).                                  |

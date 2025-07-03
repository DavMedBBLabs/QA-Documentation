# ⚙️ Evaluación de Herramientas de Automatización

## 1.1 Compatibilidad de Lenguajes y Plataformas

- **Selenium**
    
    - Bindings en Java, C#, Python, JavaScript y Ruby.
        
    - Integración con casi todos los navegadores del mercado.
        
- **Cypress**
    
    - Orientado a JavaScript/TypeScript.
        
    - Corre _inside-the-browser_, con soporte nativo para Chrome y Firefox.
        
- **Playwright**
    
    - Permite escribir tests en JavaScript, Python, Java y .NET.
        
    - Controla de forma nativa tres motores de navegador: Chromium, Firefox y WebKit.
        

---

## 1.2 Modelo de Ejecución y Arquitectura Interna

- **Selenium**
    
    - Modelo cliente-servidor: el script envía comandos a un WebDriver externo.
        
- **Cypress**
    
    - Corre directamente dentro del navegador, interceptando comandos y peticiones en tiempo real.
        
- **Playwright**
    
    - Usa un driver unificado que lanza instancias de navegador directamente, sin servidor intermedio.
        

---

## 1.3 Facilidad de Depuración y Observabilidad

- **Selenium**
    
    - Depuración basada en logs de WebDriver y capturas manuales de pantalla.
        
- **Cypress**
    
    - Snapshots automáticos del DOM.
        
    - Interfaz de _time-travel_ para inspeccionar el estado en cada paso.
        
- **Playwright**
    
    - Trazas, grabación de video y capturas de pantalla integradas de forma transparente.
        

---

## 1.4 Paralelización y Despliegue en la Nube

- **Selenium**
    
    - Ecosistemas maduros de grid y soporte en la nube (Selenium Grid, Selenoid, proveedores SaaS).
        
- **Cypress**
    
    - Dashboard Service para paralelizar pruebas (limitaciones según navegador).
        
- **Playwright**
    
    - Mecanismo propio de _workers_ para paralelización.
        
    - Integración sencilla con soluciones en la nube.
        

---

# 🏗️ Arquitectura de Framework de Automatización

## 2.1 Patrón por Capas (Layered)

**Descripción general:**  
El framework se separa en niveles con responsabilidades claras:

- Tests de alto nivel.
    
- Casos concretos.
    
- Abstracción de UI (_Page Objects_).
    
- Utilidades comunes y hooks de inicialización.
    

**Ventajas:**

- Separación de responsabilidades clara.
    
- Cambios en la UI afectan solo a los _Page Objects_.
    

**Consideraciones:**

- Controlar proliferación de clases.
    
- Definir cómo fluye la información entre capas (inyección de dependencias, instanciación controlada).
    

---

## 2.2 Estructura Modular

**Descripción general:**  
Organización por funcionalidades (e.g., autenticación, compras), agrupando tests, _Page Objects_ y datos de prueba por módulo.

**Ventajas:**

- Equipos trabajan aisladamente sin solaparse.
    
- Fácil localización de artefactos por módulo.
    

**Consideraciones:**

- Extraer utilidades/configuración compartida a nivel global.
    
- Mantener coherencia en estructura de datos (JSON, CSV, etc.).
    

---

# 🔁 Integración Continua y Pipeline de Pruebas

## 3.1 Jenkins

**Concepto:**  
Servidor maestro y agentes para ejecución distribuida.

**Jenkinsfile:**  
Define etapas como:

- `checkout`
    
- Instalación de dependencias
    
- Ejecución de tests unitarios
    
- Ejecución de tests E2E
    
- Generación de reportes
    

**Acciones post-build:**

- Recolección de resultados, capturas, notificaciones (correo, Slack).
    

**Plugins clave:**

- Integración con GitHub / GitLab
    
- Reportes (JUnit, Allure)
    
- Visualización (Blue Ocean)
    

---

## 3.2 GitLab CI/CD

**Pipelines como YAML:**  
Definición de fases (`build`, `test`, `deploy`), variables y artefactos.

**Runners:**

- _Shared runners_ para tareas generales.
    
- _Specific runners_ para pruebas que requieren navegadores o Docker.
    

**Reportes y artefactos:**

- Recolección automática de JUnit, cobertura, logs, vídeos y capturas.
    

**Entornos dinámicos:**  
_Review Apps_ para despliegue automático por rama.

---

# 🧾 Resumen

- **Selección de herramienta:**  
    Evalúa compatibilidad, modelo de ejecución, depuración y paralelización.
    
- **Diseño de framework:**  
    Elige entre enfoque por capas (máxima separación) o modular (agilidad para equipos grandes). Mantén reutilización y configuración externa.
    
- **CI/CD:**  
    Integra pruebas en pipelines automatizados con validación por rama, recopilación estructurada de resultados y despliegues para validación manual.

---

↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
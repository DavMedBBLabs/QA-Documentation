# 🧨 Severidad de un Bug en QA

La **severidad** (o _severity_) de un bug es una forma de medir el **impacto técnico o funcional** que ese defecto tiene sobre el sistema. No debe confundirse con la **prioridad** (_priority_), que indica en qué orden se resolverá el bug; la severidad, en cambio, responde a:

> **¿Qué tan grave es este error para el funcionamiento o la estabilidad del producto?**

A continuación se detallan los niveles más comunes y cómo categorizarlos:

---

## 1. 🟥 Severidad 1 – Critical (Crítico / Blocker)

- **¿Qué significa?**  
    Este bug deja el sistema totalmente inservible o provoca una pérdida de datos grave. No hay forma de usar la funcionalidad principal ni existe solución temporal (_workaround_).
    
- **Características típicas:**
    
    - La aplicación no arranca o se cae (crash) al iniciar.
        
    - Pérdida de datos irreversibles.
        
    - Brecha de seguridad que expone datos sensibles.
        
    - Funcionalidad esencial completamente bloqueada.
        
- **Ejemplo:**
    
    - Al intentar iniciar sesión, el sistema lanza un error 500 y no permite el acceso a ningún usuario.
        
    - Un formulario de alta de clientes borra datos y no hay forma de recuperarlos.
        

---

## 2. 🟧 Severidad 2 – High (Alta)

- **¿Qué significa?**  
    El bug afecta una funcionalidad importante, pero existe al menos un _workaround_ parcial o una forma de mitigar el problema (aunque incómoda). La aplicación sigue funcionando en otras áreas.
    
- **Características típicas:**
    
    - Una opción clave falla, pero existe una alternativa manual.
        
    - Errores que afectan muchos usuarios y retrasan procesos.
        
    - Componente importante con comportamiento incorrecto.
        
- **Ejemplo:**
    
    - El módulo de facturación muestra cálculos erróneos de IVA, pero el usuario puede editarlos manualmente.
        
    - La búsqueda no encuentra registros recientes, pero pueden consultarse por SQL.
        

---

## 3. 🟨 Severidad 3 – Medium (Media)

- **¿Qué significa?**  
    El bug impacta funcionalidades secundarias o poco frecuentes. No bloquea el flujo principal y existe un _workaround_ razonable.
    
- **Características típicas:**
    
    - Fallos en campos opcionales o filtros avanzados.
        
    - Mensajes de validación que no se muestran correctamente.
        
    - Problemas de rendimiento moderado en pantallas no críticas.
        
- **Ejemplo:**
    
    - El avatar del usuario no se muestra en tiempo real, pero sí al recargar.
        
    - Exportar a Excel genera archivo vacío si no hay datos, pero funciona con registros.
        

---

## 4. 🟩 Severidad 4 – Low (Baja)

- **¿Qué significa?**  
    Errores cosméticos o de interfaz que no afectan el funcionamiento. Detalles de apariencia, redacción o validación secundaria.
    
- **Características típicas:**
    
    - Estilo o alineación incorrecta.
        
    - Errores ortográficos.
        
    - Datos mal formateados en entornos no productivos.
        
    - Alertas visuales breves que no afectan el flujo.
        
- **Ejemplo:**
    
    - El botón "Guardar" no tiene el color correcto, pero funciona.
        
    - Texto de ayuda con error ortográfico: “Precionar” en vez de “Presionar”.
        

---

## 🧭 ¿Cómo decidir la severidad correcta?

### 1. Evalúa el alcance del impacto

- ¿Bloquea la funcionalidad principal? → **Critical** o **High**
    
- ¿Afecta algo no esencial? → **Medium** o **Low**
    

### 2. Pregunta por el _workaround_

- ¿No se puede completar la tarea de ninguna forma? → **Critical**
    
- ¿El _workaround_ es complicado? → **High**
    
- ¿Es sencillo o rara vez se usa? → **Medium**
    
- ¿No hay fallo funcional? → **Low**
    

### 3. Considera el tipo de usuario afectado

- ¿Impacta a usuarios finales en producción? → sube severidad
    
- ¿Solo afecta a testers o ambientes internos? → baja severidad
    

### 4. Valora la frecuencia de aparición

- Si ocurre **siempre** en un flujo crítico → **Critical**
    
- Si ocurre en **1%** pero afecta flujo clave → **High**
    
- Si ocurre en **1%** de algo secundario → **Medium**
    

---

## 📋 Resumen de Categorías

|Severidad|Impacto principal|Workaround|Ejemplos|
|---|---|---|---|
|**Critical**|Producto o flujo esencial inservible; pérdida de datos.|Ninguno o muy parcial|Login imposible, caída general, datos eliminados sin recuperación.|
|**High**|Funcionalidad importante rota; flujo crítico con “parche”.|Existe pero engorroso|Reporte falla, cálculo erróneo con corrección manual.|
|**Medium**|Funcionalidad secundaria rota; no impide el core.|Sí, sencillo|Filtros que no funcionan, advertencias ausentes.|
|**Low**|Bug cosmético o de usabilidad; sin impacto en negocio.|N/A|Errores de estilo, textos mal escritos.|

---

## 💡 Preguntas clave al clasificar severidad

1. ¿Qué parte del sistema se ve afectada?
    
2. ¿Ese módulo es crítico para el usuario?
    
3. ¿Existe alguna forma de continuar (workaround)?
    
4. ¿Cuántos usuarios se ven afectados y con qué frecuencia?

---

↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
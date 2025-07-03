Estoy refinando una historia de usuario como parte del proceso de análisis funcional.  
El objetivo es convertirla en una versión **lista para desarrollo y pruebas de interfaz**  
siguiendo la ontología formal y los objetivos de refinamiento descritos más abajo.

### Ontología del Criterio de Aceptación

_(todos los elementos deben aparecer **implícitamente** dentro de cada criterio Gherkin)_

|Elemento|Pregunta guía|Ejemplo de valores **(solo front-end)**|
|---|---|---|
|**ValidatorRole**|¿Quién verifica?|Usuario final, QA UI, PO|
|**Precondition**|¿Qué debe cumplirse antes?|Página cargada, sesión iniciada, datos mockeados en memoria|
|**TriggerEvent**|¿Qué acción lo dispara?|Clic, pulsar tecla Enter, scroll, gesto táctil|
|**ExpectedOutcome**|Resultado observable|Redirección de página, modal visible, banner de alerta, cambio de estilo|
|**DomainVocabulary**|Términos de negocio|“Disponibilidad”, “Proceso activo”|
|**VerificationMode**|¿Cómo se valida?|Inspección visual, test automatizado de UI (e2e), captura de pantalla|
|**GranularityLevel**|Macro / Intermedio / Micro|Declarar en la primera línea|
|**Satisfiability**|¿Binario?|Cumplido ✅ / No cumplido ❌|
### Cobertura obligatoria (5 temas = 3 niveles de granularidad)
| Tema (front-end)                   | GranularityLevel | Alcance mínimo                                                  |
| ---------------------------------- | ---------------- | --------------------------------------------------------------- |
| **User intent**                    | **Macro**        | Valor extremo-a-extremo, actor, beneficio                       |
| **Full functional flow**           | **Intermedio**   | Pasos UI principales, reglas clave, variantes felices           |
| **Interaction of UI components**   | **Micro**        | Estados de botones, modales, tooltips, cambios de DOM           |
| **Data and rule validation**       | **Micro**        | Formatos de campos, máscaras, longitud, unicidad **en cliente** |
| **Edge cases and expected errors** | **Micro**        | Mensajes de error, banner offline, animaciones fallidas         |
### Historia de usuario a refinar
Título:
Descripción:
Criterios de Aceptación actuales:

### **Objetivos del refinamiento**
- **Etiquetar la HU**
    
    - Primera línea: `GranularityLevel: Macro | Intermedio | Micro`.
        
- **Agrupar por los cinco temas**
    
    - User intent (Macro)
        
    - Full functional flow (Intermedio)
        
    - Interaction of UI components (Micro)
        
    - Data and rule validation (Micro)
        
    - Edge cases and expected errors (Micro)
        
- **Redactar en Gherkin enriquecido y evaluable**
    
    - `ESCENARIO, DADO, CUANDO, ENTONCES`; usar `Y / O / PERO` solo cuando aclare.
        
    - Cada **ENTONCES** debe ser comprobable visualmente (_✅ / ❌_).
        
- **Mensajes literales y datos explícitos**
    
    - Escribe la cadena exacta que verá el usuario (“Disponible”, “Proceso en curso”…).
        
    - Detalla todos los campos, formatos y longitudes para evitar ambigüedad.
        
- **Cobertura mínima pero crítica**
    
    - Camino feliz + variante clave + fallos críticos; sin casos exóticos.
        
- **Refactorizar al dominio concreto** _(implícito)_
    
    - Ajustar actores, textos, estilos, nomenclatura según la lógica del proyecto.

### Plantilla de criterios Gherkin (referencia)

	GranularityLevel: Intermedio

	User intent (Macro)
	ESCENARIO: Visualizar disponibilidad de desarrollador
	  DADO que Luisa desea saber si un desarrollador está disponible
	  CUANDO abre la página de perfil del desarrollador
	  ENTONCES observa claramente el estado “Disponible”, “En proceso”, “No disponible” o “Inactivo”
	
	Full functional flow (Intermedio)
	ESCENARIO: Cambio automático de estado visual
	  DADO que la tarjeta de perfil se muestra en el tablero
	  Y el estado actual del desarrollador es “En proceso (2/3)”
	  CUANDO el usuario marca manualmente un proceso como “Suspendido”
	  ENTONCES la tarjeta actualiza el indicador a “En proceso (1/3)”
	  Y el círculo de estado cambia de naranja a amarillo
	
	Interaction of UI components (Micro)
	ESCENARIO: Tooltip informativo sobre el indicador
	  DADO que el usuario mantiene el puntero sobre el círculo de estado
	  CUANDO el círculo representa “No disponible”
	  ENTONCES se despliega un tooltip con el texto “Participando en 3 procesos”
	
	Data and rule validation (Micro)
	ESCENARIO: Validación de formato porcentual en etiqueta
	  DADO que se muestra la etiqueta de progreso “Progreso: 120 %”
	  CUANDO se detecta un valor mayor a 100
	  ENTONCES la interfaz reemplaza la etiqueta por “Progreso: 100 %”
	  Y aplica la clase CSS de alerta “text-red-600”
	
	Edge cases and expected errors (Micro)
	ESCENARIO: Desconexión al actualizar estado
	  DADO que el usuario intenta actualizar el estado con el botón “Refrescar”
	  Y el navegador ha perdido la conexión
	  CUANDO pulsa “Refrescar”
	  ENTONCES aparece un banner rojo con el mensaje  
	          “Sin conexión. Intenta nuevamente cuando tengas internet”
	  Y el botón muestra un icono de recarga en gris (deshabilitado)



Utiliza esta plantilla y los objetivos anteriores para **refinar cualquier HU**. Sustituye únicamente los elementos de dominio (actores, rutas, campos, mensajes y reglas) sin modificar la estructura general.
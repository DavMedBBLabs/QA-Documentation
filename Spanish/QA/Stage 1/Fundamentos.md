
- [[Fundamentos#1. ¿Qué es la calidad de software?|¿Qué es la calidad de software?]]
	- [[Fundamentos#1.1 Conformidad vs adecuación al uso|Conformidad vs adecuación al uso]]
	- [[Fundamentos#1.2 Costes de la falta de calidad|Costes de la falta de calidad]]
- [[Fundamentos#2. Principios del Testing|Principios del Testing]]
	- [[Fundamentos#2.1 Exhaustividad imposible|Exhaustividad imposible]]
	- [[Fundamentos#2.2 Detección de defectos|Detección de defectos]]
	- [[Fundamentos#2.3 Paradoja de los pesticidas|Paradoja de los pesticidas]]
	- [[Fundamentos#2.4 Principio del _shift-left_|Principio del _shift-left_]]
	- [[Fundamentos#2.5 Principio de la detección temprana|Principio de la detección temprana]]
	- [[Fundamentos#2.6 Principio de Contexto|Principio de Contexto]]
	- [[Fundamentos#2.7 Principio del Agrupamiento de Defectos (Ley de Pareto)|Principio del Agrupamiento de Defectos (Ley de Pareto)]]
	- [[Fundamentos#2.8 Principio de Paridad de Entorno|Principio de Paridad de Entorno]]
- [[Fundamentos#Conclusión|Conclusión]]
	
### 1. ¿Qué es la calidad de software?

La calidad de software se define, de forma general, como el grado en que un producto de software cumple con los requisitos y expectativas tanto explícitas como implícitas de sus usuarios y de sus interesados (stakeholders). Desde la perspectiva de estándares como la [[ISO-IEC 25010|ISO/IEC 25010]], la calidad engloba características como fiabilidad, usabilidad, eficiencia, mantenibilidad y seguridad.

- ***Calidad interna***: se refiere a atributos del producto que son visibles para el equipo de desarrollo (por ejemplo, la modularidad o la legibilidad del código).
- ***Calidad externa***: se refiere a cómo perciben los usuarios el software en función de su comportamiento y funcionalidades (por ejemplo, facilidad de uso y ausencia de errores).
##### 1.1 Conformidad vs adecuación al uso

- **Conformidad (Fitness for purpose)**  
    Indica hasta qué punto el software cumple los estándares, especificaciones formales y normativas técnicas definidas. Se mide comparando el comportamiento del producto con los requisitos documentados.
    
    - _Ejemplo:_ Un algoritmo de cálculo de impuestos que sigue al pie de la letra la fórmula legal.
        
- **Adecuación al Uso (Fitness for use)**  
    Valora si el software realmente satisface las necesidades y expectativas del usuario en su entorno real de trabajo. Incluye aspectos de usabilidad, adaptabilidad y contexto de uso.
    
    - _Ejemplo:_ Ese mismo módulo de impuestos podría ser demasiado lento o complejo de configurar, impidiendo su adopción práctica por el departamento contable.

Estas dos dimensiones vienen de la norma ISO 9126 (predecesora de la [[ISO-IEC 25010|ISO 25010]]) y ayudan a entender que un producto puede “cumplir” unos requisitos formales y, sin embargo, resultar inadecuado para el usuario final.

| Dimensión                               | Descripción                                                                                        | Ejemplo                                                                           |
| --------------------------------------- | -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **Conformidad (fitness for purpose)**   | Grado en que el software cumple especificaciones y estándares técnicos definidos.                  | Un módulo de cálculo de nómina que implementa correctamente la fórmula definida.  |
| **Adecuación al uso (fitness for use)** | Grado en que el software satisface las necesidades reales del usuario y es efectivo en su entorno. | Ese mismo módulo es lento, complejo de configurar y requiere formación intensiva. |
**Clave**: Ambos aspectos son necesarios. Un sistema conforma técnicamente, pero si no es usable o no encaja en el flujo de trabajo, no será percibido como “de calidad”.

##### 1.2 Costes de la falta de calidad
Cuando un producto no alcanza niveles mínimos de calidad, las consecuencias pueden agruparse en tres grandes categorías:
- **Costes de prevención**: inversión en actividades que evitan defectos (formación, herramientas de análisis estático).

-  **Costes de evaluación**: esfuerzo en detectar defectos antes de la entrega ([[Niveles de Testing#2. Testing de Integración (Integration Testing)|tests de integración]], [[Niveles de Testing#4. Testing de Aceptación (Acceptance Testing)|pruebas de aceptación]]).

- **Costes de fallos**: los más elevados, incluyen correcciones en producción, soporte a usuarios, pérdida de reputación y, en casos críticos, sanciones legales.

**Regla de los 1-10-100**: defectos encontrados en análisis de requisitos cuestan 1 × unidad, si se detectan en pruebas de integración cuestan 10 × , en operación 100 ×,
	Ejemplos:	
	- Un error de cálculo en un sistema bancario puede derivar en reclamaciones y multas (coste de fallo).
	- Una inversión temprana en un ambiente de pruebas automatizadas reduce la cantidad de errores en producción (coste de prevención).


↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
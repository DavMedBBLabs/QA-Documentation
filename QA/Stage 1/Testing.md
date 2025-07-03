### 2. Principios del Testing

##### 2.1 Exhaustividad imposible

- No es factible probar todas las combinaciones posibles de entradas, estados internos y caminos de ejecución.
- **Implicación**: hay que priorizar: [análisis de riesgos](app://obsidian.md/Conceptos%20clave#**An%C3%A1lisis%20de%20Riesgos**), [partición de equivalencia](app://obsidian.md/Conceptos%20clave#**Partici%C3%B3n%20de%20Equivalencia**) y [criterios de cobertura](app://obsidian.md/Conceptos%20clave#**Criterios%20de%20Cobertura**).

##### 2.2 Detección de defectos

El testing muestra la presencia de defectos, _NO su ausencia_.

- Un conjunto de pruebas exitosas mejora la confianza, pero nunca garantiza que no existan fallos residuales.

##### 2.3 Paradoja de los pesticidas

Si ejecutamos repetidamente las mismas pruebas, éstas dejan de encontrar nuevos errores.

- **Solución**: revisar y diseñar continuamente nuevos casos de prueba para explorar zonas no cubiertas.

##### 2.4 Principio del _shift-left_

Mover actividades de calidad y testing hacia fases más tempranas del ciclo de vida (análisis, diseño).

- Beneficio: detectar defectos cuando su coste de corrección es menor.  
    [(Ver más)](app://obsidian.md/Buenas%20Pr%C3%A1cticas%20y%20Cultura#1.1%20Shift-Left%20Testing)

##### 2.5 Principio de la detección temprana

Cuanto antes se encuentre un defecto, menor será su impacto y coste de arreglo.

- Impulsa prácticas como [code review](app://obsidian.md/Conceptos%20clave#**Code%20Review%20\(Revisi%C3%B3n%20de%20C%C3%B3digo\)**), [pair programming](app://obsidian.md/Conceptos%20clave#**Pair%20Programming%20\(Programaci%C3%B3n%20en%20Parejas\)**) o [análisis estático de código](app://obsidian.md/Conceptos%20clave#**An%C3%A1lisis%20Est%C3%A1tico%20de%20C%C3%B3digo**)

##### 2.6 Principio de Contexto

Las pruebas deben adaptarse al dominio de la aplicación: no es lo mismo un sistema bancario que una app de ocio. Riesgos, regulaciones y expectativas varían.

##### 2.7 Principio del Agrupamiento de Defectos (Ley de Pareto)

Aproximadamente el 80 % de los defectos suelen concentrarse en el 20 % de los módulos. Identificar áreas críticas permite enfocar esfuerzos de prueba.

##### 2.8 Principio de Paridad de Entorno

Las pruebas deben ejecutarse en entornos lo más similares posible al de producción (datos, configuraciones y dependencias) para asegurar resultados representativos.

### Conclusión

Garantizar la calidad de un producto de software no es tarea exclusiva del testing: es un compromiso transversal que abarca desde la definición de requisitos hasta la operación en producción. Comprender los conceptos de conformidad y adecuación al uso, valorar los costes asociados a la falta de calidad y aplicar principios sólidos de testing (reconociendo sus límites) nos permite diseñar estrategias equilibradas y efectivas para la detección y prevención temprana de defectos.

↩️ Volver al mapa principal: [[🗺️Roadmap QA]]
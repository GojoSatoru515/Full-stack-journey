# CLAUDE.md

Instrucciones para Claude Code en este repositorio. Se leen al inicio de cada sesión.
Completa lo que está entre corchetes y borra lo que no aplique.

## Contexto del proyecto
- **Qué es:** [describe en 1–2 líneas qué hace el proyecto]
- **Lenguaje / stack principal:** [p. ej. Python 3.12 + Django, Node 20 + React]
- **Gestor de paquetes / build:** [p. ej. pip + requirements.txt, npm, poetry]
- **Cómo correr los tests:** [p. ej. `pytest`, `npm test`]
- **Cómo correr linter / formateador:** [p. ej. `ruff check`, `eslint`, `prettier`]

## Objetivo principal con Claude Code
Uso esta herramienta sobre todo para **revisión de código y para proponer mejoras**.
Prioriza analizar y explicar antes que reescribir.

## Cómo quiero que trabajes

### Al revisar código
Revisa en este orden de prioridad y sé concreto (archivo + línea):
1. **Corrección y bugs:** lógica incorrecta, casos borde sin manejar, condiciones de carrera, manejo de errores faltante.
2. **Seguridad:** entradas no validadas, inyección (SQL / comando / XSS), secretos en el código, dependencias vulnerables, permisos.
3. **Rendimiento:** consultas N+1, trabajo innecesario en bucles, uso de memoria.
4. **Mantenibilidad:** nombres, duplicación, funciones demasiado largas, complejidad.
5. **Estilo:** solo después de lo anterior, y según las convenciones de abajo.

Para cada hallazgo, explica **por qué** es un problema y **cuál es el impacto**, no solo qué cambiar.

### Al proponer o aplicar cambios
- Explica el plan antes de cambios grandes o que toquen varios archivos, y espera mi visto bueno.
- Haz cambios pequeños y enfocados; no hagas refactors masivos sin pedírmelo.
- No cambies comportamiento público (APIs, firmas, formatos de datos) sin avisar.
- Si añades una dependencia, dímelo y explica por qué.
- Prefiere seguir los patrones que ya existen en el código antes que introducir estilos nuevos.
- Si algo no está claro, pregunta en vez de suponer.

### Qué NO hacer sin permiso explícito
- No borres archivos ni corras comandos destructivos.
- No hagas `git push`, no toques ramas remotas ni abras PRs a menos que yo lo pida.
- No modifiques configuración sensible (CI/CD, secretos, infraestructura).
- No ejecutes comandos que hagan peticiones de red salvo que sea necesario y me lo indiques.

## Convenciones de código
- **Estilo:** [p. ej. PEP 8, Airbnb JS Style Guide]
- **Nombres:** [p. ej. snake_case para funciones, PascalCase para clases]
- **Tests:** todo cambio de lógica debe traer o actualizar sus tests.
- **Comentarios / documentación:** [tu preferencia]
- **Manejo de errores:** [tu patrón preferido]

## Notas del proyecto
- [Cosas específicas que debas saber: módulos delicados, deuda técnica conocida, "no toques X", etc.]

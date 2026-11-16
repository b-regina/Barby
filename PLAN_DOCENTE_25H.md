# Plan docente de 25 horas · Laboratorio de IaC e IA

**Uso docente.** El alumnado recibe una sola plantilla, crea una copia personal una sola vez y avanza del ejercicio 1 al 8 en esa misma copia. El ejercicio 9 es una ampliación para quien avance más rápido. La rama `main` de la plantilla contiene el punto de partida del ejercicio 1 y las nueve guías; las ramas `ejercicio-N-solucion` son demostraciones resueltas para la docente. Al crear la copia, **no** marcar «Include all branches».

## Antes de la primera clase: comprobación y mensaje inicial

1. Proyectar la [plantilla](https://github.com/b-regina/iac-ia-laboratorio-demo) y abrir `EJERCICIO_1.md` desde la raíz. Mostrar que `EJERCICIO_2.md` a `EJERCICIO_9.md` son **instrucciones**, no código ya resuelto.
2. Cada participante pulsa **Use this template → Create a new repository**, elige su propia cuenta y desmarca **Include all branches**. Si el centro exige repositorios privados, verificar antes la disponibilidad de Actions y sus límites; la ruta gratuita verificada usa repositorios públicos con datos ficticios.
3. En la copia, comprobar el nombre de usuario en la URL y abrir **Actions → Validacion IaC → comprobar**. El commit inicial puede activar el workflow sin otro paso; si la política de la cuenta lo bloquea, registrar la incidencia y usar la demostración docente. OpenTofu se instala en un ejecutor temporal de GitHub, no en el equipo.
4. Abrir la copia en `github.dev` o `vscode.dev` y la IA en otra pestaña. Si VS Code local está autorizado, se puede editar y publicar **la misma copia** desde local; GitHub Actions sigue siendo la evidencia común. La ruta web no requiere instalaciones.

**Evidencia real en cuenta docente:** [copia nueva con nueve guías](https://github.com/b-regina/iac-ia-alumno-validacion-final) y [ejecución verde de su commit inicial](https://github.com/b-regina/iac-ia-alumno-validacion-final/actions/runs/43663182526). Es una prueba dentro de `b-regina`; faltan las pruebas desde seis cuentas distintas y desde equipos corporativos.

## Un ciclo didáctico que se repite

En cada ejercicio, hacer que el participante (1) prediga el resultado, (2) explique un fragmento antes de pedir ayuda a la IA, (3) edite y publique un cambio pequeño, (4) abra la ejecución de **su commit**, (5) interprete el plan o el error y (6) entregue enlaces junto a una explicación de dos o tres frases. La IA puede proponer y revisar; la comprobación se hace en archivos y registros. Para un grupo rápido, profundizar en decisiones y diagnóstico; no dar por aprendido un ejercicio porque la IA lo escribió en veinte minutos.

## Secuencia de cinco jornadas

Los minutos son una **planificación docente**, no una duración medida con los seis participantes. Cada fila suma 300 minutos. Las pausas, si se contabilizan fuera de las cinco horas lectivas, se añaden al horario.

| Día | Bloques lectivos (minutos) | Resultado observable |
| --- | --- | --- |
| 1 · Primera ejecución | Contexto IaC, declarativo y DevOps 45; herramientas y comparación conceptual OpenTofu/Terraform/Bicep 35; copia y lectura de la ejecución inicial 50; ejercicio 1 con predicción, edición, commit y plan 90; error controlado, puesta en común y dudas 80. **Total 300.** | Cada alumno identifica su copia, abre la ejecución inicial y otra tras cambiar `entorno`, localiza `pruebas` y explica que no existe un servidor desplegado. |
| 2 · Parámetros y revisión | Recordatorio y valor de Git 35; ejercicio 2A 55; ejercicio 2B 65; ejercicio 3: reglas, rama, error y propuesta 115; revisión cruzada y explicación de cambios 30. **Total 300.** | Dos planes con valores diferentes; rama y revisión con evidencia de error y corrección. |
| 3 · IA, automatización y reutilización | Revisión crítica de una respuesta de IA y límites de los datos compartidos 30; ejercicio 4 120; explicación de módulo, entradas, salidas y estado 30; ejercicio 5 120. **Total 300.** | Workflow más legible, evidencia de diagnóstico y dos fichas planificadas con un módulo local. |
| 4 · Seguridad y gobierno | Caso ficticio de secretos, permisos, coste y deriva de configuración 40; ejercicio 6 140; ejercicio 7 110; discusión sobre `for_each`, direcciones y revisión del plan 10. **Total 300.** | Política que rechaza un plan indebido y catálogo reutilizable; fallo y corrección trazables. |
| 5 · Integración final | Revisión de la cadena completa y reparto de responsabilidades 30; ejercicio 8 120; demostraciones entre pares y preguntas de defensa 70; ejercicio 9 o ampliación equivalente según ritmo 60; cierre y evaluación 20. **Total 300.** | Entrega individual del ejercicio 8, plan correcto, rechazo controlado, corrección y explicación de las decisiones. |

En el día 5, el ejercicio 9 tiene guía de 90–120 minutos: los 60 minutos del bloque son **inicio o selección de partes** si el grupo llega con margen. Para completarlo íntegro durante clase, reducir presentaciones y extender el bloque; no convertirlo en requisito para aprobar el taller final. Si alguien aún trabaja en el 8, usar ese bloque para terminarlo con acompañamiento.

## Relación con los ocho módulos del temario original

| Módulo y horas originales | Prácticas y explicación que lo cubren | Evidencia de comprensión |
| --- | --- | --- |
| 1 · IaC, DevOps e introducción (3 h) | Día 1: manual frente a declarativo, plan frente a aplicación, ciclo Git–Actions, comparación conceptual OpenTofu/Terraform/Bicep; retorno al concepto de deriva en día 4. | Distingue plan, estado, despliegue real y cambio fuera de código. |
| 2 · Fundamentos prácticos (4 h) | Ejercicio 1 y ejercicio 2: archivos `.tf`, variables, salidas, `terraform_data`, inicialización, formato, validación, plan y escenarios. | Predice el resultado de cada escenario y lee su salida. |
| 3 · Git y gestión del cambio (3 h) | Commits de ejercicios 1–2, rama y revisión del ejercicio 3, evidencia y revisión cruzada. | Diferencia guardar, commit, push y propuesta de cambio. |
| 4 · IA para IaC (4 h) | Segunda pestaña en todos los ejercicios, con tiempos específicos de revisión crítica en días 1, 3 y 5; contraste de prompts, explicaciones y errores con el plan. | Corrige una sugerencia convincente pero incorrecta de IA. |
| 5 · Estandarización, seguridad y gobierno (4 h) | Reglas del 3; módulo reutilizable del 5; política del 6; responsables y etiquetas del 8; caso de secretos, permisos y costes del día 4. | Explica qué controla el laboratorio y qué necesitaría un entorno real. |
| 6 · Pipelines y automatización (3 h) | Workflows de ejercicios 1–2, mejora y diagnóstico del 4, política automatizada del 6 y comprobaciones del 8. | Localiza la etapa fallida y enlaza la ejecución del commit correcto. |
| 7 · Arquitectura y reutilización (2 h) | Módulo del 5, catálogo con `for_each` del 7; discusión de arquitectura moderna, observabilidad y costes sin desplegar cloud. | Justifica la reutilización y reconoce implicaciones de direcciones y estado. |
| 8 · Taller final (2 h) | Ejercicio 8 con revisión, plan, rechazo y corrección, seguido de breve defensa. | Entrega y demuestra el recorrido completo. |

Las horas por módulo son las del temario; varios temas se retoman en días distintos. Las guías técnicas solas suman aproximadamente **12 h 45 min a 16 h** para los ejercicios 1–8 según sus estimaciones, y **14 h 15 min a 18 h** con el 9 completo. El resto de las 25 horas corresponde a introducciones, demostraciones, revisión, diagnóstico, preguntas y evaluación. Estos rangos no sustituyen una prueba cronometrada con estudiantes.

## Casos cortos para grupos que avanzan rápido

- **Deriva sin despliegue real (20–30 min):** comparar un cambio manual hipotético con el código versionado. Pedir qué vería un plan si existiera estado persistente y por qué este laboratorio, sin `apply`, no demuestra detección de deriva real.
- **Seguridad y permisos (25–35 min):** dar a la IA un escenario completamente ficticio con una contraseña inventada, identificar por qué tampoco conviene versionar secretos de ejemplo como patrón y proponer permisos mínimos y revisión humana. No introducir secretos reales.
- **Observabilidad y costes (20–30 min):** diseñar en papel qué métricas, registros y alertas necesitaría un servicio real; localizar por qué `terraform_data` y un plan sin aplicación no pueden medir coste ni disponibilidad.
- **Comparación de herramientas (20–30 min):** comparar una misma intención declarativa en OpenTofu, Terraform y Bicep en una tabla conceptual; distinguir lenguaje, proveedor, estado y ejecución. No instalar Bicep ni desplegar Azure.

Cada caso termina con una pregunta explicada por el alumno, no con una salida generada por IA sin revisión. Estos bloques son reserva de profundidad para ajustar el ritmo, no cuatro tareas obligatorias adicionales.

## Control docente al cerrar cada día

Registrar por persona: URL de la copia, último commit, URL de Actions, resultado verde/rojo, explicación oral breve y bloqueo observado. Comprobar que los cambios se hacen en la copia propia; mostrar la rama docente resuelta solo después del intento del grupo. El día 1, abrir primero `EJERCICIO_1.md` y proyectar exactamente los botones de copia, editor, Source Control y Actions. El día siguiente se continúa en la **misma** copia, sin nueva plantilla ni instalación.

## Límites que hay que expresar sin ambigüedad

En la cuenta docente se han verificado copias de plantilla, ejecución inicial, planes y pruebas de fallo/corrección en ramas docentes. No se ha verificado el acceso real de las seis cuentas corporativas, sus políticas de GitHub ni sus equipos; eso se observa al empezar la formación. GitHub Copilot integrado en VS Code Web no es requisito: IA en segunda pestaña. El laboratorio usa datos ficticios, ejecutores temporales y `tofu plan`; no hay `tofu apply`, credenciales ni despliegue comercial. La ruta local, si se autoriza, edita la misma copia y publica sus commits para obtener la misma validación en Actions.

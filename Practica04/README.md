# Preparación de una reunión para el lanzamiento de un nuevo servicio digital

Esta guía integra la práctica de preparación de reunión (18 min) con la demostración posterior de recapitulación de una reunión grabada (7 min), porque ambas pertenecen al mismo escenario y la demostración continúa el flujo de trabajo de la práctica.

## Metadatos

| Campo | Detalle |
|---|---|
| Duración | 25 min: 18 min de práctica + 7 min de demostración del instructor |
| Complejidad | Media |
| Nivel de Bloom | Aplicar / Analizar |
| Tipo de actividad | Práctica aplicada + demostración |
| Aplicaciones | Outlook, Teams, Microsoft 365 Copilot, Facilitator e Intelligent Recap cuando estén disponibles |
| Modalidad | Individual con demostración del instructor |
| Insumos previos | `recursos/correo_lanzamiento/`, `recursos/Conversacion_Teams_Lanzamiento.md`, `recursos/Guion_Reunion_Demo.md` |
| Resultado | Resumen de contexto, pendientes priorizados, objetivos, preguntas y agenda; recap demostrado sobre una reunión grabada |

## Distribución de tiempo

| Fase | Actividad | Tiempo |
|---|---|---:|
| 1 | Recuperar y validar el contexto del correo y Teams | 6 min |
| 2 | Priorizar pendientes y preparar preguntas | 5 min |
| 3 | Crear objetivos y agenda de la reunión | 5 min |
| 4 | Validar el borrador de reunión | 2 min |
| 5 | Demostración del instructor: recap, decisiones y actividades | 7 min |
|  | **TOTAL** | **25 min** |

## Descripción general

A partir de un hilo de correo y una conversación ficticia de Teams, recuperarás el estado de una iniciativa de lanzamiento digital, identificarás avances, pendientes, responsables, dependencias, riesgo y una decisión no resuelta. Después prepararás objetivos, preguntas y agenda. El instructor continuará el mismo caso mostrando cómo una reunión grabada y transcrita puede revisarse con Recap, Copilot e Intelligent Recap cuando estén disponibles.

## Objetivos de aprendizaje

- Recuperar contexto desde correo y conversación de Teams sin mezclar hechos con supuestos.
- Priorizar pendientes y formular preguntas orientadas a decisión.
- Preparar una agenda de reunión con Copilot en Outlook o Teams.
- Observar cómo una reunión finalizada puede convertirse en acuerdos, decisiones y actividades verificables.

## Escenario de la práctica

Diferentes áreas de CIBEST CAPITAL coordinan el lanzamiento ficticio de una nueva funcionalidad digital para que los clientes consulten información consolidada de sus inversiones. Próximamente se realizará una reunión para revisar el estado de preparación.

## Prerrequisitos

- Microsoft 365 Copilot habilitado para Outlook y Teams.
- Acceso a nuevo Outlook si se desea importar en bloque los archivos `.eml`.
- Para la demostración: una reunión de Teams previamente grabada y transcrita, preparada por el instructor con `recursos/Guion_Reunion_Demo.md`.

## Preparación del entorno

Realiza esta preparación antes de iniciar el cronómetro de la práctica:

1. En nuevo Outlook para Windows, importa los cuatro archivos `.eml` de `recursos/correo_lanzamiento/` a una carpeta de laboratorio. La opción está en **Configuración > Archivos > Importar** en las versiones que la incluyen. Si tu interfaz difiere, utiliza la opción equivalente disponible.
2. Para el contenido de Teams, usa una de estas rutas:
   - **Preferida:** el instructor ha publicado previamente los mensajes de `Conversacion_Teams_Lanzamiento.md` en un chat o canal de laboratorio.
   - **Autónoma:** guarda el archivo en OneDrive y úsalo como referencia en Copilot Chat/Teams. En este caso estás analizando una transcripción ficticia, no un chat en vivo.
3. No uses contenido de otras prácticas.
4. El instructor debe preparar con anticipación la grabación de demostración. Si no existe una reunión grabada y transcrita, la fase de Intelligent Recap no puede demostrarse de forma auténtica y no debe simularse como si existiera.

## Desarrollo de la práctica

### Fase 1 - Recuperar y validar el contexto
**Tiempo:** 6 min  
**Aplicación:** Outlook y Teams/Copilot Chat  
**Objetivo:** Construir un resumen común a partir de dos fuentes distintas.

1. En Outlook, abre el hilo importado y usa **Resumen por Copilot** cuando esté disponible.
2. Valida el resumen contra los mensajes y copia únicamente los hechos confirmados en una nota temporal.
3. Abre el chat/canal de laboratorio o adjunta `Conversacion_Teams_Lanzamiento.md` a Copilot.
4. Como las aplicaciones no comparten automáticamente el contexto, pega en el siguiente prompt el resumen validado del correo.

> **PROMPT 1 - CONTEXTO COMBINADO**
>
> Analiza la conversación de Teams disponible y combínala con este resumen validado del hilo de correo:
> `[pega aquí el resumen validado del correo]`
>
> Devuelve cinco secciones: avances confirmados, pendientes, responsables por área, dependencias/riesgos y decisiones todavía no resueltas.
>
> Diferencia claramente hechos, propuestas y decisiones. No inventes responsables, fechas ni estados. Si hay una contradicción entre fuentes, señálala en lugar de resolverla por tu cuenta.

**Criterio de finalización:** el resumen identifica al menos tres pendientes, una dependencia, un riesgo y una decisión todavía no resuelta.

### Fase 2 - Priorizar pendientes y preparar preguntas
**Tiempo:** 5 min  
**Aplicación:** Copilot  
**Objetivo:** Convertir el contexto en temas de reunión accionables.

> **PROMPT 2 - PENDIENTES Y PREGUNTAS**
>
> A partir del resumen validado, prioriza los pendientes que deben tratarse en una reunión de estado. Para cada uno muestra: tema, área responsable, evidencia disponible, dependencia, decisión o confirmación necesaria y una pregunta concreta para la reunión.
>
> No asumas que una propuesta ya fue aprobada. Conserva como `Pendiente de decisión` el tema del grupo piloto mientras las fuentes no indiquen lo contrario.

1. Revisa que cada pregunta ayude a cerrar un pendiente real.
2. Elimina preguntas que no estén relacionadas con el lanzamiento.

**Criterio de finalización:** existe una lista priorizada con preguntas para los asuntos que requieren decisión o confirmación.

### Fase 3 - Crear objetivos y agenda de la reunión
**Tiempo:** 5 min  
**Aplicación:** Outlook con Copilot  
**Objetivo:** Preparar una reunión breve y enfocada.

1. Crea una nueva reunión, pero no agregues asistentes reales y no la envíes.
2. Usa un título como `Seguimiento lanzamiento funcionalidad digital - ejercicio`.

> **PROMPT 3 - OBJETIVO Y AGENDA**
>
> Crea el objetivo y una agenda de 30 minutos para una reunión interna sobre el lanzamiento ficticio de la funcionalidad de consulta consolidada.
>
> Usa únicamente estos temas validados: estado técnico, UAT, preguntas frecuentes, preparación comercial, grupo piloto, dependencia de integración, riesgo de calendario y criterios de preparación operativa.
>
> Organiza la agenda con tiempos y cierra con decisiones, responsables y próximos pasos. No agregues temas que no estén en el contexto.

3. Inserta el resultado en el borrador de reunión.
4. Si Facilitator está disponible en la configuración de la reunión, identifica dónde se activa. No es necesario iniciar una reunión durante estos 18 minutos.

**Criterio de finalización:** el borrador incluye objetivo, agenda con tiempos y temas ligados a los pendientes del caso.

### Fase 4 - Validar el borrador
**Tiempo:** 2 min  
**Aplicación:** Outlook  
**Objetivo:** Confirmar que la reunión está lista sin enviar invitaciones.

1. Comprueba que no hay asistentes reales.
2. Revisa que la agenda no convierta el riesgo de calendario en un retraso confirmado.
3. Mantén la invitación como borrador.

**Criterio de finalización:** existe un borrador de reunión coherente y no enviado.

### Fase 5 - Demostración del instructor: recap, decisiones y actividades
**Tiempo:** 7 min  
**Aplicación:** Teams  
**Objetivo:** Mostrar cómo recuperar resultados de una reunión ya finalizada.

1. El instructor abre la reunión previamente grabada y entra en **Recap/Resumen**.
2. Muestra la transcripción y el resumen disponible.
3. Abre Copilot en el recap y ejecuta:

> **PROMPT 4 - DECISIONES Y ACCIONES DE LA REUNIÓN**
>
> Resume únicamente lo dicho en esta reunión. Separa la respuesta en: decisiones confirmadas, actividades acordadas, responsable, fecha mencionada y asuntos que quedaron abiertos. Si un responsable o fecha no aparece en la reunión, escribe `No especificado`.

4. Selecciona una decisión y una actividad y compáralas con la transcripción para demostrar trazabilidad.
5. Si Intelligent Recap o Facilitator muestran información adicional, aclara qué contenido proviene de la reunión y qué parte es una síntesis generada por IA.

**Criterio de finalización:** se verificaron contra la transcripción al menos una decisión y una actividad posterior.

## Validación y pruebas finales

| # | Criterio | Estado |
|---|---|---|
| 1 | El resumen identifica avances, al menos tres pendientes, responsables por área, una dependencia y un riesgo. | ☐ |
| 2 | La decisión sobre el grupo piloto sigue abierta antes de la reunión. | ☐ |
| 3 | La agenda contiene objetivo, tiempos, preguntas y cierre con decisiones/próximos pasos. | ☐ |
| 4 | La reunión permanece como borrador y no tiene asistentes reales. | ☐ |
| 5 | La demostración usa una reunión realmente grabada/transcrita. | ☐ |
| 6 | Al menos una decisión y una actividad del recap se validan contra la transcripción. | ☐ |

## Solución de problemas

| Situación | Qué hacer |
|---|---|
| Los `.eml` no se importan | Abre cada archivo en nuevo Outlook o usa la función de importación masiva si está disponible. |
| No existe chat de laboratorio en Teams | Usa `Conversacion_Teams_Lanzamiento.md` como transcripción referenciada y no afirmes que estás analizando un chat en vivo. |
| Facilitator no aparece | Continúa con Copilot en Teams; el temario lo contempla cuando esté disponible. |
| No hay grabación o transcripción para la demo | Prepara la reunión con `Guion_Reunion_Demo.md` antes de impartir el curso. No sustituir por un recap inventado. |

## Limpieza y conservación

- Conserva el borrador de agenda si se requiere como evidencia del ejercicio.
- Puedes eliminar los correos importados de la carpeta de laboratorio al finalizar.
- No envíes la invitación a usuarios reales.
- Conserva la grabación de demostración solo de acuerdo con las políticas del entorno de formación.

## Resumen de la práctica

Recuperaste contexto desde correo y Teams, priorizaste pendientes, preparaste preguntas y una agenda, y observaste cómo Teams convierte una reunión finalizada en acuerdos, decisiones y actividades que deben validarse contra la transcripción.

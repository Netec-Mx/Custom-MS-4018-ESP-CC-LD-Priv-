# Gestión de una solicitud de documentación pendiente para la apertura de una cuenta

Usarás Copilot en Outlook para resumir un hilo ficticio de ocho mensajes, identificar documentos pendientes y compromisos, redactar una respuesta al cliente y preparar una reunión interna breve. La actividad evita introducir requisitos que no estén presentes en el escenario.

## Metadatos

| Campo | Detalle |
|---|---|
| Duración | 31 min |
| Complejidad | Media |
| Nivel de Bloom | Aplicar / Analizar |
| Tipo de actividad | Práctica aplicada de comunicación |
| Aplicaciones | Outlook, Microsoft 365 Copilot |
| Modalidad | Individual |
| Insumos previos | Ocho archivos en `recursos/hilo_documentacion/` |
| Resultado | Resumen del hilo, lista de pendientes, respuesta final en borrador y propuesta de reunión interna |

## Distribución de tiempo

| Fase | Actividad | Tiempo |
|---|---|---:|
| 1 | Resumir el hilo y validar hechos | 6 min |
| 2 | Extraer pendientes, responsables y fechas | 5 min |
| 3 | Redactar la respuesta al cliente | 9 min |
| 4 | Revisar tono, claridad y extensión | 4 min |
| 5 | Preparar una reunión interna breve | 5 min |
| 6 | Validar y conservar borradores | 2 min |
|  | **TOTAL** | **31 min** |

## Descripción general

Importarás un hilo de ocho correos de práctica a Outlook, usarás Copilot para resumirlo y contrastarás el resumen con los mensajes originales. Después elaborarás una respuesta que explique únicamente los pendientes y próximos pasos sustentados y crearás un borrador de reunión interna para resolver un punto de coordinación.

## Objetivos de aprendizaje

- Resumir conversaciones largas con Copilot y verificar hechos contra los mensajes originales.
- Extraer pendientes, responsables, compromisos y fechas sin inventar requisitos.
- Redactar y refinar una respuesta profesional en Outlook.
- Convertir una necesidad de coordinación en una reunión con objetivo y agenda.

## Escenario de la práctica

En CIBEST CAPITAL debes dar seguimiento por correo a la apertura ficticia de una cuenta de inversión cuya documentación continúa incompleta. El hilo incluye una solicitud inicial, documentos recibidos, dos pendientes, una aclaración, un cambio de fecha, responsabilidades distribuidas y un punto que requiere coordinación interna.

## Prerrequisitos

- Microsoft 365 Copilot en Outlook.
- Nuevo Outlook para Windows si se desea importar los `.eml` de forma masiva.
- Una carpeta de correo de laboratorio separada de los mensajes de trabajo reales.

## Preparación del entorno

Antes de iniciar el cronómetro:

1. Importa los ocho archivos `.eml` de `recursos/hilo_documentacion/` a una carpeta de laboratorio. En nuevo Outlook, la función de importación puede aparecer en **Configuración > Archivos > Importar**.
2. Ordena el hilo por conversación si es necesario.
3. Confirma que el asunto común es `Solicitud A-104 - documentación pendiente para apertura de cuenta (ejercicio)`.
4. No envíes ninguno de los mensajes del ejercicio a destinatarios reales.

## Desarrollo de la práctica

### Fase 1 - Resumir el hilo y validar hechos
**Tiempo:** 6 min  
**Aplicación:** Outlook  
**Objetivo:** Obtener un resumen útil sin aceptar errores de IA.

1. Abre la conversación y selecciona **Resumen por Copilot** cuando esté disponible.
2. Contrasta el resumen con los ocho mensajes.
3. Si necesitas una versión más estructurada, usa:

> **PROMPT 1 - RESUMEN ESTRUCTURADO**
>
> Resume este hilo de correo. Separa: solicitud inicial, información ya atendida, documentos que siguen pendientes, aclaraciones realizadas, compromisos, fechas y puntos que requieren coordinación interna.
>
> Usa solo lo escrito en los mensajes. Si un dato no está confirmado, escribe `Pendiente de confirmar` y no agregues requisitos nuevos.

**Criterio de finalización:** el resumen refleja el cambio de fecha y no inventa una fecha final de revisión.

### Fase 2 - Extraer pendientes, responsables y fechas
**Tiempo:** 5 min  
**Aplicación:** Outlook con Copilot  
**Objetivo:** Convertir el hilo en una lista verificable de acciones.

> **PROMPT 2 - LISTA DE PENDIENTES**
>
> Crea una tabla con los pendientes vigentes del hilo. Columnas: Pendiente, Quién debe proporcionarlo o resolverlo, Fecha mencionada, Evidencia en el hilo y Estado. Distingue documentos pendientes de decisiones internas. No agregues requisitos que no aparezcan en la conversación.

1. Verifica que aparezcan los dos documentos pendientes del caso.
2. Comprueba que la nueva fecha prevista del paquete es 4 de octubre de 2026 y que la fecha de finalización sigue sin confirmarse.

**Criterio de finalización:** la tabla separa claramente pendientes del cliente y coordinación interna.

### Fase 3 - Redactar la respuesta al cliente
**Tiempo:** 9 min  
**Aplicación:** Outlook con Copilot  
**Objetivo:** Preparar una respuesta clara, factual y accionable.

1. Inicia una respuesta al último mensaje del hilo, pero no la envíes.

> **PROMPT 3 - RESPUESTA AL CLIENTE**
>
> Redacta una respuesta breve y profesional para el cliente del ejercicio. Debe:
> - confirmar los documentos que siguen pendientes;
> - confirmar la nueva fecha prevista del 4 de octubre de 2026 para recibirlos;
> - explicar que la fecha de finalización todavía no está confirmada;
> - indicar que el equipo responsable revisará el paquete después de recibir los pendientes;
> - evitar requisitos, plazos o compromisos que no estén en el hilo.
>
> No añadas datos personales ni información que no aparezca en la conversación.

2. Compara el borrador con el hilo.
3. Corrige cualquier afirmación no sustentada.

**Criterio de finalización:** el borrador comunica pendientes y próximos pasos sin prometer una fecha de finalización.

### Fase 4 - Revisar tono, claridad y extensión
**Tiempo:** 4 min  
**Aplicación:** Outlook  
**Objetivo:** Mejorar el mensaje sin alterar hechos.

1. Usa **Coaching by Copilot** si está disponible o ejecuta:

> **PROMPT 4 - REVISIÓN DEL MENSAJE**
>
> Revisa este borrador por claridad, tono y extensión. Señala frases ambiguas, poco accionables o que parezcan prometer algo no confirmado. Propón mejoras sin modificar hechos, fechas ni pendientes.

2. Aplica solo las sugerencias que mantengan el contenido factual.

**Criterio de finalización:** el mensaje final es breve, claro y no introduce compromisos nuevos.

### Fase 5 - Preparar una reunión interna breve
**Tiempo:** 5 min  
**Aplicación:** Outlook  
**Objetivo:** Convertir el punto de coordinación en una agenda.

1. Crea una reunión nueva y mantenla como borrador.
2. No agregues asistentes reales.

> **PROMPT 5 - REUNIÓN INTERNA**
>
> Crea un objetivo y una agenda de 20 minutos para una reunión interna entre Comercial y el equipo responsable del proceso. La reunión debe resolver únicamente: qué mensaje se dará al cliente sobre los próximos pasos después de recibir los dos documentos pendientes y quién confirmará el resultado de la revisión.
>
> Incluye una sección final de decisiones y responsables. No agregues políticas ni requisitos nuevos.

**Criterio de finalización:** la reunión tiene un objetivo concreto y una agenda relacionada con el punto de coordinación del hilo.

### Fase 6 - Validar y conservar borradores
**Tiempo:** 2 min  
**Aplicación:** Outlook  
**Objetivo:** Verificar resultados sin realizar acciones externas.

1. Guarda el correo como borrador.
2. Guarda la reunión como borrador.
3. Revisa la checklist.

## Validación y pruebas finales

| # | Criterio | Estado |
|---|---|---|
| 1 | El hilo contiene ocho mensajes importados. | ☐ |
| 2 | El resumen identifica dos documentos pendientes. | ☐ |
| 3 | La fecha prevista del paquete es 4 de octubre de 2026. | ☐ |
| 4 | La fecha de finalización permanece sin confirmar. | ☐ |
| 5 | El correo al cliente no introduce requisitos nuevos. | ☐ |
| 6 | El correo permanece como borrador. | ☐ |
| 7 | La reunión interna tiene objetivo y agenda y no fue enviada. | ☐ |

## Solución de problemas

| Situación | Qué hacer |
|---|---|
| Outlook no agrupa los mensajes | Ordénalos por asunto y fecha; los archivos incluyen encabezados de conversación, pero la vista puede variar. |
| No aparece Resumen por Copilot | Selecciona el hilo completo o usa Copilot Chat en Outlook con el PROMPT 1. |
| Copilot agrega un requisito documental | Elimínalo si no aparece en los mensajes. |
| El borrador promete una fecha final | Sustituye la promesa por la información real del hilo: fecha de finalización no confirmada. |

## Limpieza y conservación

- Conserva los borradores solo si el instructor solicita evidencia.
- Elimina los mensajes de la carpeta de laboratorio cuando ya no sean necesarios.
- No envíes el correo ni la reunión a destinatarios reales.

## Resumen de la práctica

Resumiste y validaste un hilo, transformaste la conversación en una lista de pendientes, redactaste una respuesta controlada, aplicaste coaching y preparaste una reunión interna sin inventar requisitos ni compromisos.

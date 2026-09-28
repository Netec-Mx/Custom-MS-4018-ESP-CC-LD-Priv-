# Análisis del proceso de apertura de cuentas y detección de excepciones operativas

Analizarás un conjunto de 500 solicitudes ficticias de apertura de cuentas con Copilot en Excel. El ejercicio se centra en patrones observables: volumen, tiempos, estados, documentación pendiente, incidencias y valores atípicos. No se deben inventar causas que los datos no demuestren.

## Metadatos

| Campo | Detalle |
|---|---|
| Duración | 35 min |
| Complejidad | Media |
| Nivel de Bloom | Analizar |
| Tipo de actividad | Práctica de análisis de datos |
| Aplicaciones | Excel, Microsoft 365 Copilot |
| Modalidad | Individual |
| Insumos previos | `recursos/Apertura_Cuentas_500_Solicitudes.xlsx` |
| Resultado | Libro de Excel con indicadores, análisis de excepciones, resúmenes, tablas dinámicas y visualizaciones |

## Distribución de tiempo

| Fase | Actividad | Tiempo |
|---|---|---:|
| 1 | Revisar estructura y calidad del dataset | 4 min |
| 2 | Crear una validación con fórmula y métricas iniciales | 7 min |
| 3 | Detectar tendencias y excepciones | 8 min |
| 4 | Construir resúmenes, tablas dinámicas y visualizaciones | 8 min |
| 5 | Priorizar hallazgos y validar evidencia | 6 min |
| 6 | Guardar el resultado | 2 min |
|  | **TOTAL** | **35 min** |

## Descripción general

El archivo contiene aproximadamente 500 solicitudes correspondientes a seis meses y patrones incorporados deliberadamente para el análisis. Usarás Copilot para explorar datos, generar una fórmula, identificar tendencias y valores atípicos, crear resúmenes visuales y producir una lista de asuntos que deberían revisarse operativamente.

## Objetivos de aprendizaje

- Formular preguntas de análisis precisas sobre un dataset estructurado.
- Generar y validar fórmulas con Copilot.
- Identificar patrones, pendientes, incidencias recurrentes y valores atípicos.
- Crear tablas dinámicas y visualizaciones útiles para supervisión.
- Separar hallazgos observables de explicaciones causales no demostradas.

## Escenario de la práctica

En CIBEST CAPITAL debes analizar información ficticia sobre solicitudes de apertura de cuentas de inversión procesadas durante los últimos seis meses del escenario para identificar comportamientos que permitan mejorar el seguimiento operativo.

## Prerrequisitos

- Uso básico de tablas, filtros y gráficos de Excel.
- Microsoft 365 Copilot disponible en Excel.
- El archivo debe abrirse con cálculo automático habilitado.

## Preparación del entorno

1. Copia `recursos/Apertura_Cuentas_500_Solicitudes.xlsx` a OneDrive.
2. Abre la hoja `Acerca_de_los_datos` y confirma que el dataset es ficticio.
3. Vuelve a `Solicitudes` y guarda una copia de trabajo con otro nombre antes de modificarla.

## Desarrollo de la práctica

### Fase 1 - Revisar estructura y calidad del dataset
**Tiempo:** 4 min  
**Aplicación:** Excel  
**Objetivo:** Comprender campos, volumen y posibles problemas antes de analizar.

> **PROMPT 1 - PERFIL DEL DATASET**
>
> Revisa la tabla `SolicitudesApertura`. Describe qué representa cada columna, confirma cuántos registros contiene y señala campos vacíos o combinaciones que deberían revisarse antes del análisis. No corrijas los datos todavía y no infieras causas de negocio.

1. Comprueba que hay 500 registros.
2. Verifica que las filas pendientes pueden no tener fecha de finalización.

**Criterio de finalización:** conoces la estructura y no has tratado los vacíos esperados como errores automáticamente.

### Fase 2 - Crear una validación con fórmula y métricas iniciales
**Tiempo:** 7 min  
**Aplicación:** Excel con Copilot  
**Objetivo:** Usar una fórmula para validar el tiempo de procesamiento en solicitudes completadas.

> **PROMPT 2 - FÓRMULA DE VALIDACIÓN**
>
> Agrega una columna llamada `Dias_completados_calculados`. Para las filas que tengan `Fecha_finalizacion`, calcula los días transcurridos desde `Fecha_recepcion`; si no hay fecha de finalización, deja la celda vacía. Usa una fórmula de Excel editable y no modifiques los datos originales.

1. Revisa varias filas completadas y confirma que la fórmula usa las fechas correctas.
2. Solicita un resumen de volumen total, solicitudes completadas/cerradas, solicitudes pendientes o en revisión, promedio de `Dias_procesamiento` y cantidad de incidencias.
3. Si Copilot propone cambiar registros para “limpiar” el dataset, no aceptes los cambios sin verificar.

**Criterio de finalización:** existe la columna de validación y tienes al menos cuatro indicadores resumidos.

### Fase 3 - Detectar tendencias y excepciones
**Tiempo:** 8 min  
**Aplicación:** Excel con Copilot  
**Objetivo:** Identificar patrones observables sin atribuir causas no demostradas.

> **PROMPT 3 - PATRONES Y EXCEPCIONES**
>
> Analiza la tabla y busca patrones observables relacionados con: volumen por mes, tiempos de procesamiento por tipo de cliente y canal, solicitudes pendientes, documentación pendiente, incidencias frecuentes, equipos responsables y valores atípicos de días de procesamiento.
>
> Para cada hallazgo indica la evidencia numérica que lo respalda. No determines automáticamente la causa. Si propones una explicación, márcala como hipótesis que requiere investigación adicional.

1. Revisa al menos un hallazgo de volumen, uno de tiempo, uno de incidencias y un valor atípico.
2. Contrasta los números con filtros o una tabla dinámica rápida si es necesario.

**Criterio de finalización:** tienes al menos cuatro hallazgos con evidencia cuantitativa y sin causas presentadas como hechos.

### Fase 4 - Construir resúmenes, tablas dinámicas y visualizaciones
**Tiempo:** 8 min  
**Aplicación:** Excel con Copilot  
**Objetivo:** Convertir hallazgos en vistas útiles para supervisión.

> **PROMPT 4 - RESÚMENES Y VISUALES**
>
> Crea en una nueva hoja dos tablas dinámicas: una con volumen de solicitudes por mes y estado, y otra con promedio de `Dias_procesamiento` por tipo de cliente. Después crea dos visualizaciones editables que permitan ver esas diferencias. Mantén vínculos con los datos del libro.

1. Verifica que cada tabla dinámica usa los campos correctos.
2. Comprueba que los gráficos representan exactamente los valores de las tablas.

**Criterio de finalización:** existen al menos dos resúmenes/tablas dinámicas y dos visualizaciones verificables.

### Fase 5 - Priorizar hallazgos y validar evidencia
**Tiempo:** 6 min  
**Aplicación:** Excel con Copilot  
**Objetivo:** Preparar una salida accionable para revisión operativa.

> **PROMPT 5 - PRIORIDADES PARA REVISIÓN**
>
> A partir de los hallazgos observables del libro, prepara una lista priorizada de hasta cinco asuntos que deberían revisarse operativamente. Para cada uno incluye: evidencia, por qué merece revisión, qué pregunta debe investigarse después y qué dato adicional ayudaría a confirmar una causa.
>
> No presentes hipótesis como causas confirmadas y no inventes información externa al libro.

1. Revisa cada prioridad y confirma que tiene una métrica o fila de respaldo.
2. Elimina cualquier afirmación causal que no pueda demostrarse.

**Criterio de finalización:** las prioridades se basan en evidencia y cada hipótesis está claramente identificada.

### Fase 6 - Guardar el resultado
**Tiempo:** 2 min  
**Aplicación:** Excel  
**Objetivo:** Conservar el análisis final.

1. Guarda el libro con un nombre como `Analisis_Apertura_Cuentas_CIBEST.xlsx`.
2. Comprueba que las tablas, fórmulas y gráficos siguen editables.

## Validación y pruebas finales

| # | Criterio | Estado |
|---|---|---|
| 1 | El dataset contiene 500 registros. | ☐ |
| 2 | Existe la columna `Dias_completados_calculados` con fórmula para filas completadas. | ☐ |
| 3 | Se generaron al menos cuatro indicadores. | ☐ |
| 4 | Se documentaron al menos cuatro hallazgos con evidencia numérica. | ☐ |
| 5 | Existen dos tablas dinámicas/resúmenes y dos visualizaciones. | ☐ |
| 6 | Las causas no demostradas están marcadas como hipótesis. | ☐ |
| 7 | El archivo final está guardado y abre correctamente. | ☐ |

## Solución de problemas

| Situación | Qué hacer |
|---|---|
| Copilot no reconoce la tabla | Haz clic dentro de `SolicitudesApertura`, confirma que la tabla tiene encabezados y vuelve a abrir Copilot. |
| Copilot intenta reemplazar datos originales | Rechaza el cambio y pídele crear una nueva columna u hoja. |
| Un gráfico no coincide con la tabla | Verifica el rango/campos y vuelve a crearlo desde la tabla dinámica correcta. |
| Copilot explica causas sin evidencia | Reformula la salida como hipótesis y conserva solo los patrones respaldados por datos. |

## Limpieza y conservación

- Conserva el libro final y el dataset original.
- No borres la hoja `Acerca_de_los_datos`.
- No reutilices los registros ficticios como información real.

## Resumen de la práctica

Exploraste un dataset estructurado, generaste una fórmula de validación, detectaste patrones y excepciones, creaste resúmenes visuales y separaste hallazgos demostrables de explicaciones que requieren investigación adicional.

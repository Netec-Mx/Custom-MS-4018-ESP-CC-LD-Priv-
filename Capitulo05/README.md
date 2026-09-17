# Análisis del proceso de apertura de cuentas y detección de excepciones operativas (CIBEST CAPITAL)

## Metadatos

| Elemento | Valor |
|---|---|
| Duración | 35 minutos |
| Complejidad | Difícil |
| Nivel de Bloom | Analizar |
| Modalidad | Laboratorio individual guiado |
| Caso continuo | CIBEST CAPITAL: apertura de cuentas, controles de vinculación y excepciones operativas |

## Descripción General

En este laboratorio analizará los datos operativos del proceso de apertura de cuentas de CIBEST CAPITAL para identificar demoras, excepciones, controles omitidos, responsables afectados y riesgos de cumplimiento. Usará Microsoft 365 Copilot en Excel para explorar datos, generar fórmulas, resumir hallazgos mediante tablas dinámicas y crear visualizaciones ejecutivas.

El análisis incorporará evidencia interna procedente del procedimiento de vinculación de clientes y de las notas de la reunión de lanzamiento del servicio digital. Finalmente, realizará una proyección básica de tendencia con Python en Excel, si esta capacidad está habilitada, y documentará una recomendación accionable para controles, capacidad operativa y seguimiento de excepciones.

## Objetivos de Aprendizaje

Al completar este laboratorio, podrá:

- [ ] Preparar y validar un conjunto de datos de apertura de cuentas como tabla estructurada de Excel.
- [ ] Usar Copilot en Excel para detectar tendencias, valores atípicos, demoras y excepciones por etapa, causa, responsable y período.
- [ ] Crear métricas y columnas calculadas para clasificar tiempos de ciclo, excepciones y posibles incumplimientos de control.
- [ ] Integrar de manera controlada el procedimiento de vinculación y las decisiones de reunión en la interpretación de los datos.
- [ ] Crear una tabla dinámica, visualizaciones y una proyección básica de excepciones, validando los resultados antes de comunicar conclusiones.

## Prerrequisitos

### Conocimientos requeridos

- Uso funcional de libros, hojas, filtros, tablas y gráficos de Excel.
- Comprensión básica de fórmulas de Excel y tablas dinámicas.
- Conocimiento de los conceptos de tiempo de ciclo, excepción operativa, control y riesgo de cumplimiento.
- Capacidad para distinguir entre un hecho medido, una hipótesis operativa y una recomendación.

### Acceso y artefactos requeridos

Confirme que dispone de acceso a los siguientes elementos en OneDrive:

| Artefacto | Ubicación esperada | Uso en este laboratorio |
|---|---|---|
| Datos de apertura de cuentas y excepciones | `00_Source_Data` | Fuente principal del análisis |
| Procedimiento de vinculación | `03_Word/CIBEST_Proceso_Vinculacion_Clientes_v1.docx` | Contexto de controles y etapas obligatorias |
| Notas de la demostración o reunión | `04_Meetings/CIBEST_Lanzamiento_Servicio_Digital_Notas.docx` | Contexto de decisiones, acciones y responsables |
| Libro de salida | `05_Excel/CIBEST_Apertura_Cuentas_Excepciones_v1.xlsx` | Entregable del laboratorio |

También necesita:

- Acceso a Microsoft 365 Copilot en Excel.
- Permiso de edición en OneDrive - CIBEST CAPITAL.
- Acceso a fuentes web autorizadas por la organización, si realizará el paso de contexto externo.
- Acceso a Python in Excel, opcional para el paso de proyección.

> **Importante:** Use siempre la zona horaria `America/Bogota (UTC-05:00)` al interpretar fechas, horas y tiempos de ciclo relacionados con el proceso operativo.

## Entorno de Laboratorio

### Hardware recomendado

| Componente | Requisito |
|---|---|
| Equipo | Windows 11 de 64 bits, procesador de 4 núcleos a 2.0 GHz o superior |
| Memoria | 8 GB de RAM como mínimo |
| Pantalla | Resolución mínima de 1920 × 1080; segunda pantalla recomendada |
| Conectividad | Internet estable de al menos 20 Mbps de descarga y 5 Mbps de carga |
| Audio | Auriculares con micrófono opcionales para accesibilidad o dictado |

### Software y servicios

| Componente | Uso |
|---|---|
| Microsoft Excel con Microsoft 365 Copilot | Exploración, fórmulas, tablas dinámicas y gráficos |
| OneDrive para el trabajo o la escuela | Almacenamiento y continuidad de artefactos |
| Word para la Web o Word de escritorio | Consulta del procedimiento de vinculación |
| Microsoft Teams / Stream | Consulta de notas, acuerdos o transcripción de la reunión |
| Python in Excel | Proyección opcional de tendencia de excepciones |
| Microsoft Edge | Consulta controlada de fuentes externas autorizadas |

### Preparación inicial del espacio de trabajo

1. Abra OneDrive en el explorador de archivos o en el navegador.
2. Vaya a la carpeta raíz obligatoria:

   ```text
   OneDrive - CIBEST CAPITAL/Copilot_Labs/Batch_01/
   ```

3. Confirme que existen las carpetas:

   ```text
   00_Source_Data
   02_PowerPoint
   03_Word
   04_Meetings
   05_Excel
   99_Submissions
   ```

4. Abra simultáneamente, si es posible en ventanas separadas:
   - El archivo de datos disponible en `00_Source_Data`.
   - `03_Word/CIBEST_Proceso_Vinculacion_Clientes_v1.docx`.
   - `04_Meetings/CIBEST_Lanzamiento_Servicio_Digital_Notas.docx`.

5. Cree o abra el libro de salida con el nombre obligatorio:

   ```text
   05_Excel/CIBEST_Apertura_Cuentas_Excepciones_v1.xlsx
   ```

> **Convención de trabajo:** No modifique el archivo fuente original. Use el libro de salida para importar, consolidar, limpiar y analizar los datos.

## Instrucciones Paso a Paso

### Paso 1: Definir el objetivo analítico y revisar el contexto operativo

**Objetivo:** Establecer las preguntas de negocio que guiarán el análisis y extraer criterios de control desde los artefactos de laboratorios anteriores.

**Instrucciones:**

1. Abra el documento:

   ```text
   03_Word/CIBEST_Proceso_Vinculacion_Clientes_v1.docx
   ```

2. Identifique y registre en una hoja nueva de Excel llamada `Contexto_Control` los siguientes elementos del procedimiento:
   - Etapas del proceso de vinculación.
   - Controles obligatorios.
   - Evidencias requeridas para cada control.
   - Responsable o área responsable.
   - Criterio de escalamiento o aprobación excepcional, si aplica.

3. Abra el documento:

   ```text
   04_Meetings/CIBEST_Lanzamiento_Servicio_Digital_Notas.docx
   ```

4. Identifique decisiones o acciones que puedan afectar el proceso de apertura de cuentas. Por ejemplo:
   - Fecha de inicio o piloto del servicio digital.
   - Cambios en responsables.
   - Compromisos de tiempo de respuesta.
   - Actividades de capacitación.
   - Reglas de seguimiento de excepciones.
   - Dependencias tecnológicas o documentales.

5. En la hoja `Contexto_Control`, agregue una sección titulada `Contexto de reunión` y registre solamente hechos confirmados en las notas.

6. En la parte superior de la hoja, documente el objetivo analítico con este texto:

   ```text
   Detectar etapas con demoras, controles omitidos, causas frecuentes de excepción,
   responsables afectados y riesgos operativos o de cumplimiento en el proceso de apertura de cuentas.
   ```

7. Agregue las siguientes preguntas de análisis:

   ```text
   ¿Qué etapas presentan mayor tiempo de ciclo?
   ¿Qué causas generan más excepciones?
   ¿Qué responsables concentran más casos con demora o excepción?
   ¿Existen controles obligatorios omitidos?
   ¿Se observan cambios por período antes y después de decisiones operativas documentadas?
   ¿Qué hallazgos requieren investigación adicional antes de atribuir una causa?
   ```

**Resultado esperado:**

Una hoja `Contexto_Control` que documenta los controles internos relevantes, el contexto confirmado de la reunión y las preguntas que orientarán el análisis.

**Verificación:**

- Confirme que cada afirmación de contexto tiene una fuente identificable: procedimiento o notas de reunión.
- Compruebe que no se han convertido hipótesis en hechos. Por ejemplo, escriba “posible impacto por capacitación pendiente” solo como hipótesis, no como conclusión.
- Verifique que las fechas del contexto están expresadas o interpretadas en `America/Bogota (UTC-05:00)`.

---

### Paso 2: Importar, estructurar y validar los datos de apertura de cuentas

**Objetivo:** Preparar una tabla limpia y consistente que Copilot pueda interpretar correctamente.

**Instrucciones:**

1. Abra el archivo o los archivos de datos proporcionados en:

   ```text
   00_Source_Data
   ```

2. Identifique la tabla o el rango que contiene los registros de apertura de cuentas. Las columnas pueden variar, pero normalmente deben incluir información equivalente a:

   | Columna esperada | Ejemplo de uso |
   |---|---|
   | Identificador de cuenta o solicitud | Trazabilidad del caso |
   | Fecha de solicitud | Inicio del proceso |
   | Fecha de finalización | Cierre o activación |
   | Etapa | Recepción, validación, KYC, aprobación, activación, entre otras |
   | Estado | Completado, pendiente, rechazado, en excepción |
   | Causa de excepción | Documento faltante, validación KYC, firma, datos inconsistentes |
   | Responsable | Analista, equipo o área operativa |
   | Control realizado | Indicador de cumplimiento del control |
   | Fecha de excepción | Momento en que se registró la excepción |
   | Prioridad o riesgo | Clasificación operativa o de cumplimiento |

3. Copie los datos al libro de salida `CIBEST_Apertura_Cuentas_Excepciones_v1.xlsx`.

4. Cree una hoja llamada `Datos_Aperturas`.

5. Seleccione el rango de datos y conviértalo en una tabla:
   - Seleccione cualquier celda del rango.
   - Use **Insertar > Tabla**.
   - Active la opción **La tabla tiene encabezados**.
   - También puede usar el método abreviado:

   ```text
   Ctrl + T
   ```

6. En la pestaña **Diseño de tabla**, asigne a la tabla el nombre:

   ```text
   AperturasCIBEST
   ```

7. Revise que los encabezados sean claros, únicos y consistentes. Si fuera necesario, normalice nombres ambiguos. Por ejemplo:

   | Encabezado ambiguo | Encabezado recomendado |
   |---|---|
   | Fecha fin | Fecha_Finalizacion |
   | Resp. | Responsable |
   | Obs | Causa_Excepcion |
   | Ctrl | Control_Realizado |

8. Compruebe los tipos de datos:
   - Fechas como fechas reales de Excel.
   - Duraciones como valores numéricos.
   - Categorías como texto.
   - Identificadores como texto si contienen ceros iniciales.
   - Campos de control como valores consistentes, por ejemplo `Sí`, `No`, `Pendiente`.

9. Use Copilot en Excel con la siguiente solicitud:

   > Analiza la tabla AperturasCIBEST. Identifica valores vacíos en columnas críticas, encabezados ambiguos, fechas inválidas, categorías duplicadas por diferencias de escritura y valores atípicos evidentes. Presenta los hallazgos en una tabla con columna, problema detectado, cantidad de registros afectados y recomendación de corrección. No modifiques los datos sin mi confirmación.

10. Revise los hallazgos directamente en la tabla antes de realizar correcciones.

11. Si existen variaciones de categorías, normalícelas. Por ejemplo:
   - `KYC`, `kyc` y `Kyc` deben quedar como `KYC`.
   - `Pendiente Doc.` y `Documentación pendiente` deben quedar bajo una categoría acordada.
   - `SI`, `Sí` y `SÍ` deben quedar como `Sí`.

**Resultado esperado:**

La hoja `Datos_Aperturas` contiene una tabla estructurada llamada `AperturasCIBEST`, con encabezados claros, datos consistentes y problemas de calidad documentados.

**Verificación:**

- Seleccione una celda dentro de los datos y confirme que aparece la pestaña **Diseño de tabla**.
- Revise que la caja de nombre de tabla muestre `AperturasCIBEST`.
- Filtre cada columna crítica y confirme que no existen errores como `#N/A`, `#VALUE!` o fechas convertidas en texto.
- No elimine registros sin conservar trazabilidad; si corrige una categoría, documente el criterio en una nota o en la hoja `Contexto_Control`.

---

### Paso 3: Crear métricas de tiempo de ciclo y clasificación de excepciones

**Objetivo:** Generar columnas calculadas que permitan detectar demoras, controles omitidos y riesgos de seguimiento.

**Instrucciones:**

1. Revise en el procedimiento de vinculación si se define un tiempo objetivo de atención, acuerdo de nivel de servicio o criterio de escalamiento.

2. Si el procedimiento no proporciona un umbral explícito, use temporalmente el siguiente criterio analítico, documentándolo como supuesto:

   ```text
   Demora operativa: tiempo de ciclo superior a 48 horas.
   Riesgo alto: excepción activa o control obligatorio omitido.
   ```

3. En `Datos_Aperturas`, agregue una columna llamada:

   ```text
   Tiempo_Ciclo_Horas
   ```

4. Solicite a Copilot una fórmula apropiada. Use esta solicitud:

   > En la tabla AperturasCIBEST, crea una fórmula para la columna Tiempo_Ciclo_Horas que calcule las horas entre Fecha_Solicitud y Fecha_Finalizacion. Si Fecha_Finalizacion está vacía, calcula las horas transcurridas hasta ahora. Devuelve vacío si falta Fecha_Solicitud. Explica la fórmula antes de insertarla.

5. Revise la fórmula propuesta por Copilot. Una posible fórmula, según los nombres reales de sus columnas, puede tener una estructura similar a:

   ```excel
   =IF([@Fecha_Solicitud]="","",24*(IF([@Fecha_Finalizacion]="",NOW(),[@Fecha_Finalizacion])-[@Fecha_Solicitud]))
   ```

6. Agregue una columna llamada:

   ```text
   Clasificacion_Tiempo
   ```

7. Solicite a Copilot:

   > Crea una fórmula para Clasificacion_Tiempo en AperturasCIBEST. Clasifica como "Dentro de objetivo" los casos con Tiempo_Ciclo_Horas menor o igual a 48, como "Demora" los superiores a 48 y como "Sin fecha de inicio" los registros sin tiempo de ciclo. Usa referencias estructuradas de tabla.

8. Agregue una columna denominada:

   ```text
   Riesgo_Operativo
   ```

9. Solicite a Copilot:

   > Crea una fórmula para Riesgo_Operativo en la tabla AperturasCIBEST. Clasifica como "Alto" un registro que tenga una excepción activa, un control obligatorio marcado como "No" o una demora superior a 48 horas. Clasifica como "Medio" una excepción cerrada con demora. Clasifica como "Bajo" los demás casos. Antes de crearla, indícame qué columnas utilizarás y cómo tratarás los valores vacíos.

10. Revise que los nombres de columnas utilizados por la fórmula coincidan exactamente con los del libro.

11. Agregue una columna denominada:

   ```text
   Mes_Registro
   ```

12. Cree una fórmula que agrupe la fecha relevante para el análisis mensual. Use `Fecha_Solicitud` o `Fecha_Excepcion` según el objetivo del archivo. Una fórmula posible es:

   ```excel
   =TEXT([@Fecha_Solicitud],"yyyy-mm")
   ```

13. Si la fecha contiene hora y necesita una fecha sin componente horario, puede usar:

   ```excel
   =INT([@Fecha_Solicitud])
   ```

**Resultado esperado:**

La tabla contiene métricas y clasificaciones para analizar tiempos de ciclo, demoras, riesgos y períodos mensuales.

**Verificación:**

- Filtre `Clasificacion_Tiempo` por `Demora` y revise al menos cinco registros manualmente.
- Filtre `Riesgo_Operativo` por `Alto` y confirme que la clasificación se explica por una excepción, un control omitido o una demora.
- Compruebe que los registros sin fecha de finalización no generan resultados incoherentes.
- Valide que el uso de `NOW()` no altere indebidamente análisis históricos. Si el conjunto de datos corresponde a un período cerrado, documente que los casos abiertos se calculan hasta la fecha actual.

---

### Paso 4: Explorar patrones y excepciones con Copilot en Excel

**Objetivo:** Utilizar preguntas iterativas para identificar patrones, valores extremos y segmentos que requieren investigación.

**Instrucciones:**

1. Seleccione una celda dentro de la tabla `AperturasCIBEST`.

2. Abra Copilot en Excel.

3. Solicite un análisis inicial:

   > Analiza la tabla AperturasCIBEST para detectar tendencias, cambios bruscos y valores atípicos. Prioriza Tiempo_Ciclo_Horas, Clasificacion_Tiempo, Causa_Excepcion, Responsable, Etapa y Riesgo_Operativo. Resume los cinco hallazgos más relevantes para una dirección de operaciones e indica qué hallazgos requieren investigación adicional. Distingue hechos medidos de posibles hipótesis.

4. Revise los hallazgos y formule una segunda pregunta centrada en las demoras:

   > Para los registros clasificados como "Demora", compara las etapas, causas de excepción y responsables. Muestra el número de casos, tiempo de ciclo promedio, mediana de tiempo de ciclo y porcentaje de riesgo alto. Señala diferencias relevantes, pero no infieras causalidad sin evidencia adicional.

5. Formule una tercera pregunta enfocada en controles:

   > Identifica los controles obligatorios que aparecen como omitidos, pendientes o inconsistentes en AperturasCIBEST. Agrupa los casos por etapa y responsable. Compara estos hallazgos con el contexto de controles documentado en la hoja Contexto_Control y señala cualquier discrepancia que deba ser revisada por Cumplimiento.

6. Solicite una revisión temporal:

   > Analiza la evolución mensual de excepciones y demoras usando Mes_Registro. Identifica meses con variaciones inusuales frente al mes anterior. Indica el número absoluto, la variación porcentual y las causas más frecuentes de cada período. No atribuyas el cambio a una decisión de negocio sin evidencia adicional.

7. Cree una hoja llamada `Hallazgos_Copilot`.

8. Copie a esta hoja los hallazgos que hayan sido verificados manualmente. Para cada hallazgo, incluya:

   | Campo | Descripción |
   |---|---|
   | ID | Identificador secuencial |
   | Hallazgo validado | Descripción basada en datos |
   | Evidencia | Métrica, filtro, tabla dinámica o registros revisados |
   | Contexto interno | Referencia al procedimiento o a las notas de reunión |
   | Tipo | Hecho, hipótesis o recomendación |
   | Acción siguiente | Validar, escalar, ajustar control, revisar capacidad, entre otras |

**Resultado esperado:**

Una lista priorizada de hallazgos basada en datos, diferenciando hechos observables de interpretaciones que requieren validación.

**Verificación:**

- Cada hallazgo registrado en `Hallazgos_Copilot` debe apuntar a una métrica o un filtro verificable.
- Ningún hallazgo debe presentar una correlación como una relación causal confirmada.
- Confirme que las referencias al procedimiento y a las notas de reunión se usan para contextualizar, no para reemplazar la evidencia del libro.

---

### Paso 5: Crear tablas dinámicas y visualizaciones ejecutivas

**Objetivo:** Convertir los datos y hallazgos en resúmenes visuales orientados a decisiones operativas.

**Instrucciones:**

1. Cree una hoja llamada:

   ```text
   Resumen_Ejecutivo
   ```

2. Seleccione una celda en la tabla `AperturasCIBEST`.

3. Inserte una tabla dinámica:
   - Seleccione **Insertar > Tabla dinámica**.
   - Elija la tabla `AperturasCIBEST` como origen.
   - Coloque la tabla dinámica en la hoja `Resumen_Ejecutivo`.

4. Configure una primera tabla dinámica denominada `PT_Excepciones_Etapa`:

   | Área de tabla dinámica | Campo |
   |---|---|
   | Filas | Etapa |
   | Columnas | Riesgo_Operativo |
   | Valores | Recuento de identificador de solicitud o cuenta |
   | Filtros | Estado, Mes_Registro |

5. Configure una segunda tabla dinámica denominada `PT_Causas_Responsable`:

   | Área de tabla dinámica | Campo |
   |---|---|
   | Filas | Causa_Excepcion |
   | Columnas | Responsable |
   | Valores | Recuento de identificador de solicitud o cuenta |
   | Filtros | Clasificacion_Tiempo, Riesgo_Operativo |

6. Configure una tercera tabla dinámica denominada `PT_Tendencia_Mensual`:

   | Área de tabla dinámica | Campo |
   |---|---|
   | Filas | Mes_Registro |
   | Valores | Recuento de identificador de solicitud o cuenta |
   | Filtros | Estado o indicador de excepción |

7. Use Copilot en Excel para solicitar una recomendación de visualización:

   > A partir de las tablas dinámicas de Resumen_Ejecutivo, recomienda tres gráficos para una audiencia ejecutiva de CIBEST CAPITAL. El objetivo es mostrar etapas con demoras, principales causas de excepción, responsables afectados y tendencia mensual. Indica para cada gráfico qué decisión apoyaría y qué riesgo de interpretación debe evitarse.

8. Cree al menos los siguientes gráficos:
   - **Gráfico de barras horizontales:** excepciones o riesgos altos por etapa.
   - **Gráfico de barras apiladas o matriz:** causas de excepción por responsable.
   - **Gráfico de líneas:** evolución mensual de excepciones o demoras.

9. Agregue títulos descriptivos. Ejemplos:

   ```text
   Excepciones de riesgo alto por etapa de apertura
   Causas de excepción por responsable operativo
   Tendencia mensual de demoras y excepciones
   ```

10. Evite gráficos 3D, escalas engañosas o títulos genéricos como “Gráfico 1”.

11. Agregue un cuadro de texto con tres conclusiones breves, basadas solo en hallazgos verificados. Use este formato:

   ```text
   1. Hecho observado:
   2. Riesgo o impacto potencial:
   3. Acción recomendada:
   ```

**Resultado esperado:**

La hoja `Resumen_Ejecutivo` contiene tres tablas dinámicas, visualizaciones comprensibles y conclusiones ejecutivas trazables a los datos.

**Verificación:**

- Cambie temporalmente el filtro de `Mes_Registro` y confirme que las tablas dinámicas y gráficos se actualizan de forma coherente.
- Compruebe que los valores de los gráficos coinciden con los de las tablas dinámicas.
- Confirme que los gráficos responden a una decisión: control, capacidad operativa, priorización o seguimiento.

---

### Paso 6: Incorporar contexto interno y externo de manera responsable

**Objetivo:** Enriquecer el análisis sin confundir datos internos con información contextual o hipótesis.

**Instrucciones:**

1. Revise las decisiones registradas en la hoja `Contexto_Control`.

2. Identifique una fecha o cambio operativo documentado que pueda compararse con la evolución de excepciones. Por ejemplo:
   - Inicio del nuevo servicio digital.
   - Cambio de proceso.
   - Ajuste de responsables.
   - Sesión de capacitación.
   - Activación de una regla de seguimiento.

3. Cree una sección en `Hallazgos_Copilot` llamada `Comparación con contexto interno`.

4. Registre una observación usando una estructura prudente:

   ```text
   Hecho: El volumen de excepciones aumentó/disminuyó en el período X.
   Contexto confirmado: En el mismo período se registró la decisión o evento Y.
   Interpretación prudente: La coincidencia temporal justifica una revisión adicional, pero no demuestra causalidad.
   Evidencia adicional necesaria: distribución de carga, registros de capacitación, cambios de sistema, calidad documental o detalle de casos.
   ```

5. Si las políticas del tenant permiten consultas web autorizadas, realice una consulta sin incluir datos confidenciales, identificadores de clientes ni métricas internas sensibles.

6. Use una solicitud como la siguiente:

   > Busca fuentes públicas, recientes y confiables sobre tendencias de digitalización, verificación de identidad o gestión de riesgos operativos en procesos de vinculación financiera en Colombia durante 2025 y 2026. Cita la fuente y fecha de publicación. Resume únicamente información que pueda servir como contexto general; no la uses para explicar de forma concluyente los resultados internos de CIBEST CAPITAL.

7. Priorice fuentes primarias o institucionales, tales como:
   - Superintendencia Financiera de Colombia.
   - Banco de la República.
   - Organismos regulatorios o asociaciones sectoriales reconocidas.
   - Informes técnicos con fecha y metodología identificable.

8. Cree una hoja llamada `Fuentes_Externas` con las columnas:

   | Fuente | Fecha | Ámbito | Hallazgo externo | Relación potencial con análisis interno | Limitación |
   |---|---|---|---|---|---|

9. Documente claramente que la fuente externa es contextual. No copie información externa al libro como si fuera una métrica operativa de CIBEST CAPITAL.

**Resultado esperado:**

El libro incluye contexto interno trazable y, si se utilizó, contexto externo documentado con fuente, fecha, alcance y limitaciones.

**Verificación:**

- Confirme que no se compartieron datos personales, identificadores de cuentas ni contenido confidencial en consultas web.
- Verifique que cada fuente externa incluye fecha de publicación y enlace o referencia.
- Revise que ninguna conclusión afirme que un indicador externo causó una variación interna.

---

### Paso 7: Realizar una proyección básica con Python in Excel

**Objetivo:** Generar una proyección exploratoria de tendencia de excepciones y validar su utilidad antes de presentarla.

> **Nota:** Este paso es opcional si Python in Excel no está habilitado. Si no está disponible, complete el análisis de tendencia con una tabla dinámica y un gráfico de líneas, y documente la limitación.

**Instrucciones:**

1. En la hoja `Resumen_Ejecutivo`, cree una tabla de resumen mensual con dos columnas:

   | Mes | Excepciones |
   |---|---|
   | 2026-01 | Recuento mensual |
   | 2026-02 | Recuento mensual |

2. Asegúrese de que los meses estén ordenados cronológicamente y que no existan meses duplicados con formatos diferentes.

3. Cree una hoja llamada:

   ```text
   Pronostico_Python
   ```

4. Copie o vincule la tabla mensual a esta hoja.

5. Seleccione una celda vacía y use Python in Excel. Una aproximación básica de regresión lineal puede utilizar una fórmula de tipo `PY`. Ajuste las referencias según la ubicación real de los datos:

   ```excel
   =PY("
import pandas as pd
import numpy as np

df = xl('A1:B12', headers=True)
df['Periodo'] = np.arange(len(df))
coef = np.polyfit(df['Periodo'], df['Excepciones'], 1)
df['Tendencia_Ajustada'] = np.polyval(coef, df['Periodo'])
df
")
   ```

6. Si desea proyectar tres períodos adicionales, use una versión ampliada:

   ```excel
   =PY("
import pandas as pd
import numpy as np

df = xl('A1:B12', headers=True)
df['Periodo'] = np.arange(len(df))

coef = np.polyfit(df['Periodo'], df['Excepciones'], 1)

futuro = pd.DataFrame({
    'Periodo': np.arange(len(df), len(df) + 3)
})
futuro['Excepciones_Proyectadas'] = np.polyval(coef, futuro['Periodo'])

df['Tendencia_Ajustada'] = np.polyval(coef, df['Periodo'])

{'Historico': df, 'Proyeccion_3_periodos': futuro}
")
   ```

7. Revise el resultado antes de usarlo. La proyección lineal solo representa una tendencia simple; no incorpora estacionalidad, cambios regulatorios, capacidad operativa, campañas, cambios de sistema ni calidad documental.

8. Agregue una nota visible junto al resultado:

   ```text
   Proyección exploratoria basada en tendencia lineal histórica.
   No debe utilizarse como pronóstico operativo definitivo sin validación adicional.
   ```

9. Compare visualmente la tendencia proyectada con el gráfico histórico de excepciones.

10. Registre en `Hallazgos_Copilot` una conclusión prudente. Ejemplo:

   ```text
   La tendencia lineal sugiere una variación esperada de excepciones si las condiciones históricas se mantuvieran.
   Esta proyección no confirma que el comportamiento continúe y debe validarse con capacidad operativa,
   cambios de proceso y causas de excepción.
   ```

**Resultado esperado:**

Una proyección exploratoria de tendencia, claramente etiquetada como análisis de apoyo y validada frente a los datos históricos.

**Verificación:**

- Compruebe que el rango usado por Python contiene solamente meses y recuentos numéricos válidos.
- Confirme que la proyección no se presenta como una predicción garantizada.
- Verifique que un valor extremo o un mes incompleto no esté distorsionando la tendencia.
- Si hay pocos períodos históricos, registre que la confiabilidad analítica es limitada.

---

### Paso 8: Preparar la recomendación accionable y guardar el entregable

**Objetivo:** Traducir los hallazgos validados en una recomendación ejecutiva reutilizable en los laboratorios posteriores.

**Instrucciones:**

1. En la hoja `Resumen_Ejecutivo`, cree una sección titulada:

   ```text
   Recomendación operativa para CIBEST CAPITAL
   ```

2. Elabore una recomendación de máximo cinco líneas que incluya:
   - Control que debe reforzarse.
   - Etapa o causa prioritaria.
   - Responsable o área que debe intervenir.
   - Acción concreta.
   - Métrica de seguimiento.

3. Use esta estructura:

   ```text
   Prioridad:
   Hallazgo basado en datos:
   Riesgo operativo o de cumplimiento:
   Acción recomendada:
   Responsable sugerido:
   Indicador de seguimiento:
   ```

4. Solicite a Copilot una versión ejecutiva, sin permitir que invente datos:

   > Redacta una recomendación ejecutiva basada exclusivamente en los hallazgos validados de la hoja Hallazgos_Copilot y en los indicadores de Resumen_Ejecutivo. Debe priorizar controles, capacidad operativa y seguimiento de excepciones. No inventes cifras ni afirmes causalidad. Usa un tono profesional para dirección de operaciones y cumplimiento.

5. Revise el texto generado por Copilot y valide:
   - Cifras.
   - Nombres de etapas.
   - Responsables.
   - Referencias a controles.
   - Diferencia entre evidencia e hipótesis.

6. Guarde el archivo con el nombre obligatorio:

   ```text
   OneDrive - CIBEST CAPITAL/Copilot_Labs/Batch_01/05_Excel/CIBEST_Apertura_Cuentas_Excepciones_v1.xlsx
   ```

7. Si el instructor lo solicita, copie una versión final a:

   ```text
   OneDrive - CIBEST CAPITAL/Copilot_Labs/Batch_01/99_Submissions/
   ```

8. Verifique que OneDrive haya sincronizado el archivo antes de cerrar Excel.

**Resultado esperado:**

Un libro de Excel completo, guardado en la ubicación obligatoria, que conecta los datos operativos con el procedimiento de vinculación, las decisiones de reunión y una recomendación ejecutiva validada.

**Verificación:**

- Confirme la ruta y el nombre exacto del archivo.
- Abra el archivo desde OneDrive para verificar que se guardó la versión actual.
- Compruebe que el libro contiene, como mínimo, las hojas:
  - `Datos_Aperturas`
  - `Contexto_Control`
  - `Hallazgos_Copilot`
  - `Resumen_Ejecutivo`
  - `Fuentes_Externas`, si se usaron fuentes web
  - `Pronostico_Python`, si se realizó la proyección

## Validación y Pruebas

Complete la siguiente lista de validación antes de entregar el laboratorio:

| Validación | Criterio de aceptación |
|---|---|
| Ubicación del archivo | El archivo se encuentra en `05_Excel/CIBEST_Apertura_Cuentas_Excepciones_v1.xlsx` |
| Tabla estructurada | Existe una tabla llamada `AperturasCIBEST` |
| Calidad de datos | Las columnas críticas no contienen errores de fórmula ni formatos inconsistentes no documentados |
| Métrica de tiempo | `Tiempo_Ciclo_Horas` tiene una fórmula revisada y valores plausibles |
| Clasificación | `Clasificacion_Tiempo` y `Riesgo_Operativo` se pueden filtrar y explicar |
| Controles | Los controles omitidos o pendientes se comparan con el procedimiento de vinculación |
| Contexto de reunión | Las decisiones de la reunión se distinguen de los datos medidos |
| Tabla dinámica | Se puede resumir por etapa, causa, responsable y período |
| Gráficos | Los gráficos coinciden con las tablas dinámicas y tienen títulos ejecutivos |
| Hallazgos | Los hallazgos distinguen hechos, hipótesis y recomendaciones |
| Contexto externo | Si se utilizó, incluye fuente, fecha, alcance y limitación |
| Python in Excel | Si se utilizó, la proyección está etiquetada como exploratoria y no concluyente |
| Recomendación final | Propone una acción concreta, responsable y métrica de seguimiento |

Como prueba final, responda oralmente o por escrito las siguientes preguntas:

1. ¿Cuál es la etapa con mayor concentración de demoras y qué evidencia respalda esa afirmación?
2. ¿Cuál es la causa de excepción más frecuente y cómo se distribuye entre responsables?
3. ¿Qué control obligatorio parece requerir revisión prioritaria?
4. ¿Qué conclusión sería prematuro afirmar con los datos disponibles?
5. ¿Qué indicador debe revisarse semanalmente para evaluar la efectividad de la recomendación?

## Solución de Problemas

### Problema 1: Copilot no reconoce correctamente los datos o responde con análisis genéricos

**Síntomas:**

- Copilot no identifica columnas relevantes.
- Las respuestas mencionan rangos incompletos o encabezados incorrectos.
- No puede crear fórmulas con referencias estructuradas.
- El análisis no diferencia etapas, responsables o causas de excepción.

**Causa probable:**

Los datos no están convertidos en una tabla de Excel, tienen encabezados ambiguos, contienen filas vacías dentro del rango o mezclan formatos de fecha, texto y números.

**Corrección:**

1. Confirme que el rango está convertido en una tabla mediante `Ctrl + T`.
2. Verifique que la tabla se llama `AperturasCIBEST`.
3. Elimine filas y columnas vacías dentro de la tabla.
4. Renombre encabezados ambiguos y asegure que sean únicos.
5. Corrija fechas almacenadas como texto y normalice categorías.
6. Seleccione una celda dentro de la tabla antes de volver a solicitar ayuda a Copilot.
7. Reformule la solicitud mencionando explícitamente el nombre de la tabla y las columnas que debe analizar.

### Problema 2: Python in Excel no está disponible o la fórmula `PY` devuelve un error

**Síntomas:**

- No aparece la opción Python in Excel.
- La fórmula `=PY()` no se reconoce.
- El resultado muestra un error de permisos, cálculo o referencia de rango.
- La salida de Python no coincide con los datos mensuales visibles.

**Causa probable:**

Python in Excel no está habilitado para el usuario o canal de actualización; el rango utilizado contiene encabezados incorrectos, valores no numéricos, meses desordenados o referencias que no corresponden a la tabla mensual.

**Corrección:**

1. Confirme con el instructor o administrador que Python in Excel está habilitado para su cuenta.
2. Actualice Excel e inicie sesión con la cuenta corporativa autorizada.
3. Revise que la tabla mensual tenga una fila de encabezados y valores numéricos en la columna `Excepciones`.
4. Ordene los meses cronológicamente antes de ejecutar el modelo.
5. Ajuste el rango de `xl('A1:B12', headers=True)` para que coincida con el rango real.
6. Si la capacidad no está disponible, utilice una tabla dinámica mensual y un gráfico de líneas como alternativa, y documente que no se realizó la proyección con Python.

## Limpieza

1. Guarde todos los cambios en el libro obligatorio:

   ```text
   05_Excel/CIBEST_Apertura_Cuentas_Excepciones_v1.xlsx
   ```

2. Cierre los archivos fuente sin guardar cambios sobre los originales.
3. No elimine los documentos de contexto ni los archivos de `00_Source_Data`.
4. Si creó archivos temporales, borradores o exportaciones no requeridas, elimínelos o muévalos fuera de la carpeta del lote según la política de la organización.
5. Confirme que OneDrive muestra el estado de sincronización completada.
6. Cierre Excel, Word y las sesiones de navegador que ya no necesite.

## Resumen

En este laboratorio preparó y analizó datos de apertura de cuentas de CIBEST CAPITAL usando tablas estructuradas, Copilot en Excel, fórmulas, tablas dinámicas, gráficos y una proyección opcional con Python in Excel. También relacionó los resultados con el procedimiento de vinculación de clientes y con decisiones documentadas en la reunión de lanzamiento del servicio digital.

El resultado principal es un análisis trazable que permite priorizar controles, identificar capacidad operativa requerida y establecer un seguimiento de excepciones. Los hallazgos deben utilizarse como apoyo a la toma de decisiones, manteniendo revisión humana, validación de métricas y una clara separación entre datos, contexto, hipótesis y recomendaciones.

### Recursos de continuidad

| Artefacto | Próximo uso recomendado |
|---|---|
| `05_Excel/CIBEST_Apertura_Cuentas_Excepciones_v1.xlsx` | Fuente para comunicaciones ejecutivas, seguimiento operativo y presentaciones |
| `03_Word/CIBEST_Proceso_Vinculacion_Clientes_v1.docx` | Referencia para controles, responsables y cumplimiento |
| `04_Meetings/CIBEST_Lanzamiento_Servicio_Digital_Notas.docx` | Evidencia de decisiones, acciones y responsables |
| `02_PowerPoint/CIBEST_Portafolios_Modelo_v1.pptx` | Posible destino para incorporar la recomendación ejecutiva y el análisis de riesgos |

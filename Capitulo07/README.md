# Análisis preliminar del crecimiento de los ETFs activos como oportunidad de conversación comercial (CIBEST CAPITAL)

## Metadatos

| Elemento | Valor |
|---|---|
| Duración | 28 minutos |
| Complejidad | Media |
| Nivel de Bloom | Aplicar |
| Organización del caso | CIBEST CAPITAL |
| Zona horaria aplicable | America/Bogota (UTC-05:00) |
| Producto principal | Página de Copilot titulada `07_Analisis_preliminar_ETFs_activos_CIBEST_CAPITAL` |

## Descripción General

En este laboratorio continuará el caso de CIBEST CAPITAL a partir del archivo documental generado en el Laboratorio 06-00-01. Usará Microsoft 365 Copilot Chat en modo **Trabajo**, Copilot Search, Prompt Coach y, si está disponible, un agente autorizado para identificar información interna relevante y construir un análisis preliminar sobre el crecimiento de los ETFs activos.

El resultado no será una recomendación de inversión ni asesoramiento financiero. Será una base controlada para preparar una posible conversación comercial futura, separando de forma explícita los hechos documentados, las fuentes externas, las hipótesis comerciales, los riesgos y los temas que requieren validación por las áreas de Cumplimiento, Productos e Inversiones.

## Objetivos de Aprendizaje

Al finalizar el laboratorio, podrá:

- [ ] Consultar información organizacional mediante Copilot Chat en modo **Trabajo** y validar sus citas.
- [ ] Encontrar materiales internos relevantes con Copilot Search usando consultas contextuales.
- [ ] Referenciar el archivo `06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx` sin mezclar el proceso documental con asesoramiento financiero.
- [ ] Refinar una indicación con Prompt Coach para solicitar un análisis comercial responsable sobre ETFs activos.
- [ ] Crear una Página de Copilot reutilizable con fuentes, limitaciones, preguntas de descubrimiento y acciones siguientes.

## Prerrequisitos

### Conocimientos requeridos

Antes de comenzar, debe comprender:

- La diferencia entre **datos de trabajo**, contenido aportado directamente en una conversación y **datos públicos de la web**.
- Que Copilot responde únicamente con la información a la que el usuario tiene permisos de acceso y que una respuesta debe validarse en sus fuentes.
- La diferencia entre información de mercado, hipótesis comerciales, asesoramiento financiero, recomendación de inversión y evaluación de idoneidad.
- La necesidad de mantener separación entre una solicitud documental de apertura de cuenta y una futura conversación comercial.
- El uso básico de OneDrive para el trabajo o la escuela, Copilot Chat y Microsoft 365.

### Accesos requeridos

Confirme antes de iniciar:

- Finalización del Laboratorio 06-00-01.
- Acceso a Microsoft 365 Copilot Chat con el modo **Trabajo** habilitado.
- Acceso a OneDrive - CIBEST CAPITAL.
- Acceso a Copilot Search y Páginas de Copilot.
- Permisos para consultar el archivo `06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx`.
- Acceso a agentes aprobados por el tenant, si existen.
- Acceso web en Copilot Chat, únicamente si está habilitado por la política corporativa.

> **Importante:** Si una capacidad no está disponible en su tenant —por ejemplo, búsqueda web, Prompt Coach o un agente— no intente usar cuentas personales ni copiar información corporativa fuera de Microsoft 365. Siga la ruta alternativa indicada en cada paso.

## Entorno de Laboratorio

### Estructura obligatoria de OneDrive

Toda la actividad del curso debe conservarse bajo la siguiente carpeta raíz:

```text
OneDrive - CIBEST CAPITAL/Copilot_Labs/Batch_01/
```

La estructura esperada es:

```text
Copilot_Labs/
└── Batch_01/
    ├── 00_Source_Data/
    ├── 02_PowerPoint/
    ├── 03_Word/
    ├── 04_Meetings/
    ├── 05_Excel/
    └── 99_Submissions/
```

El archivo de continuidad del Laboratorio 06-00-01 debe estar disponible en la ubicación definida por el instructor, normalmente dentro de `00_Source_Data`:

```text
OneDrive - CIBEST CAPITAL/Copilot_Labs/Batch_01/00_Source_Data/
└── 06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx
```

No cambie el nombre del archivo de continuidad ni lo mueva a una ubicación personal.

### Hardware recomendado

| Componente | Requisito recomendado |
|---|---|
| Sistema operativo | Windows 11 Pro o Enterprise de 64 bits |
| Procesador | Intel Core i5 de 11.ª generación o equivalente |
| Memoria | 8 GB de RAM como mínimo |
| Pantalla | Resolución mínima de 1920 × 1080 |
| Conectividad | 20–25 Mbps de descarga y 5 Mbps de carga |
| Audio | Auriculares con micrófono opcionales |
| Pantalla secundaria | Recomendada para validar fuentes mientras se edita la Página de Copilot |

### Software y servicios

| Componente | Uso en este laboratorio |
|---|---|
| Microsoft 365 Copilot Chat | Análisis, consultas de trabajo y generación de borradores |
| Copilot Search | Localización de materiales internos |
| Prompt Coach | Mejora de la indicación comercial |
| Agentes autorizados | Investigación especializada, si están disponibles |
| Páginas de Copilot | Conservación estructurada del análisis |
| OneDrive para el trabajo o la escuela | Acceso al archivo de continuidad |
| Microsoft Edge | Navegación recomendada hacia Microsoft 365 Copilot |

### Preparación inicial

1. Abra Microsoft Edge e inicie sesión con su cuenta profesional de CIBEST CAPITAL.
2. Abra OneDrive para el trabajo o la escuela.
3. Navegue a:

   ```text
   OneDrive - CIBEST CAPITAL/Copilot_Labs/Batch_01/00_Source_Data/
   ```

4. Localice el archivo:

   ```text
   06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx
   ```

5. Ábralo y confirme que contiene el resumen de la solicitud documental pendiente de apertura de cuenta.
6. Mantenga el archivo abierto en una pestaña o copie su vínculo de OneDrive mediante **Compartir** > **Copiar vínculo**, respetando los permisos existentes.
7. Abra Microsoft 365 Copilot Chat en otra pestaña.

> **Control de seguridad:** No copie información documental sensible en servicios no autorizados. Al utilizar el archivo como contexto, use la referencia o el adjunto dentro del entorno corporativo de Microsoft 365.

## Instrucciones Paso a Paso

### Paso 1: Confirmar el modo Trabajo y definir el alcance de la conversación

**Objetivo:** Iniciar una conversación fundamentada en datos de trabajo y establecer los límites comerciales, regulatorios y documentales del análisis.

**Instrucciones:**

1. En Microsoft 365 Copilot Chat, seleccione **Nuevo chat**.
2. Verifique el modo de respuesta disponible.
3. Seleccione **Trabajo** o la opción equivalente que indique que Copilot usará información organizacional a la que usted tiene acceso.
4. Si la interfaz muestra un indicador de protección de datos empresariales, confirme que está activo.
5. Escriba la siguiente indicación inicial:

   ```text
   Actúa como asistente de investigación comercial interna para CIBEST CAPITAL.

   Trabaja únicamente con información organizacional a la que tengo acceso. Necesito preparar un análisis preliminar para una posible conversación comercial futura sobre ETFs activos.

   No proporciones asesoramiento financiero, recomendaciones de inversión, evaluación de idoneidad ni instrucciones para completar, aprobar o modificar una apertura de cuenta.

   Primero, indícame qué tipo de fuentes internas serían apropiadas para investigar:
   1. tendencias de productos de inversión aprobadas;
   2. perfiles institucionales o segmentos comerciales autorizados;
   3. guías de conversación comercial;
   4. políticas de cumplimiento aplicables a comunicaciones comerciales.

   Devuelve una tabla con: tipo de fuente, propósito, ejemplo de términos de búsqueda y limitación de uso.
   ```

6. Revise si la respuesta incluye referencias, vínculos o citas a datos de trabajo.
7. No trate una lista de fuentes sugeridas como evidencia. Úsela únicamente para orientar la búsqueda posterior.

**Resultado esperado:**

Copilot genera una tabla que diferencia las fuentes internas útiles para preparar una conversación comercial de los documentos operativos de apertura de cuenta. La respuesta debe incluir limitaciones explícitas, como la necesidad de validar contenidos con Cumplimiento y Productos.

**Verificación:**

- El modo **Trabajo** está seleccionado.
- La respuesta no presenta recomendaciones de inversión.
- La respuesta distingue entre material comercial, políticas internas, información operativa y aprobación regulatoria.
- Si se muestran citas, puede abrir al menos una para comprobar que corresponde a un recurso al que tiene acceso.

---

### Paso 2: Localizar fuentes internas con Copilot Search

**Objetivo:** Encontrar materiales internos de práctica relacionados con productos de inversión, tendencias de mercado aprobadas y guías comerciales.

**Instrucciones:**

1. Abra **Copilot Search** desde Microsoft 365 Copilot, desde la experiencia de búsqueda disponible o desde el punto de acceso indicado por el instructor.
2. Realice la siguiente búsqueda contextual:

   ```text
   Encuentra materiales internos de CIBEST CAPITAL relacionados con ETFs activos, productos de inversión, tendencias de mercado aprobadas o guías de conversación comercial para clientes institucionales. Prioriza documentos publicados o actualizados durante los últimos 24 meses. Muestra el título, propietario o área responsable, fecha, ubicación y una breve explicación de su relevancia.
   ```

3. Revise los resultados recuperados.
4. Abra los documentos más relevantes, si están disponibles, y valide manualmente:
   - título;
   - fecha de creación o modificación;
   - área responsable;
   - propósito del documento;
   - vigencia aparente;
   - restricciones o avisos de cumplimiento.
5. Identifique entre uno y tres recursos internos pertinentes. Ejemplos posibles:
   - guía de conversación comercial aprobada;
   - presentación de tendencias de productos;
   - documento de segmentación institucional;
   - política de comunicaciones comerciales;
   - material de capacitación interna sobre ETFs.
6. Copie los vínculos o anote los títulos exactos de las fuentes validadas.
7. Si la búsqueda no devuelve recursos específicos sobre ETFs activos, amplíe la búsqueda con términos relacionados:

   ```text
   productos de inversión gestión activa guía comercial cumplimiento comunicación con clientes institucionales
   ```

8. Registre las fuentes encontradas para agregarlas después a la Página de Copilot.

**Resultado esperado:**

Se identifican fuentes internas accesibles y verificables, o se documenta claramente que no se encontraron fuentes internas específicas sobre ETFs activos.

**Verificación:**

- Ha revisado las fuentes originales, no solo el resumen de Copilot Search.
- Cada fuente seleccionada tiene un título, fecha o ubicación identificable.
- Puede explicar por qué cada recurso es relevante.
- Si no hay fuentes, ha anotado la limitación: “No se localizaron materiales internos específicos en el alcance de permisos actual”.

> **Buena práctica:** No infiera que un documento es oficial únicamente porque aparece en resultados de búsqueda. Confirme su propietario, fecha y contexto antes de citarlo.

---

### Paso 3: Incorporar el archivo de continuidad del Laboratorio 06-00-01

**Objetivo:** Usar el resumen documental anterior como contexto controlado para identificar aspectos que podrían orientar una conversación futura, sin usarlo para recomendar productos ni alterar el proceso de apertura.

**Instrucciones:**

1. Regrese a Copilot Chat en modo **Trabajo**.
2. Adjunte el archivo `06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx` mediante el selector de archivos de Copilot o inserte el vínculo corporativo si esa es la opción permitida.
3. Confirme visualmente que el archivo se muestra como contexto adjunto o referenciado.
4. Envíe la siguiente indicación:

   ```text
   Usa exclusivamente el archivo adjunto o referenciado 06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx como fuente para este análisis.

   Identifica aspectos documentados que podrían ser relevantes para preparar una conversación comercial futura después de que el proceso operativo correspondiente esté gestionado por el equipo responsable.

   Organiza la respuesta en tres secciones:
   A. Datos documentados en el archivo.
   B. Posibles temas de descubrimiento comercial derivados de esos datos, marcados claramente como inferencias.
   C. Información ausente que no debe suponerse.

   Restricciones:
   - No recomiendes ETFs, fondos, estrategias ni productos.
   - No realices evaluación de idoneidad.
   - No sugieras que la conversación comercial sustituye requisitos documentales, controles KYC, AML, cumplimiento o aprobaciones.
   - No inventes datos del cliente.
   - Incluye una cita o referencia al archivo para cada dato documentado relevante.
   ```

5. Revise la sección **A. Datos documentados** y compare cada afirmación con el archivo original.
6. Revise la sección **B. Inferencias**. Confirme que usa expresiones condicionales, por ejemplo:
   - “Podría explorarse…”
   - “Sería necesario confirmar…”
   - “No debe asumirse…”
7. Si Copilot mezcla un dato documentado con una inferencia, solicite una corrección:

   ```text
   Revisa tu respuesta. Separa cada afirmación en una de estas etiquetas: [Dato documentado], [Inferencia comercial] o [Información no disponible]. Elimina cualquier afirmación que no pueda sustentarse en el archivo.
   ```

**Resultado esperado:**

Una respuesta estructurada que distingue de manera clara los hechos del archivo, las inferencias comerciales permitidas y la información que sigue siendo desconocida.

**Verificación:**

- El archivo del Laboratorio 06-00-01 aparece como fuente adjunta o citada.
- Todos los hechos relevantes pueden verificarse en el documento original.
- Las inferencias no se presentan como datos.
- No hay recomendaciones, lenguaje de inversión personalizado ni modificación del flujo documental.

---

### Paso 4: Mejorar la indicación con Prompt Coach

**Objetivo:** Refinar una indicación para obtener un análisis preliminar más preciso, verificable y apropiado para una conversación comercial.

**Instrucciones:**

1. Redacte la siguiente indicación base en Copilot Chat, pero no la envíe todavía si la interfaz permite usar Prompt Coach antes del envío:

   ```text
   Analiza el crecimiento de los ETFs activos y dime cómo hablar de ello con este cliente.
   ```

2. Abra **Prompt Coach**, **Entrenador de indicaciones** o la función equivalente disponible en su tenant.
3. Solicite que mejore la indicación considerando:
   - audiencia: equipo comercial y responsables internos de CIBEST CAPITAL;
   - fuentes: datos de trabajo validados y, si está permitido, fuentes públicas;
   - alcance: análisis preliminar de oportunidad de conversación;
   - formato: resumen ejecutivo, tendencias, preguntas, riesgos, supuestos y validaciones;
   - restricciones: no asesoramiento financiero ni recomendación de inversión.
4. Revise la propuesta de Prompt Coach. Acepte únicamente elementos consistentes con el caso.
5. Ajuste la indicación refinada para que incluya el siguiente contenido mínimo:

   ```text
   Prepara un análisis preliminar para uso interno de CIBEST CAPITAL sobre el crecimiento de los ETFs activos como posible tema de conversación comercial.

   Usa las fuentes internas validadas que he identificado y separa claramente:
   1. hechos internos documentados;
   2. hechos externos con fuente, vínculo y fecha;
   3. hipótesis comerciales;
   4. preguntas de descubrimiento;
   5. riesgos y limitaciones;
   6. temas que requieren validación de Cumplimiento, Productos e Inversiones.

   Contexto: el archivo 06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx solo puede utilizarse para identificar datos documentados y temas de descubrimiento. No debe utilizarse para recomendar productos, evaluar idoneidad ni modificar el proceso de apertura de cuenta.

   Redacta para revisión interna en tono ejecutivo. No presentes ninguna afirmación como asesoramiento financiero ni como recomendación de inversión.
   ```

6. Guarde la versión refinada en el chat o cópiela temporalmente en un bloc de notas corporativo para reutilizarla en el paso siguiente.

**Resultado esperado:**

Una indicación contextualizada que define propósito, audiencia, fuentes, formato, límites y validaciones requeridas.

**Verificación:**

Compruebe que la indicación responde a estas preguntas:

| Pregunta de calidad | Debe estar presente |
|---|---|
| ¿Qué se necesita? | Análisis preliminar sobre ETFs activos |
| ¿Para quién? | Uso interno del equipo comercial y responsables de CIBEST CAPITAL |
| ¿Con qué fuentes? | Fuentes internas validadas y fuentes web, si están permitidas |
| ¿Qué formato debe tener? | Secciones explícitas y diferenciadas |
| ¿Qué no debe hacer Copilot? | Asesoramiento, recomendación, idoneidad o cambios documentales |
| ¿Quién debe validar? | Cumplimiento, Productos e Inversiones |

---

### Paso 5: Obtener y validar el análisis preliminar sobre ETFs activos

**Objetivo:** Elaborar un análisis fundamentado que distinga fuentes internas, información externa, hipótesis y asuntos pendientes de validación.

**Instrucciones:**

1. En Copilot Chat, mantenga el modo **Trabajo** para la parte interna.
2. Si hay un agente autorizado apropiado —por ejemplo, un agente de Productos, Cumplimiento, Investigación de Mercado o Comunicaciones Comerciales— selecciónelo.
3. Antes de usar el agente, revise su nombre, propósito y alcance. No use un agente cuya función no sea clara.
4. Envíe la indicación refinada del paso anterior.
5. Si utiliza un agente, agregue esta línea al inicio:

   ```text
   Usa únicamente las fuentes y funciones autorizadas para tu alcance. Indica cualquier limitación de cobertura, fecha o acceso.
   ```

6. Revise la respuesta y clasifique cada sección:
   - **Hechos internos documentados:** deben tener fuente interna verificable.
   - **Hechos externos:** deben incluir fuente, vínculo y fecha, si se usó web.
   - **Hipótesis comerciales:** deben indicar que requieren validación.
   - **Preguntas de descubrimiento:** deben ser neutrales y no prescriptivas.
   - **Riesgos y limitaciones:** deben incluir cumplimiento, precisión, actualidad y segmentación.
   - **Validaciones requeridas:** deben asignarse a Cumplimiento, Productos e Inversiones cuando corresponda.
7. Solicite una versión más controlada con esta indicación de seguimiento:

   ```text
   Revisa el análisis anterior y genera una tabla de control de afirmaciones con estas columnas:
   - Afirmación
   - Clasificación: hecho interno, hecho externo, hipótesis comercial, pregunta de descubrimiento o limitación
   - Fuente o evidencia
   - Fecha de la fuente, si aplica
   - Responsable de validación
   - ¿Puede utilizarse en una conversación externa sin revisión adicional? Sí/No

   Marca “No” de forma predeterminada para cualquier afirmación relacionada con productos, rendimiento, riesgos de inversión, regulación o comunicaciones comerciales.
   ```

8. Revise particularmente las afirmaciones sobre crecimiento, activos bajo gestión, flujos, desempeño o adopción de ETFs activos. Estas afirmaciones deben tener evidencia actual, fuente identificable y fecha.
9. Si un dato no tiene fuente clara, elimínelo del resultado o márquelo como pendiente de validación.

**Resultado esperado:**

Un análisis preliminar con estructura ejecutiva y una tabla de control que permite diferenciar información utilizable como contexto interno de información que necesita revisión especializada.

**Verificación:**

- Las hipótesis no se presentan como hechos.
- Las afirmaciones sobre mercado tienen fuente y fecha, o se marcan como pendientes.
- Las preguntas de descubrimiento no incluyen recomendaciones de productos.
- Existe una lista explícita de validaciones para Cumplimiento, Productos e Inversiones.
- La respuesta contiene una advertencia o restricción de uso interno.

---

### Paso 6: Ampliar con fuentes públicas, si la política lo permite

**Objetivo:** Complementar el análisis con información pública reciente, separándola de la información interna y verificando manualmente las fuentes.

**Instrucciones:**

1. Determine si Copilot Chat permite seleccionar **Web**, **Trabajo y Web** o una capacidad equivalente autorizada.
2. Si la búsqueda web no está habilitada, omita este paso y documente la limitación en la Página de Copilot.
3. Si la búsqueda web está habilitada, cree un nuevo bloque de conversación o ajuste el modo según la interfaz.
4. Envíe esta indicación:

   ```text
   Usa únicamente fuentes públicas y confiables para investigar tendencias recientes de crecimiento de ETFs activos.

   Prioriza fuentes primarias u oficiales, tales como reguladores, bolsas, asociaciones sectoriales reconocidas, proveedores de índices, administradores de activos que publiquen datos metodológicos o informes de mercado con fecha identificable.

   Para cada afirmación, proporciona:
   - fuente;
   - vínculo;
   - fecha de publicación;
   - fecha de consulta;
   - resumen de máximo 40 palabras;
   - limitación o posible sesgo de la fuente.

   Limita el resultado a información de mercado general. No proporciones asesoramiento financiero, recomendaciones de inversión ni previsiones sobre productos específicos.
   ```

5. Abra manualmente al menos dos vínculos proporcionados por Copilot.
6. Para cada fuente seleccionada, confirme:
   - que el vínculo abre una fuente real y pertinente;
   - que la fecha de publicación es visible o identificable;
   - que la afirmación de Copilot coincide con el contenido de la fuente;
   - que el contenido no se interpreta como una recomendación de inversión.
7. Si una fuente no puede verificarse, no la incluya como hecho en el entregable final.
8. Solicite a Copilot una separación final entre fuentes:

   ```text
   Presenta los resultados en dos apartados independientes:
   1. Información interna de CIBEST CAPITAL, con sus referencias internas.
   2. Información pública externa, con vínculo y fecha.

   Añade un tercer apartado llamado “Hipótesis y preguntas pendientes”. No combines afirmaciones internas y externas en una misma viñeta.
   ```

**Resultado esperado:**

Un conjunto reducido de fuentes públicas verificadas que aporta contexto de mercado sin confundirlo con información interna ni con una recomendación.

**Verificación:**

- Hay al menos dos fuentes externas verificadas manualmente, si la web está habilitada.
- Cada fuente externa tiene vínculo y fecha.
- Las fuentes externas están separadas de las fuentes internas.
- No se incluyen afirmaciones no verificables como hechos.
- Si la web no estaba disponible, se ha registrado esa limitación.

---

### Paso 7: Crear la Página de Copilot reutilizable

**Objetivo:** Consolidar el análisis, las fuentes, las limitaciones y las acciones siguientes en una Página de Copilot disponible para laboratorios posteriores.

**Instrucciones:**

1. En la respuesta final validada, seleccione **Editar en Páginas**, **Agregar a una página**, **Crear página de Copilot** o la opción equivalente disponible.
2. Cree una nueva Página de Copilot.
3. Asigne exactamente el siguiente título:

   ```text
   07_Analisis_preliminar_ETFs_activos_CIBEST_CAPITAL
   ```

4. Organice el contenido con la siguiente estructura:

   ```markdown
   # 07_Analisis_preliminar_ETFs_activos_CIBEST_CAPITAL

   ## Propósito y límite de uso
   ## Referencia de continuidad del Laboratorio 06-00-01
   ## Resumen ejecutivo
   ## Fuentes internas validadas
   ## Fuentes externas verificadas
   ## Tendencias preliminares sobre ETFs activos
   ## Preguntas de descubrimiento comercial sugeridas
   ## Riesgos, supuestos y limitaciones
   ## Validaciones requeridas
   ## Acciones siguientes
   ```

5. En **Propósito y límite de uso**, incluya un texto equivalente al siguiente:

   > Este análisis es un material preliminar para uso interno de CIBEST CAPITAL. No constituye asesoramiento financiero, recomendación de inversión, evaluación de idoneidad ni aprobación de comunicaciones externas. Cualquier uso comercial externo requiere la revisión aplicable de Cumplimiento, Productos e Inversiones.

6. En **Referencia de continuidad del Laboratorio 06-00-01**, agregue:

   ```text
   Archivo de referencia: 06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx
   Ubicación: OneDrive - CIBEST CAPITAL/Copilot_Labs/Batch_01/00_Source_Data/
   Uso permitido en este análisis: identificación de datos documentados y preparación de preguntas de descubrimiento.
   Uso no permitido: recomendación de productos, evaluación de idoneidad, decisiones de inversión o modificación del proceso documental.
   ```

7. En **Resumen ejecutivo**, incluya entre tres y cinco viñetas con:
   - el contexto general de mercado validado;
   - la oportunidad de conversación, expresada como hipótesis;
   - la necesidad de no vincular la conversación con la resolución del proceso documental;
   - la necesidad de validaciones internas.
8. En **Fuentes internas validadas**, agregue los títulos, vínculos, fechas y responsables de los documentos revisados en el Paso 2.
9. En **Fuentes externas verificadas**, incluya únicamente las fuentes web que haya abierto y validado manualmente. Si la web no estaba habilitada, escriba:

   ```text
   No se incorporaron fuentes públicas en este laboratorio porque la búsqueda web no estaba habilitada o no estaba autorizada para este ejercicio.
   ```

10. En **Preguntas de descubrimiento comercial sugeridas**, incluya entre cuatro y seis preguntas neutrales. Puede utilizar ejemplos como:

   - “¿Qué objetivos institucionales o de gestión de portafolio considera prioritarios para los próximos períodos?”
   - “¿Qué criterios utiliza actualmente para evaluar vehículos de inversión gestionados de forma activa o pasiva?”
   - “¿Qué necesidades de transparencia, liquidez, gobierno o reporte son relevantes para su organización?”
   - “¿Qué áreas internas participan en la evaluación de nuevos vehículos o soluciones de inversión?”
   - “¿Qué documentación o validaciones necesitaría antes de considerar una conversación más detallada con especialistas?”
   - “¿Hay restricciones de política, mandato o cumplimiento que debamos conocer antes de preparar material informativo?”

11. En **Riesgos, supuestos y limitaciones**, incluya al menos:
   - acceso limitado a fuentes internas según permisos;
   - posible desactualización de documentos o datos de mercado;
   - necesidad de validar afirmaciones de productos y mercado;
   - prohibición de usar el análisis como recomendación;
   - separación entre proceso documental y conversación comercial;
   - necesidad de proteger datos sensibles del cliente.
12. En **Validaciones requeridas**, cree una tabla similar a la siguiente:

   | Tema | Área responsable | Validación requerida |
   |---|---|---|
   | Mensajes externos sobre ETFs activos | Cumplimiento | Aprobación de lenguaje y divulgaciones |
   | Información de productos | Productos | Vigencia, características y público objetivo |
   | Datos de mercado y tendencias | Inversiones o Investigación | Exactitud, metodología, fuente y fecha |
   | Datos del cliente | Equipo responsable de la cuenta | Confirmación documental y permiso de uso |
   | Apertura de cuenta pendiente | Operaciones y Cumplimiento | Gestión independiente del proceso comercial |

13. En **Acciones siguientes**, agregue acciones concretas, por ejemplo:
   - validar materiales internos con el propietario del contenido;
   - solicitar revisión de Cumplimiento antes de crear comunicaciones externas;
   - confirmar con Productos e Inversiones las afirmaciones de mercado;
   - preparar una agenda de descubrimiento sin recomendaciones;
   - conservar la Página de Copilot como insumo para los laboratorios posteriores.
14. Revise que la página se guarde en el espacio de Copilot permitido por la organización o se vincule con OneDrive según la configuración del tenant.
15. Copie el vínculo de la Página de Copilot y guárdelo en la ubicación indicada por el instructor, si se solicita una entrega.

**Resultado esperado:**

Una Página de Copilot titulada `07_Analisis_preliminar_ETFs_activos_CIBEST_CAPITAL`, estructurada, reutilizable y con límites de uso claramente definidos.

**Verificación:**

- El título coincide exactamente con el requerido.
- La página referencia el archivo del Laboratorio 06-00-01.
- Las fuentes internas y externas están separadas.
- Las preguntas comerciales son neutrales y no recomiendan productos.
- Las limitaciones y validaciones requeridas aparecen de forma visible.
- La Página de Copilot se abre correctamente desde su vínculo.

## Validación y Pruebas

Complete la siguiente lista de control antes de finalizar el laboratorio.

| Prueba | Criterio de aprobación |
|---|---|
| Modo de Copilot | Se utilizó modo **Trabajo** para consultar información organizacional. |
| Archivo de continuidad | Se referenció o adjuntó `06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx`. |
| Separación de información | Los datos documentados, inferencias y vacíos de información están diferenciados. |
| Copilot Search | Se realizó una búsqueda contextual de materiales internos y se validó al menos una fuente o se documentó su ausencia. |
| Prompt Coach | La indicación fue refinada para incluir objetivo, fuentes, restricciones y formato. |
| Agente | Si se usó un agente, se revisó su alcance y se conservaron sus limitaciones. |
| Fuentes web | Si estaban habilitadas, se verificaron manualmente al menos dos fuentes externas. |
| Cumplimiento | El análisis indica que requiere revisión de Cumplimiento, Productos e Inversiones antes de uso externo. |
| Página de Copilot | Existe una página con el título exacto requerido y se puede abrir mediante su vínculo. |
| Lenguaje comercial | No hay recomendaciones de inversión, evaluación de idoneidad ni promesas de rendimiento. |

Realice una revisión final del contenido para detectar expresiones que deban eliminarse o reformularse:

| Expresión no permitida | Reformulación apropiada |
|---|---|
| “El cliente debería invertir en…” | “Podría explorarse si existe interés, sujeto a validación y revisión especializada.” |
| “Los ETFs activos ofrecen mejores resultados.” | “Las fuentes externas describen tendencias; el desempeño depende de múltiples factores y requiere validación.” |
| “Este cliente es adecuado para…” | “La idoneidad no ha sido evaluada y debe ser tratada por los procesos autorizados.” |
| “Cuando complete los documentos, ofrézcale…” | “La gestión documental y una posible conversación comercial futura son procesos separados.” |
| “El mercado crecerá sin duda…” | “La fuente X describe una tendencia observada a fecha Y; no constituye una previsión garantizada.” |

## Solución de Problemas

### Problema 1: Copilot Chat no muestra el modo Trabajo, no encuentra datos internos o no permite adjuntar el archivo

**Síntomas:** Solo aparece una experiencia pública o personal; no se muestran citas a documentos de trabajo; el archivo de OneDrive no aparece en el selector de archivos; Copilot indica que no puede acceder al documento.

**Causa:** La sesión puede haberse iniciado con una cuenta incorrecta, el usuario puede no tener permisos sobre el archivo o el tenant puede no tener habilitado el modo Trabajo para su licencia o grupo de seguridad.

**Solución:**

1. Cierre sesión y confirme que inicia sesión con la cuenta profesional de CIBEST CAPITAL.
2. Abra el archivo directamente desde OneDrive y compruebe que puede visualizar su contenido.
3. Solicite al instructor o propietario del archivo acceso de lectura si recibe un mensaje de permisos insuficientes.
4. Vuelva a abrir Copilot Chat desde el portal corporativo de Microsoft 365.
5. Si el modo Trabajo sigue sin estar disponible, documente la limitación y use únicamente el contenido autorizado que pueda aportar manualmente, sin copiar datos sensibles fuera del entorno aprobado.

### Problema 2: Las respuestas sobre ETFs activos no incluyen fuentes verificables, mezclan hipótesis con hechos o parecen recomendaciones

**Síntomas:** Copilot presenta cifras sin fecha o vínculo; combina información interna y externa en una sola afirmación; utiliza lenguaje como “debería invertir”, “es adecuado” o “mejor opción”.

**Causa:** La indicación no especificó con suficiente precisión el tipo de fundamento requerido, el alcance comercial o las restricciones regulatorias. También puede haber datos de mercado desactualizados o fuentes web no verificables.

**Solución:**

1. Solicite una tabla de control de afirmaciones con fuente, fecha, clasificación y responsable de validación.
2. Pida a Copilot que etiquete cada elemento como hecho interno, hecho externo, hipótesis, pregunta o limitación.
3. Elimine cualquier afirmación que no tenga evidencia verificable.
4. Reformule el lenguaje prescriptivo como pregunta de descubrimiento o hipótesis sujeta a validación.
5. Abra manualmente los vínculos externos y conserve solo las fuentes que pueda comprobar.
6. Marque el contenido relacionado con productos, rendimiento, riesgo o comunicaciones externas como pendiente de revisión por Cumplimiento, Productos e Inversiones.

## Limpieza

1. Cierre las pestañas de documentos que ya no necesite, especialmente si trabaja en un equipo compartido.
2. No elimine ni modifique el archivo:

   ```text
   06_Resumen_solicitud_documental_CIBEST_CAPITAL.docx
   ```

3. Confirme que la Página de Copilot se guardó con el título requerido:

   ```text
   07_Analisis_preliminar_ETFs_activos_CIBEST_CAPITAL
   ```

4. Si creó borradores temporales o archivos descargados localmente con información del ejercicio, elimínelos de acuerdo con la política corporativa de CIBEST CAPITAL.
5. Mantenga las fuentes, vínculos y la Página de Copilot disponibles para los laboratorios posteriores.
6. Cierre sesión de Microsoft 365 si utiliza un equipo de formación compartido.

## Resumen

En este laboratorio utilizó Copilot Chat en modo Trabajo para investigar información organizacional disponible, localizar recursos mediante Copilot Search y analizar el archivo de continuidad del Laboratorio 06-00-01 con una separación explícita entre datos documentados e inferencias.

También refinó una indicación mediante Prompt Coach, evaluó la posibilidad de usar un agente autorizado y, cuando fue permitido, incorporó fuentes públicas verificadas sobre ETFs activos. El resultado final fue una Página de Copilot reutilizable que conserva el análisis preliminar, las fuentes, las preguntas de descubrimiento, los riesgos, las limitaciones y las acciones de validación requeridas.

> **Principio clave:** Copilot acelera la investigación y la estructuración de contenido, pero la revisión humana sigue siendo obligatoria. Ningún resultado de este laboratorio debe utilizarse como asesoramiento financiero, recomendación de inversión, evaluación de idoneidad ni comunicación externa sin las validaciones corporativas aplicables.

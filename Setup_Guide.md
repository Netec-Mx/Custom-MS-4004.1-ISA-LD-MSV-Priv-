# SETUP GUIDE — Productividad estratégica para directivos con Microsoft 365 Copilot y agentes de IA

[Inicio](README.md)

## Descripción del entorno

Las prácticas emplean **Microsoft 365 Copilot empresarial**, Investigador, Analista y seis agentes basados en plantillas de **Agent Builder**, además de Word, Excel, PowerPoint, Outlook, Teams, OneDrive, SharePoint y Loop. No se requieren conocimientos de programación ni Copilot Studio.

La creación y publicación de agentes especializados **no forma parte de las actividades del participante**: deben encontrarse preparados antes de iniciar la sesión. La **única práctica de creación de agentes es la 12**.

Los materiales son documentos de trabajo destinados a los escenarios del curso. No deben confundirse con información oficial de proyectos en operación ni circularse como comunicaciones institucionales.

## Requisitos de hardware y software

| Elemento | Requisito |
| --- | --- |
| Equipo | Windows o macOS con navegador compatible, conexión estable a Internet y espacio para descargar los 13 recursos de entrada |
| Navegador | Microsoft Edge o Chrome actualizado |
| Suite | Microsoft 365 Copilot, Word, Excel, PowerPoint, Outlook, Teams, OneDrive, SharePoint y Loop disponibles para la organización |
| Accesos | Cuenta corporativa con Microsoft 365 Copilot, permisos de lectura sobre las fuentes y creación de agentes para la práctica 12 |
| Licencia | El temario la denomina «Microsoft 365 Copilot Premium»; TI debe comprobar que la licencia efectivamente asignada habilite cada función y agente requerido |

Accesos: [Microsoft 365 Copilot](https://m365.cloud.microsoft/), [OneDrive](https://onedrive.office.com/), [Outlook](https://outlook.office.com/), [Teams](https://teams.microsoft.com/).

## Licencias, cuentas, agentes y permisos

| Práctica | Herramienta | Verificación indispensable antes del curso |
| --- | --- | --- |
| 1 | Investigador (Researcher) | Disponible y capaz de recuperar fuentes web citables |
| 2 | Analista (Analyst) | Disponible y capaz de leer un libro Excel y generar visualizaciones |
| 3 | Entrenador de ideas (Idea Coach) | Agente habilitado, publicado y compartido con el grupo |
| 4 | Copilot, Outlook, Teams y Facilitator | Reunión futura en calendario, contenido de diferentes canales y configuración de Facilitator accesible |
| 5 | Copilot, Teams, Facilitator y Loop | **Reunión previa finalizada con notas nativas de Facilitator en Loop**, visible para participantes, y transcripciones accesibles |
| 6 | Project Delta Digest | Agente publicado con acceso a la carpeta/sitio de Conecta+ |
| 7 | Resumen personal de noticias (Personal News Digest) | Agente publicado con acceso a las fuentes de comunicaciones |
| 8 | Agente de informe ejecutivo (Executive Briefing Agent) | Agente publicado y con acceso a los expedientes Word y PDF de PMS |
| 9 | Diseñador de comunicaciones (Corporate Communications Crafter) | Agente publicado con la guía de comunicaciones y el resumen de Conecta+ |
| 10 | Asistente de información sobre clientes (Customer Insight Assistant) | Agente publicado con el expediente de Río Sereno |
| 11 | Copilot en PowerPoint | Opción para crear presentación desde archivo Word habilitada |
| 12 | Agent Builder | Creación de agente, edición de instrucciones, conocimiento y panel de prueba habilitados |

**Importante:** Investigador y Analista son agentes de Microsoft 365 Copilot; los seis restantes indicados como especializados (Idea Coach, Project Delta Digest, Personal News Digest, Executive Briefing Agent, Corporate Communications Crafter y Customer Insight Assistant) corresponden a **plantillas de Agent Builder**. Tener disponible una plantilla no equivale a disponer del agente listo para usar; la configuración y el acceso al material correspondiente deben prepararse antes de la clase.

Documentación del fabricante: [plantillas oficiales](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-templates-overview), [cómo crear agentes con Agent Builder](https://support.microsoft.com/en-us/microsoft-365-copilot/build-your-own-agent-with-microsoft-365-copilot), [Preparar reuniones con Copilot](https://support.microsoft.com/en-us/outlook/prepare-for-your-meeting-with-copilot) y [Facilitator en Teams](https://support.microsoft.com/es-es/teams/copilot/facilitator-in-microsoft-teams-meetings).

## Preparación

### 1. Archivos de trabajo y rutas

1. Descargar y extraer el ZIP del curso, conservando el árbol `Capitulo01/Practica01/...` hasta `Capitulo04/Practica12/...`.
2. Abrir OneDrive corporativo y crear `Laboratorio_Copilot_ISA`, con las subcarpetas `Entregables` y `Practica01` a `Practica12`.
3. Para cada práctica, cargar el contenido de `CapituloNN/PracticaNN/recursos/` en su carpeta `PracticaNN` de OneDrive. **No hay archivo de entrada para la práctica 11**; utilizará los entregables creados en las prácticas 6, 9 y 10.
4. Confirmar que cada archivo se puede abrir con la cuenta del participante y elegirlo desde Copilot mediante **Adjuntar/Agregar contenido** o el selector `/` donde esté disponible. La forma de adjuntar varía según el agente y la experiencia de Microsoft 365.
5. En los agentes basados en plantillas, configurar **Conocimiento** o accesos a las bibliotecas con los recursos de su práctica. Verificar que el agente cite la sección correspondiente. No incorporar fuentes empresariales ajenas al caso.

**Archivos requeridos por práctica:**

| Práctica | Archivos de entrada | Uso |
| --- | --- | --- |
| 1 | `Escenario_Confiabilidad_Transmision.docx` | Criterios y restricciones para Researcher |
| 2 | `Portafolio_Inversiones_2026.xlsx` | 18 iniciativas, ejecución trimestral y diccionario de indicadores |
| 3 | `Propuesta_Modernizacion_Activos.docx` | Supuestos a evaluar con Idea Coach |
| 4 | `Dossier_Comite_PMS.docx` | Agenda, acta, solicitud, avance y contenido base de correos y chat |
| 5 | `Historial_Reuniones_PMS_ConectaMas.docx` | Transcripciones y contenido base de la nota; **no sustituye la página nativa de Loop** |
| 6 | `Estado_ConectaMas_Consolidado.docx` | Comparativo de semanas 43/45, cronograma y riesgos |
| 7 | `Panorama_Senales_Organizacionales.docx` | Cinco comunicaciones con asuntos diferenciados |
| 8 | `Dossier_Gestion_PMS.docx` y `Informes_Financieros_y_Riesgos_PMS.pdf` | Antecedentes operativos, resultados, finanzas y riesgos, en Word y PDF |
| 9 | `Dossier_Comunicaciones_ConectaMas.docx` | Contexto y lineamientos de las dos audiencias |
| 10 | `Expediente_Cliente_Rio_Sereno.docx` | Ficha, acta, correos e historial completo de solicitudes |
| 11 | Ninguno | Reutiliza tres entregables previos |
| 12 | `Lineamientos_y_Criterios_Solicitudes.docx` y `Casos_Prueba_Solicitudes.docx` | **Solo el primero se carga como conocimiento**; el segundo se utiliza al probar el agente |

### 2. Crear las fuentes reales de Copilot para las prácticas 4 y 5

La preparación multifuente requiere objetos de Microsoft 365 que **no se crean al cargar un Word**. Se necesita la intervención de personas autorizadas para programar una reunión, publicar mensajes y habilitar Facilitator antes de iniciar el curso.

**Práctica 4 — comité futuro, no iniciar una reunión:**

1. En Outlook/Teams, crear la reunión futura `Comité Directivo - Seguimiento PMS`, agregar como descripción la sección **Agenda del comité próximo** de `Dossier_Comite_PMS.docx`, invitar a los participantes y verificar que la cuenta que revisará Facilitator sea organizadora o coorganizadora.
2. Cargar el dossier a OneDrive/SharePoint y compartirlo con los asistentes de la reunión.
3. Utilizar la sección **Comunicaciones para Outlook y Teams** del dossier para publicar desde cuentas de formación, dentro del tenant, los tres correos `PMS - causas del retraso`, `RE: PMS - causas del retraso` y `Validación sobrecosto PMS`. Conservar las diferencias entre versiones de los responsables.
4. Crear el chat de Teams `Seguimiento PMS` e incorporar los tres mensajes indicados en el dossier. Las comunicaciones deben estar disponibles para los participantes antes de la práctica.
5. Abrir el evento en el calendario y comprobar la disponibilidad de **Preparar para esta reunión**. En las opciones de reunión, verificar **Copilot y Facilitator** cuando estén permitidos por la directiva, **sin iniciar la reunión**.

**Práctica 5 — reunión ya finalizada con notas nativas de Facilitator:**

1. Preparar **antes de la clase** una reunión de Teams de seguimiento del comité, con Facilitator habilitado y una conversación sobre los acuerdos de la sección del **22 de octubre** de `Historial_Reuniones_PMS_ConectaMas.docx`.
2. Terminar la reunión, abrir el chat de la reunión y comprobar la existencia de la página de notas de Loop generada por Facilitator, mediante **Resumen > Notas**. Compartir la reunión/notas con el grupo cuando los permisos lo permitan.
3. Cargar y compartir `Historial_Reuniones_PMS_ConectaMas.docx` para ofrecer las transcripciones de **10-sep, 08-oct y 15-oct** y contrastarlas con la página de Loop.
4. Comprobar con una cuenta de participante que la página de Loop y el documento pueden ser consultados por Copilot. **Si solo se dispone del DOCX, la parte de uso de notas nativas de Facilitator queda pendiente** y no debe reportarse como ejecutada.

### 3. Preparar agentes especializados para las prácticas 6 a 10

1. Crear/publicar previamente los agentes basados en las plantillas correspondientes con **Agent Builder**, asignarles nombres del temario y permitir su uso al grupo del curso. Solo la práctica 12 crea su agente durante la sesión.
2. Para **Project Delta Digest (P6)**, configurar el documento `Estado_ConectaMas_Consolidado.docx` en una biblioteca de SharePoint o fuente que consulte el agente; verificar ambas actualizaciones semanales.
3. Para **Personal News Digest (P7)**, publicar las cinco secciones de `Panorama_Senales_Organizacionales.docx` en una biblioteca de comunicaciones accesible y configurar el agente para consultar el dossier. Si la búsqueda web está deshabilitada, limitarse a los mensajes internos sin inventar noticias externas.
4. Para **Executive Briefing Agent (P8)**, habilitar `Dossier_Gestion_PMS.docx` y `Informes_Financieros_y_Riesgos_PMS.pdf` y comprobar que puede identificar las diferencias entre reportes.
5. Para **Corporate Communications Crafter (P9)**, vincular `Dossier_Comunicaciones_ConectaMas.docx` y, si la plataforma lo permite, el documento resultante de P6 al terminar esa práctica.
6. Para **Customer Insight Assistant (P10)**, vincular `Expediente_Cliente_Rio_Sereno.docx` y confirmar que las consultas solo usan datos del expediente, sin acceder a sistemas de clientes en producción.
7. Para **P12**, mantener `Casos_Prueba_Solicitudes.docx` **fuera del conocimiento** del agente; el participante copiará solo el caso A o B en cada prueba.

### 4. Verificación funcional antes de comenzar

- Iniciar sesión con una cuenta equivalente a la del participante y abrir Investigador, Analista y los seis agentes correspondientes al temario.
- Comprobar que Analista identifica las **18 iniciativas** del Excel, sin tratar las columnas de avance como importes monetarios.
- Confirmar que el comité está programado y que **Preparar para esta reunión** tiene acceso a un correo, al chat y al dossier; la disponibilidad de información depende de permisos e indexación.
- Confirmar que existe una reunión terminada con **notas nativas de Facilitator en Loop** accesibles en Teams y que Copilot puede consultar las tres transcripciones por sesión.
- Consultar con Project Delta Digest el avance de Conecta+ por semanas; solicitar al agente de informe ejecutivo información tanto del PDF como del Word.
- Comprobar que Outlook permite guardar **Borradores** sin envío y que PowerPoint dispone de **Copilot** para trabajar a partir de un documento.
- Abrir Agent Builder, verificar **Configurar**, **Conocimiento** y **Prueba**.

## Consideraciones de ejecución

La duración total de las 12 prácticas es **230 minutos**. Los tiempos presuponen cuentas, agentes, reuniones, permisos, documentos y canales ya preparados; la carga e indexación iniciales quedan fuera de la sesión de cuatro horas.

Los agentes pueden formular preguntas de aclaración y presentar resultados variables. Revisar citas y cifras contra las fuentes, distinguir hechos de hipótesis y mantener los correos de la práctica 9 **sin enviar**. No confirmar que una función está habilitada si no aparece en el entorno.

Referencias: [Microsoft Learn — Agent Builder](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents), [plantillas de agentes](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-templates-overview), [Facilitator en Teams](https://support.microsoft.com/es-es/teams/copilot/facilitator-in-microsoft-teams-meetings), [preparación de reuniones](https://support.microsoft.com/en-us/outlook/prepare-for-your-meeting-with-copilot) y [Copilot en PowerPoint](https://support.microsoft.com/es-es/powerpoint/copilot/create-a-new-presentation-with-copilot-in-powerpoint).

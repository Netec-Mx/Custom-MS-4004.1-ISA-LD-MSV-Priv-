# Setup Guide General

## Productividad estratégica para directivos con Microsoft 365 Copilot y agentes de IA

| Control documental | Información |
|---|---|
| Clave del curso | Custom MS-4004.1 ISA LD MSV (Priv) |
| Versión del documento | 1.0 |
| Estado | BORRADOR: revisión documental completa; pendiente de validación funcional en el tenant de ISA INTERCOLOMBIA |
| Instructor responsable | Por asignar por Netec |
| Fecha de elaboración | 2026-11-06 |
| Fecha de última validación | 2026-11-06 (revisión del repositorio) |
| Repositorio de laboratorios | Se registra al publicar en GitHub |
| Rama y revisión analizada | `main`, versión inicial 1.0 |
| Alcance revisado | 4 capítulos (uno por módulo), 12 prácticas, 39 archivos de recursos, 25 imágenes, README principal y Setup Guide |
| Modalidad del entorno | Cloud (servicios SaaS de Microsoft 365) con aplicaciones de escritorio opcionales |

[Inicio](README.md)

# Objetivo

Preparar, para cada participante, un entorno de Microsoft 365 con licencia de Microsoft 365 Copilot, acceso a los agentes preconstruidos y especializados del curso, permiso para crear agentes con Agent Builder, una reunión de Teams con Facilitator disponible y los materiales ficticios del curso cargados en OneDrive, SharePoint, Outlook, Teams y Loop. El entorno se considera listo cuando todas las validaciones obligatorias de la sección [Validación del Entorno](#validacion-entorno) se aprueban con una cuenta equivalente a la de un participante.

# Requisitos de Hardware

| Recurso | Mínimo requerido | Recomendado | Observaciones |
|---|---|---|---|
| Procesador y arquitectura | Procesador de 64 bits, 2 núcleos, 1.6 GHz | 4 núcleos o más | Requisito de Microsoft 365 Apps |
| Memoria RAM | 8 GB | 16 GB | Varias aplicaciones y pestañas abiertas simultáneamente |
| Espacio libre | 4 GB | 10 GB | Microsoft 365 Apps, Teams y carpeta sincronizada de OneDrive (los recursos ocupan menos de 1 MB) |
| Pantalla | 1366 x 768 | 1920 x 1080 o dos monitores | Un monitor para las instrucciones y otro para Copilot facilita el ritmo de la práctica |
| Conectividad | 10 Mbps por participante | 25 Mbps por participante | Todas las prácticas requieren conexión permanente a Microsoft 365 |
| Audio | No obligatorio | Diadema con micrófono | Solo si el curso se imparte en línea por Teams |

# Sistemas Operativos Compatibles

| Sistema operativo | Edición y versión | Arquitectura | Condición de soporte o validación |
|---|---|---|---|
| Windows 11 | Pro o Enterprise, 23H2 o posterior | x64 | Plataforma base del curso. Compatible según fabricante; validar en el tenant |
| macOS | 14 Sonoma o posterior | Apple silicon o Intel | Compatible según fabricante; no validado para este curso |

Las prácticas se ejecutan en el navegador (aplicación Microsoft 365 Copilot, Outlook web, Teams web) y en Microsoft 365 Apps de escritorio. La plataforma base es Windows 11 con Microsoft Edge. En macOS los nombres de menú de las aplicaciones de escritorio pueden variar. Windows 10 no se recomienda porque su soporte general finalizó en octubre de 2025.

# Software Requerido

| Componente | Edición y versión requerida | Arquitectura | Obligatorio u opcional | Fuente oficial |
|---|---|---|---|---|
| Microsoft Edge | Versión estable vigente | x64 | Obligatorio (o Google Chrome vigente) | [microsoft.com/edge](https://www.microsoft.com/es-es/edge) |
| Aplicación Microsoft 365 Copilot (web) | Servicio administrado | N/A | Obligatorio | [m365.cloud.microsoft](https://m365.cloud.microsoft/) |
| Microsoft 365 Apps para empresas (Word, Excel, PowerPoint, Outlook) | Canal Actual o Canal mensual para empresas, con Copilot habilitado | x64 | Obligatorio para las prácticas 1 a 12 (Word y Excel), 9 (Outlook) y 11 (PowerPoint); pueden usarse las versiones web | [Requisitos de Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/plan/microsoft-copilot-requirements) |
| Microsoft Teams | Nuevo Teams de escritorio o Teams web | x64 | Obligatorio (prácticas 4 y 5) | [teams.microsoft.com](https://teams.microsoft.com/) |
| OneDrive para el trabajo o la escuela | Cliente de sincronización vigente | x64 | Obligatorio (versión web) / opcional (cliente de sincronización) | Incluido en Microsoft 365 |
| Microsoft Loop | Servicio administrado | N/A | Obligatorio (práctica 5) | Incluido en Microsoft 365 |

Los servicios de Microsoft 365 son administrados y no tienen versión fijable. Registrar en el [Registro de validación](#registro-validacion) la fecha de prueba y los nombres de los agentes tal como aparecen en el tenant.

# Herramientas y Dependencias

## Paquetes, frameworks y componentes adicionales

| Dependencia | Versión o restricción | Componente que la necesita | Método de instalación o habilitación |
|---|---|---|---|
| Agente Investigador (Researcher) | Servicio administrado | Práctica 1 | Disponible con la licencia de Microsoft 365 Copilot; verificar en Agentes |
| Agente Analista (Analyst) | Servicio administrado | Práctica 2 | Disponible con la licencia de Microsoft 365 Copilot; verificar en Agentes |
| Entrenador de ideas (Idea Coach) | Servicio administrado | Práctica 3 | Centro de administración de Microsoft 365 > Agentes; asignar al grupo del curso |
| Facilitator en reuniones de Teams | Servicio administrado | Prácticas 4 y 5 | Directiva de reuniones de Teams con transcripción habilitada ([documentación](https://learn.microsoft.com/es-es/microsoftteams/facilitator-teams)) |
| Project Delta Digest | Servicio administrado | Práctica 6 | Centro de administración de Microsoft 365 > Agentes; asignar al grupo del curso |
| Resumen personal de noticias | Servicio administrado | Práctica 7 | Centro de administración de Microsoft 365 > Agentes; asignar al grupo del curso |
| Agente de informe ejecutivo | Servicio administrado | Práctica 8 | Centro de administración de Microsoft 365 > Agentes; asignar al grupo del curso |
| Diseñador de comunicaciones | Servicio administrado | Práctica 9 | Centro de administración de Microsoft 365 > Agentes; asignar al grupo del curso |
| Asistente de información sobre clientes | Servicio administrado | Práctica 10 | Centro de administración de Microsoft 365 > Agentes; asignar al grupo del curso; verificar si requiere conexión a un CRM |
| Agent Builder | Servicio administrado | Práctica 12 | Configuración de Copilot: permitir la creación de agentes al grupo del curso ([documentación](https://learn.microsoft.com/es-es/microsoft-365/copilot/extensibility/agent-builder)) |
| Copilot en PowerPoint y en Outlook | Microsoft 365 Apps con Copilot | Prácticas 9 y 11 | Incluido en Microsoft 365 Apps con licencia de Copilot |
| Materiales ficticios del curso | Versión 1.0 de este repositorio | Prácticas 1 a 12 | Subcarpetas `CapituloNN/PracticaNN/recursos/` de este repositorio |

Los nombres de los agentes en español corresponden al temario. En el tenant pueden aparecer con su nombre en inglés. La disponibilidad de cada agente depende de la región, del programa de lanzamiento y de la configuración del tenant, por lo que debe confirmarse con la [validación V-03](#validacion-entorno).

## Licencias, cuentas y permisos

| Recurso o servicio | Licencia o suscripción | Cuenta o rol requerido | Permiso mínimo | Responsable de habilitación |
|---|---|---|---|---|
| Microsoft 365 | Microsoft 365 E3/E5 o Business Standard/Premium | Cuenta corporativa del participante | Usuario | Administrador de TI de ISA INTERCOLOMBIA |
| Microsoft 365 Copilot | Licencia de Microsoft 365 Copilot (el temario la denomina "Premium") | Cuenta corporativa del participante | Licencia asignada | Administrador de licencias |
| Agentes del curso | Incluidos o habilitados según el tenant | Grupo de seguridad del curso | Agentes asignados al grupo | Administrador de IA o Administrador global |
| Agent Builder | Licencia de Microsoft 365 Copilot | Grupo de seguridad del curso | Creación de agentes permitida | Administrador de IA o Administrador global |
| Reuniones de Teams con Facilitator | Licencia de Microsoft 365 Copilot | Participante como coorganizador de la reunión del curso | Transcripción y Copilot permitidos por directiva | Administrador de Teams |
| Sitio de SharePoint `Conecta+ (Laboratorio)` | Incluido en Microsoft 365 | Participantes como miembros | Lectura | Administrador de SharePoint o instructor |
| Cuentas de laboratorio para sembrar datos | Microsoft 365 con buzón | 3 cuentas: `lab.gerente.pms`, `lab.abastecimiento`, `lab.finanzas` (nombres sugeridos) | Enviar correo y chatear en Teams | Administrador de TI |

Las credenciales se entregan por el canal autorizado por ISA INTERCOLOMBIA. No registrar contraseñas, códigos MFA ni tokens en este repositorio ni en los entregables.

# Instalación y Configuración

## 1. Obtener los materiales

- Repositorio o paquete autorizado: este repositorio de GitHub (botón **Code > Download ZIP**).
- Revisión que se utilizará: rama `main`, versión 1.0.
- Directorio de trabajo local: `C:\Cursos\MS-4004.1-ISA\` (Windows).
- Archivos de entrada: subcarpetas `Capitulo01/Practica01/recursos/` a `Capitulo04/Practica12/recursos/`.

Los archivos de `recursos` se distribuyen. Los entregables los crean los participantes durante el curso en `Laboratorio_Copilot_ISA/Entregables/`.

## 2. Instalar o habilitar los componentes

### Licencias y agentes (administrador)

1. Crear el grupo de seguridad `Curso-Copilot-Directivos` con los participantes y el instructor.
2. Asignar la licencia de Microsoft 365 Copilot a los miembros del grupo.
3. En el [Centro de administración de Microsoft 365](https://admin.microsoft.com/), abrir **Agentes** (o **Copilot > Agentes**), localizar cada agente de la tabla de dependencias y asignarlo al grupo `Curso-Copilot-Directivos`. Consultar [Administrar agentes en el centro de administración](https://learn.microsoft.com/es-es/microsoft-agent-365/admin/manage-copilot-agents-integrated-apps).
4. En la configuración de Copilot, permitir la creación de agentes con Agent Builder para el grupo del curso.
5. Esperar la propagación de la configuración (puede tardar hasta 24 horas).

**Plataforma y terminal:** navegador web, Centro de administración de Microsoft 365.

**Resultado esperado:** con una cuenta de participante, la sección **Agentes** de la aplicación Microsoft 365 Copilot muestra los ocho agentes del curso y la opción **Crear agente**.

### Directiva de reuniones de Teams (administrador de Teams)

1. En el [Centro de administración de Teams](https://admin.teams.microsoft.com/), abrir **Reuniones > Directivas de reunión**.
2. En la directiva asignada a los participantes, en **Grabación y transcripción**, habilitar la **Transcripción**.
3. Verificar que Copilot en reuniones esté habilitado y que Facilitator esté permitido según la [documentación de Facilitator](https://learn.microsoft.com/es-es/microsoftteams/facilitator-teams).

**Resultado esperado:** en las **Opciones de reunión** de un evento, el participante ve la configuración de Copilot y Facilitator.

### Estructura de carpetas en OneDrive (cada participante o instructor)

1. Instalar o iniciar el cliente de sincronización de OneDrive con la cuenta del participante.
2. Descomprimir el ZIP del repositorio en `C:\Cursos\MS-4004.1-ISA\`.
3. Ejecutar el siguiente script para crear la estructura y copiar los recursos a la carpeta sincronizada.

**Plataforma y terminal:** Windows 11, PowerShell 5.1 o posterior.

```powershell
$repo = "C:\Cursos\MS-4004.1-ISA"
$dest = Join-Path $env:OneDriveCommercial "Laboratorio_Copilot_ISA"
New-Item -ItemType Directory -Force -Path (Join-Path $dest "Entregables") | Out-Null
1..12 | ForEach-Object {
    $prac = "Practica{0:D2}" -f $_
    $cap = "Capitulo{0:D2}" -f ([int][math]::Floor(($_ - 1) / 3) + 1)
    $target = Join-Path $dest $prac
    New-Item -ItemType Directory -Force -Path $target | Out-Null
    Copy-Item -Path (Join-Path $repo "$cap\$prac\recursos\*") -Destination $target -Force
}
Get-ChildItem $dest -Recurse -File | Measure-Object | Select-Object Count
```

**Resultado esperado:** `Count` igual a **39** y, en OneDrive web, la carpeta `Laboratorio_Copilot_ISA` con `Practica01` a `Practica12` y `Entregables`. Si `$env:OneDriveCommercial` está vacío, el cliente de OneDrive no ha iniciado sesión con la cuenta corporativa.

Sin cliente de sincronización: crear las carpetas en OneDrive web y cargar el contenido de cada `CapituloNN/PracticaNN/recursos/` con **Cargar > Archivos**.

## 3. Preparar archivos de configuración

| Archivo | Ruta completa o relativa a la raíz definida | Configuración necesaria | Origen |
|---|---|---|---|
| Recursos ficticios por práctica | `OneDrive/Laboratorio_Copilot_ISA/PracticaNN/` | Ninguna; cargar sin modificar nombres | Incluido en repositorio |
| Correos, chat y reunión del comité | Buzones y Teams | Sembrar según [Preparación previa por práctica](#preparacion-por-practica) | Guion en [Correos_y_Chats_Comite_PMS.docx](Capitulo02/Practica04/recursos/Correos_y_Chats_Comite_PMS.docx) |
| Página de Loop de notas | Espacio de Loop del participante o compartido | Crear la página `Notas Comité de iniciativas 22-oct` | Contenido en [Notas_Facilitator_Comite_2026-10-22.docx](Capitulo02/Practica05/recursos/Notas_Facilitator_Comite_2026-10-22.docx) |
| Biblioteca de Conecta+ | Sitio de SharePoint `Conecta+ (Laboratorio)` | Cargar los archivos de `Capitulo02/Practica06/recursos/` | Incluido en repositorio |

# Variables de Entorno

| Variable | Propósito | Valor o formato esperado | Alcance | Método de configuración |
|---|---|---|---|---|
| `OneDriveCommercial` | Ruta de la carpeta sincronizada de OneDrive corporativo usada por el script de preparación | `C:\Users\<usuario>\OneDrive - <Organización>` | Usuario | La define automáticamente el cliente de OneDrive al iniciar sesión |

**Configuración — Windows 11, PowerShell:** no se requiere configuración manual.

**Verificación sin exponer secretos:**

```powershell
Test-Path $env:OneDriveCommercial
```

Resultado esperado: `True`.

# Configuración Base para los Laboratorios

## Parámetros comunes

| Parámetro | Valor o convención | Observaciones |
|---|---|---|
| Raíz de trabajo | `OneDrive/Laboratorio_Copilot_ISA/` | Una por participante |
| Carpeta de entregables | `OneDrive/Laboratorio_Copilot_ISA/Entregables/` | Las prácticas 9 y 11 reutilizan entregables previos |
| Nomenclatura de entregables | `Nombre_Del_Entregable_[INICIALES].ext` | Ejemplo: `Diagnostico_ConectaMas_LMR.docx` |
| Fecha de corte del escenario | 6 de noviembre de 2026 | Se usa para determinar compromisos vencidos |
| Unidad monetaria | Millones de pesos colombianos (MCOP) | En todos los recursos |
| Idioma de Copilot | Español | Las instrucciones se redactan en español |

## Estructura de carpetas

```text
OneDrive/
└── Laboratorio_Copilot_ISA/
    ├── Practica01/ ... Practica12/   Recursos de cada práctica (copiados del repositorio)
    └── Entregables/                  Archivos que crea el participante
```

## Recursos compartidos

| Recurso | Nombre o identificador | Estructura o configuración base | Responsable de creación |
|---|---|---|---|
| Reunión de Teams | `Comité Directivo - Seguimiento PMS` | Programada entre 1 y 7 días después del curso, con la agenda de [Agenda_Comite_Directivo_PMS.docx](Capitulo02/Practica04/recursos/Agenda_Comite_Directivo_PMS.docx) en la descripción y los participantes como coorganizadores | Instructor |
| Chat grupal de Teams | `Seguimiento PMS` | Participantes y cuentas de laboratorio, con los mensajes del guion | Instructor |
| Página de Loop | `Notas Comité de iniciativas 22-oct` | Contenido del archivo de notas de Facilitator | Instructor |
| Sitio de SharePoint | `Conecta+ (Laboratorio)` | Biblioteca **Documentos** con los archivos de `Capitulo02/Practica06/recursos/`; participantes con permiso de lectura | Administrador de SharePoint o instructor |

Cada participante trabaja en su propio OneDrive, por lo que los entregables no se mezclan. Los recursos compartidos son de solo lectura, excepto la reunión, en la que los participantes son coorganizadores para revisar las opciones de Facilitator.

<a id="preparacion-por-practica"></a>

## Preparación previa por práctica

Completar al menos **48 horas antes** del curso para que Copilot indexe correos, chats y archivos.

| Práctica | Preparación requerida | Verificación |
|---|---|---|
| 1 | Cargar `Escenario_Confiabilidad_Transmision.docx`. Confirmar que Investigador puede consultar la web | Investigador responde una consulta de prueba con citas web |
| 2 | Cargar `Portafolio_Inversiones_2026.xlsx` | Analista lee el archivo y reporta 18 iniciativas |
| 3 | Cargar `Propuesta_Modernizacion_Activos.docx` | Entrenador de ideas resume la propuesta |
| 4 | Enviar los 3 correos del guion desde las cuentas de laboratorio a cada participante; crear el chat `Seguimiento PMS` con los 3 mensajes; programar la reunión del comité; cargar los 4 documentos | Copilot encuentra el correo `PMS - causas del retraso` y la reunión con `/` |
| 5 | Cargar las 3 transcripciones; crear la página de Loop con el contenido de las notas y compartirla con los participantes. Opción alternativa: realizar una reunión breve con Facilitator activo, leyendo el contenido de las notas, para generar notas reales | Copilot encuentra la página de Loop con `/` |
| 6 | Crear el sitio `Conecta+ (Laboratorio)` y cargar los 3 archivos; también están en OneDrive | Project Delta Digest lee el informe de la semana 45 |
| 7 | Cargar las 5 comunicaciones. Opcional: publicarlas como noticias en el sitio de laboratorio | Resumen personal de noticias menciona al menos una comunicación interna |
| 8 | Cargar 3 documentos Word y 2 PDF | El Agente de informe ejecutivo cita un PDF |
| 9 | Cargar los 2 documentos; definir la cuenta de laboratorio que se usará como destinatario de los borradores | Copilot en Outlook está disponible al crear un correo |
| 10 | Cargar los 4 archivos del cliente. Confirmar si el agente requiere conexión a un CRM | El agente resume la ficha del cliente |
| 11 | Cargar los 3 archivos de respaldo | Copilot en PowerPoint muestra la opción de crear a partir de un archivo |
| 12 | Cargar los 5 archivos; confirmar el permiso de Agent Builder | La opción **Crear agente** está disponible |

## Correcciones de coherencia

| Inconsistencia o dependencia omitida | Configuración unificada | Ajuste necesario en las copias de trabajo |
|---|---|---|
| La plantilla de referencia muestra 11 capítulos; el temario define 4 módulos con 12 prácticas | Una carpeta por módulo (`Capitulo01` a `Capitulo04`) y, dentro, una carpeta por práctica (`Practica01` a `Practica12`) con su propio `README.md` | Ninguno |
| La solicitud menciona `SetupGuide.md`; la plantilla y la estructura de referencia usan `Setup_Guide.md` | Se conserva `Setup_Guide.md` | Ninguno |
| El temario indica "Microsoft 365 Copilot Premium" | Se documenta como licencia de Microsoft 365 Copilot | Confirmar con ISA INTERCOLOMBIA el nombre comercial de la licencia asignada |
| El temario requiere notas de Loop generadas por Facilitator y transcripciones previas, que no pueden distribuirse en un repositorio | Se distribuye su contenido en Word para crear la página de Loop o generar una reunión real | Preparación del instructor según la tabla anterior |
| El logotipo de la plantilla se llama `neteclogo (2).png` (con espacio y paréntesis) | Se renombró a `images/neteclogo.png` | Ninguno |
| Los nombres de los agentes pueden mostrarse en inglés en el tenant | Se usa el nombre en español del temario y el nombre en inglés entre paréntesis cuando se conoce | Ninguno |

# Servicios Externos Requeridos

| Servicio | URL, endpoint o región | Uso | Acceso requerido |
|---|---|---|---|
| Aplicación Microsoft 365 Copilot | [m365.cloud.microsoft](https://m365.cloud.microsoft/) | Chat de Copilot, agentes y Agent Builder | Cuenta con licencia de Copilot |
| Microsoft Teams | [teams.microsoft.com](https://teams.microsoft.com/) | Reunión, chat y Facilitator | Cuenta corporativa |
| Outlook | [outlook.office.com](https://outlook.office.com/) | Correos sembrados y borradores | Cuenta con buzón |
| OneDrive y SharePoint | Tenant de ISA INTERCOLOMBIA | Recursos y entregables | Cuenta corporativa |
| Búsqueda web de Copilot | Servicio de Microsoft | Investigador y noticias externas | Búsqueda web permitida por la organización |

## Configuración de red

| Origen | Destino | Protocolo y puerto | Sentido | Condición |
|---|---|---|---|---|
| Equipo del participante | Endpoints de Microsoft 365 | HTTPS 443 | Saliente | Permitidos según la [lista oficial de endpoints](https://learn.microsoft.com/es-es/microsoft-365/enterprise/microsoft-365-endpoints?view=o365-worldwide) |
| Equipo del participante | Endpoints de Microsoft 365 | WebSocket seguro (WSS) sobre 443 | Saliente | Necesario para respuestas en tiempo real de Copilot |
| Equipo del participante | Teams (medios) | UDP 3478-3481 | Saliente | Solo si el curso se imparte en línea |

Si la organización usa proxy con inspección TLS, excluir los dominios de Microsoft 365 según la lista oficial.

# Creación de Entornos / Máquinas Virtuales / Emuladores

El curso no requiere máquinas virtuales, contenedores ni emuladores. El entorno es el tenant de Microsoft 365 de ISA INTERCOLOMBIA.

| Elemento | Tipo o plataforma | Imagen y versión | Recursos asignados | Red o región | Persistencia |
|---|---|---|---|---|---|
| Tenant de laboratorio | Entorno cloud de Microsoft 365 | Servicio administrado | Licencias del grupo `Curso-Copilot-Directivos` | Región del tenant de ISA INTERCOLOMBIA | Los entregables y el agente creado persisten en la cuenta del participante |
| Sitio `Conecta+ (Laboratorio)` | SharePoint Online | Servicio administrado | Biblioteca de documentos | Región del tenant | Eliminar después del curso |

1. Crear el grupo de seguridad y asignar licencias y agentes.
2. Crear el sitio de SharePoint, el chat, la reunión y la página de Loop.
3. Cargar los recursos y esperar 48 horas de indexación.
4. Después del curso: eliminar el sitio de laboratorio, el chat y la reunión, y retirar los agentes de prueba si la política de la organización lo exige.

<a id="validacion-entorno"></a>

# Validación del Entorno

| ID | Componente o capacidad | Procedimiento | Resultado esperado | Evidencia mínima |
|---|---|---|---|---|
| V-01 | Licencia de Copilot | Iniciar sesión en [m365.cloud.microsoft](https://m365.cloud.microsoft/) con una cuenta de participante y abrir Copilot | El chat de Copilot responde con datos de trabajo | Captura del chat |
| V-02 | Acceso a archivos | Escribir `/Portafolio_Inversiones_2026` en el chat | El archivo aparece en la lista de sugerencias | Captura |
| V-03 | Agentes del curso | Abrir **Agentes** y buscar los ocho agentes | Los ocho agentes aparecen y abren una conversación | Lista de agentes con su nombre en el tenant |
| V-04 | Investigador | Ejecutar una consulta corta con fuentes web | Respuesta con citas | Captura |
| V-05 | Analista | Adjuntar el portafolio y pedir el total aprobado | 153.850 MCOP | Captura |
| V-06 | Correo y chat sembrados | Preguntar a Copilot: "¿Qué dice el correo PMS - causas del retraso?" | Resume el correo del Gerente PMS | Captura |
| V-07 | Reunión y Facilitator | Abrir la reunión del comité > Opciones de reunión | Opción de Facilitator visible y modificable | Captura |
| V-08 | Loop | Escribir `/Notas Comité` en Copilot | La página de Loop aparece | Captura |
| V-09 | Copilot en Outlook y PowerPoint | Crear un correo y una presentación en blanco | El icono de Copilot está disponible en ambas aplicaciones | Captura |
| V-10 | Agent Builder | Seleccionar **Crear agente** y abrir la pestaña Configurar | El formulario de configuración se muestra | Captura (sin guardar el agente) |

**Criterio de entorno listo:** las validaciones V-01 a V-10 deben aprobarse con una cuenta de participante. Si un agente no está disponible (V-03), la práctica correspondiente no puede ejecutarse según el temario; documentar el bloqueo y acordar con ISA INTERCOLOMBIA una alternativa antes del curso.

# Comandos de Verificación

## Estructura local de recursos

**Plataforma y terminal:** Windows 11, PowerShell.  
**Directorio de ejecución:** `C:\Cursos\MS-4004.1-ISA\`.  
**Prerrequisito:** ZIP del repositorio descomprimido.

```powershell
Get-ChildItem -Path . -Recurse -File -Include *.docx,*.xlsx,*.pdf | Group-Object { $_.Directory.Parent.Name } | Select-Object Name, Count
```

**Resultado esperado:**

```text
Name        Count
----        -----
Practica01      1
Practica02      1
Practica03      1
Practica04      5
Practica05      4
Practica06      3
Practica07      5
Practica08      5
Practica09      2
Practica10      4
Practica11      3
Practica12      5
```

**Interpretación:** confirma que los 39 recursos están disponibles para cargar. No acredita que Copilot pueda leerlos; para eso se usan V-02 y V-05.

## Servicios de Microsoft 365

Las capacidades de Copilot, los agentes, Facilitator y Agent Builder se validan únicamente en la interfaz web con los procedimientos V-01 a V-10. No se requiere instalar módulos de PowerShell ni SDK para el curso.

# Troubleshooting

| Síntoma | Causa probable | Comprobación | Corrección | Validación posterior |
|---|---|---|---|---|
| Un agente no aparece en **Agentes** | No está asignado al usuario o no está disponible en el tenant | Buscarlo en **Todos los agentes** | Asignarlo al grupo del curso en el Centro de administración y esperar la propagación | V-03 |
| Al escribir `/` no aparece un archivo | El archivo aún no está indexado | Abrir el archivo en OneDrive web | Esperar la indexación (hasta 48 h) o adjuntarlo con el botón **+** | V-02 |
| Investigador tarda más de 10 minutos | Consulta extensa o alta demanda | Revisar el historial de conversaciones | Reabrir la conversación desde el historial; reducir el alcance de la consulta | V-04 |
| Analista no lee el Excel | Formato o tamaño no compatible, o archivo abierto con cambios sin guardar | Abrir el archivo en Excel web | Cerrar el archivo y volver a adjuntarlo | V-05 |
| Copilot no encuentra los correos o el chat | No se sembraron los datos o no están indexados | Buscar el correo en Outlook | Reenviar los correos del guion y esperar la indexación | V-06 |
| No aparece la opción de preparación de la reunión | La función no está disponible en el cliente o versión | Probar en Teams web y en la aplicación Microsoft 365 Copilot | Usar la alternativa descrita en la Práctica 4 (chat de Copilot con `/` y el nombre de la reunión) | V-07 |
| Facilitator no aparece en Opciones de reunión | Directiva de transcripción o Copilot deshabilitada; el participante no es organizador | Revisar la directiva de reuniones del usuario | Habilitar la transcripción y agregar al participante como coorganizador | V-07 |
| **Crear agente** no está disponible | La creación de agentes está restringida | Revisar la configuración de Copilot del grupo | Permitir la creación de agentes al grupo del curso | V-10 |
| Copilot en PowerPoint no ofrece crear a partir de un archivo | Versión de Microsoft 365 Apps desactualizada | Revisar **Archivo > Cuenta > Actualizaciones** | Actualizar Microsoft 365 Apps o usar PowerPoint web | V-09 |
| El borrador de correo se envía por error | Uso de **Enviar** en lugar de guardar | Revisar **Elementos enviados** | Usar solo cuentas de laboratorio como destinatarias; informar al instructor | V-09 |

# Checklist Final

- [ ] Equipos con Windows 11, navegador vigente y Microsoft 365 Apps actualizadas.
- [ ] Licencia de Microsoft 365 Copilot asignada a todos los participantes y al instructor.
- [ ] Ocho agentes del curso asignados al grupo `Curso-Copilot-Directivos` y visibles (V-03).
- [ ] Creación de agentes con Agent Builder permitida (V-10).
- [ ] Directiva de reuniones con transcripción y Facilitator habilitados (V-07).
- [ ] Estructura `Laboratorio_Copilot_ISA` creada con los 39 recursos en cada OneDrive.
- [ ] Correos, chat, reunión, página de Loop y sitio de SharePoint preparados con 48 horas de anticipación.
- [ ] Cuentas de laboratorio disponibles para sembrar datos y recibir borradores.
- [ ] Validaciones V-01 a V-10 completadas con una cuenta de participante.
- [ ] Evidencias y fecha de validación registradas en el registro de validación.

# Resumen

Para iniciar el curso, cada participante necesita una cuenta corporativa con licencia de Microsoft 365 Copilot, acceso a los ocho agentes del temario, permiso para crear agentes con Agent Builder, una reunión de Teams con Facilitator disponible y la carpeta `Laboratorio_Copilot_ISA` en OneDrive con los recursos ficticios de este repositorio. Los datos de correo, chat, Loop y SharePoint deben sembrarse con al menos 48 horas de anticipación.

<a id="registro-validacion"></a>

## Registro de validación

| Fecha | Responsable | Plataforma o entorno probado | Resultado | Limitaciones o acciones pendientes |
|---|---|---|---|---|
| 2026-11-06 | Desarrollo de contenido Netec | Revisión del repositorio: estructura, rutas relativas, imágenes, enlaces externos, recursos y alineación con el temario | APTO para publicación del repositorio | No se ejecutaron las prácticas en el tenant de ISA INTERCOLOMBIA. Pendiente: validaciones V-01 a V-10 con una cuenta de participante |

## Referencias oficiales

| Documento o recurso | URL | Fecha de consulta |
|---|---|---|
| Información general de Microsoft 365 Copilot | https://learn.microsoft.com/es-es/copilot/plan/copilot-overview | 2026-11-06 |
| Requisitos de Microsoft 365 Copilot | https://learn.microsoft.com/es-es/copilot/plan/microsoft-copilot-requirements | 2026-11-06 |
| Opciones de licencia de Copilot | https://learn.microsoft.com/es-es/copilot/plan/copilot-license-options | 2026-11-06 |
| Agente Investigador (Researcher) | https://learn.microsoft.com/es-es/copilot/manage/researcher-agent | 2026-11-06 |
| Agent Builder | https://learn.microsoft.com/es-es/microsoft-365/copilot/extensibility/agent-builder | 2026-11-06 |
| Crear agentes con Agent Builder | https://learn.microsoft.com/es-es/microsoft-365/copilot/extensibility/agent-builder-build-agents | 2026-11-06 |
| Agregar conocimiento a un agente | https://learn.microsoft.com/es-es/microsoft-365/copilot/extensibility/agent-builder-add-knowledge | 2026-11-06 |
| Compartir y administrar agentes | https://learn.microsoft.com/es-es/microsoft-365/copilot/extensibility/agent-builder-share-manage-agents | 2026-11-06 |
| Administrar agentes en el centro de administración | https://learn.microsoft.com/es-es/microsoft-agent-365/admin/manage-copilot-agents-integrated-apps | 2026-11-06 |
| Facilitator en Microsoft Teams | https://learn.microsoft.com/es-es/microsoftteams/facilitator-teams | 2026-11-06 |
| Transcripción de reuniones de Teams | https://learn.microsoft.com/es-es/microsoftteams/meeting-transcription-captions | 2026-11-06 |
| Copilot en Teams y transcripción | https://learn.microsoft.com/es-es/microsoftteams/copilot-teams-transcription | 2026-11-06 |
| Privacidad de datos de Microsoft 365 Copilot | https://learn.microsoft.com/es-es/copilot/plan/microsoft-365-copilot-privacy | 2026-11-06 |
| URL y rangos de direcciones IP de Microsoft 365 | https://learn.microsoft.com/es-es/microsoft-365/enterprise/microsoft-365-endpoints?view=o365-worldwide | 2026-11-06 |

[Inicio](README.md)

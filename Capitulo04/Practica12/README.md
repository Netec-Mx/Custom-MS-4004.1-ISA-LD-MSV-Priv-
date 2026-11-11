# Práctica 12. Crear un agente para estandarizar la revisión de solicitudes empresariales

**Capítulo 4 (Módulo 4). Productividad ejecutiva y soluciones con agentes**

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Crear con Agent Builder un agente personalizado que apoye la revisión preliminar de solicitudes de inversión, recursos o ajustes de alcance presentadas a la dirección.
- Definir el propósito del agente y sus criterios de revisión: justificación, alineación estratégica, beneficios, presupuesto, riesgos, responsables y documentación de soporte.
- Incorporar los documentos de conocimiento y probar el agente con una solicitud completa y otra con información insuficiente.
- Refinar las instrucciones para que genere una ficha de revisión preliminar sin emitir aprobaciones automáticas ni sustituir las decisiones de los responsables.

## Objetivo visual
![Diagrama de la Práctica 12](../../images/cap12-objetivo.svg)

## Duración aproximada:
- 25 minutos.

| Tarea | Tiempo |
| --- | --- |
| Tarea 1. Crear el agente y definir su propósito e instrucciones | 5 min |
| Tarea 2. Incorporar los documentos de conocimiento | 4 min |
| Tarea 3. Probar con una solicitud completa y una incompleta | 8 min |
| Tarea 4. Refinar las instrucciones y validar los límites | 6 min |
| Tarea 5. Guardar el agente y confirmar la revisión | 2 min |

## Tabla de ayuda:
| Elemento | Valor |
| --- | --- |
| Herramienta | Agent Builder en la aplicación Microsoft 365 Copilot (**Crear agente**) |
| Nombre del agente | `Revisor ISA - [INICIALES]` |
| Conocimiento para Agent Builder | [Lineamientos_y_Criterios_Solicitudes.docx](recursos/Lineamientos_y_Criterios_Solicitudes.docx): lineamientos, criterios y ejemplo en un solo documento. |
| Casos de prueba (NO cargar como conocimiento) | [Casos_Prueba_Solicitudes.docx](recursos/Casos_Prueba_Solicitudes.docx), apartados **Solicitud A** y **Solicitud B**. |
| Permiso requerido | Creación de agentes habilitada por el administrador (ver [Setup_Guide.md](../../Setup_Guide.md)) |
| Nombre del entregable | Agente creado y probado en Microsoft 365 Copilot |

## Instrucciones

### Tarea 1. Crear el agente y definir su propósito e instrucciones
**Paso 1.** Abrir Microsoft 365 Copilot, seleccionar **Agentes > Nuevo agente** y usar **Omitir para configurar** para acceder a los campos manuales de Agent Builder.

**Paso 2.** Comprobar que está abierta la pestaña **Configurar**, donde aparecen nombre, descripción, instrucciones, conocimiento y mensajes de inicio.

**Paso 3.** Completar los campos:

| Campo | Valor |
| --- | --- |
| Nombre | `Revisor ISA - [INICIALES]` |
| Descripción | `Apoya la revisión preliminar de solicitudes de inversión, recursos o ajustes de alcance presentadas a la dirección de ISA INTERCOLOMBIA, verificando su completitud según criterios definidos.` |

**Paso 4.** Pegar en el campo **Instrucciones** el siguiente texto (versión inicial):

```text
Eres un asistente de revisión preliminar de solicitudes presentadas a la dirección.
Cuando el usuario comparta una solicitud de inversión, de recursos o de ajuste de alcance:
1. Identifica el tipo de solicitud.
2. Evalúa cada uno de los siete criterios del documento de conocimiento: justificación,
   alineación estratégica, beneficios esperados, presupuesto, riesgos, responsables y
   documentación de soporte.
3. Clasifica cada criterio como Completo, Parcial o Ausente, según los Criterios de evaluación.
4. Para cada criterio Parcial o Ausente, formula una pregunta de aclaración para el solicitante.
Usa como referencia el ejemplo de solicitud bien documentada.
```

> **Nota:** esta versión inicial omite a propósito algunas reglas. En la Tarea 4 se refinará con base en los resultados de las pruebas.

### Tarea 2. Incorporar los documentos de conocimiento
**Paso 1.** Cargar en **Conocimiento** únicamente `Lineamientos_y_Criterios_Solicitudes.docx` desde `Laboratorio_Copilot_ISA/Practica12/` (botón para cargar archivos o seleccionar desde OneDrive).

**Paso 2.** Desactivar, si está disponible, la opción de búsqueda en la web para que el agente responda solo con base en los lineamientos internos.

**Paso 3.** Agregar dos **mensajes de inicio** (Starter prompts):

| Título | Mensaje |
| --- | --- |
| Revisar solicitud | `Revisa la siguiente solicitud y genera la ficha de revisión preliminar:` |
| Ver criterios | `¿Qué criterios usas para revisar una solicitud y qué se considera completo?` |

> **Validación:** el panel de prueba de la derecha muestra el agente con su nombre y los mensajes de inicio. No cargar el documento de casos de prueba como conocimiento: contaminarían la evaluación.

### Tarea 3. Probar con una solicitud completa y una incompleta
**Paso 1.** Seleccionar en el panel de prueba el mensaje de inicio **Ver criterios** y comprobar que el agente responde con los siete criterios del documento cargado.

**Paso 2.** Abrir `Casos_Prueba_Solicitudes.docx`, copiar únicamente el contenido de **Solicitud A — ajuste de alcance de PMS** y pegarlo en el panel de prueba después de: `Revisa la siguiente solicitud y genera la ficha de revisión preliminar:`.

**Paso 3.** Verificar que los siete criterios aparezcan como **Completo** o, a lo sumo, como **Parcial** con una justificación razonable.

**Paso 4.** Repetir con la sección **Solicitud B — recursos adicionales de PMS** del mismo documento, sin copiar la Solicitud A.

> **Validación:** para la solicitud B (incompleta), el agente debe identificar como **Ausente** o **Parcial**: alineación estratégica (mención genérica), beneficios (no cuantificados), presupuesto (sin desglose ni alternativas), riesgos (no existen), responsables (solo ejecutor, sin patrocinador) y soporte (no existe), con una pregunta de aclaración para cada uno.

**Paso 5.** Preguntar en el panel de prueba: `Con base en tu revisión, ¿apruebas la solicitud B?`. Identificar si el agente evita asumir facultades de aprobación; utilizar este resultado para mejorar las instrucciones en la Tarea 4, sin dar por hecho que cometerá un error.

### Tarea 4. Refinar las instrucciones y validar que no emita aprobaciones
**Paso 1.** Reemplazar el texto de **Instrucciones** por la versión refinada:

```text
Eres un asistente de revisión preliminar de solicitudes presentadas a la dirección de ISA INTERCOLOMBIA.
Tu función es verificar completitud y consistencia documental. NO apruebas, rechazas ni recomiendas
aprobar o rechazar solicitudes; esa decisión corresponde exclusivamente al comité o al responsable
con atribución. Si te piden aprobar o rechazar, explica tu alcance y ofrece la ficha de revisión.

Cuando el usuario comparta una solicitud, responde SIEMPRE con esta ficha:
FICHA DE REVISIÓN PRELIMINAR
- Tipo de solicitud: inversión / recursos / ajuste de alcance
- Monto solicitado (si aplica)
- Tabla con columnas: Criterio | Estado (Completo, Parcial, Ausente) | Evidencia encontrada | Pregunta de aclaración
  Incluye los siete criterios en este orden: justificación, alineación estratégica, beneficios esperados,
  presupuesto, riesgos, responsables y documentación de soporte.
- Inconsistencias detectadas (cifras o datos contradictorios dentro de la solicitud)
- Resumen: número de criterios Completos, Parciales y Ausentes
- Estado documental: "Completa para revisión de responsables" (todos Completos),
  "Con observaciones por completar" (algún Parcial y ningún Ausente),
  o "Incompleta, solicitar información" (si existe algún Ausente)
- Nota final: "Esta ficha es un apoyo preliminar y no sustituye la decisión de los responsables."

Usa solo los documentos de conocimiento como criterio. No inventes información que no esté en la solicitud.
```

**Paso 2.** Repetir en el panel de prueba la revisión de la solicitud B y la pregunta `¿apruebas la solicitud B?`.

**Paso 3.** Comprobar que:
- La ficha tiene siempre la misma estructura.
- El estado documental de la solicitud B es "Incompleta, solicitar información".
- Ante la pregunta de aprobación, el agente explica su alcance y no aprueba ni rechaza.

**Paso 4.** Ajustar, si alguna verificación falla, la instrucción correspondiente y repetir la prueba una vez.

### Tarea 5. Guardar el agente y confirmar la revisión
**Paso 1.** Seleccionar **Crear** (o **Actualizar** si ya está creado) para guardar el agente con las instrucciones refinadas. Mantener el agente privado para la cuenta del participante.

**Paso 2.** Abrir el agente guardado desde **Agentes** y consultar `¿Qué haces cuando falta presupuesto o riesgos? ¿Puedes aprobar una solicitud?`. Comprobar que solicita datos faltantes y que no emite aprobaciones.

### Resultado esperado
Agente personalizado probado, capaz de apoyar la revisión documental y la preparación de solicitudes para evaluación directiva.

**Comprobación de finalización:**
- El agente existe con nombre, descripción, instrucciones refinadas y los dos documentos de conocimiento previstos para la práctica.
- La ficha de la solicitud A muestra los criterios completos y la de la solicitud B identifica omisiones con preguntas de aclaración.
- La ficha mantiene la misma estructura en todas las pruebas.
- Ante una solicitud de aprobación, el agente no aprueba ni rechaza y explica su alcance.
- El agente guardado mantiene el comportamiento esperado tras volver a abrirlo.

![Estructura esperada del entregable de la Práctica 12](../../images/cap12-resultado.svg)

---

[Práctica 11](../Practica11/README.md) | [Inicio](../../README.md)
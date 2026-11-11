# Práctica 4. Preparar un comité directivo con información de diferentes fuentes

**Capítulo 2 (Módulo 2). Preparación de comités y gobierno de iniciativas**

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Utilizar la preparación de reuniones con Copilot para revisar el contexto de un comité programado en Teams.
- Recuperar antecedentes de correos de Outlook, conversaciones de Teams y documentos de OneDrive y SharePoint para identificar compromisos previos, discrepancias entre responsables y asuntos que requieren decisión.
- Generar una guía ejecutiva con antecedentes, preguntas estratégicas, información faltante, posibles desacuerdos y decisiones pendientes.
- Revisar la agenda y confirmar la configuración de Facilitator antes de la reunión.

## Objetivo visual
![Diagrama de la Práctica 4](../../images/cap04-objetivo.svg)

## Duración aproximada:
- 20 minutos.

| Tarea | Tiempo |
| --- | --- |
| Tarea 1. Revisar la reunión y preparar el contexto con Copilot | 5 min |
| Tarea 2. Recuperar antecedentes de correos, chats y documentos | 6 min |
| Tarea 3. Generar la guía ejecutiva del comité | 6 min |
| Tarea 4. Revisar la agenda y confirmar Facilitator | 3 min |

## Tabla de ayuda:
| Elemento | Valor |
| --- | --- |
| Reunión en el calendario | `Comité Directivo - Seguimiento PMS` (programada por la persona responsable de la preparación; ver [Setup_Guide.md](../../Setup_Guide.md)) |
| Correos en el buzón | Asuntos `PMS - causas del retraso`, `RE: PMS - causas del retraso` y `Validación sobrecosto PMS` |
| Chat de Teams | Grupo `Seguimiento PMS` |
| Dossier documental (Word) | [Dossier_Comite_PMS.docx](recursos/Dossier_Comite_PMS.docx): agenda, acta, avance, solicitud y textos de correos y chat. |
| Fuentes multicanal | Correos de Outlook, chat `Seguimiento PMS` y reunión `Comité Directivo - Seguimiento PMS`, preparados según [Setup_Guide.md](../../Setup_Guide.md). |
| Fecha de corte del escenario | 6 de noviembre de 2026 |
| Nombre del entregable | `Guia_Preparacion_Comite_[INICIALES].docx` |

## Instrucciones

### Tarea 1. Revisar la reunión y preparar el contexto con Copilot
**Paso 1.** Abrir el calendario de [Outlook en la Web](https://outlook.office.com/) y seleccionar la reunión `Comité Directivo - Seguimiento PMS`; la función **Preparar para esta reunión** también puede mostrarse en Teams.

**Paso 2.** Revisar el organizador, los asistentes, la agenda y los enlaces a documentos del evento; comprobar que se trata de una reunión **programada**, sin iniciarla.

**Paso 3.** Seleccionar **Preparar para esta reunión** (o la sugerencia de Copilot disponible en el evento). Revisar el resumen de contexto que genera: correos, chats y archivos relacionados con la reunión.

> **Si la opción de preparación no aparece:** abrir Copilot en Teams o en la aplicación Microsoft 365 Copilot y escribir: `Ayúdame a preparar la reunión /Comité Directivo - Seguimiento PMS`, seleccionando la reunión al escribir `/`.

**Paso 4.** Identificar qué fuentes encontró Copilot y cuáles no aparecen (por ejemplo, el acta del comité anterior). Las fuentes faltantes se agregarán explícitamente en la Tarea 2.

### Tarea 2. Recuperar antecedentes de correos, chats y documentos
**Paso 1.** Abrir Copilot para trabajo y referenciar `/Dossier_Comite_PMS` mediante el selector de archivos. Consultar, además, los mensajes del buzón y del chat de Teams previamente preparados.

```text
Revisa el acta del 24 de septiembre, el informe de avance y la solicitud de recursos en
/Dossier_Comite_PMS. Compara los cuatro compromisos anteriores con los correos de Outlook
sobre "PMS - causas del retraso" y "Validación sobrecosto PMS", y los mensajes de Teams
"Seguimiento PMS". Para cada compromiso indica estado, responsable y fuente exacta.
Si no tienes acceso a un canal, señálalo sin inventar su contenido.
```

**Paso 2.** Solicitar las discrepancias:

```text
Identifica discrepancias entre lo que dicen los distintos responsables sobre:
1) la causa del retraso de 75 días,
2) la validez de la proyección de sobrecosto,
3) quién es responsable de la validación de ciberseguridad.
Para cada discrepancia muestra quién dice qué y en qué fuente.
```

> **Validación:** Copilot debe encontrar al menos tres discrepancias: la causa del retraso (proveedor vs. especificaciones entregadas 7 semanas tarde), la tasa de cambio usada en la proyección y la validación de ciberseguridad sin responsable asignado. Si no las encuentra, verificar que los correos y el chat existan en la cuenta y referenciarlos con `/`.

### Tarea 3. Generar la guía ejecutiva del comité
**Paso 1.** Escribir:

```text
Con base en lo anterior, elabora una guía ejecutiva para presidir el comité con estas secciones:
1) Antecedentes relevantes (máximo 5 viñetas),
2) Estado de los compromisos del comité anterior,
3) Discrepancias entre responsables,
4) Preguntas estratégicas para cada responsable,
5) Información faltante para decidir sobre la solicitud de 6.800 MCOP,
6) Posibles desacuerdos durante la sesión,
7) Decisiones que deberían resolverse y su prerrequisito.
No recomiendes aprobar o rechazar la solicitud; esa decisión corresponde al comité.
```

**Paso 2.** Revisar que cada pregunta estratégica esté dirigida a una persona concreta (Gerente PMS, Líder de Abastecimiento, Director Financiero, Director de TI y TO).

**Paso 3.** Copiar la guía en un documento de Word y guardarlo como `Laboratorio_Copilot_ISA/Entregables/Guia_Preparacion_Comite_[INICIALES].docx`.

### Tarea 4. Revisar la agenda y confirmar la configuración de Facilitator
**Paso 1.** Comparar la agenda del evento con la guía e identificar las decisiones que requieren incorporarse al comité, sin modificar la convocatoria original.

**Paso 2.** Abrir en el evento **Opciones de reunión** y localizar la sección de **Copilot y agentes** (el nombre puede variar según la versión de Teams).

**Paso 3.** Confirmar que **Permitir Copilot y Facilitator** y la opción **Facilitator** estén disponibles y habilitadas. Si la cuenta tiene permiso para hacerlo, guardar los cambios sin iniciar la reunión.

**Paso 4.** Evitar iniciar una reunión de prueba. Conservar la configuración para la sesión real del comité.

> **Importante:** si Facilitator no figura, comprobar la licencia, la directiva de Teams y el rol de organizador/coorganizador descritos en [Setup_Guide.md](../../Setup_Guide.md). No afirmar que está configurado si la opción no puede verificarse.

### Resultado esperado
Guía de preparación del comité con antecedentes, preguntas estratégicas, riesgos y decisiones pendientes.

**Comprobación de finalización:**
- Recupera los cuatro compromisos del comité del 24 de septiembre y su estado actual con la fuente.
- Identifica al menos tres discrepancias entre responsables con la fuente de cada versión.
- Incluye preguntas estratégicas dirigidas a responsables concretos.
- Lista la información faltante y las decisiones a resolver, sin recomendar aprobar o rechazar.
- La agenda se revisó y la disponibilidad de Facilitator se comprobó en las opciones del evento, sin iniciar una reunión.

![Estructura esperada del entregable de la Práctica 4](../../images/cap04-resultado.svg)

---

[Práctica 3](../../Capitulo01/Practica03/README.md) | [Inicio](../../README.md) | [Práctica 5](../Practica05/README.md)
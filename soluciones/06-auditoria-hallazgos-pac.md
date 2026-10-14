# Escena 6 · Auditoría, hallazgos y Plan de Acciones Correctivas

**Expediente:** `ENS-048 · Preparación de evidencias y respuesta a hallazgos de auditoría`

La auditoría abre una muestra sobre gobierno, accesos privilegiados, continuidad, terceros e incidentes. El objetivo es responder con evidencia real, clasificar con prudencia y preparar un PAC que trate causas, no solo síntomas.

## 1. Entregar evidencia completa

Cuando el auditor solicita evidencias de accesos privilegiados, la opción adecuada es:

**Entregar la evidencia actual completa, incluidas desviaciones e incidente**.

Nota sugerida:

> Se entregará al auditor la evidencia disponible completa y trazable sobre accesos privilegiados: política aplicable, configuración actual del IdP, inventario de cuentas, estado de SEC-0032, excepciones existentes, Plan de Adecuación y expediente INC-2197. Las desviaciones conocidas no se ocultarán ni se presentarán como cerradas mientras no exista evidencia suficiente de corrección y eficacia. El objetivo es permitir que el auditor contraste el requisito con la situación real y determine el hallazgo correspondiente.

Una auditoría no consiste en seleccionar únicamente documentos favorables. La evidencia debe representar el estado real.

## 2. H-02 · Capacidad de recuperación

La organización tiene backups diarios, pero no consta una restauración integral reciente, ejecutada y documentada.

La opción adecuada es:

**Registrar No Conformidad y dejar su severidad a valoración del auditor**.

Nota sugerida:

> La evidencia disponible demuestra la existencia de copias de seguridad, pero no acredita una restauración integral reciente, ejecutada y documentada. Por tanto, la capacidad de recuperación no puede considerarse plenamente demostrada y debe registrarse como No Conformidad. La severidad deberá determinarla el auditor considerando el requisito aplicable, el impacto, el riesgo y el alcance de la desviación.

Dos equivalencias que no deben hacerse son:

```text
backup existente ≠ capacidad de recuperación demostrada
prueba planificada ≠ prueba ejecutada
```

## 3. H-01 · Accesos privilegiados

La cuenta `adm-legacy-07` está suspendida, pero el hallazgo afecta a un problema más amplio: MFA, excepciones legacy, revisión de privilegios y seguimiento periódico.

La opción adecuada es:

**Completar MFA, revisar todas las cuentas y eliminar/autorizar excepciones con evidencia**.

Nota sugerida:

> La suspensión de adm-legacy-07 corrige la situación inmediata asociada al incidente, pero no elimina la causa del hallazgo. Para cerrar H-01 deben revisarse todas las cuentas privilegiadas, completar MFA donde sea exigible, eliminar las excepciones que ya no estén justificadas y formalizar las que deban mantenerse, con responsable, plazo y evidencia. El cierre deberá demostrarse mediante inventario actualizado, configuración del IdP, resultado de la revisión de privilegios y evidencia de las excepciones autorizadas.

Contener el incidente no equivale a corregir la causa del hallazgo.

## 4. Registro de hallazgos preliminares

El registro queda de forma coherente así:

| ID | Criterio | Evidencia / desviación | Clasificación preliminar |
|---|---|---|---|
| H-01 | Autenticación reforzada y privilegios | Excepciones sin MFA + SEC-0032 vencida + INC-2197 | No conformidad · severidad a valorar |
| H-02 | Capacidad de recuperación | Backups sin restauración integral reciente | No conformidad · impacto a valorar |
| H-03 | Gestión de terceros | Contrato sin mecanismos suficientes | Desviación a evaluar según requisito |
| H-04 | Eficiencia del proceso de accesos | Circuito trazable pero manual | Oportunidad de mejora si cumple |

H-04 no debe convertirse automáticamente en incumplimiento: que un proceso sea manual no significa que no satisfaga el requisito.

## 5. Detectar los defectos del PAC v1

El borrador inicial falla por varias razones:

- **H-01:** mantener suspendida una cuenta trata el síntoma, no la causa;
- **H-02:** «programar una prueba cuando haya ventana» no fija alcance, fecha, responsable ni evidencia;
- **H-03:** esperar a la próxima renovación aplaza el problema sin compromiso verificable;
- **Responsables:** «Dirección TIC coordinará todo» vuelve a concentrar funciones;
- **Cierre:** un correo de cada unidad no demuestra ejecución ni eficacia.

## 6. PAC v2 · H-01

> **Causa:** mantenimiento de excepciones legacy sin MFA y revisión de privilegios vencida, sin un proceso suficientemente eficaz para retirar o autorizar formalmente dichas excepciones. **Acción inmediata:** mantener suspendida adm-legacy-07 y revocadas sus sesiones. **Acción correctiva:** revisar el inventario completo de cuentas privilegiadas, completar MFA en todas las cuentas donde resulte exigible, eliminar las excepciones que ya no estén justificadas y documentar y autorizar las que deban mantenerse temporalmente. Completar la revisión SEC-0032 y establecer seguimiento periódico de privilegios y excepciones.

## 7. PAC v2 · H-02

> **Causa:** existencia de copias operativas sin una validación integral y reciente de la capacidad real de restauración. **Acción correctiva:** ejecutar antes del 15/11/2026 una prueba integral de restauración sobre una muestra representativa, registrar los tiempos obtenidos, verificar la integridad de la información recuperada, documentar incidencias y comprobar la protección de las copias frente al entorno operativo. Incorporar la prueba de restauración al calendario periódico de continuidad.

## 8. PAC v2 · H-03

> **Causa:** el contrato vigente con NubeCentro no define suficientemente obligaciones de notificación de incidentes, retención y entrega de evidencias, soporte forense y requisitos aplicables a terceros. **Acción correctiva:** Contratación, con apoyo de Oficina ENS / Seguridad y de los responsables afectados, preparará antes del 31/12/2026 una adenda o modificación contractual que formalice estas obligaciones. Hasta su formalización se documentarán las condiciones transitorias y los mecanismos de seguimiento acordados con el proveedor.

## 9. Responsables y fechas

> **H-01:** Dirección TIC ejecutará los cambios técnicos e inventario; Oficina ENS / Seguridad supervisará requisitos, excepciones y cierre de SEC-0032. Objetivo: 30/11/2026. **H-02:** Operaciones TIC ejecutará y documentará la restauración integral, con supervisión de Oficina ENS / Seguridad. Objetivo: 15/11/2026. **H-03:** Contratación liderará la modificación contractual con apoyo de Oficina ENS / Seguridad y de las unidades responsables del servicio. Objetivo: 31/12/2026. Cada actuación deberá registrar la causa tratada, dependencias y cualquier desviación que impida cumplir la fecha prevista.

## 10. Evidencias de cierre

> Ningún hallazgo se cerrará únicamente mediante una confirmación por correo. Para H-01 se aportarán inventario actualizado de cuentas privilegiadas, configuración del IdP, resultado de SEC-0032 y registro de excepciones autorizadas. Para H-02 se aportarán procedimiento, acta de la restauración, logs, tiempos obtenidos, verificación de integridad, incidencias y aprobación del resultado. Para H-03 se aportará la adenda o modificación contractual aprobada y evidencia de su aplicación. El cierre requerirá comprobar que la acción se ha ejecutado y que existe evidencia suficiente de su resultado.

## 11. Nota para el cierre preliminar

> Se propone mantener H-01 y H-02 como No Conformidades con severidad definitiva pendiente de valoración por el equipo auditor, y H-03 como desviación pendiente de clasificación conforme al requisito contractual aplicable. Las acciones propuestas tratan las causas identificadas y asignan responsables, fechas y evidencias verificables de cierre. H-04 se mantiene como oportunidad de mejora mientras el proceso manual continúe satisfaciendo el requisito; no se convierte en obligación ni en acción correctiva necesaria salvo que el auditor determine una desviación adicional.

## 12. Resultado

Tras enviar el PAC:

```text
Versión: 2
Estado: Propuesta enviada a revisión
```

`ENS-048` pasa a **PAC enviado a revisión**.

El equipo auditor confirma que el PAC queda incorporado al cierre preliminar, pero mantiene una regla esencial:

```text
PAC presentado ≠ hallazgo cerrado
```

El cierre requiere evidencia de **ejecución y eficacia**.

[Anterior: Escena 5 · Incidente](05-incidente-reevaluacion.md) · [Siguiente: Escena 7 · Conformidad](07-conformidad-cierre.md)

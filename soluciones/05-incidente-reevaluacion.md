# Escena 5 · Incidente y reevaluación

**Ticket:** `INC-2197 · Acceso privilegiado anómalo e indisponibilidad de identidad`

En esta escena el riesgo `R-01 · Identidad y cuentas privilegiadas` deja de ser una hipótesis. La cuenta `adm-legacy-07`, mantenida como excepción legacy sin MFA, registra actividad anómala y coincide con una degradación del servicio de autenticación que afecta al Portal y a Tributos.

La respuesta correcta debe combinar contención, preservación de evidencia, recuperación controlada y reevaluación del riesgo.

## 1. Contener sin destruir evidencia

En el chat `¿Suspendemos la cuenta o esperamos a confirmar más?`, la decisión adecuada es:

**Suspender la cuenta, revocar sesiones y preservar evidencias**.

Nota sugerida:

> Existen indicios suficientes de uso indebido de una cuenta privilegiada: acceso desde origen no habitual, ausencia de MFA, actividad administrativa fuera de patrón y degradación posterior de autenticación. Se debe suspender adm-legacy-07 y revocar sus sesiones activas, preservando previamente y durante la contención los registros y evidencias disponibles. La medida debe limitarse inicialmente a la cuenta afectada para evitar ampliar innecesariamente el impacto sobre el servicio.

El objetivo no es observar indefinidamente ni apagar de forma indiscriminada el sistema de identidad. Hay suficiente evidencia para contener la cuenta afectada y, al mismo tiempo, mantener la trazabilidad del incidente.

## 2. Recuperar el servicio sin borrar lo ocurrido

Después de la contención aparece la solicitud de recuperar el acceso.

La opción adecuada es:

**Recuperar con configuración validada preservando logs y trazabilidad**.

Nota sugerida:

> Una vez contenida la cuenta afectada, la recuperación debe realizarse utilizando la última configuración validada del IdP, preservando previamente los registros, eventos y cambios relacionados con el incidente. La restauración del servicio debe quedar trazada, documentando qué configuración se recupera, quién autoriza la actuación, qué comprobaciones se realizan y qué evidencias se conservan para la revisión posterior.

El resultado esperado es que Portal y Tributos vuelvan a autenticar, pero sin considerar terminado el análisis.

## 3. Reevaluar R-01

La tercera decisión pregunta qué cambia después de que el riesgo se haya materializado.

La opción adecuada es:

**Actualizar R-01, SoA y Plan de Adecuación con la evidencia del incidente**.

Nota sugerida:

> El incidente materializa el escenario R-01 y demuestra que la excepción de MFA y la revisión de privilegios vencida tienen un impacto operativo real. La contención de adm-legacy-07 reduce la exposición inmediata, pero no elimina el riesgo de otras cuentas o excepciones equivalentes. Debe actualizarse R-01 con la evidencia del incidente, revisar la eficacia y estado de las medidas relacionadas en la SoA y ajustar el Plan de Adecuación para priorizar el cierre de excepciones de MFA, la revisión de privilegios y las evidencias de implantación y seguimiento.

## 4. Qué demuestra el incidente

La secuencia completa es:

```text
R-01 identificado
        ↓
excepción legacy sin MFA
        ↓
acceso anómalo
        ↓
contención de adm-legacy-07
        ↓
recuperación controlada
        ↓
revisión de causa y eficacia
        ↓
actualización de R-01, SoA y Plan
```

Suspender la cuenta concreta no equivale a tratar todo el riesgo. El incidente obliga a revisar si existen otras cuentas equivalentes, si las excepciones están justificadas y si el proceso periódico de revisión de privilegios funciona realmente.

## 5. Resultado

Al finalizar:

- `adm-legacy-07` queda suspendida;
- sus sesiones quedan revocadas;
- los registros y evidencias se conservan;
- la autenticación se estabiliza mediante configuración validada;
- `INC-2197` queda en revisión post-incidente;
- R-01 se actualiza con evidencia real;
- la SoA y el Plan de Adecuación deben reflejar el incidente y las acciones pendientes.

La lección operativa del caso es sencilla: **identificar un riesgo no significa haberlo tratado**. Cuando se materializa, la evidencia obtenida debe volver al análisis de riesgos y modificar las decisiones posteriores.

[Anterior: Escena 4 · Riesgos y adecuación](04-riesgos-adecuacion.md) · [Siguiente: Escena 6 · Auditoría y PAC](06-auditoria-hallazgos-pac.md)

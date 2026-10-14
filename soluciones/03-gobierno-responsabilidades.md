# Escena 3 · Gobierno y responsabilidades ENS

**Expediente:** `ENS-021 · Regularización del modelo de responsabilidades ENS`

El problema de partida es que Dirección TIC aparece concentrando demasiadas funciones: decide medidas, opera el sistema y valida su propio cumplimiento. La solución consiste en separar decisiones funcionales, seguridad y operación técnica, y dejar trazabilidad sobre accesos, conflictos y riesgos residuales.

## 1. Separar Seguridad de Sistema

En el chat `Seguridad y Sistema aparecen concentrados en TIC`, la opción adecuada es:

**Separar decisión de Seguridad de la operación del Sistema**.

Una nota válida sería:

> La responsabilidad de Seguridad debe diferenciarse de la responsabilidad operativa sobre el Sistema. Dirección TIC puede mantener la administración técnica y la operación, pero la definición, seguimiento y verificación de las medidas de seguridad debe quedar atribuida a una función diferenciada, con capacidad de supervisión sobre la operación.

La separación puede resumirse así:

```text
Seguridad → determina, coordina y supervisa requisitos de protección
Sistema   → implementa, administra y opera
```

## 2. Resolver el acceso privilegiado del proveedor

En `REQ-1087` el proveedor solicita una cuenta administrativa durante dos semanas.

La decisión coherente es:

**Autorización del Responsable del Sistema + validación de Seguridad + cuenta temporal trazable**.

La justificación puede documentarse así:

> El acceso administrativo del proveedor debe responder a una necesidad operativa justificada y no concederse por simple correo. El Responsable del Sistema debe autorizar el acceso necesario para la operación, Seguridad debe validar las condiciones y restricciones aplicables, y Dirección TIC debe implementar una cuenta individual, temporal, limitada al privilegio necesario, registrada y revocada al finalizar el trabajo.

El circuito resultante es:

```text
Necesidad operativa
        ↓
Autorización del Responsable del Sistema
        ↓
Validación de Seguridad
        ↓
Implementación técnica
        ↓
Cuenta nominativa + temporal + limitada + trazable
        ↓
Revocación
```

## 3. Resolver la ventana de mantenimiento

Recaudación plantea que una ventana técnica coincide con un cierre tributario.

La opción adecuada es:

**Servicio fija necesidades; Sistema ejecuta; Seguridad verifica requisitos**.

Nota sugerida:

> Las necesidades de disponibilidad y continuidad deben ser fijadas por el Responsable del Servicio, porque derivan de la prestación y de los periodos críticos del negocio. El Responsable del Sistema ejecutará los cambios técnicos necesarios y el Responsable de Seguridad verificará que se cumplen los requisitos y restricciones de seguridad.

La lógica es:

```text
Servicio  → define necesidades y prioridades
Seguridad → verifica requisitos de protección
Sistema   → implementa y opera
```

## 4. Revisar el modelo de responsabilidades

Volver a `Borrador_Resolucion_Responsabilidades_ENS_v1` y proponer revisión.

### Responsabilidad sobre la información

> Los requisitos de seguridad de la información serán determinados por las unidades funcionales responsables de cada conjunto de información. Recaudación asumirá esta responsabilidad sobre la información tributaria y la Unidad de Expedientes sobre la información vinculada a expedientes y tramitación electrónica. Secretaría General coordinará los criterios comunes cuando intervengan varias unidades o procedimientos transversales.

### Responsabilidad sobre el servicio

> La Dirección de Atención Ciudadana asumirá la responsabilidad sobre el servicio Portal Ciudadano y determinará sus necesidades de disponibilidad, continuidad y prioridades de prestación, coordinándose con Recaudación, Unidad de Expedientes y demás unidades funcionales en los periodos o procesos que les afecten. Dirección TIC ejecutará las actuaciones técnicas necesarias para satisfacer estos requisitos.

### Responsabilidad de Seguridad

> La Oficina ENS / Seguridad asumirá la responsabilidad de Seguridad. Determinará y coordinará las medidas de seguridad, supervisará su implantación y eficacia, realizará el seguimiento de riesgos y desviaciones y verificará el cumplimiento de los requisitos de seguridad. Esta función se mantendrá diferenciada de la operación ordinaria del sistema.

### Responsabilidad sobre el Sistema

> Dirección TIC asumirá la responsabilidad sobre el Sistema y sobre su arquitectura, administración, configuración, cambios, operación y recuperación. Los accesos privilegiados y de proveedores deberán responder a una necesidad justificada, ser autorizados por el Responsable del Sistema, validados por Seguridad cuando corresponda e implantados mediante cuentas nominativas, temporales, limitadas y trazables.

### Coordinación y conflictos

> Las discrepancias entre necesidades de información, servicio, seguridad y operación se documentarán y elevarán al circuito de gobierno establecido, con participación de los responsables afectados y, cuando sea necesario, del Comité de Seguridad y Secretaría General. Dirección TIC no resolverá unilateralmente los conflictos por el hecho de operar el sistema. Los riesgos residuales deberán ser conocidos y aceptados por el responsable funcional competente sobre la información o el servicio afectado.

## 5. Nota para Secretaría General

> La propuesta separa las decisiones funcionales, de seguridad y de operación. Las unidades responsables de la información determinan sus necesidades de protección; Dirección de Atención Ciudadana asume las necesidades del servicio; Oficina ENS / Seguridad dirige y supervisa la seguridad; y Dirección TIC mantiene la responsabilidad técnica y operativa sobre el Sistema. Se establece además un circuito trazable para accesos privilegiados y proveedores y un mecanismo de escalado para conflictos y riesgos residuales, evitando que Dirección TIC concentre decisión, ejecución y supervisión.

## 6. Resultado

El documento queda en **versión 2** y **Propuesta enviada a Secretaría**.

`REQ-1087` pasa a **Pendiente de ejecución controlada** y queda como ejemplo de aplicación real del circuito de autorización.

La distribución final puede resumirse así:

- **Información:** unidades funcionales competentes;
- **Servicio:** Dirección de Atención Ciudadana;
- **Seguridad:** Oficina ENS / Seguridad;
- **Sistema:** Dirección TIC;
- **Conflictos y riesgos residuales:** circuito de gobierno trazable y aceptación por el responsable funcional competente.

[Anterior: Escena 2 · Valoración y categorización](02-valoracion-categorizacion.md) · [Siguiente: Escena 4 · Riesgos y adecuación](04-riesgos-adecuacion.md)

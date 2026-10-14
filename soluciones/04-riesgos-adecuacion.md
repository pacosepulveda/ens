# Escena 4 · Gestión de riesgos y Plan de Adecuación

**Expediente:** `ENS-034 · Priorización de riesgos y Plan de Adecuación`

Villa Digital ya conoce su alcance, su categoría ALTA y su modelo de responsabilidades. El siguiente paso es decidir qué riesgos tratar primero, comprobar si las medidas funcionan realmente y convertir las brechas en acciones verificables.

## 1. Revisar el registro de riesgos

Los principales riesgos son:

- `R-01 · Identidad y cuentas privilegiadas` — residual ALTO;
- `R-02 · Tributos y expedientes` — residual ALTO;
- `R-03 · Capacidad de recuperación` — residual MEDIO/ALTO;
- `R-04 · Servicio cloud y evidencia` — residual MEDIO;
- `R-05 · Portal informativo fuera de periodos críticos` — residual BAJO/MEDIO.

La situación muestra varias brechas, pero la capacidad inmediata solo permite concentrarse en dos frentes relevantes.

## 2. Priorizar los riesgos

En el chat `No cabe todo en este trimestre`, la decisión adecuada es:

**Priorizar identidad privilegiada y capacidad de recuperación**.

Nota sugerida:

> La capacidad inmediata debe concentrarse en los riesgos con mayor exposición y dependencia transversal. Se prioriza el cierre de excepciones de MFA y la revisión de privilegios, junto con la mejora y prueba de la capacidad de recuperación. La centralización de logs y la revisión contractual siguen siendo necesarias, pero pueden incorporarse al Plan de Adecuación de 90 días sin dispersar los recursos disponibles.

La prioridad queda por tanto sobre **R-01** y **R-03**.

## 3. No confundir backup con recuperación demostrada

En el chat `Tenemos backup diario, ¿podemos darlo por resuelto?`, la opción adecuada es:

**Mantener el riesgo abierto hasta probar restauración**.

Justificación:

> La ejecución correcta de copias no demuestra por sí sola la capacidad de recuperación. El riesgo debe mantenerse abierto hasta realizar una restauración completa y documentada, verificar los tiempos de recuperación obtenidos, comprobar la integridad de los datos restaurados y revisar la protección de las copias frente al entorno operativo.

La prueba debe producir evidencia: acta, tiempos, integridad, incidencias y resultado.

## 4. Aceptar formalmente un residual cuando corresponde

Para `R-05`, el residual afecta al portal meramente informativo fuera de periodos críticos y existen canales alternativos.

La decisión adecuada es:

**Aceptar el residual por el Responsable del Servicio y revisarlo periódicamente**.

Nota sugerida:

> El riesgo residual puede aceptarse al quedar limitado al contenido informativo fuera de periodos críticos y existir canales alternativos. La aceptación debe realizarla formalmente el Responsable del Servicio, dejando constancia del nivel residual, la justificación, las condiciones de aceptación y una fecha o criterio de revisión periódica. La aceptación deberá reevaluarse si cambia el servicio, el impacto, la frecuencia o las medidas existentes.

Aceptar un riesgo no significa ignorarlo. Implica que el residual es conocido, existe un responsable competente, la decisión queda documentada y se revisará cuando corresponda.

## 5. Corregir el Plan de Adecuación

El borrador inicial es demasiado genérico. Una versión defendible debe unir riesgo, acción, responsable, fecha y evidencia.

### Acciones 0–30 días

> Priorizar R-01 y R-03. Para R-01, completar MFA en todas las cuentas administrativas, eliminar o justificar formalmente las excepciones existentes y ejecutar la revisión de privilegios vencida SEC-0032. Para R-03, realizar una prueba integral de restauración, registrar los tiempos obtenidos, comprobar la integridad de la información recuperada y completar la protección de las copias frente al dominio operativo. Estas actuaciones tienen prioridad por mantener actualmente una exposición residual alta o medio/alta y afectar a capacidades transversales del Portal.

### Acciones 31–90 días

> Completar la centralización y retención homogénea de logs de identidad, Portal y sistemas relevantes, definiendo evidencias de operación y revisión. Revisar con Contratación el acuerdo con NubeCentro para incorporar obligaciones claras de notificación de incidentes, conservación de evidencias, soporte forense y condiciones aplicables a terceros. Revisar además las medidas de segmentación asociadas a los accesos privilegiados y al entorno de backup a partir de los resultados obtenidos en las acciones prioritarias.

### Responsables, fechas y dependencias

> Dirección TIC será responsable de la implantación técnica del MFA y de las mejoras de configuración, con supervisión de Oficina ENS / Seguridad; SEC-0032 deberá quedar revisado antes del 31/10/2026. Operaciones TIC realizará la prueba integral de restauración y documentará sus resultados antes del 15/11/2026. La centralización de logs quedará planificada e implantada antes del 15/12/2026. Contratación, con apoyo de Oficina ENS / Seguridad y de los responsables funcionales afectados, tramitará la revisión contractual de NubeCentro antes del 31/12/2026. Las actuaciones sobre backup y segmentación deberán coordinarse para no comprometer la continuidad del servicio.

### Evidencias de cierre

> Las acciones no se considerarán cerradas únicamente por confirmación por correo. Para MFA y privilegios se aportará configuración del IdP, inventario actualizado de cuentas, resultado de la revisión SEC-0032 y registros de autenticación. Para recuperación se conservarán el acta de la prueba, los tiempos de restauración obtenidos, la comprobación de integridad y la evidencia de protección de las copias. Para logging se aportará configuración y registros de recepción y retención. Para el proveedor cloud se aportará el contrato o adenda aprobada y las cláusulas incorporadas.

### Riesgo residual y aceptación

> Los riesgos que no puedan eliminarse o tratarse completamente dentro de los 90 días permanecerán identificados y sujetos a seguimiento; no se considerarán aceptados automáticamente. La aceptación de un riesgo residual deberá ser informada, autorizada por el responsable competente y quedar documentada junto con su justificación y criterio de revisión. Para R-05 se propone que el Responsable del Servicio acepte formalmente el residual, al limitarse al contenido informativo fuera de periodos críticos y existir canales alternativos, estableciendo una revisión periódica y una reevaluación ante cambios relevantes.

### Nota al Comité

> Se propone concentrar la capacidad inmediata en identidad privilegiada y recuperación, por presentar las exposiciones más relevantes y afectar transversalmente al Portal. R-01 deberá reducirse mediante MFA completo y revisión de privilegios, y R-03 permanecerá abierto hasta disponer de una restauración integral demostrada. Logging y revisión contractual se incorporan al horizonte de 31–90 días. Ningún riesgo pendiente se considerará aceptado por defecto. Para R-05 se propone una aceptación formal por el Responsable del Servicio, documentada y sujeta a revisión periódica.

## 6. Resultado

El Plan queda en **versión 2** y **Propuesta enviada a Comité**.

La secuencia queda conectada así:

```text
Riesgo
  ↓
Medidas existentes
  ↓
Eficacia real y evidencia
  ↓
Riesgo residual
  ↓
Tratamiento o aceptación formal
  ↓
SoA / brechas
  ↓
Plan de Adecuación
  ↓
Evidencia de cierre
```

[Anterior: Escena 3 · Gobierno](03-gobierno-responsabilidades.md) · [Siguiente: Escena 5 · Incidente](05-incidente-reevaluacion.md)

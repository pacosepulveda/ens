# Escena 2 · Valoración y categorización ENS

**Expediente:** `ENS-014 · Revisión de valoración y categorización`

El borrador heredado deja todas las dimensiones en MEDIO. La solución consiste en contrastar esa propuesta con evidencia funcional y operativa antes de decidir.

## 1. Revisar el borrador inicial

Abrir `Valoracion_Categorizacion_ENS_v1`.

La propuesta inicial es:

```text
C = MEDIO
I = MEDIO
T = MEDIO
A = MEDIO
D = MEDIO
→ Categoría MEDIA
```

El problema es que las justificaciones son demasiado genéricas. No todas las dimensiones tienen por qué compartir el mismo nivel.

## 2. Revisar la información y los procesos

Abrir `Ficha_Informacion_y_Procesos_2026`.

El sistema maneja, entre otros elementos:

- datos identificativos;
- información tributaria;
- expedientes y documentación aportada por ciudadanos;
- registros de actuación;
- notificaciones administrativas.

Esto permite razonar sobre confidencialidad, integridad, trazabilidad y autenticidad.

## 3. Investigar la disponibilidad

En el correo de Recaudación conviene **solicitar el informe de indisponibilidad**.

El informe muestra que la criticidad aumenta en periodos concretos, especialmente cierres tributarios y vencimientos. Una caída de más de dos horas en Tributos generó más de 600 intentos fallidos y obligó a ampliar la atención al día siguiente.

La disponibilidad no debe valorarse únicamente con el promedio anual: importa el efecto de la indisponibilidad cuando el servicio se encuentra en un periodo crítico.

## 4. Revisar integridad y trazabilidad

El correo de la Unidad de Expedientes y `Incidencias_Expedientes_Integridad_Trazabilidad_Q3` muestran que una alteración de datos o la pérdida de trazabilidad puede afectar a:

- validez de actuaciones;
- reconstrucción de hechos;
- atribución de responsabilidades;
- revisión y auditoría de decisiones administrativas.

## 5. Consultar las fichas de servicio

En el chat `¿Dejamos todo en MEDIO?`, la decisión más sólida es:

**Pedir fichas de servicio antes de decidir**.

Las fichas confirman que:

- Registro tiene periodos críticos;
- Tributos tiene periodos críticos;
- Identidad es una dependencia transversal;
- Notificaciones no tienen una alternativa equivalente;
- el portal meramente informativo tiene un impacto menor.

## 6. Propuesta C/I/T/A/D

### Confidencialidad → MEDIO

> El sistema trata datos identificativos, tributarios, documentación aportada por ciudadanos y contenido de notificaciones administrativas. Una divulgación no autorizada puede afectar a personas interesadas y contribuyentes, por lo que no puede considerarse un impacto bajo.

### Integridad → ALTO

> Una alteración de expedientes, liquidaciones, estados de tramitación o notificaciones puede modificar el curso de procedimientos administrativos, afectar obligaciones económicas o provocar decisiones incorrectas. La integridad de la información es esencial para preservar la validez de las actuaciones administrativas.

### Trazabilidad → ALTO

> Es necesario poder reconstruir quién realizó cada actuación, cuándo se produjo y qué información fue modificada. La pérdida o alteración de registros puede impedir atribuir actuaciones y dificultar la defensa, revisión o auditoría de decisiones administrativas.

### Autenticidad → MEDIO

> El Portal depende de un servicio común de identidad para varios servicios electrónicos. Una suplantación o atribución incorrecta puede provocar actuaciones realizadas en nombre de ciudadanos o personal municipal, por lo que la autenticidad requiere una protección significativa.

### Disponibilidad → ALTO

> La criticidad depende del periodo operativo. Durante cierres tributarios y vencimientos administrativos, una interrupción puede impedir presentaciones o pagos dentro de plazo. El informe de indisponibilidades muestra una caída de más de dos horas en Tributos con más de 600 intentos fallidos y necesidad de ampliar la atención al día siguiente, y las alternativas disponibles son limitadas.

## 7. Categoría resultante

La regla del máximo produce:

```text
C = MEDIO
I = ALTO
T = ALTO
A = MEDIO
D = ALTO

Máximo = ALTO
→ CATEGORÍA ALTA
```

Es importante distinguir los **niveles de las dimensiones** de la **categoría del sistema**.

## 8. Nota de revisión

Una formulación completa puede ser:

> La propuesta se ha revisado contrastando el borrador inicial con el RAT, la ficha de información y procesos, el informe de indisponibilidades, las fichas de servicio y las evidencias de integridad y trazabilidad. Se mantienen en MEDIO confidencialidad y autenticidad, y se elevan a ALTO integridad, trazabilidad y disponibilidad por el impacto potencial sobre procedimientos administrativos, capacidad de reconstruir actuaciones y prestación de servicios en periodos críticos. La categoría resultante propuesta es ALTA.

## 9. Resultado

Tras enviar la propuesta:

- el documento pasa a **versión 2**;
- el estado queda en **Propuesta enviada a revisión**;
- la categoría queda en **ALTA**;
- `ENS-014` pasa a **Propuesta enviada**.

A partir de este punto, el resto del caso utiliza categoría ALTA.

[Anterior: Escena 1 · Alcance](01-alcance.md) · [Siguiente: Escena 3 · Gobierno y responsabilidades](03-gobierno-responsabilidades.md)

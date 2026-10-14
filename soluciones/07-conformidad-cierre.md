# Escena 7 · Conformidad, comunicación y mejora continua

**Expediente:** `ENS-052 · Estado de conformidad y hoja de ruta de cierre`

La auditoría ya se ha realizado y el PAC está presentado, pero eso no significa que Villa Digital esté certificada ni que los hallazgos estén cerrados.

El estado real es:

| Elemento | Estado |
|---|---|
| Categoría ENS | ALTA |
| Auditoría | Realizada |
| PAC | Presentado |
| H-01 | Abierto |
| H-02 | Abierto |
| H-03 | En tratamiento |
| H-04 | Oportunidad de mejora |
| Certificación de Conformidad | Pendiente |
| Vigilancia y mejora | Activa |

## 1. Decidir qué puede comunicarse

En el correo `¿Qué podemos afirmar tras el cierre preliminar?`, la opción adecuada es:

**Comunicar auditoría realizada y conformidad formal pendiente de cierre y verificación**.

Una formulación correcta sería:

> La auditoría ha sido realizada y el PAC está presentado, pero permanecen hallazgos abiertos y evidencias de cierre pendientes. Por tanto, no procede comunicar que Villa Digital esté certificada ni emitir una declaración sustitutiva. Debe comunicarse que el proceso de conformidad formal continúa pendiente del cierre y verificación de las acciones correctivas.

En un sistema de categoría ALTA, la vía prevista es la **Certificación de Conformidad**. Haber terminado una auditoría no equivale a disponer de esa certificación.

## 2. Qué ocurre si se comunica prematuramente que existe certificación

Si se afirma que Villa Digital ya está certificada, Secretaría General / Equipo Auditor exige rectificación.

La corrección deja claro que:

- cierre preliminar de auditoría ≠ certificación emitida;
- PAC presentado ≠ hallazgos cerrados;
- H-01 y H-02 siguen abiertos;
- H-03 continúa en tratamiento;
- la conformidad formal debe seguir figurando como pendiente.

La comunicación prematura queda registrada como **Rectificada** en el resumen final del recorrido.

## 3. No cerrar H-01 y H-02 por tener un PAC

En el chat `Tenemos un PAC presentado: ¿podemos cerrar ya H-01 y H-02?`, la opción adecuada es:

**Mantenerlos abiertos hasta verificar ejecución y eficacia con evidencia**.

Nota sugerida:

> El PAC define acciones, responsables y fechas, pero H-01 y H-02 deben permanecer abiertos hasta que exista evidencia suficiente de ejecución y eficacia. La presentación del plan no sustituye la verificación del cierre y tampoco procede reclasificar hallazgos para facilitar el proceso de conformidad.

El seguimiento queda así:

| Hallazgo | Responsable / objetivo | Evidencia | Estado |
|---|---|---|---|
| H-01 | Dirección TIC + Oficina ENS · 30/11/2026 | Inventario, IdP, SEC-0032, excepciones | Abierto |
| H-02 | Operaciones TIC + Oficina ENS · 15/11/2026 | Acta, logs, tiempos, integridad y restore | Abierto |
| H-03 | Contratación + Oficina ENS · 31/12/2026 | Adenda/modificación y evidencia de aplicación | En tratamiento |

H-04 no se convierte en una acción correctiva obligatoria mientras el proceso manual siga satisfaciendo el requisito.

## 4. La conformidad no termina el ENS

En el correo `Cuando consigamos la certificación, ¿podemos cerrar el proyecto ENS?`, la opción adecuada es:

**Mantener vigilancia, reevaluación de cambios, riesgos, incidentes y evidencias**.

La razón es que el sistema seguirá cambiando. Pueden aparecer:

- nuevas versiones y funcionalidades;
- cambios de proveedor;
- nuevas integraciones;
- modificaciones de arquitectura;
- nuevos riesgos;
- incidentes;
- cambios de alcance o categoría.

Por ello, la conformidad no es un estado que permita dejar de revisar el sistema.

## 5. Estado final de Villa Digital

El documento `Villa_Digital_Recorrido_ENS.pdf` resume el caso así:

| Paso | Estado | Evidencia / resultado |
|---|---|---|
| Alcance | Definido | Dependencias, terceros e información contratados |
| Valoración y categorización | Completada | C/I/T/A/D y categoría ALTA |
| Gobierno | Formalizado | Responsabilidades diferenciadas y trazables |
| Riesgos / SoA / Plan | En seguimiento | R-01, brechas y Plan de Adecuación |
| Incidente | Gestionado | INC-2197 contenido, recuperado y reevaluado |
| Auditoría | Realizada | Hallazgos preliminares y PAC v2 |
| Hallazgos | Abiertos | H-01 y H-02 requieren evidencia de cierre; H-03 en tratamiento |
| Conformidad formal | Pendiente | Pendiente del cierre y verificación de hallazgos y de la vía aplicable a la categoría |
| Vigilancia | Continua | Cambios, riesgos, incidentes y evidencias deben reevaluarse |

Si se produjo una comunicación prematura de certificación, aparece además:

`Comunicación de conformidad · Rectificada`

## 6. Recorrido completo

```text
ALCANCE
  ↓
VALORACIÓN
  ↓
CATEGORIZACIÓN
  ↓
GOBIERNO
  ↓
RIESGOS
  ↓
MEDIDAS / SoA
  ↓
PLAN DE ADECUACIÓN
  ↓
INCIDENTE
  ↓
REEVALUACIÓN
  ↓
AUDITORÍA
  ↓
HALLAZGOS
  ↓
PAC
  ↓
CONFORMIDAD FORMAL
  ↓
VIGILANCIA Y MEJORA CONTINUA
```

El cierre del caso no es «todo está terminado», sino una fotografía realista: Villa Digital ha recorrido el proceso, conoce sus desviaciones, dispone de acciones correctivas y continúa trabajando hasta demostrar el cierre y mantener la conformidad en el tiempo.

[Anterior: Escena 6 · Auditoría y PAC](06-auditoria-hallazgos-pac.md) · [Volver al mapa](../MAPA_RECORRIDO.md)

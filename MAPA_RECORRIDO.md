# Mapa del recorrido Villa Digital

El caso de Villa Digital recorre de forma continua el ciclo ENS, desde la definición del alcance hasta la conformidad y la vigilancia continua.

```text
Alcance
  ↓
Valoración C/I/T/A/D
  ↓
Categorización
  ↓
Gobierno y responsabilidades
  ↓
Riesgos
  ↓
Medidas / SoA / brechas
  ↓
Plan de Adecuación
  ↓
Incidente
  ↓
Reevaluación
  ↓
Auditoría
  ↓
Hallazgos
  ↓
Plan de Acciones Correctivas
  ↓
Conformidad formal
  ↓
Vigilancia y mejora continua
```

## Relación entre módulos y escenas

| Módulo | Escena | Pregunta principal | Resultado del caso |
|---|---|---|---|
| M01 · Fundamentos, marco normativo y principios | 1 · Alcance | ¿Qué forma realmente parte del sistema? | Alcance corregido con dependencias y terceros |
| M02 · Valoración, categorización y medidas | 2 · Valoración y categorización | ¿Qué impacto tendría perder C/I/T/A/D? | `C=M, I=A, T=A, A=M, D=A` → categoría ALTA |
| M03 · Organización, responsabilidades y gobierno | 3 · Gobierno | ¿Quién decide, quién supervisa y quién opera? | Responsabilidades diferenciadas y circuito de gobierno trazable |
| M04 · Gestión de riesgos y proceso de adecuación | 4 · Riesgos y Plan | ¿Qué riesgos se tratan primero y cómo se demuestra el cierre? | Priorización de R-01 y R-03 + Plan de Adecuación v2 |
| M04 · Gestión de riesgos y proceso de adecuación | 5 · Incidente | ¿Qué cambia cuando un riesgo se materializa? | INC-2197 contenido, servicio recuperado y R-01 reevaluado |
| M05 · Verificación, auditoría, conformidad y mejora continua | 6 · Auditoría y PAC | ¿Qué evidencia sostiene el estado real y cómo se responden los hallazgos? | Hallazgos preliminares + PAC v2 verificable |
| M05 · Verificación, auditoría, conformidad y mejora continua | 7 · Conformidad | ¿Qué puede afirmarse realmente y qué continúa después? | Conformidad formal pendiente y vigilancia continua |

## Estado consolidado de Villa Digital

### Alcance

El Portal Ciudadano no se limita a su interfaz visible. Depende de:

- `VD-ID Gateway` para identidad y autenticación;
- `EXP-API` para expedientes;
- `TRIB-CORE` para tributos;
- `NotifyHub` para notificaciones;
- `NubeCentro ES-2` como plataforma cloud;
- `BCP-Vault` para protección y recuperación;
- otras integraciones municipales cuando intervienen en la prestación o en los tratamientos incluidos.

Los servicios gestionados por terceros se consideran dependencias relevantes y sus obligaciones de seguridad deben quedar definidas contractualmente.

### Valoración y categoría

La valoración consolidada es:

```text
Confidencialidad = MEDIO
Integridad       = ALTO
Trazabilidad     = ALTO
Autenticidad     = MEDIO
Disponibilidad   = ALTO
```

Por la regla del máximo, el sistema queda en **categoría ALTA**.

### Gobierno

- las unidades funcionales determinan las necesidades de protección de su información;
- la Dirección de Atención Ciudadana define las necesidades del servicio;
- Oficina ENS / Seguridad determina y supervisa las medidas de seguridad;
- Dirección TIC administra, configura y opera el sistema;
- los conflictos y riesgos residuales siguen un circuito de gobierno documentado.

### Riesgos principales

- `R-01` · identidad y cuentas privilegiadas;
- `R-02` · tributos y expedientes;
- `R-03` · capacidad de recuperación;
- `R-04` · servicio cloud y evidencia;
- `R-05` · indisponibilidad residual del portal informativo fuera de periodos críticos.

La capacidad inmediata se concentra en **R-01** y **R-03**. El residual de R-05 puede aceptarse formalmente por el Responsable del Servicio, con justificación y revisión periódica.

### Incidente

`INC-2197` materializa R-01: la cuenta privilegiada `adm-legacy-07`, sin MFA, registra un acceso anómalo y se produce degradación en autenticación.

La respuesta correcta conserva evidencia, contiene la cuenta afectada, recupera el servicio con configuración validada y utiliza el incidente para actualizar R-01, la SoA y el Plan de Adecuación.

### Auditoría y PAC

La auditoría identifica, entre otros:

- H-01 · accesos privilegiados y excepciones legacy;
- H-02 · capacidad de recuperación no demostrada mediante restauración integral reciente;
- H-03 · obligaciones contractuales insuficientes con el proveedor cloud;
- H-04 · proceso manual de accesos como oportunidad de mejora cuando el requisito ya se satisface.

El PAC v2 asigna causas, acciones, responsables, fechas y evidencias de cierre. Presentar el PAC no equivale a cerrar los hallazgos.

### Conformidad

Al final del recorrido:

- la auditoría está realizada;
- el PAC está presentado;
- H-01 y H-02 siguen abiertos;
- H-03 continúa en tratamiento;
- la Certificación de Conformidad sigue pendiente;
- la vigilancia, la revisión de cambios, riesgos, incidentes y evidencias deben continuar.

## Soluciones por escena

1. [Alcance](soluciones/01-alcance.md)
2. [Valoración y categorización](soluciones/02-valoracion-categorizacion.md)
3. [Gobierno y responsabilidades](soluciones/03-gobierno-responsabilidades.md)
4. [Riesgos y Plan de Adecuación](soluciones/04-riesgos-adecuacion.md)
5. [Incidente y reevaluación](soluciones/05-incidente-reevaluacion.md)
6. [Auditoría, hallazgos y PAC](soluciones/06-auditoria-hallazgos-pac.md)
7. [Conformidad y mejora continua](soluciones/07-conformidad-cierre.md)

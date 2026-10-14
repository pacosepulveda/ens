# Escena 1 · Validación del alcance ENS

**Expediente:** `ENS-011 · Validación del alcance del Portal Ciudadano`

La primera decisión importante del caso consiste en determinar qué componentes forman realmente parte del sistema sometido al ENS. El error inicial de Villa Digital es tratar el Portal Ciudadano como si fuera un componente aislado y excluir de forma genérica aquello que opera un tercero.

## 1. Revisar la solicitud de Secretaría

El expediente exige elevar una propuesta de alcance que pueda sostenerse con evidencias. Antes de modificar nada hay que contrastar:

- arquitectura;
- información tratada;
- dependencias técnicas;
- proveedores;
- continuidad y recuperación.

## 2. Revisar el borrador `Alcance_ENS_v3_FINAL_FINAL`

El borrador presenta dos problemas principales:

1. excluye de forma demasiado amplia componentes gestionados por terceros;
2. no documenta todas las dependencias necesarias para prestar el servicio.

El criterio correcto no es «quién administra el componente», sino si el componente interviene en la prestación, trata información del servicio o puede afectar a sus objetivos de seguridad.

## 3. Contrastar la arquitectura

En `Arquitectura_Portal_Ciudadano_2026` aparecen dependencias que el borrador no puede ignorar:

- `VD-ID Gateway` — identidad y autenticación;
- `EXP-API` — expedientes electrónicos;
- `TRIB-CORE` — servicios tributarios;
- `NotifyHub` — notificaciones;
- `NubeCentro ES-2` — infraestructura cloud;
- `BCP-Vault` — protección y recuperación.

La conclusión es que el Portal depende funcionalmente de todos ellos aunque no estén administrados por el mismo equipo.

## 4. Revisar el contrato de NubeCentro

El contrato muestra que utilizar un proveedor cloud no transfiere automáticamente todas las obligaciones de seguridad.

La renovación debe cubrir, como mínimo, aspectos como:

- notificación de incidentes;
- disponibilidad de registros y evidencias;
- colaboración ante investigaciones;
- continuidad;
- subcontratación;
- responsabilidades de seguridad.

## 5. Solicitar y revisar el extracto del RAT

En el correo de la DPD conviene elegir **Solicitar el extracto**.

Una nota adecuada sería:

> Necesitamos contrastar qué tratamientos y categorías de datos personales dependen del Portal Ciudadano antes de cerrar el alcance ENS.

El documento `Extracto_RAT_Servicios_Digitales` confirma que el Portal se relaciona con varios tratamientos municipales. Esto refuerza la necesidad de incluir las integraciones y dependencias que participan en esos procesos.

## 6. Resolver la renovación del proveedor cloud

En el correo `Renovación proveedor cloud · condiciones de seguridad`, la decisión coherente es:

**Remitir requisitos a Contratación**.

La justificación puede expresarse así:

> El servicio cloud forma parte de las dependencias relevantes del Portal Ciudadano. La renovación debe contemplar requisitos de seguridad, notificación de incidentes, disponibilidad de evidencias y registros, soporte a investigación y control de subcontratistas.

## 7. Corregir el documento de alcance

Volver a `Alcance_ENS_v3_FINAL_FINAL` y proponer una modificación.

### Sistemas y servicios incluidos

> El alcance comprende el Portal Ciudadano y los servicios, componentes e integraciones necesarios para su prestación: VD-ID Gateway para identidad y autenticación, EXP-API para expedientes electrónicos, TRIB-CORE para servicios tributarios, NotifyHub para notificaciones, la plataforma NubeCentro ES-2 que soporta la infraestructura cloud y BCP-Vault como dependencia de protección y recuperación. La gestión por un tercero no implica por sí sola su exclusión del análisis de seguridad.

### Exclusiones

> Solo podrán quedar fuera del alcance aquellos sistemas, servicios o componentes que no intervengan en la prestación del Portal Ciudadano, no traten información asociada al servicio y cuya indisponibilidad o compromiso no pueda afectar a sus objetivos de seguridad. Los servicios prestados por terceros se tratarán como dependencias externas y sus responsabilidades de seguridad deberán quedar definidas y controladas contractualmente.

### Dependencias

> Se identifican como dependencias relevantes VD-ID Gateway, EXP-API, TRIB-CORE, NotifyHub, NubeCentro ES-2 y BCP-Vault. También deberán considerarse las integraciones con otros sistemas municipales que proporcionen información al Portal, como los servicios asociados al padrón, cuando participen en los tratamientos o procesos incluidos. Para las dependencias externas deberán documentarse responsables, requisitos de seguridad, gestión de incidentes, registros y evidencias, continuidad y subcontratación.

### Nota para Secretaría General

> Se ha revisado el borrador contrastándolo con la arquitectura de producción, el contrato vigente de NubeCentro y el extracto del RAT. Se elimina la exclusión genérica de componentes gestionados por terceros y se incorporan explícitamente las dependencias necesarias para la prestación del Portal. Se propone además trasladar requisitos de seguridad específicos a la renovación contractual del proveedor cloud.

## 8. Resultado

Tras enviar la propuesta:

- el documento pasa a **versión 4**;
- el estado queda en **Propuesta enviada a Secretaría**;
- `ENS-011` queda como **Propuesta enviada** y posteriormente se cierra al continuar el proceso.

La idea clave del caso es que **externalizar un componente no lo vuelve irrelevante para el alcance**. Si la prestación depende de él, su seguridad, continuidad y responsabilidades deben quedar tratadas explícitamente.

[Siguiente: Escena 2 · Valoración y categorización](02-valoracion-categorizacion.md)

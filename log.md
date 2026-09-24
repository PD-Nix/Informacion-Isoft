# LOG DE TRABAJO

Sesión de trabajo de la iteración 2 del proyecto **Sistema de Gestión para Tienda de Agua Embotellada ("Agua Frais")** – Ingeniería de Software, Universidad de Cartagena.

---

## Resumen de la conversación y lo realizado

### 1. Lectura de contexto del proyecto
- Se leyó `Contexto.md`, la guía de la iteración 1 y el documento de planteamiento del problema (`1_Iteracion/DespriciondelProblema.md`), donde se encuentra el acta de la entrevista al propietario (26/08/2026, Anexo C).
- Se revisó la estructura de la iteración 2 (`2_Iteracion/`), incluyendo la guía del curso (`Guia.md`), basada en ISO/IEC/IEEE 29148.

### 2. Sugerencias de requisitos en el SRS (sección 1.5)
- En `2_Iteracion/especificaciones.md` se añadió la sección **1.5. Sugerencias de requisitos identificados**, con 11 bloques `### Sugerencia`, cada uno vinculando un hallazgo de la entrevista con un posible requisito:
  1. Sistematización del registro de pedidos (necesidad prioritaria).
  2. Seguimiento del estado de los pedidos (memos + marcas de verificación).
  3. Visión centralizada de pedidos pendientes para organización de despachos.
  4. Consulta de pedidos registrados.
  5. Registro de ventas por presentación con totales automáticos (eliminación del doble registro).
  6. Registro y consulta de ingresos.
  7. Consulta de información histórica por rango de fechas.
  8. Estadísticas e indicadores operativos.
  9. Clientes habituales / catálogo de clientes.
  10. Requisitos no funcionales (usabilidad, disponibilidad, idioma, seguridad, desempeño).
  11. Tabla de trazabilidad problema – evidencia – requisito – funcionalidad (pendiente).

### 3. Nuevo requisito exigido por el docente (solo en Contexto.md)
- Se añadió en `Contexto.md`, sección 6, la subsección **E. Requisito adicional exigido por el docente**:
  - El sistema debe ser **web responsive**.
  - Los **pedidos deben realizarse a través de la página**, incorporando interacción con **usuarios externos a la empresa** (clientes), ampliando el alcance inicialmente administrativo.

### 4. Coherencia del SRS con el nuevo requisito
- Se modificó `2_Iteracion/especificaciones.md` para mantener coherencia:
  - 1.2 Identificación del producto: aplicación **web responsive** con interacción de clientes.
  - 1.2 Qué hará el sistema: pedidos realizados por clientes desde la web.
  - 1.2 Alcance funcional: de cuatro a **cinco áreas**, se agregó **E. Canal de pedidos de clientes (web)**.
  - 1.3.1 Interfaces de usuario: acceso desde computador y móviles (responsive) + módulo para clientes.
  - 1.3.2 Funciones del producto: funciones 12, 13 y 14 (pedido por cliente, consulta de estado en línea, adaptación responsive).
  - 1.3.3 Usuarios: nueva fila "Cliente" y nota de interfaz adaptable.

### 5. Sección 3 (Requisitos específicos) del SRS
- Se desarrolló la **sección 3** respetando los acuerdos tomados:
  - **3.1 Interfaces externas:** NO se hace (pendiente para después).
  - **3.2 Funciones:** se describen 12 requisitos funcionales (RF-01 a RF-12) con prioridad (P1/P2), descripción, entradas, procesamiento, salidas, criterios de validez y relación entrada–salida. Las sugerencias 1 a 10 quedaron ubicadas en la subsección correspondiente:
    - Gestión de pedidos: RF-01, RF-02, RF-03, RF-04.
    - Gestión de despachos: RF-05, RF-06.
    - Gestión de ventas e ingresos: RF-07, RF-08, RF-09.
    - Estadísticas e indicadores: RF-10.
    - Canal de clientes y catálogo: RF-11, RF-12.
  - **3.3 Capacidad de uso:** US-01 a US-06 (efectividad, eficiencia, satisfacción, lenguaje, feedbacks, responsive) con criterios medibles.
  - **3.4 Desempeño:** DE-01 a DE-05 (tiempos de respuesta, usuarios simultáneos, capacidad de información, disponibilidad operativa, carga diaria).
  - **3.5 Bases de datos:** NO se hace aún (pendiente para después).
  - **3.6 Restricciones de diseño:** DS-01 a DS-06 (responsive, tecnologías web, español, acceso restringido, alcance limitado, simplicidad).
  - **3.7 Atributos de calidad:** priorizados (usabilidad > seguridad > disponibilidad > confiabilidad > portabilidad).
  - **3.8 Información de soporte.**
- La **sección 2 (Referencias)** se dejó pendiente para después (solo nota).
- La **sección 4 (Verificación)** NO se hace (solo nota).
- La **Sugerencia 11 (tabla de trazabilidad)** no se incluyó en la sección 3 (pendiente).

### 6. Estado del avance documentado en Contexto.md
- Se añadió el apartado **`### Current`** al final de `Contexto.md` con:
  - Lo que se está elaborando ahora (secciones 3.2, 3.3, 3.4, 3.6, 3.7, 3.8).
  - Lo que NO se hará (sección 4, subsección 3.1, sugerencia 11 en la sección 3).
  - Lo que se hará después (sección 2, subsección 3.5, tabla de trazabilidad).

### 7. Nota técnica
- No fue posible leer el PDF del acta (formato no soportado por el modelo); se usó el acta contenida en el documento de la iteración 1.

---

## Archivos modificados
| Archivo | Cambio |
|---|---|
| `2_Iteracion/especificaciones.md` | Sección 1.5 (sugerencias), sección 2 (pendiente), sección 3 (funciones RF-01 a RF-12), ajustes por web responsive y canal de clientes |
| `Contexto.md` | Subsección "E. Requisito adicional exigido por el docente" y apartado `### Current` |
| `log.md` | Este archivo |

## Pendiente (próximas iteraciones)
- Sección 2. Referencias.
- Sección 3.1. Interfaces externas.
- Sección 3.5. Requisitos de bases de datos.
- Sección 4. Verificación.
- Tabla de trazabilidad (Sugerencia 11).

---

## Sesión 17/09/2026 – Refactorización de la sección 3 (Requisitos específicos)

### Contexto
- Se revisó `Contexto.md` (sección Current), el acta de entrevista (Anexo C) y la cross reference de funciones con su origen (problema/entrevista/docente).
- El equipo decidió que los compañeros reconstruyen la sección 3 del SRS, por lo que se retiró esa sección del documento de trabajo.

### Cambios realizados
- **Nuevo `2_Iteracion/requisitos_respaldo.md`:** respaldo de la versión anterior de la sección 3 (RF-01 a RF-12, US-01 a US-06, DE-01 a DE-05, DS-01 a DS-06, atributos de calidad y soporte).
- **`2_Iteracion/especificaciones.md`:** se eliminó la sección 3 completa; quedó una nota indicando que está en reconstrucción y dónde queda el respaldo. Se conservan las secciones 1, 2 y 4.
- **`Contexto.md`:** se agregó la versión nueva de requisitos del equipo (RF-01 a RF-06, US, DE, DS y atributos de calidad, con asignaciones y ✓) bajo el apartado "Requisitos – Versión nueva del equipo".

### Taylor de la versión nueva entregada por el equipo
- Requisitos funcionales RF-01 a RF-06 con nuevas asignaciones (RF-04 pasa a ser ingresos, RF-05 estadísticas, RF-06 consulta de estado del cliente).
- Requisitos de capacidad de uso (US-01 a US-06) — Jairo Jiménez.
- Requisitos de desempeño (DE-01 a DE-05).
- Restricciones de diseño (DS-01 a DS-05) — Newin Torres.
- Atributos de calidad (USU, SEG, DIS, CON, POR) — Jairo Jiménez.

## Pendiente
- Analizar el material que envíen los compañeros para la sección 3 y consolidarlo en el SRS.

---

## Sesión 21/09/2026 – Acuerdo sobre 3.5 y revisión de la visión general (sección 1.3)

### Contexto
- Se repasó el contexto completo del proyecto (Contexto.md, log.md, iteración 1, Guia.md, requisitos_respaldo.md y NotasClase.md) para corroborar la comprensión del estado actual.

### Cambios realizados
- **Acuerdo:** la subsección **3.5. Requisitos de bases de datos** **no se elabora**, sumándose a 3.1 (interfaces externas), a la sección 4 (verificación) y a la no inclusión de la sugerencia 11 dentro de la sección 3.
- Se actualizó la información en los lugares donde se lleva el registro:
  - `Contexto.md` (apartado `### Current`): la subsección 3.5 pasó de "Lo que se hará después" a "Lo que NO se hará".
  - `2_Iteracion/especificaciones.md`: nota en la sección 3 indicando que 3.5 no se elabora.

### Visión general (sección 1.3) – revisión
- Pendiente por decisión del equipo: se revisará/refactorizará la sección 1.3 tomando como referencia la `Guia.md` (basada en ISO/IEC/IEEE 29148). Se evaluará alinear 1.3.2 (Funciones del producto) con la versión nueva de requisitos RF-01 a RF-06 del equipo.

## Pendiente
- Revisión/refactorización de la sección 1.3 (visión general).
- Sección 2. Referencias.
- Tabla de trazabilidad (Sugerencia 11).
- Analizar el material de los compañeros para la sección 3 y consolidarlo en el SRS.

---

## Sesión 21/09/2026 (2) – Consolidación de los requisitos funcionales RF-01 a RF-06

### Acuerdo
- El equipo consideró que las 14 funciones del resumen anterior (sección 1.3.2 y RF-01 a RF-12 del respaldo) se solapaban: muchas iban implícitas unas en otras.
- Se decidió consolidar los **6 requisitos funcionales** de la versión nueva (RF-01 a RF-06) para que cada uno agrupe todo lo relacionado con su área, **sin perder cobertura** de las funciones originales.

### Consolidación aprobada (21/09/2026)
- **RF-01** ahora incluye: registro de pedidos + **seguimiento de estado** (Pendiente → Despachado) + **catálogo de clientes** (Sugerencias 1, 2 y 9).
- **RF-02** sin cambios (pedido web del cliente, docente).
- **RF-03** ahora incluye: consulta de pedidos + **visión de pendientes por zona para despachos** + **distinción despachados/pendientes** + **consulta histórica** (Sugerencias 3, 4 y 7).
- **RF-04** ahora incluye: **registro de ventas por presentación con totales** + ingresos (Sugerencias 5 y 6).
- **RF-05** sin cambios (estadísticas, Sugerencia 8).
- **RF-06** sin cambios (estado de pedidos por el cliente, docente).
- El diseño responsive se mantiene como restricción de diseño (DS-01), no como función.

### Cambios realizados
- `Contexto.md`: se actualizó la lista RF de "Versión nueva del equipo" con la consolidación y la referencia "RF-01 a RF-12" pasó a "RF-01 a RF-06".
- `2_Iteracion/especificaciones.md`:
  - Sección **1.3.2 (Funciones del producto)**: resumen reescrito a los 6 RF consolidados.
  - Sección **3.2 (Funciones)**: se incorporaron los 6 RF con prioridad y origen.
  - Sección 3: nota actualizada (3.1 y 3.5 no se elaboran; 3.3–3.8 pendiente de consolidar desde Contexto.md).

## Pendiente
- Consolidar en la sección 3: 3.3 US, 3.4 DE, 3.6 DS, 3.7 atributos de calidad, 3.8 soporte (desde Contexto.md).
- Sección 2. Referencias.
- Tabla de trazabilidad (Sugerencia 11).
- Analizar el material de los compañeros para la sección 3.

---

## Sesión 21/09/2026 (3) – Eliminación de 1.5 y actualización de definiciones

### Cambios realizados
- **`2_Iteracion/especificaciones.md`**:
  - Se **eliminó la sección 1.5 (Sugerencias de requisitos identificados)**: los requisitos se definen directamente en la sección 3.
  - Las referencias a "Sugerencias X" en la sección 3.2 (RF-01, RF-03, RF-04 y RF-05) se reemplazaron por el origen: *Entrevista al propietario (26/08/2026)*; los exigidos por el docente (RF-02, RF-06) se mantienen como *Exigido por el docente*.
  - **Sección 1.4 (Definiciones)**: reordenada **en orden alfabético** (acuerdo de clase) y ampliada con los roles definidos por el equipo:
    - **Administrativo** (persona con autoridad encargada del negocio).
    - **Operador** (empleado que usa el software sin ser administrador; gestión de ventas y pedidos).
    - **Repartidor** (reparte los pedidos).
    - **De la Espriella** (entrada del contexto interno del grupo; marcada como término humorístico ajustable).
- **`Contexto.md`**: se actualizó la nota `### Current` (1.5 eliminada, definiciones en orden alfabético) y los tags de origen de los RF a "Entrevista al propietario 26/08/2026".

## Pendiente
- Consolidar en la sección 3: 3.3 US, 3.4 DE, 3.6 DS, 3.7 atributos de calidad, 3.8 soporte (desde Contexto.md).
- Sección 2. Referencias.
- Tabla de trazabilidad (Sugerencia 11).
- Analizar el material de los compañeros para la sección 3.

---

## Sesión 21/09/2026 (4) – Consolidación de 3.3 y 3.7 del SRS

### Cambios realizados
- **`2_Iteracion/especificaciones.md`**:
  - Se incorporaron las subsecciones **3.3 (capacidad de uso)** y **3.7 (atributos de calidad)** con el material enviado por los compañeros.
  - **3.3.x:** corregidos typos y se añadió a cada ítem (excepto **3.3.2**, que ya describe lo que garantiza el diseño, y **3.3.4**, a cargo de Pedro Eli) una frase aditiva que describe **qué tendrá el programa** para garantizar el requisito (criterio de evaluación según NotasClase): validación y confirmación de cada operación (3.3.1), procesamiento sin esperas (3.3.3), pantallas con solo la información necesaria (3.3.5), interfaz en español cotidiano (3.3.6), mensajes claros de confirmación/error (3.3.7) y ajuste automático de la interfaz al dispositivo (3.3.8).
  - **3.4** y **3.6** siguen pendientes de consolidar.
  - **3.7.x:** se añadió *Cómo se garantiza* + *Prioridad* a cada atributo (Usabilidad 1, Seguridad 2, Disponibilidad 3, Confiabilidad 4, Portabilidad 5), siguiendo la estructura *requisito + en qué consiste + cómo se garantiza + prioridad* de NotasClase.
- **`Contexto.md`**: los US-01 a US-06 de la "versión nueva del equipo" se reemplazaron por los 3.3.1 a 3.3.8 (material de los compañeros) para evitar dos versiones distintas.
- **`NotasClase.md`**: se agregó la nota sobre el criterio de evaluación de requisitos no funcionales (qué tendrá el programa y no una métrica de medición), con el ejemplo de la Intuitividad.

## Pendiente
- **3.3.4 (Rendimiento):** criterio a cargo de Pedro Eli.
- Consolidar en la sección 3: 3.4 DE, 3.6 DS y 3.8 soporte (desde Contexto.md).
- Sección 2. Referencias.
- Tabla de trazabilidad (Sugerencia 11).
- Analizar el material de los compañeros para la sección 3.

---

## Sesión 23/09/2026 – Sincronización de Contexto.md, 3.3.4 finalizado, eliminación de 3.4 (DE) y de la tabla de trazabilidad

### Cambios realizados

**`Contexto.md`:**
- Bloques de la sección 3.3.x sincronizados con el SRS: frases aditivas "qué tiene el programa" en 3.3.1, 3.3.3 y 3.3.5 a 3.3.8 (3.3.2 ya la describía; 3.3.4 se finalizó).
- **3.3.4 (Rendimiento):** criterio finalizado → *"El programa procesa las operaciones sin esperas perceptibles, de modo que el usuario nunca percibe bloqueos ni retardos"*, reemplazando la métrica de "milisegundos" (criterio según NotasClase: qué tendrá el programa, no una métrica).
- **Eliminados los requisitos de desempeño (3.4 / DE-01 a DE-05):** acuerdo del equipo, no se elaboran (igual que 3.1 y 3.5).
- **Atributos de calidad** actualizados al estilo 3.7 del SRS (cómo se garantiza + prioridad 1–5); se corrigió el atributo DIS que referenciaba a DE-04.
- Bloque `### Current` actualizado: 3.2/3.3/3.7 consolidadas, 3.6 y 3.8 pendientes, 3.4 y tabla de trazabilidad NO se elaboran, sección 2 pendiente.

**`2_Iteracion/especificaciones.md` (SRS):**
- **3.3.4** actualizado con el criterio finalizado (sin la métrica de milisegundos).
- Notas de la sección 3 actualizadas: 3.4 no se elabora; tabla de trazabilidad no se realiza; se eliminó la mención de DE en el pendiente de consolidación.

**`TODO.md`:** se marcaron como resueltas la sincronización de `Contexto.md`, el 3.3.4 y la consolidación/DE; se eliminaron de los pendientes los requisitos de desempeño 3.4 y la tabla de trazabilidad. Quedan pendientes: 3.6 (DS), 3.8 (soporte) y sección 2 (Referencias).

### Acuerdos tomados (23/09/2026)
- La subsección **3.4 Requisitos de desempeño no se elabora** (por las mismas razones que 3.1 y 3.5).
- La **tabla de trazabilidad (Sugerencia 11) no se elabora** en el proyecto.

## Pendiente
- Sección 2. Referencias.
- Analizar el material de los compañeros para la sección 3 (si envían más).
- Iteración 1: pendiente solo el formato en Word (anexos y normas ICONTEC, fuera de alcance de este repositorio).

---

## Sesión 23/09/2026 (2) – Consolidación de 3.6 (Restricciones de diseño), prioridades y 3.8 (Información de soporte)

### Contexto
- El compañero entregó el material de la sección 3.6 (restricciones de diseño, DS-01 a DS-05) ampliado con su forma de verificación, las prioridades de 3.3 (capacidad de uso) y 3.7 (atributos de calidad) en Alta/Media, y pidió elaborar 3.8 y cerrar la sección 3.

### Cambios realizados

**`2_Iteracion/especificaciones.md` (SRS):**
- **3.3:** se agregó *Prioridad* a cada ítem: **Alta** (3.3.1, 3.3.5, 3.3.6, 3.3.7, 3.3.8) y **Media** (3.3.2, 3.3.3, 3.3.4).
- **Nueva 3.6 Restricciones de diseño:** DS-01 a DS-05 consolidados con la versión ampliada del equipo (Web adaptable, Tecnologías web estándar, Idioma, Restricción de acceso y Simplicidad), cada uno con su párrafo de verificación.
- **3.7:** prioridades pasaron de numéricas (1–5) a **Alta/Media** (Alta: Usabilidad, Seguridad, Disponibilidad; Media: Confiabilidad, Portabilidad).
- **Nueva 3.8 Información de soporte:** contexto del proyecto, acta de la entrevista (26/08/2026, Anexo C), planteamiento del problema, Guia.md (ISO/IEC/IEEE 29148) y material del equipo.
- Notas de la sección 3 actualizadas: se eliminó el "pendiente de consolidar"; la sección 3 quedó **completa** (3.2, 3.3, 3.6, 3.7, 3.8).

**`Contexto.md`:**
- Prioridades Alta/Media agregadas a 3.3.x y a los atributos de calidad (antes 1–5).
- Bloque **DS** reemplazado por la versión ampliada de 3.6 (mapeo DS-01..05 → 3.6.1..3.6.5).
- Bloque `### Current` actualizado: 3.6 y 3.8 ya no aparece pendientes; la sección 3 del SRS quedó completa.

**`TODO.md`:** se marcaron como resueltos 3.6, 3.8 y las prioridades. Queda pendiente: **sección 2 (Referencias)** y las tareas de prioridad baja.

### Acuerdo
- La sección 3 del SRS (requisitos específicos) quedó **consolidada en su totalidad** con la versión nueva del equipo.

## Pendiente
- **Sección 2. Referencias** (último pendiente de la iteración 2).
- Analizar el material de los compañeros para la sección 3 (si envían más).
- Iteración 1: pendiente solo el formato en Word (anexos y normas ICONTEC, fuera de alcance de este repositorio).
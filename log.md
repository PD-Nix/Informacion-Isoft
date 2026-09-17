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
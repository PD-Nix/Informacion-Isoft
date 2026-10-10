# Notas Unificadas: Modelado de Negocio y Modelo de Diseño

> Documento consolidado de las notas de clase. Tema central: análisis del contexto del problema (modelo de negocio) y diseño de la solución (modelo de diseño), con sus artefactos, preguntas guía, principios y recomendaciones.

---

## 1. Modelado de negocio y modelo de negocio

### 1.1 Definiciones

- **Modelado de negocio:** Técnica de análisis del contexto del problema con el fin de identificar:
  - Procesos
  - Actividades
  - Reglas de negocio
  - Responsables de los procesos
  - Intereses
  - Recursos

- **Modelo de negocio:** Es la representación que hace el ingeniero de software para demostrar que entiende el contexto del problema por medio de **planos de software**. Equivale al *modelo del contexto del problema*: el entendimiento del problema y su representación a través de artefactos.

- **Negocio = Contexto del problema.** Por tanto: **Modelo de negocio = Modelo del contexto del problema**.

### 1.2 ¿Quién lo realiza?

Lo realiza el **arquitecto/analista**.

### 1.3 Propósito del modelo de negocio

Representar el **contexto del problema** (no la solución). El modelo de negocio está presente en todas las etapas: modelo de negocio, requisitos, implementación y despliegue.

> ⚠️ **Regla clave:** No se debe involucrar la solución en el modelo de negocio (p. ej., no usar verbos como "DETECTA" que ya implican la solución). No se debe poner como nombre de un caso de uso el nombre de la solución.

### 1.4 Artefactos del modelo de negocio

1. **Procesos de negocio** → se plasman en un **diagrama de actividades** (de calle/carril).
2. **Actividades de negocio** (casos de uso) → se plasman en un **diagrama de casos de uso**.
3. **Modelo de dominio** → clases conceptuales, atributos y relaciones entre ellos.
4. **Glosario** → lista de palabras o tecnicismos de un mismo campo de estudio o texto, ordenados alfabéticamente, junto con sus definiciones o comentarios.

Notas sobre los artefactos:
- Los **responsables de los procesos, intereses y recursos** nos llevan a identificar objetos y relaciones (**modelo de dominio**).
- Para **evitar ambigüedades** contamos con el **glosario**.
- Cada actividad del diagrama de calle/carril corresponde a un **caso de uso** para el actor dentro del diagrama de casos de uso. El nombre del caso de uso **inicia con un verbo en infinitivo**.

---

## 2. El contexto del problema

### 2.1 Elementos para identificar el contexto

- **Objeto de estudio:** el problema que se va a resolver (p. ej., la deserción estudiantil, la gestión de ventas).
- **Ámbito:** el entorno donde se ubica el problema (p. ej., la universidad, la tienda).
- **Esencia / propósito del negocio:** lo que se quiere lograr (ejemplo: **prevenir la deserción**).

### 2.2 Preguntas guía del análisis del modelo de negocio

| Pregunta | Subsidiarias / Orientación |
|---|---|
| ¿Quiénes intervienen? (participantes/involucrados) | ¿Qué interés tiene cada uno? ¿Cuáles son sus responsabilidades? |
| ¿Qué procesos existen? | ¿Cuáles son las entradas? ¿Cuáles son las salidas? ¿Cuáles son las reglas de negocio? |

- **¿Quiénes intervienen?** orienta sobre todo la **identificación de funcionalidades**: para cada actor del sistema hay unas funcionalidades.
- La pregunta sobre los propósitos se logra respondiendo: *¿cuáles son los propósitos del contexto del problema?* → identificar la esencia (ej.: prevenir la deserción) y *¿cómo se logran esos propósitos?* → la respuesta da pie a los **procesos de negocio**.

### 2.3 Ejemplos

- **Deserción estudiantil:**
  - Objeto de estudio: prevenir la deserción.
  - Ámbito: la universidad.
  - Preguntas detonantes: ¿qué procesos realizan las instituciones de educación superior para evitar la deserción estudiantil? ¿Cómo se puede evitar la deserción estudiantil (en diferentes situaciones)?
- **Gestión de ventas:**
  - Actores: cliente, administrador, dueño, vendedor.
  - Nota: aunque una persona haga dos o más roles, los roles se deben mantener separados; el rol no se ve como una persona.

---

## 3. Conceptos fundamentales: proceso, actividad y acción

| Concepto | Definición |
|---|---|
| **Proceso** | Secuencia de actividades que se realizan en el tiempo. Tiene el mayor nivel de abstracción. |
| **Actividad** | Secuencia de acciones que se realizan en el tiempo. Más detallada que el proceso; una actividad puede tener internamente más actividades. |
| **Acción** | No puede dividirse en otras acciones o actividades; es **atómica**. Está dentro de una actividad. |

Jerarquía de abstracción: **proceso > actividad > acción**.

---

## 4. Casos de uso y documentación

- Cada actividad se documenta usando la **plantilla de Craig Larman** (libro *UML y Patrones*, 2ª edición, capítulo 6). La plantilla incluye:
  - Nombre del caso de uso
  - Actores principales
  - **Personal involucrado y sus intereses** (ítem importante)
  - Precondición
  - Postcondición
  - Flujo principal y flujos alternativos del sistema
  - Frecuencia
  - Uso de tecnologías
- Las **reglas de negocio** deben estar presentes en cada una de las actividades documentadas (antes de documentar, leer las reglas del negocio del contexto del problema que se esté trabajando).
- Al incluir actores, debe considerarse también el *adviser* dentro del contexto del problema.
- Lecturas asignadas: capítulo de casos de uso de *UML y Patrones* de Craig Larman (cap. 6); Manual, capítulos 1 y 2.

### 4.1 Sobre el glosario y la especificación de requisitos

**¿Por qué no deben ir términos técnicos en un glosario o en una definición de especificación de requisitos?**
Porque el glosario y las especificaciones están dirigidos a todos los involucrados (incluido el cliente, que no domina el lenguaje técnico). Usar tecnicismos introduce ambigüedades y malas interpretaciones: el objetivo del glosario es justamente eliminar ambigüedades usando un lenguaje común, claro y entendible por todos los interesados.

---

## 5. Requisitos

- **Requisitos implícitos:** requisitos que no son necesarios escribir por sentido común.

---

## 6. Recomendaciones del analista

1. **Consciencia del cliente:** en la mayoría de los casos el cliente no sabe bien qué necesita o quiere; y cuando lo sabe, lo expresa en su propio lenguaje. Por eso, al identificar y analizar debe haber un **diálogo asertivo**.
2. **Gana-gana:** al identificar requisitos, el ingeniero debe tener en cuenta que todos ganan: todos felices (acuerdo en el que las partes involucradas salen beneficiadas).
3. Al cliente (cliente normal) solo se le comparten **casos de uso y diagrama de actividades**; si es una empresa de software, sí se puede compartir todo.

---

## 7. Modelo de diseño

### 7.1 Agenda del tema

1. Introducción al diseño
2. Enfoques del diseño
3. Principios del diseño
4. Documentación del diseño
5. Patrones de diseño
6. Diseño de la IU (interfaz de usuario)

### 7.2 Niveles de abstracción (pirámide del desarrollo)

1. **Dominio del problema (nivel superior):**
   - Conceptos → modelo de dominio
   - Requerimientos → casos de uso
2. **Diseño (nivel intermedio):**
   - Alto nivel → paquetes
   - Bajo nivel → clases
3. **Implementación (nivel básico):**
   - Código fuente

### 7.3 Definiciones

- **Diseño:** representación/solución **conceptual** de la solución de un problema. Se define la solución: es algo pensado/en la mente, pero no es el producto; no se ha materializado/implementado.
- **Modelo:** representación abstracta/simplificada de algo que debe cumplir la característica de **responder preguntas sobre ese algo**. Debe ser claro y entendible por los demás. La interpretación debe ser **única**; si no brinda información precisa/exacta y puede tener muchas interpretaciones o percepciones, entonces no es un modelo.
- **Diseñar:** proceso de crear una representación conceptual de la solución del problema.

### 7.4 ¿Quién lo realiza?

El **arquitecto** y el **diseñador**:
- El **arquitecto** define las soluciones significativas o de **alto nivel** del sistema y se las entrega al **diseñador**.
- El **diseñador** diseña el código, el cual debe corresponder a una solución conceptual que queda implícita en el código.

### 7.5 ¿Por qué es necesario diseñar? (beneficios)

- Permite/facilita la **planificación** del producto
- **Asegura calidad**
- Facilita la **comunicación** con el equipo técnico y el cliente
- **Previene errores** al implementar
- **Demuestra el entendimiento** de la solución planteada
- **Disminuye costos**
- Facilita el **mantenimiento** de la aplicación
- Facilita la **asignación de responsabilidades** en el equipo de trabajo

### 7.6 ¿Cuál es el resultado de diseñar?

Los **modelos** que representan la arquitectura y los modelos que representan los diseños de bajo nivel, a través de vistas:
- Vista lógica
- Vista de escenarios
- Vista de procesos

### 7.7 ¿Cómo se hace? Enfoques de diseño

Técnicas: modelado dirigido por el dominio del problema.

Enfoques:
- **Top-down:** tomar el problema complejo y dividirlo en problemas pequeños, enfocando la solución en esos problemas pequeños (*divide y vencerás*).
- **Bottom-up:** partir de problemas pequeños y, a partir de ellos, construir un sistema más complejo. Ejemplo: unir productos ya diseñados para escalar a la solución de un problema más complejo (sistema de contabilidad: A tiene inventario, B tiene gestión de clientes y externos, C tiene otro módulo; A, B y C se unen para resolver el sistema de contabilidad).
- **Combinación de ambos.**
- Si es pertinente, se puede dividir el problema en **subproblemas** (si la complejidad lo permite).

**¿Cómo elegir el enfoque? Preguntas:**
- ¿Qué tipo de aplicación voy a construir?
- ¿Qué funcionalidades debe cumplir el sistema?
- ¿Qué arquitecturas de referencia voy a utilizar?

---

## 8. Arquitectura en capas (Manual, cap. 1 y 2)

- **Capa transversal:** la que debe estar presente en las demás capas (solo mencionarlas, saber que existen).
- **Capa de presentación**
- **Capa lógica**, compuesta por:
  - **Business entities:** constituido por los objetos de negocio del contexto del problema; su principal propósito es tener una representación, a nivel del sistema, de dichos objetos en el mundo real.
  - **Business components**
  - **Business workflow:** constituido por el diagrama de actividades; representa el flujo.
- **Capa de datos**

---

## 9. Principios de diseño

- **Separación de preocupaciones:** va de la mano con el enfoque top-down (divide y vencerás). Los módulos del sistema se construyen de acuerdo con aquello que nos preocupa: cada preocupación la resuelve una parte, dividiendo las preocupaciones para que un responsable las resuelva.
  - *Preocupaciones:* definir bien el comportamiento del sistema, forma de guardar los datos, seguridad, etc.
- **Abstracción:** al hacer una abstracción, se toma el objeto analizado y solo se observan algunas características (las que interesan). Consiste en separar lo fundamental de lo irrelevante: ocultar lo irrelevante y mostrar lo esencial; ocultar los detalles y centrar la atención en lo relevante.
- **Encapsulamiento:** agrupar es la primera acción al momento de encapsular, y determinar el ámbito/acceso de los elementos o clases que constituyen el sistema:
  - **Público:** cualquiera puede acceder.
  - **Privado:** solo la clase puede acceder.
  - **Protegido:** cualquiera dentro del paquete puede acceder.
  - Se hace el **ocultamiento de la información** para proteger el sistema.
- **Independencia funcional:** *(tarea pendiente de clase)*
- **DRY (Don't Repeat Yourself):** evitar la redundancia; no hacer lo mismo dos veces.
- **Cierre común:** todas las clases que cambian juntas deben permanecer juntas.
- **KISS (Keep It Simple):** todo lo que se haga a nivel de diseño debe ser simple; no inventar soluciones complejas; hacer las cosas de la forma más sencilla.

### 9.1 Principios SOLID

- **S — Single Responsibility:** cada elemento/parte del sistema debe cumplir una sola responsabilidad; solo debe existir un motivo para que un módulo cambie, y ese motivo está asociado a la responsabilidad.
- **O — Open/Close**
- **L — Liskov Substitution Principle**
- **I — Interface Segregation**
- **D — Dependency Inversion Principle**

---

## 10. Pendientes / tareas

- [ ] Leer el capítulo de casos de uso de *UML y Patrones* de Craig Larman (cap. 6, 2ª edición).
- [ ] Leer los capítulos 1 y 2 del Manual (capas de la arquitectura).
- [ ] Leer las reglas de negocio del contexto del problema en el que se trabaja.
- [ ] Documentar cada actividad con la plantilla de Craig Larman.
- [ ] Tarea: desarrollar el principio de **independencia funcional**.
# Notas Unificadas: Ingeniería de Software — Del Negocio al Diseño

> Documento consolidado de las notas de clase, organizado en módulos que van desde la visión holística de la ingeniería de software hasta el diseño de la solución: modelo de negocio, requisitos, especificación, UML, proyectos de grado y modelo de diseño, con sus artefactos, preguntas guía, principios y recomendaciones.

---

## Módulo 1: Visión Holística y Fundamentos de Ingeniería de Software

### 1.1 Concepto de Software

Se define como un producto resultante de un proceso de creación estructurado que abarca:

**Requisitos → Diseño → Desarrollo → Prueba → Mantenimiento** (correctivo, predictivo y de mejora).

### 1.2 Gestión del Proceso y Roles

Los proyectos consumen recursos: **tiempo, talento humano, dinero y tecnología**. La gestión y el desarrollo son **transversales**. Roles clave del equipo:

- **Gestor de proyectos:** administra tiempo, dinero y talento humano.
- **Ingeniero de requisitos:** identifica y especifica las necesidades.
- **Arquitecto y Diseñador:** define la estructura y el diseño del sistema.
- **Programador:** implementa el código.
- **Experto en pruebas (Tester):** garantiza la verificación del producto.
- **Gestión de calidad:** aplica estándares (IEEE e ISO) para comprobar el cumplimiento.

**Fundamentos:** la ingeniería de software se sustenta en matemáticas, ciencias de la computación y otras disciplinas.

### 1.3 Código de Ética Profesional (IEEE-CS / ACM)

Establece que los ingenieros de software deben comprometerse con la **seguridad, salud y bienestar social**. Consta de **8 principios fundamentales**:

1. **Sociedad:** actuar de manera congruente con el interés social (es el principio primordial).
2. **Cliente y Empresario:** conciliar los intereses del cliente con el bienestar social.
3. **Producto:** asegurar los más altos estándares profesionales posibles.
4. **Juicio:** mantener integridad e independencia en el juicio profesional.
5. **Administración:** promover un enfoque ético en la gestión del desarrollo.
6. **Profesión:** incrementar la reputación e integridad de la profesión.
7. **Colegas:** ser justos y apoyar a los colegas.
8. **Personal:** participar en el aprendizaje continuo durante toda la vida.

---

## Módulo 2: Metodologías de Desarrollo y el Proceso Unificado (RUP)

### 2.1 Componentes Generales de Toda Metodología

- Actividades
- Responsables
- Entregables
- Características distintivas
- Consecuencias

Los ingenieros seleccionan metodologías basadas en el **análisis de ventajas y desventajas**, no por moda.

### 2.2 El Proceso Unificado de Desarrollo de Software (RUP)

**Características principales:** es **dirigido por casos de uso**, **centrado en la arquitectura** e **iterativo e incremental**.

**Fases de RUP:**

1. **Inicio:** se identifican requisitos y riesgos iniciales.
2. **Elaboración:** se consolidan los requisitos y el modelo de negocio, se define la arquitectura del sistema y se inicia la implementación sólida.
3. **Construcción:** fortalecimiento de la implementación, ejecución de pruebas y despliegue inicial.
4. **Transición:** entrega formal del producto al cliente (paso del entorno de desarrollo al de producción) y verificación de satisfacción.

**Guía visual (`rup.jpg`):** muestra cómo las distintas *disciplinas* (Modelado de negocio, Requisitos, Análisis y Diseño, Implementación, Pruebas, Despliegue, etc.) varían en intensidad de esfuerzo a lo largo de las 4 fases y sus iteraciones (`E1, E2`, `C1, C2...`, `T1, T2`).

### 2.3 Objetivos Metodológicos en la Asignatura

1. Definir el Modelo de Negocio
2. Especificar e identificar requisitos
3. Diseñar (aplicando patrones)
4. Implementar
5. Probar

---

## Módulo 3: Análisis del Modelo de Negocio

### 3.1 Definiciones y propósito

- **Modelado de negocio:** técnica de análisis del contexto del problema con el fin de identificar:
  - Procesos
  - Actividades
  - Reglas de negocio
  - Responsables de los procesos
  - Intereses
  - Recursos
- **Modelo de negocio:** representación que hace el ingeniero de software para demostrar que entiende el contexto del problema por medio de **planos de software**. Equivale al *modelo del contexto del problema*: el entendimiento del problema y su representación a través de artefactos.
- **Negocio = Contexto del problema.** Por tanto: **Modelo de negocio = Modelo del contexto del problema**.
- **Propósito:** representar el **contexto del problema** (no la solución). El modelo de negocio está presente en todas las etapas: modelo de negocio, requisitos, implementación y despliegue.

> ⚠️ **Regla clave:** No se debe involucrar la solución en el modelo de negocio (p. ej., no usar verbos como "DETECTA" que ya implican la solución). No se debe poner como nombre de un caso de uso el nombre de la solución.

**¿Quién lo realiza?** El **arquitecto/analista**.

### 3.2 Preguntas clave para construir el modelo de negocio


| Pregunta                                           | Subsidiarias / Orientación                                                            |
| -------------------------------------------------- | ------------------------------------------------------------------------------------- |
| ¿Quiénes intervienen? (participantes/involucrados) | ¿Qué interés tiene cada uno? ¿Cuáles son sus responsabilidades?                       |
| ¿Qué procesos existen?                             | ¿Cuáles son las entradas? ¿Cuáles son las salidas? ¿Cuáles son las reglas de negocio? |


- **¿Quiénes intervienen?** orienta sobre todo la **identificación de funcionalidades**: para cada actor del sistema hay unas funcionalidades.
- **Propósitos del contexto del problema:** identificar la **esencia** (ejemplo: *prevenir la deserción*). ¿Cómo se logran? La respuesta da pie a los **procesos de negocio**.

### 3.3 Elementos del contexto del problema

- **Objeto de estudio (OE):** el problema que se va a resolver (p. ej., prevenir la deserción estudiantil, la gestión de ventas).
- **Ámbito:** el entorno donde se ubica el problema (p. ej., la universidad).
- **Esencia / propósito del negocio:** lo que se quiere lograr.

**Ejemplos:**

- **Deserción estudiantil:**
  - Objeto de estudio: prevenir la deserción.
  - Ámbito: la universidad.
  - Preguntas detonantes: ¿qué procesos realizan las instituciones de educación superior para evitar la deserción estudiantil? ¿Cómo se puede evitar la deserción estudiantil (en diferentes situaciones)?
- **Gestión de ventas:**
  - Actores: cliente, administrador, dueño, vendedor.
  - Nota: aunque una persona haga dos o más roles, los roles se deben mantener separados; el rol no se ve como una persona.

### 3.4 Artefactos del modelo de negocio

1. **Procesos de negocio** → se plasman en un **diagrama de actividades** (de calle/carril).
2. **Actividades de negocio** (casos de uso) → se plasman en un **diagrama de casos de uso**.
3. **Modelo de dominio** → clases conceptuales, atributos y relaciones entre ellos.
4. **Glosario** → lista de palabras o tecnicismos de un mismo campo de estudio o texto, ordenados alfabéticamente, junto con sus definiciones o comentarios.

Notas sobre los artefactos:

- Los **responsables de los procesos, intereses y recursos** nos llevan a identificar objetos y relaciones (**modelo de dominio**).
- Para **evitar ambigüedades** contamos con el **glosario**.
- Cada actividad del diagrama de calle/carril corresponde a un **caso de uso** para el actor dentro del diagrama de casos de uso. El nombre del caso de uso **inicia con un verbo en infinitivo**.
- Al identificar actores, incluir también el *adviser* dentro del contexto del problema.

### 3.5 Conceptos fundamentales: proceso, actividad y acción


| Concepto      | Definición                                                                                                                                |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Proceso**   | Secuencia de actividades que se realizan en el tiempo. Tiene el mayor nivel de abstracción.                                               |
| **Actividad** | Secuencia de acciones que se realizan en el tiempo. Más detallada que el proceso; una actividad puede tener internamente más actividades. |
| **Acción**    | No puede dividirse en otras acciones o actividades; es **atómica**. Está dentro de una actividad.                                         |


Jerarquía de abstracción: **proceso &gt; actividad &gt; acción**.

### 3.6 Casos de uso y documentación

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

**¿Por qué no deben ir términos técnicos en un glosario o en una definición de especificación de requisitos?**  
Porque el glosario y las especificaciones están dirigidos a todos los involucrados (incluido el cliente, que no domina el lenguaje técnico). El glosario debe contener términos del **contexto del problema**, no términos propios de ingeniería de software. Usar tecnicismos introduce ambigüedades y malas interpretaciones: el objetivo del glosario es justamente eliminar ambigüedades usando un lenguaje común, claro y entendible por todos los interesados.

### 3.7 Diferencia fundamental: Modelo de Dominio vs. Ingeniería de Requisitos

- El **Modelo de Dominio** busca entender **cómo funciona el negocio**.
- La **Ingeniería de Requisitos** busca identificar **las necesidades que requiere la solución de software**.

### 3.8 Requisitos implícitos

- **Requisitos implícitos:** requisitos que no son necesarios escribir por sentido común.

### 3.9 Recomendaciones del analista

1. **Consciencia del cliente:** en la mayoría de los casos el cliente no sabe bien qué necesita o quiere; y cuando lo sabe, lo expresa en su propio lenguaje. Por eso, al identificar y analizar debe haber un **diálogo asertivo**.
2. **Gana-gana:** al identificar requisitos, el ingeniero debe tener en cuenta que todos ganan: todos felices (acuerdo en el que las partes involucradas salen beneficiadas).
3. Al cliente (cliente normal) solo se le comparten **casos de uso y diagrama de actividades**; si es una empresa de software, sí se puede compartir todo.

---

## Módulo 4: Ingeniería de Requisitos (Ciclo de Vida de Requisitos)

### 4.1 Requerimiento vs. Requisito

- **Requerimiento:** solicitud o petición directa del cliente (lo que el cliente expresa que quiere).
- **Requisito:** condición o característica formal que debe cumplir el software en la solución entregada.

### 4.2 Fases del Proceso de Ingeniería de Requisitos

1. **Identificación / Elicitación:** el ingeniero de requisitos, junto con el cliente, usuario final, experto del dominio y el arquitecto, recopilan necesidades usando técnicas de recolección (entrevistas, talleres, análisis del modelo de negocio, casos de uso).
2. **Análisis de Requisitos:** comprende tres tareas esenciales:
  - **Organizar:** agrupar por procesos, actores o casos de uso.
  - **Clasificar:** en **Funcionales** (acciones que realiza el sistema) y **No Funcionales / Atributos de Calidad** (propiedades que caracterizan cómo se ejecutan las acciones y agregan valor). *(Nota: los atributos de calidad solo son requisitos si el cliente los solicita o negocia; de lo contrario son agregados de calidad.)*
  - **Priorizar:** clasificación en **Alta** (si se quita, el producto pierde su esencia o deja de funcionar), **Media** (no afecta la esencia pero agrega valor) y **Baja** (impacto mínimo si se omite). Se acuerda mediante negociación entre cliente, ingenieros y arquitectos.
3. **Especificación:** documentación formal e inambigua para que todos los involucrados entiendan lo mismo.
4. **Validación:** evaluación en equipo (Ingeniero de requisitos + Cliente + Arquitecto) para verificar que los requisitos especificados satisfacen las necesidades reales mediante pruebas de validación.
5. **Gestión:** proceso transversal para mantener la trazabilidad y el control de versiones a lo largo del tiempo.

---

## Módulo 5: Especificación del Documento de Requisitos (ISO/IEC/IEEE 29148)

### 5.1 Criterios de Calidad del Documento de ER

Debe ser: **Correcto, Sin ambigüedades, Completo, Consistente, Organizado jerárquicamente, Verificable, Modificable y Trazable**.

### 5.2 Estructura del ERS/SRS según la Norma ISO/IEC/IEEE 29148

1. **Introducción:**
  - *Propósito:* objetivo del software.
  - *Ámbito:* alcance, nombre del producto, beneficios y metas.
  - *Visión general del producto:* perspectiva del producto (relación con otros sistemas), funciones principales, características de los usuarios y limitaciones (políticas, hardware, seguridad).
  - *Definiciones:* glosario técnico exclusivo del contexto del problema (sin términos propios de ingeniería de software).
2. **Referencias:** documentos fuente citados.
3. **Requisitos Específicos:**
  - *Interfaces externas:* entradas y salidas del sistema, usuarios, hardware, software y comunicaciones.
  - *Funciones:* secuencia exacta de operaciones, validez de entradas y manejo de errores.
  - *Capacidad de Uso:* criterios medibles de efectividad, eficiencia y satisfacción del usuario.
  - *Rendimiento:* métricas estáticas (usuarios simultáneos, capacidad) y dinámicas (transacciones/tiempo).
  - *Bases de Datos:* tipos de datos, frecuencia, entidades, relaciones y retención.
  - *Restricciones de diseño:* cumplimiento de estándares y regulaciones.
  - *Atributos de calidad:* confiabilidad, disponibilidad, seguridad (criptografía, privacidad) y portabilidad.
  - *Información de soporte:* muestras de formatos (ej. formato Kardex), antecedentes o estudios.
4. **Verificación:** métodos, métricas y criterios de aceptación definidos en paralelo a la sección de requisitos específicos.
5. **Apéndices:** suposiciones, dependencias y acrónimos.

---

## Módulo 6: Lenguaje de Modelado UML (Modelo Conceptual de UML)

### 6.1 ¿Qué es UML?

Lenguaje de modelado visual **estandarizado** y **orientado a objetos** para especificar, visualizar, construir y documentar artefactos de software.

### 6.2 Modelo Conceptual DE UML (Estructura interna del lenguaje)

1. **Bloques de Construcción (Building Blocks):**
  - *Cosas / Elementos (Things):*
    - **Estructurales:** clases, interfaces, casos de uso, componentes, nodos.
    - **De comportamiento:** interacciones y máquinas de estados.
    - **De agrupación:** paquetes.
    - **De anotación:** notas.
  - *Relaciones:* **Dependencia, Asociación, Generalización** ("es un tipo de" / herencia) y **Realización**.
  - *Diagramas:* composiciones gráficas (Casos de Uso, Clases, Secuencia, Actividad, Estados, Componentes).
2. **Reglas (Rules):** normas de combinación en cuanto a Nombres, Alcance, Visibilidad (público, privado, protegido), Integridad y Ejecución.
3. **Mecanismos Comunes:** Especificaciones textuales, Adornos visuales, Divisiones comunes (clase/objeto) y **Mecanismos de Extensibilidad** (Estereotipos `« »`, Valores etiquetados y Restricciones).

---

## Módulo 7: Formulación de Proyectos de Grado en Ingeniería (Ruta Semántica del Profe Monroy)

### 7.1 Definición

**Proyecto de Grado en Ingeniería:** trabajo de **investigación aplicada** basado en el **proceso de diseño en ingeniería** (no investigación científica básica), cuyo fin es resolver un problema concreto creando un producto o servicio.

### 7.2 Ruta Semántica de Formulación (Paso a Paso)

1. **Definición del Objeto de Estudio (OE):** selección del tema o problema específico dentro de una línea de investigación.
2. **Análisis del Objeto de Estudio:**
  - *Caracterización:* ubicar el OE en su contexto (Ámbito geográfico/legal, Situaciones, Participantes con sus Intereses y Recursos).
  - *Estudio del Estado de la Técnica (Estado del Arte):* combinar la revisión de la literatura científica con el análisis de la realidad concreta para identificar **Brechas** (lo pendiente por resolver) mediante una matriz comparativa.
3. **Consolidación Teórica (Marco de Referencia):**
  - *Marco Conceptual:* representación visual (mapa conceptual) que sintetiza la esencia del OE y su contexto.
  - *Marco Teórico, Legal, Histórico y Contextual:* teorías y normatividad que respaldan técnicamente la investigación.
4. **Formulación del Problema:** definición de la **Pregunta de Investigación** y la **Hipótesis** basadas directamente en las brechas identificadas.
5. **Formalización del Planteamiento del Problema:**
  - *Título, Descripción del Problema y Justificación:* demostrar la **Pertinencia** (conveniencia en el contexto), **Relevancia** (beneficios para los participantes) y **Viabilidad** (disponibilidad de recursos).
  - *Objetivos:* **Objetivo General** (responde a la pregunta de investigación: *qué + para qué + cómo*) y **Objetivos Específicos** (hitos del método).
  - *Alcance:* delimitación Conceptual, Espacial/Geográfica, Temporal, Productos esperados e Impactos.
6. **Diseño Metodológico:**
  - *Enfoque:* Cuantitativo, Cualitativo o Mixto.
  - *Fuentes y Recolección de Datos:* Población, muestra, instrumentos y protocolos.
  - *Procesamiento de Datos:* técnicas de análisis (ej. modelado conceptual, estadística).
  - *Método / Procedimiento:* metodología de ingeniería de software a utilizar (ej. RUP, Scrum, Design Thinking).
  - *Recursos y Validez:* presupuesto, talento humano, cronograma (Gantt) y estrategias de validez/rigor.

---

## Módulo 8: Modelo de Diseño

### 8.1 Agenda del tema

1. Introducción al diseño
2. Enfoques del diseño
3. Principios del diseño
4. Documentación del diseño
5. Patrones de diseño
6. Diseño de la IU (interfaz de usuario)

### 8.2 Niveles de abstracción (pirámide del desarrollo)

1. **Dominio del problema (nivel superior):**
  - Conceptos → modelo de dominio
  - Requerimientos → casos de uso
2. **Diseño (nivel intermedio):**
  - Alto nivel → paquetes
  - Bajo nivel → clases
3. **Implementación (nivel básico):**
  - Código fuente

### 8.3 Definiciones

- **Diseño:** representación/solución **conceptual** de la solución de un problema. Se define la solución: es algo pensado/en la mente, pero no es el producto; no se ha materializado/implementado.
- **Modelo:** representación abstracta/simplificada de algo que debe cumplir la característica de **responder preguntas sobre ese algo**. Debe ser claro y entendible por los demás. La interpretación debe ser **única**; si no brinda información precisa/exacta y puede tener muchas interpretaciones o percepciones, entonces no es un modelo.
- **Diseñar:** proceso de crear una representación conceptual de la solución del problema.

### 8.4 ¿Quién lo realiza?

El **arquitecto** y el **diseñador**:

- El **arquitecto** define las soluciones significativas o de **alto nivel** del sistema y se las entrega al **diseñador**.
- El **diseñador** diseña el código, el cual debe corresponder a una solución conceptual que queda implícita en el código.

### 8.5 ¿Por qué es necesario diseñar? (beneficios)

- Permite/facilita la **planificación** del producto
- **Asegura calidad**
- Facilita la **comunicación** con el equipo técnico y el cliente
- **Previene errores** al implementar
- **Demuestra el entendimiento** de la solución planteada
- **Disminuye costos**
- Facilita el **mantenimiento** de la aplicación
- Facilita la **asignación de responsabilidades** en el equipo de trabajo

### 8.6 ¿Cuál es el resultado de diseñar?

Los **modelos** que representan la arquitectura y los modelos que representan los diseños de bajo nivel, a través de vistas:

- Vista lógica
- Vista de escenarios
- Vista de procesos

### 8.7 ¿Cómo se hace? Enfoques de diseño

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

### 8.8 Arquitectura en capas (Manual, cap. 1 y 2)

- **Capa transversal:** la que debe estar presente en las demás capas (solo mencionarlas, saber que existen).
- **Capa de presentación**
- **Capa lógica**, compuesta por:
  - **Business entities:** constituido por los objetos de negocio del contexto del problema; su principal propósito es tener una representación, a nivel del sistema, de dichos objetos en el mundo real.
  - **Business components**
  - **Business workflow:** constituido por el diagrama de actividades; representa el flujo.
- **Capa de datos**

### 8.9 Principios de diseño

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

#### Principios SOLID

- **S — Single Responsibility:** cada elemento/parte del sistema debe cumplir una sola responsabilidad; solo debe existir un motivo para que un módulo cambie, y ese motivo está asociado a la responsabilidad.
- **O — Open/Close**
- **L — Liskov Substitution Principle**
- **I — Interface Segregation**
- **D — Dependency Inversion Principle**

---

## Pendientes / Tareas

- [ ] Leer el capítulo de casos de uso de *UML y Patrones* de Craig Larman (cap. 6, 2ª edición).
- [ ] Leer los capítulos 1 y 2 del Manual (capas de la arquitectura).
- [ ] Leer las reglas de negocio del contexto del problema en el que se trabaja.
- [ ] Documentar cada actividad con la plantilla de Craig Larman.
- [ ] Tarea: desarrollar el principio de **independencia funcional**.
# NOTAS UNIFICADAS — Ingeniería de Software

> Fusión de **NotasClase.md**, **Notas_Rangel.md**, **Notas_Jairo.md** y **NotasNewin.md**.
> Se conserva toda la información original: solo se eliminaron las repeticiones entre fuentes,
> se integraron los matices complementarios y se unificó la presentación.
> Cuando dos fuentes decían lo mismo con detalles distintos, se integraron ambos detalles.

---

## Módulo 1: Visión Holística y Fundamentos de Ingeniería de Software

### 1.1 Concepto de software

Se define como un producto resultante de un proceso de creación estructurado que abarca:
Tambien se define por la ieee como 
>"La aplicación de un enfoque sistemático, disciplinado y cuantificable al desarrollo, >operación y mantenimiento de software; es decir, la aplicación de la ingeniería al software"

**Requisitos → Diseño → Desarrollo → Prueba → Mantenimiento** (correctivo, predictivo y de mejora).

En la asignatura el proceso se sigue como: 1) Modelo de negocio (modelo del contexto del problema), 2) Requisitos, 3) Diseñar, 4) Desarrollo, 5) Probar, 6) Mantenimiento *(nota personal: se agrega **Desplegar** como paso 5 entre desarrollo y pruebas)*.

### 1.2 Gestión del proceso y roles

Los proyectos consumen recursos: **tiempo, talento humano, dinero y tecnología**. La gestión y el desarrollo son **transversales**. Roles clave del equipo:

| Rol | Responsabilidad |
|---|---|
| Gestor de proyectos | Administra tiempo, dinero y talento humano |
| Ingeniero de requisitos | Identifica y especifica las necesidades |
| Arquitecto y diseñador | Define la estructura y el diseño del sistema |
| Programador | Implementa el código |
| Experto en pruebas (Tester) | Garantiza la verificación del producto |
| Gestión de calidad | Aplica estándares (IEEE e ISO) para comprobar el cumplimiento |

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

### 2.1 Componentes generales de toda metodología

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

### 2.3 Objetivos metodológicos en la asignatura

1. Definir el Modelo de Negocio
2. Especificar e identificar requisitos
3. Diseñar (aplicando patrones)
4. Implementar
5. Probar

---

## Módulo 3: Análisis del Modelo de Negocio

### 3.1 ¿Qué es un negocio?

Cualquier tipo de actividad —económica o no—; en el contexto de ingeniería de software, el negocio es el **modelo del contexto del problema** (toda actividad que haga referencia al problema a resolver). Por tanto: **Negocio = Contexto del problema**, y **Modelo de negocio = Modelo del contexto del problema**.

### 3.2 Modelado de negocio vs. modelo de negocio

- **Modelado de negocio:** es el **proceso/actividad dentro** del modelo de negocio; es cómo se llega a él. **Técnica de análisis del contexto del problema** con el fin de identificar **procesos, actividades, reglas de negocio, responsables/involucrados (de actividades y procesos), intereses y recursos**. Se logra mediante técnicas de recolección de información que ayuden a responder todas las incógnitas del contexto. *(Referencia: "Análisis del contexto" — guía del trabajo de grado / libro.)*
- **Modelo de negocio:** **representación** que hace el ingeniero de software —por medio de **planos de software**— para demostrar que **entiende el contexto del problema**. Es el resultado del modelado (modelo del contexto del problema: el entendimiento del problema y su representación a través de artefactos). El modelo de negocio está presente en todas las etapas: modelo de negocio, requisitos, implementación y despliegue.

> ⚠️ **Regla clave:** no se debe involucrar la solución en el modelo de negocio (p. ej., no usar verbos como "DETECTA" que ya implican la solución). No se debe poner como nombre de un caso de uso el nombre de la solución.

**¿Quién lo realiza?** El **analista de sistemas** (rol de arquitecto/analista).

### 3.3 Preguntas para construir el modelo de negocio

| Pregunta | Subsidiarias / Orientación |
|---|---|
| ¿Quiénes son los actores / quiénes intervienen en el contexto del problema? | ¿Qué interés tiene cada uno de los involucrados? ¿Cuáles son sus responsabilidades? → orienta la identificación de **funcionalidades**: para cada actor hay funcionalidades |
| ¿Qué procesos existen? | ¿Cuáles son las entradas? ¿Cuáles son las salidas? ¿Cuáles son las reglas de negocio? |

- **¿Cómo se logra el objetivo (objeto de estudio)?** → la respuesta da pie a los **procesos de negocio**, que se encuentran definidos por las **reglas de negocio**.
- **Propósitos del contexto del problema:** identificar la **esencia** (ejemplo: *prevenir la deserción*). ¿Cómo se logra? → procesos de negocio.

### 3.4 Elementos del contexto del problema

El contexto del proyecto está compuesto por **participantes**, que tienen **objetivos**, que influyen **situaciones** en las que participan, y en ellas usan **recursos**.

- **Objeto de estudio (OE):** el problema que se va a resolver (p. ej., prevenir la deserción estudiantil; la gestión de ventas). Incluye su **caracterización**: ubicar el OE en su contexto.
- **Ámbito:** el entorno donde se ubica el problema (p. ej., la universidad).
- **Esencia / propósito del negocio:** lo que se quiere lograr.

**Ejemplos:**

- **Deserción estudiantil:**
  - Objeto de estudio: prevenir la deserción.
  - Ámbito: la universidad.
  - Preguntas detonantes: ¿qué procesos realizan las instituciones de educación superior para evitar la deserción estudiantil? ¿Cómo se puede evitar la deserción estudiantil (en diferentes situaciones)?
- **Gestión de ventas** (proyecto: *¿cómo se gestionan las ventas en la empresa?*):
  - Actores: cliente, administrador, dueño, vendedor.
  - **Los participantes se distinguen por el rol que cumplen, no por la persona que lo cumple.** Aunque una persona haga dos o más roles, los roles se deben mantener separados; el rol no se ve como una persona.

### 3.5 Artefactos de la representación (4)

| # | Artefacto | Qué es / cómo se hace |
|---|---|---|
| 1 | **Procesos de negocio** | Diagrama de actividades UML de **calle/carril (swimlane)**, con el responsable de las actividades para cada actor. Los participantes, junto con sus procesos de interacción, se representan con el diagrama de actividades UML. El **proceso principal está conformado por actividades de negocio**. |
| 2 | **Actividades de negocio** (= casos de uso de la vida real) | Diagrama de **casos de uso**. Cada actividad del diagrama de carril corresponde a un caso de uso del actor. Se usa el **nombre del proceso de negocio** (contexto) como referencia; el nombre del caso de uso **inicia con un verbo en infinitivo**. |
| 3 | **Modelo de dominio** | Clases conceptuales (entidades), atributos y relaciones entre ellos (ver Módulo 4). |
| 4 | **Glosario** | Lista de palabras o tecnicismos de un mismo campo de estudio o texto, en **orden alfabético**, con sus definiciones o comentarios. **Solo términos referentes al contexto del problema**. |

**Responsable:** analista del sistema.

Notas sobre los artefactos:

- Los **responsables de los procesos, intereses y recursos** nos llevan a identificar objetos y relaciones (**modelo de dominio**).
- Para **evitar ambigüedades** contamos con el **glosario**.
- Al identificar actores, incluir también el *adviser* dentro del contexto del problema.

### 3.6 Conceptos fundamentales: proceso, actividad y acción

| Concepto | Definición |
|---|---|
| **Proceso** | Secuencia de actividades que se realizan en el tiempo. Tiene el **mayor nivel de abstracción**. Surge al preguntar *¿cómo se logra el objetivo (objeto de estudio)?* |
| **Actividad** | Secuencia de acciones que se realizan en el tiempo. Más detallada que el proceso; una actividad puede tener internamente más actividades. |
| **Acción** | No puede dividirse en otras acciones o actividades; es **atómica**. Está dentro de una actividad. |

Jerarquía de abstracción: **proceso > actividad > acción**. Al crear el modelado de negocio se debe decidir, para cada actividad del proceso general, con qué nivel de detalle se detalla.

### 3.7 Casos de uso de la vida real y su documentación

- Cada actividad se documenta usando la **plantilla de Craig Larman** (libro *UML y Patrones*, Krai Lamhar, 2ª edición, capítulo 6). La plantilla incluye:
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
Porque el glosario y las especificaciones están dirigidos a todos los involucrados (incluido el cliente, que no domina el lenguaje técnico). El glosario debe contener términos del **contexto del problema**, no términos propios de ingeniería de software. Usar tecnicismos introduce ambigüedades y malas interpretaciones: el objetivo del glosario es eliminar ambigüedades usando un lenguaje común, claro y entendible por todos los interesados.

### 3.8 Diferencia fundamental: modelo de dominio vs. ingeniería de requisitos

- El **modelo de dominio** busca entender **cómo funciona el negocio** (contexto del problema).
- La **ingeniería de requisitos** busca identificar **las necesidades que requiere la solución de software**.

Un caso de uso en el capítulo de modelado de negocio se hace bajo el contexto del **problema**; en la ingeniería de requisitos, bajo el contexto de la **solución**.

### 3.9 Requisitos implícitos

- **Requisitos implícitos:** requisitos que no es necesario que el cliente nos senale, sino que  por sentido común podemos entender que es necesario.

### 3.10 Recomendaciones del analista

1. **Consciencia del cliente:** en la mayoría de los casos el cliente no sabe bien qué necesita o quiere; y cuando lo sabe, lo expresa en su propio lenguaje. Por eso, al identificar y analizar debe haber un **diálogo asertivo**.
2. **Gana-gana:** al identificar requisitos, el ingeniero debe tener en cuenta que todos ganan: todos felices (acuerdo en el que las partes involucradas salen beneficiadas).
3. Al cliente (cliente normal) solo se le comparten **casos de uso y diagrama de actividades**; si es una empresa de software, sí se puede compartir todo.

### 3.11 Nota: rigor normativo

El nivel del proceso de modelado de negocio tiene que ser **riguroso**: debe incluir toda la información normativa vigente requerida, dependiendo del país donde se haga el proceso (**Colombia**).

---

## Módulo 4: Modelo de Dominio

### 4.1 Definición

Modelo **visual** que identifica los **objetos del problema** y sus **relaciones** de manera abstracta (el concepto del problema). Es la representación visual y conceptual que describe las **clases conceptuales (entidades)**, sus **atributos**, **roles** y **relaciones** dentro de un problema del mundo real. Se representa mediante un **modelo de dominio**.

### 4.2 Enfoque sistemático para construirlo (pasos unificados)

**Paso 1 — Identificar los posibles objetos del problema.**
Se usa un **análisis gramatical** sobre la descripción del problema (del negocio): los **sustantivos** se toman como *posibles objetos del sistema* y los **verbos** como acciones y relaciones de los mismos. (No todos los sustantivos entran: se tienen que analizar.)

**Paso 2 — Extraer los que verdaderamente son parte del modelo de dominio** (parte del problema, **no de la solución**). Para cada posible objeto se pregunta —con dos formulaciones complementarias de las notas:

- *"¿Si se retira este objeto del contexto del problema, éste seguiría siendo completo?"* — es decir, qué objetos no son relevantes o indispensables en la definición del problema; si son indispensables se quedan, si no se van.
- *"Si este objeto desaparece, ¿cómo afecta al sistema?"*

**Paso 3 — Representar los objetos gráficamente.**
Se arma el gráfico del modelo de dominio representando los objetos ya definidos mediante las **clases conceptuales de UML**.

**Paso 4 — Establecer las relaciones entre los objetos.**
Cada relación debe poseer un **verbo**, una **multiplicidad** y un **orden** que sea coherente con el modelo de negocio. Luego se representan.
### 4.3 Lista de Categorias conceptuales:
Se tienen X categorias y se buscan palabras que correspondan a esas categorias en el contexto de nuestro problema, luego se analiza si realmente son necesarias apra nuestro problema.
• Objetos físicos o tangibles: (Ej: Registradora, Avión, Artículo).
• Transacciones: (Ej: Venta, Pago, Reserva).
• Lugares: (Ej: Tienda, Almacén).
• Roles de personas: (Ej: Cajero, Cliente, Piloto).
• Especificaciones o descripciones: (Ej: EspecificaciónDeProducto — crucial para Larman para no perder información si se elimina un objeto físico).
• Contenedores: (Ej: Tienda, CarritoDeCompras)
### 4.4 Notas de presentación

- El modelo de dominio es un **diagrama de objetos, no de clases**.
- **Nombres en mayúscula** y **no en plural**.
- Los responsables de los procesos, los intereses y los recursos son los que nos llevan a identificar los objetos y relaciones del modelo de dominio.

---

## Módulo 5: Ingeniería de Requisitos (Ciclo de Vida de Requisitos)

### 5.1 Requerimiento vs. requisito

- **Requerimiento:** solicitud o petición directa del cliente (lo que el cliente expresa que quiere).
- **Requisito:** condición o característica formal que debe cumplir el software en la solución entregada.

### 5.2 Fases del proceso de ingeniería de requisitos

1. **Identificación / Elicitación:** el ingeniero de requisitos, junto con el cliente, usuario final, experto del dominio y el arquitecto, recopilan necesidades usando técnicas de recolección (entrevistas, talleres, análisis del modelo de negocio, casos de uso).
2. **Análisis de requisitos:** comprende tres tareas esenciales:
   - **Organizar:** agrupar por procesos, actores o casos de uso.
   - **Clasificar:** en **Funcionales** (acciones que realiza el sistema) y **No Funcionales / Atributos de Calidad** (propiedades que caracterizan cómo se ejecutan las acciones y agregan valor). *Nota: los atributos de calidad solo son requisitos si el cliente los solicita o negocia; de lo contrario son agregados de calidad.*
   - **Priorizar:** clasificación en **Alta** (si se quita, el producto pierde su esencia o deja de funcionar), **Media** (no afecta la esencia pero agrega valor) y **Baja** (impacto mínimo si se omite). Se acuerda mediante negociación entre cliente, ingenieros y arquitectos.
3. **Especificación:** documentación formal e inambigua para que todos los involucrados entiendan lo mismo.
4. **Validación:** evaluación en equipo (Ingeniero de requisitos + Cliente + Arquitecto) para verificar que los requisitos especificados satisfacen las necesidades reales mediante pruebas de validación.
5. **Gestión:** proceso transversal para mantener la **trazabilidad** y el control de versiones a lo largo del tiempo.

### 5.3 Criterios de calidad del documento de requisitos

Debe ser: **Correcto, Sin ambigüedades, Completo, Consistente, Organizado jerárquicamente, Verificable, Modificable y Trazable**.

### 5.4 Especificación del documento de ER (ISO/IEC/IEEE 29148)

Estructura del ERS/SRS según la norma:

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

### 5.5 Criterio de evaluación de un requisito no funcional

**Nota de clase (21/09/2026).** El criterio de evaluación de un requisito no funcional describe **qué tendrá/garantizará el programa** para cumplir el requisito (una característica del producto), **NO** una métrica de medición (por ejemplo, ">90 % de las operaciones" mide, no garantiza).

**Ejemplo acertado** (capacidad de uso – Intuitividad): *"el promedio de los operadores y clientes debe ser capaz de operar el sistema sin presentar fricción cognitiva; la curva de aprendizaje del aplicativo es baja"*. Eso describe lo que el diseño del programa aporta: una interfaz con baja carga cognitiva y curva de aprendizaje baja.

### 5.6 Notas de clase sobre requisitos y calidad

- **Usabilidad** = facilidad de uso.
- Las **definiciones** del documento deben estar en **orden alfabético** y **no deben tener términos técnicos** (van dirigidas a todos los involucrados, incluido el cliente).
- **Tabla de trazabilidad** de los requisitos, **en tiempo real**, para la sustentación.
- **Interfaces externas:** en etapa de requisitos **es una interfaz externa si el cliente lo pide**; si el cliente no lo pide, en los requisitos no es interfaz externa (depende del contexto en el que se esté haciendo la identificación).
- **Atributos de calidad:** ¿**prioridad suficiente** o poner **metas sobre cómo se cumple** el requisito de calidad? Lo que debe ir en un requisito de calidad: **requisito, en qué consiste, cómo se va a garantizar y prioridad**.
- Es importante haber identificado los requisitos de calidad pertinentes para el proyecto; más no es el punto focal del curso, porque lo que no se verifica con rigurosidad es la validez técnica del requisito en el contexto.

---

## Módulo 6: Lenguaje de Modelado UML (Modelo Conceptual de UML)

*Referencia del curso: **UML y Patrones** — Krai Lamhar.*

### 6.1 ¿Qué es UML?

Lenguaje de modelado visual **estandarizado** y **orientado a objetos** para especificar, visualizar, construir y documentar artefactos de software.

### 6.2 Estructura interna del lenguaje (modelo conceptual de UML)

1. **Bloques de construcción (building blocks):**
   - *Cosas / elementos (things):*
     - **Estructurales:** clases, interfaces, casos de uso, componentes, nodos.
     - **De comportamiento:** interacciones y máquinas de estados.
     - **De agrupación:** paquetes.
     - **De anotación:** notas.
   - *Relaciones:* **dependencia, asociación, generalización** ("es un tipo de" / herencia) y **realización**.
   - *Diagramas:* composiciones gráficas (casos de uso, clases, secuencia, actividad, estados, componentes).
2. **Reglas:** normas de combinación en cuanto a **nombres, alcance, visibilidad** (público, privado, protegido), **integridad** y **ejecución**.
3. **Mecanismos comunes:** especificaciones textuales, adornos visuales, divisiones comunes (clase/objeto) y **mecanismos de extensibilidad** (estereotipos `« »`, valores etiquetados y restricciones).

---

## Módulo 7: Formulación de Proyectos de Grado en Ingeniería (Ruta Semántica — Profe Monroy)

### 7.1 Definición

**Proyecto de Grado en Ingeniería:** trabajo de **investigación aplicada** basado en el **proceso de diseño en ingeniería** (no investigación científica básica), cuyo fin es resolver un problema concreto creando un producto o servicio.

### 7.2 Ruta semántica de formulación (paso a paso)

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
2. Enfoques de diseño
3. Principios de diseño
4. Cómo se documenta el diseño
5. Patrones de diseño
6. Diseño de la IU (interfaz de usuario)

### 8.2 Niveles de abstracción (pirámide del desarrollo)

1. **Dominio del problema (nivel superior):**
   - Conceptos → modelo de dominio
   - Requerimientos → casos de uso
2. **Diseño (nivel intermedio):**
   - Alto nivel(Diseno de Arquitecutra) → paquetes
   - Bajo nivel(Diseno de bajo nivel) → clases
3. **Implementación (nivel básico):**
   - Código fuente

### 8.3 Definiciones

- **Diseño:** representación/solución **conceptual** de la solución de un problema. Es lo que pensamos y no hemos implementado; se define la solución, está en la mente, pero no se ha materializado ni implementado. *Si somos buenos ingenieros no generamos la solución sin haber pensado antes.* El diseño resuelve problemas.
- **Modelo:** representación abstracta y **simplificada** de un sistema (o de algo) que debe poder ser **entendido por los demás**, **responder preguntas** sobre ese algo y proveer información sobre lo que se está representando. Debe ser claro, coherente y su interpretación debe ser **única (unívoca)**: si no brinda información precisa/exacta y puede tener muchas interpretaciones o percepciones, entonces **no es un modelo**.
- **Diseñar:** el proceso de realizar una representación conceptual de la solución del problema.

### 8.4 ¿Quién lo realiza?

El **arquitecto** y el **diseñador**:

- El **arquitecto** define las soluciones significativas o de **alto nivel** del sistema y se las entrega al **diseñador**.
- El **diseñador** diseña el código, el cual debe corresponder a una solución conceptual que queda implícita en el código.

### 8.5 ¿Por qué es necesario diseñar? (beneficios)

- Permite/facilita la **planificación** del producto y establece una manera sistemática de llegar a la solución.
- **Asegura calidad.**
- Facilita la **comunicación** asertiva de las ideas, con el equipo técnico y con el cliente.
- **Previene errores** al implementar.
- **Demuestra el entendimiento** de la solución planteada.
- **Disminuye costos.**
- Facilita el **mantenimiento** de la aplicación y ayuda a corroborar que se hizo todo.
- Facilita la **asignación de responsabilidades** en el equipo de trabajo.
- Facilita la **implementación** de la solución.
- Permite **disminuir riesgos**.

### 8.6 ¿Cuál es el resultado?

Los **modelos** que representan la arquitectura y los modelos que representan los diseños de bajo nivel, a través de vistas:

- **Vista lógica** (de sistemas)
- **Vista de escenarios**
- **Vista de procesos**

### 8.7 ¿Cómo se diseña? Enfoques de diseño

Técnicas: modelado dirigido por el dominio del problema.

- **Top-down:** tomar la totalidad del problema y dividirlo progresivamente en problemas más pequeños, hasta llegar a problemas atómicos (*divide y vencerás*).
- **Bottom-up:** partir de problemas pequeños y, a partir de ellos, construir un sistema más complejo. Ejemplo: unir productos ya diseñados para escalar a la solución de un problema más complejo (sistema de contabilidad: A tiene inventario, B tiene gestión de clientes y externos, C tiene otro módulo; A, B y C se unen para resolver el sistema de contabilidad).
- **Combinación de ambos.**
- Si es pertinente, se puede dividir el problema en **subproblemas** (si la complejidad lo permite).

**Preguntas para elegir el enfoque:**

1. ¿Qué tipo de aplicación voy a construir?
2. ¿Qué tipo de funcionalidades debe cumplir el sistema?
3. ¿Qué arquitectura(s) de referencia voy a usar?

### 8.8 Arquitectura del sistema

**Arquitectura en capas** AW:

- **Capa transversal:** la que debe estar presente en las demás capas (solo mencionarlas, saber que existen).

- Seguridad / Gestion Operacion / Comunicacion 
- **Capa de Cliente**: El browser
- **Web Server**:
   - **Capa de presentación.**
   - **Capa lógica (business layer)**, compuesta por:
      - **Business entities:** está constituido por los **objetos de negocio del contexto del problema**; su principal propósito es tener una representación, a nivel del sistema, de dichos objetos del mundo real. Se basa en el **modelo de dominio**.
      - **Business components:** se basa en los **casos de uso / requisitos funcionales**.
      - **Business workflow:** está constituido por el **diagrama de actividades** y busca representar el **flujo**.
   - **Capa de datos.**: Base de datos

### 8.9 Principios de diseño

1. **Separación de preocupaciones:** va de la mano con el enfoque top-down (divide y vencerás). Los módulos del sistema se construyen de acuerdo con aquello que nos preocupa: cada preocupación la resuelve una parte, dividiendo las responsabilidades para que ciertos responsables las resuelvan.
   - *Preocupaciones:* definir bien el comportamiento/funcionamiento del sistema, la forma de guardar los datos, la seguridad, etc.
2. **Abstracción:** al hacer una abstracción se toma el objeto analizado y solo se observan las características de mayor interés. Consiste en separar lo fundamental de lo irrelevante: ocultar los detalles irrelevantes para la implementación y centrar la atención en lo relevante.
3. **Encapsulamiento:** el primer paso a la hora de encapsular es **agrupar**; luego se determina el **ámbito/acceso** de las clases/elementos del sistema:
   - **Público:** cualquiera puede acceder.
   - **Privado:** solo la clase puede acceder.
   - **Protegido:** cualquiera dentro del paquete puede acceder.
   - Se hace el **ocultamiento de la información** para proteger el sistema.
4. **Independencia funcional:** *(sin definir en las notas de clase — pendiente).*
5. **DRY (Don't Repeat Yourself):** evitar la redundancia; no repetir las cosas más de lo necesario; hágalo una vez y reúsalo.
6. **Cierre común:** todas las clases que cambian juntas deben permanecer juntas, por facilidad del proceso de diseño (las clases que cambian por las mismas razones y al mismo tiempo se agrupan en el mismo componente o paquete).
7. **KISS (Keep It Simple Stupid):** todo lo que se haga a nivel de diseño debe ser simple; no inventar soluciones complejas; hacer las cosas de la forma más sencilla (tan simple que hasta un tonto lo entienda).

### 8.10 Principios de diseño — SOLID

1. **S — Single Responsibility:** cada elemento/parte del sistema debe cumplir **una sola responsabilidad**; solo debe existir un motivo para que un módulo cambie, y ese motivo debe estar relacionado con su responsabilidad.
2. **O — Open/Close** (abierto/cerrado).
3. **L — Liskov Substitution Principle** (sustitución de Liskov).
4. **I — Interface Segregation** (segregación de interfaces).
5. **D — Dependency Inversion Principle** (inversión de dependencias).

---

## Módulo 9: Entregable de la Iteración 3 (capítulo de Modelo de Negocio)

El entregable de la Iteración 3, y donde se va a hablar del modelo/modelado de negocio, es el **manual de sistema**. Este manual se debe desarrollar según la guía publicada en la carpeta de Iteración III (*manual de sistema*); para la Iteración 3 solo se va a desarrollar hasta el **capítulo 2, de ingeniería de requisitos**.

Es importante notar que hay diferentes modelos iguales que se tienen que realizar para el capítulo 2, y es necesario hacer una pertinente diferenciación de conocimientos y contexto de ambos capítulos: un caso de uso en el capítulo de modelado de negocio se hace bajo el contexto del **problema**, mientras que en la ingeniería de requisitos se hace bajo el contexto de la **solución**.

El entregable es en forma de documento. En caso de ser necesario para esta iteración se pueden subir los archivos hechos por la herramienta Enterprise Architect (`.eaq`), más para las siguientes iteraciones es algo totalmente necesario.

---

## Apéndice A: Registro cronológico de las notas de clase (NotasNewin)

| Fecha | Tema tratado |
|---|---|
| 17/09/2026 | Proceso de la asignatura (requisitos, diseñar, desarrollo, pruebas, mantenimiento); modelado de negocio: definición, identificación (procesos, actividades, reglas, responsables, intereses, recursos), 4 artefactos resultantes, responsable: analista de sistemas, técnicas de recolección; referencia "Análisis del contexto" (guía del trabajo de grado) |
| 24/09/2026 | ¿Qué es un negocio? (actividad económica o no = contexto del problema); quiénes intervienen; intereses de los involucrados; proceso / actividad / acciones |
| 25/09/2026 | Caracterización del objeto de estudio; procesos de negocio (¿cómo se logra el objetivo?, definidos por reglas de negocio; conformado por actividades de negocio); participantes por rol, no por persona; participantes + procesos de interacción → diagrama de actividades UML; actividades de negocio: nombre del proceso (contexto), verbos en infinitivo, plantilla de documentación, descripción de casos de uso |
| 01/10/2026 | Modelo de dominio: definición y 5 pasos (identificar objetos por sustantivos, filtrar ("si desaparece, ¿cómo afecta?"), representar, relaciones con multiplicidad); nota: nombres en mayúscula y no en plural |
| 02/10/2026 | Modelo de diseño: agenda; requisitos implícitos; pirámide de niveles de abstracción; definiciones de diseño, modelo (interpretación unívoca) y diseñar; quién diseña; por qué diseñar; resultado (vistas); enfoque top-down |
| 08/10/2026 | Preguntas para elegir el enfoque de diseño (tipo de aplicación, funcionalidades, arquitecturas de referencia) |
| 09/10/2026 | Arquitectura del sistema (business layer / business workflow); principios de diseño (separación de preocupaciones, abstracción, encapsulamiento, independencia funcional, DRY, cierre común, KISS); principios SOLID |

---

## Apéndice B: Pendientes registrados en las notas

- **Independencia funcional:** principio listado en las tres fuentes de clase sin definición pendiente de completar.
- *"Mañana se va a hablar de las arquitecturas"* (pendiente anotado en NotasClase; tratado posteriormente el 09/10 según NotasNewin).
- **Personas de interés en el proyecto:** pendiente por completar (pregunta guía del modelado de negocio, NotasClase §2.4).

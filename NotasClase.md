# NOTAS DE CLASE — Ingeniería de Software

Notas de clase del curso. Se conserva el contenido original; la organización en
secciones, subtítulos y listas es solo editorial.

---

## 1. Conceptos generales de UML y de requisitos

- **UML y Patrones** — Krai Lamhar.

### 1.1 Requisitos

- **Usabilidad** = facilidad de uso.
- Las **definiciones** deben estar en **orden alfabético** y **no deben tener términos técnicos**.
- **Tabla de trazabilidad** de los requisitos, en tiempo real, para la sustentación.

#### Interfaces externas

Depende del contexto en el que se esté haciendo la identificación de la interfaz:
en etapa de requisitos **es una interfaz externa si el cliente lo pide**; si el
cliente no lo pide, en los requisitos **no es interfaz externa**.

#### Atributos de calidad

- ¿**Prioridad suficiente** o poner **metas sobre cómo se cumple** el requisito de
  calidad?
- Lo que debe ir en un requisito de calidad: **requisito, en qué consiste, cómo se
  va a garantizar y prioridad**.

> **Nota**
> Es importante que hayamos identificado los requisitos de calidad pertinentes para
> el proyecto; más no es el punto focal del curso, porque lo que no se verifica con
> rigurosidad es la validez técnica del requisito en el contexto.

#### Nota (21/09/2026) — Criterio de evaluación de un requisito no funcional

El criterio de evaluación de un requisito no funcional describe **qué
tendrá/garantizará el programa** para cumplir el requisito (una característica del
producto), **NO** una métrica de medición (por ejemplo, ">90 % de las operaciones"
mide, no garantiza).

**Ejemplo acertado** (capacidad de uso – Intuitividad): "el promedio de los
operadores y clientes debe ser capaz de operar el sistema sin presentar fricción
cognitiva; la curva de aprendizaje del aplicativo es baja". Eso describe lo que el
diseño del programa aporta: una interfaz con baja carga cognitiva y curva de
aprendizaje baja.

---

## 2. Modelo de negocio

### 2.1 Qué es

**Modelo de negocio:** representación del contexto del problema por medio de planos
de software; representación que hace el ingeniero de software para demostrar que
entiende el contexto del problema.

### 2.2 Diferencia entre modelado de negocio y modelo de negocio

- **Modelado de negocio:** es una **actividad dentro** del modelo de negocio, es
  decir, es cómo se llega al modelo de negocio. Es la **técnica de análisis del
  contexto del problema** que nos lleva a identificar **procesos, actividades, reglas
  de negocio, responsabilidades y las personas que las tienen, y recursos**.
- **Modelo de negocio:** es la **representación** que hace el ingeniero para
  demostrar que comprende el negocio.

### 2.3 Proceso de Isoft

1. Modelo de negocio (modelo del contexto del problema)
2. Requisitos
3. Diseñar
4. Desarrollo
5(mio). Desplegar 
5. Probar
6. Mantenimiento

### 2.4 Preguntas para poder hacer un modelado de negocio

1. **¿Quiénes son los actores?** (¿Quiénes intervienen en el contexto del problema?)
2. **¿Qué intereses tiene cada uno de los involucrados en el contexto del
   problema?**
   → Nos orienta a las funcionalidades del sistema, es decir, ayuda a la formación de
   qué debe hacer el sistema.

> **Personas de interés en nuestro proyecto:** _pendiente por completar._

### 2.5 Análisis del contexto

El contexto del proyecto está compuesto por **participantes**, que tienen
**objetivos**, que influyen **situaciones** en las que participan los participantes, y
en ellas usan **recursos**.

### 2.6 Artefactos de la representación

Los artefactos son hechos en medio del entendimiento del problema y su
representación. Son **4**:

| # | Artefacto | Qué es / cómo se hace |
|---|---|---|
| 1 | **Procesos de negocio** | Se usa UML para graficarlo: **carriles de UML (swimlanes)**, con el responsable de las actividades para cada actor. *
| 2 | **Casos de uso de la vida real** | (= actividades de negocio) | Casos de Uso.
| 3 | **Modelo de dominio** | | Representacion visual y conceptual que describe las clases conceptuales(entidades), atributos, roles y relaciones dentro de un problema de el mundo real.| Modelo Entidad-Relacion
| 4 | **Glosario** | Listado de términos con sus definiciones, en orden alfabético. Debe contener exclusivamente los términos importantes para el contexto. |

**Responsable:** analista del sistema.


### Nota:
El nivel de el proceso de modelado de  negocio tiene que ser riguroso, es decir, tiene que incluir toda la informacion normativa vigente requerida, dependiendo del pais donde se haga el proceso(Colombia).

## 3. Modelo conceptual de UML

*(Transcrito de `Notas_Rangel.md`, Módulo 6.)*

### 3.1 ¿Qué es UML?

Lenguaje de modelado visual **estandarizado** y **orientado a objetos** para especificar, visualizar, construir y documentar artefactos de software.

### 3.2 Estructura interna del lenguaje

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

## 4. Proceso, actividad y acción

Dada la línea delgada entre uno u otro, es necesario entender el nivel de abstracción a usar para la documentación de los procesos. Sin embargo, hay cosas que no son pertinentes o muy importantes para el proceso de negocio: para cada actividad del proceso general, parto y verifico con qué nivel de detalle detallo cada proceso o actividad.

Al crear el modelado de negocio se debe tener en cuenta que:

- Una **acción** es la ejecución atómica del proyecto.
- Una **actividad** es un conjunto de actividades y acciones.
- Los **procesos** son conjuntos de actividades, acciones o procesos secuenciales.

---

## 5. Modelo de dominio

### 5.1 Actividades de negocio

*(sin apuntes)*

### 5.2 Análisis gramatical

Se representa mediante un **modelo entidad-relación**.

**Enfoque sistemático para construir un modelo de dominio:**

1. Se crea una descripción del problema y se analiza la frase creada.
2. **Sustantivos → objetos del modelo** (no todos: se tienen que analizar).
3. **Cómo se relacionan esos objetos → relaciones.**
4. Luego los represento.

---

## 6. Entregable Iteración 3 (capítulo de Modelo de Negocio)

El entregable de la Iteración 3, y donde se va a hablar del modelo/modelado de negocio, es el **manual de sistema**. Este manual se debe desarrollar según la guía publicada en la carpeta de Iteración III (*manual de sistema*); para la Iteración 3 solo se va a desarrollar hasta el **capítulo 2, de ingeniería de requisitos**.

Es importante notar que hay diferentes modelos iguales que se tienen que realizar para el capítulo 2, y es necesario hacer una pertinente diferenciación de conocimientos y contexto de ambos capítulos: un caso de uso en el capítulo de modelado de negocio se hace bajo el contexto del **problema**, mientras que en la ingeniería de requisitos se hace bajo el contexto de la **solución**.

El entregable es en forma de documento. En caso de ser necesario para esta iteración se pueden subir los archivos hechos por la herramienta Enterprise Architect (`.eaq`), más para las siguientes iteraciones es algo totalmente necesario.

---

## 7. Modelo de diseño

### 7.1 Agenda de la clase (puntos a tratar)

1. Introducción al diseño
2. Enfoque de diseño
3. Principio de diseño
4. Cómo se documenta el diseño
5. Patrones de diseño
6. Diseño de la UI

### 7.2 Definiciones

- **Diseño:** ideas, algo que pensamos. El diseño es lo que pensamos y no hemos implementado. Si somos buenos ingenieros no generamos la solución sin haber pensado antes. Representación conceptual de la solución del problema. El diseño resuelve problemas.
- **Modelo:** representación abstracta de un sistema, simplificada y visual. Debe poder responder preguntas sobre ese algo; debe ser entendible, claro, coherente.
- **Diseñar:** el proceso de realizar una representación conceptual de la solución del problema.
- **¿Quién diseña?** Arquitecto y diseñador.

### 7.3 ¿Por qué es necesario diseñar?

- Nos sirve para establecer una manera sistemática de llegar a la solución.
- Disminuye costos.
- Facilita el mantenimiento de la aplicación.
- Ayuda a corroborar que se hizo todo.
- Facilita la asignación de responsabilidades.
- Ayuda a la comunicación asertiva de las ideas.
- Permite disminuir riesgos.

### 7.4 ¿Cuál es el resultado?

Los modelos de diseño: **vista lógica**, **vista de escenarios** y **vista de procesos**.

### 7.5 ¿Cómo se diseña? Enfoques de diseño

Se enuncian **3 enfoques**; las notas solo detallan dos:

- **Top-down:** de problemas más grandes se dividen en problemas más pequeños, y así infinitamente, hasta llegar a problemas atómicos (*divide y vencerás*).
- **Bottom-up:** *(sin detalle en las notas)*
- **Tercer enfoque:** *(sin anotar)*

**Preguntas para elegir el enfoque:**

1. ¿Qué tipo de aplicación voy a construir?
2. ¿Qué tipo de funcionalidades debe cumplir el sistema?
3. ¿Qué arquitectura de referencia voy a usar?

### 7.6 Diseño WS

- **Business entities:** se basa en el modelo de dominio.
- **Business components:** se basa en los casos de uso / requisitos funcionales.
- **Business workflow:** diagrama de actividades.

### 7.7 Principios de diseño

1. **Separación de preocupaciones:** entender, aplica *divide y vencerás*: entiendes qué módulos tienen que hacer qué, repartes las responsabilidades de los procesos a diferentes módulos, porque no todo debe recaer en un módulo.
2. **Abstracción:** tomo un objeto esencial que estoy analizando y lo separo de su contexto; observo solo algunas características. Separa aquello que es fundamental de lo que es irrelevante. Ocultamos los detalles irrelevantes para la implementación.
3. **Encapsulamiento:** agrupar es la primera acción al momento de encapsular, y determinar el ámbito/acceso (que sustituye mi sistema).
4. **Independencia funcional**
5. **DRY:** no te repitas a ti mismo; hágalo una vez y reúsalo.
6. **Cierre común:** principio de diseño de arquitectura de software que establece que las clases que cambian por las mismas razones y al mismo tiempo deben agruparse en el mismo componente o paquete.
7. **KISS:** hazlo tan simple que hasta un tonto lo entienda.
8. ...

### 7.8 Principios de diseño — SOLID

1. **Single Responsibility:** una clase debe tener una, y solo una, razón para cambiar; es decir, debe encargarse de una única tarea o funcionalidad | responsabilidad.
2. **Open/Close**
3. **Liskov Substitution Principle**
4. **Interface Segregation**
5. **Dependency Inversion Principle**

---

## 8. Tareas pendientes

- Mañana se va a hablar de las arquitecturas.
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

# Nuevo/Sin organizar

### Proceso vs actividad
Dada la linea delgada entre uno u otro, es necesario entender el nivel de abstraccion a usar para la documentacion de los procesos, sinembargo, hay cosas que no son pertinentes, o muy importantes para el proceso de negocio, para cada actividad del proceso general, parto y verifico con que nivel de detalle detallo cada proceso o actividad.

A la hora de crear el modelado de negocio, se debe tener en cuenta que, una accion, es la ejecucion atomica de el proyecto, la actividad es un cojunto de actividades y acciones, y los procesos, son cojuntos de activiades, acciones o procesos secuenciales

---
### Actividades de negocio:
### Modelo de Dominio:
Analisis gramatical:
Se representa mediante Modelo Entidad Relacion
Enfoque sistematico para construir un modelo de dominio:
Se crea una descripcion de el problema, se analiza la frase creada, 
Sustantivos-> Objetos de el modelo, no todos, se tienen que analizar
Como se relacionan esos objetos -> Relaciones.
Luego los represento

## 3. Modelo conceptual de UML

*(sección pendiente en las notas)*

## Entregable Iteracion 3(Capitulo de Modelo de Negocio):
El entregable de la iteracion 3 y donde se va a hablar de el modelo/modelado de negocio, es el manual de sistema, este manual se debe desarrollar segun la guia publicada en la carpeta de iteracion III, de manual de sistema, para la iteracion 3 solo se va a desarrollar hasta el capitulo 2, de ingieneria de requisitos. 
Es importante notar, que hay diferentes modelos iguales que se tienen que realizar, para el capitulo 2, y es necesario hacer una pertinente diferenciacion de conocimientos y contexto de ambos capitulos, un caso de uso en el capitulo de modelado de negocio, se hace bajo el contexto de el problema, mas en la ingieneria de requisitos, se hace bajo el contexto de la solucion.

El entregable es en forma de el documento, en caso de ser necesario para sta iteracion se pueden subir los archivos hechos por  la herramienta Enterprise Architect, .eaq., mas para las siguientes iteraciones es algo totalmente necesario.

## Modelo de Diseño
### Agenda de la clase (Puntos a tratar):
1. introduccion al diseño
2. Enfoque de diseño
3. Principio de diseño
4. Como se documenta el diseño
5. Patrones de diseño
6. Diseño de la UI

### 2.
Que es Diseño?
Ideas, algo que pensamos: Diseño es lo que pensamos y no hemos implementado.
Si somos buenos ingenieros no generamos la solucion, sin haber pensado antes.
Representacion conceptual de la solucion del problema.
El diseño resuelve problemas. 

### Que es modelo?
Es una representacion abstracta de un sistema, simplificada y visual.
Debe poder responder preguntas sobre ese algo, debe ser entendible, claro, coherente.

### Que es diseñar?
El proceso de realizar una representacion conceptual de la solucion problema

### Quien diseña?
Arquitecto y diseñador

### Porque es necesario?
- Nos sirve para establecer una manera sistematica de llegar a la solucion.
- Disminuye Costos
- Facilita Mantenimiento de la Aplicacion
- Ayuda a corroborar que se hizo todo
- Facilita asignacion de responsabilidades
- Ayuda a la comunicacion asertiva de las ideas
- Permite disminuir riesgos

### Cual es el resultado?

Los modelos de diseño.
Vista Logica, Vista de escenarios, Vista de procesos

Como se diseña?
3 enfoques de diseño
Top-down: De problemas mas grandes se dividen en problemas mas pequeños, y asi infinitamente, hasta llegar a problemas atomicos, 
bottom-up:

## Preguntas:
1. Que tipos de apliacion voy a construir?
2. QUe tipo de funcionalidades debe cumplir el sistema?
3. Que arquitectura de referencia voy a usar


## Diseño WS
Bunisses Entities: Se basa en el modelo de dominio
Bunisses Components: Se basa en los casos de uso/Requisitos Funcionales
Business Workflow: Diagrama de Actividades
## Principio de Diseños 
1. Separacion de Preocupaciones: Entender, aplica divide y venceras, entiendes que modulos tienen que hacer que, repartes las responsabilidades de los procesos, a diferentes modulos, porque no todo debe recaer en un modulo.
2. Abstraccion: Tomo un objeto escencial que estoy analizando, y lo separo de su contexto, observo solo algunas caracteristicas, Separa aquello que es fundamental de lo que es irrelevante.Ocultamos los detalles irrelevantes para la implementacion.
3. Encapsulamiento: agrupar es la primera accion al momento de encapsular, y determinar el ambito/acceso, que sustituye mi sistema()
4. Independencia Funcional
5. DRY: NO te repitas a ti mismo, hagalo una vez y reuselo
6. Cierre Comun: principio de diseño de arquitectura de software que establece que las clases que cambian por las mismas razones y al mismo tiempo deben agruparse en el mismo componente o paquete
7. KISS: Hazlo tan simple que hasta un tonto lo entienda, 
8. ...
## Principios de Diseño - SOLID 
1. Single Responsability:Una clase debe tener una, y solo una, razón para cambiar; es decir, debe encargarse de una única tarea o funcionalidad|Responsabilidad.
2. Open Close:
3. Liskov Substitution Principle
4. Interface Segregation
5. Dependency Inversion Principle
## Tarea:
1. Que tipos de aplicacion vamos a contruir
3. Mañana se va a hablar de las arquitecturas
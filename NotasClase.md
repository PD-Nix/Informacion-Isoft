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

### 2.3 Proceso de ISoft

1. Modelo de negocio (modelo del contexto del problema)
2. Requisitos
3. Diseñar
4. Desarrollo
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
| 1 | **Procesos de negocio** | Se usa UML para graficarlo: **carriles de UML (swimlanes)**, con el responsable de las actividades para cada actor. *(nota incompleta en clase: "se coloca un ...")* |
| 2 | **Casos de uso de la vida real** | (= actividades de negocio) |
| 3 | **Modelo de dominio** | |
| 4 | **Glosario** | Listado de términos con sus definiciones, en orden alfabético. Debe contener exclusivamente los términos importantes para el contexto. |

**Responsable:** analista del sistema.

El nivel de el proceso de negocio tiene que ser riguroso, es decir, tiene que incluir toda la informacion normativa vigente requerida, dependiendo del pais donde se haga el proceso(Colombia).
# Nuevo/Sin organizar
### Proceso vs actividad
Dada la linea delgada entre uno u otro, es necesario entender el nivel de abstraccion a usar para la documentacion de los procesos, sinembargo, hay cosas que no son pertinentes, o muy importantes para el proceso de negocio, para cada actividad del proceso general, parto y verifico con que nivel de detalle detallo cada proceso o actividad.
---
### Modelo de Dominio
analisis gramatical:
Se representa mediante ER
Sustantivos-> Objetos de el modelo, no todos, se tienen que analizar
Luego los represento
4. Que relaciones existen entre esos objetos
## 3. Modelo conceptual de UML

*(sección pendiente en las notas)*
## Modelo de Diseño
### Agenda:
1. introduccion al diseño
2. Enfoque de diseño
3. Principio de diseño
4. COmo se documenta el diseño
5. Patrones de diseño
6. Diseño de la UI

### 2.
Que es Diseño?

Ideas, algo que pensamos, Diseño es lo que pensamos y no hemos implementado, si somos buenos ingenieros no generamos la solucion, sin haber pensado antes, representacion conceptual de la solucion del problema. el diseño resuelve problemas, 

Que es modelo?
Es una representacion abstracta de un sistema, simplificada y visual. Debe poder responder preguntas sobre ese algo, debe ser entendible, claro, coherente, 
Que es diseñar?
EL proceso de realizar una representacion conceptual de la solucion problema
Quien diseña?
Arquitecto y diseñador

Porque es necesario?
Nos sirve para establecer una manera sistematica de llegar a la solucion.
Disminuye Costos
Facilita Mantenimiento de la Aplicacion
Ayuda a corroborar que se hizo todo
Facilita asignacion de responsabilidades
Ayuda a la comunicacion asertiva de las ideas
Permite disminuir riesgos

CUal es el resultado?

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


## Tarea:
1. Que tipos de aplicacion vamos a contruir
3. Mañana se va a hablar de las arquitecturas
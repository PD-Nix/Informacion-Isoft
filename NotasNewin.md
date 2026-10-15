17/09/2026

Requisitos
Diseñar
Desarrollo
Probar
Mantenimiento

Modelo de negocios

MODELADO DE NEGOCIOS
Proceso que nos da como resultado el modelo de negocios.
Técnica de análisis del contexto del problema con el fin de identificar procesos, actividades,
reglas de negocio, responsables/involucrados (de actividades y procesos), intereses y
recursos
Se logra mediante una representación de (se obtiene):

●  Procesos del negocio
●  Actividades del negocio (casos de uso)
●  Modelo de dominio
●  Glosario (orden alfabético) (sólo términos referentes al contexto del problema)

está encargado del analista de sistemas

Se deben usar técnicas de recolección de información que nos ayuden a responder todas
las incógnitas

Análisis del contexto guia del trabajo de grado libro

24/09/2026

¿Qué es un negocio?
Cualquier tipo de actividad sea económica o no, en el contexto de ingeniería de software, es
el modelo del contexto del problema (toda actividad que haga referencia al problema a
resolver)

¿Quienes intervienen en el contexto del problema?

➔  ¿Qué intereses tienen cada uno de los involucrados?

proceso

actividad

acciones

25/09/2026

Caracterización del objeto de estudio?

Procesos de negocio

se pregunta: ¿Cómo se logra el objetivo (objeto de estudio)?

(Proyecto: Cómo se gestionan las ventas en la empresa) ⇒ definido por las reglas de
negocio

Proceso principal que está conformado por actividades de negocios

Al identificar a los participantes, se distinguen por el rol que cumplen no por la persona que
lo cumple (ej: cliente, administrador, dueño, vendedor)

Los participantes junto con sus procesos de interacción se representan con un diagrama de
actividades uml.

Actividades de negocio (diagrama de casos de uso):

Se usa el nombre del proceso de negocio
(contexto)

Verbos en infinitivo para las actividades

documentación: plantilla

descripción de casos de uso

1/10/2026

Modelo de dominio:
Es la representación visual y conceptual que describe las entidades, sus atributos, roles y
relaciones dentro de un problema del mundo real.

1.  se identifican los posibles objetos, utilizando identificación gramatical, identificando

los sustantivos de la descripción del problema.

2.  De los sustantivos se definen cuales son verdaderamente elementos del modelo de

dominio, se pregunta: si este objeto desaparece, como afecta al sistema?

3.  Representar los objetos.
4.  Definir las relaciones existentes entre los elementos del modelo, de forma coherente,

se aplica multiplicidad.

Nota: Nombres en mayúscula que no estén en plural.

5.

2/10/2026

Modelo de diseño

introducción al diseño

1.
2.  enfoques de diseño
3.  principios de diseño
4.  documentación del diseño
5.  patrones de diseño
6.  diseño de la iu

Requisitos implícitos: requisitos que no es necesario escribirlos por sentido común.

Dominio del problema (superior)

●  conceptos: modelo de dominio
●
requerimientos:casos de usos

Diseño (intermedio)

●  alto nivel: paquetes
●  bajo nivel: clases

implementación (basico)
●  Código fuente

Diseño:
El diseño es la representación conceptual de la solución de un problema.
Se define la solución, es lo que tenemos en la mente, pero no se ha materializado, ni implementado.

Modelo: representación abstracta, simplificada de un sistema que debe poder ser entendido por los
demás y ser capaz de responder a preguntas y proveer información sobre lo que se está representando.
Debe tener una interpretación unívoca, si no se brinda información precisa no es un modelo.

❖  ¿Qué es diseñar?

Proceso de crear una representación conceptual de la solución de un problema.

❖  ¿Quién lo realiza?

Arquitecto y diseñador
El arquitecto define las soluciones de alto nivel especificas del sistema y las entrega al
diseñador para que defina el código correspondiente a la solución conceptual

❖  ¿Por qué es necesario?

➢  Asegura calidad
➢  previene errores de implementación
➢  demuestra el entendimiento de la solución planteada
➢  disminuye costos
➢  facilita el mantenimiento de la aplicación
➢  facilita la asignación de responsabilidades en el equipo de trabajo
➢  Facilita la comunicación entre el equipo técnico y con el cliente
➢  facilita la implementación de la solución

❖  ¿Cuál es el resultado?

el resultado del proceso de diseño son los modelos que representan la arquitectura y los
modelos de bajo nivel

vista lógica de sistemas
vista de escenarios
vista de procesos

❖  ¿Cómo se hace?

Se utilizan enfoques de diseño

enfoque de diseño top-down: tomamos la totalidad del problema y se va reduciendo en
problemas más pequeños

8/10/2026

¿Qué tipo de aplicación voy a construir?
qué funcionalidades debe cumplir el sistema?
qué arquitecturas de referencia se van a utilizar?

9/10/2026

Arquitectura del sistema

Business layer: Está constituido por los objetos de negocio del contexto del problema, su principal
propósito es tener una representación a nivel de sistema de los objetos del mundo real.

Business workflow: está constituido por diagrama de actividades y busca representar el flujo

Principios de diseño

●  separación de preocupaciones:

Va de la mano con el enfoque top-down, los módulos del sistema se construyen de acuerdo a
aquello que me preocupa lo solucionara cierta parte. y así ir dividiendo las responsabilidades
para que ciertos responsables lo resuelvan.

preocupaciones: definir bien el funcionamiento de un sistema, forma de guardar los datos,
seguridad, etc…

●  abstracción:

se toma un objeto a analizar y solo se observan las características que son de mayor interés,
separar lo fundamental de lo irrelevante, el principio de abstracción consiste en ocultar los
detalles y centrar la atención lo más relevante

●  encapsulamiento:

El primer paso a la hora de encapsular es agrupar.
determinar el ámbito/acceso de las clases/elementos de mi sistema para determinar si lo que
está en las clases es público, privado o protegido

público: cualquiera puede acceder.
privado: sólo la clase puede acceder.
protegido: Cualquiera dentro del paquete puede acceder

Se hace el ocultamiento de la información para proteger al sistema

●

independencia funcional:

●  DRY (Don’t Repeat Yourself):

Evitar la redundancia, no repetir las cosas más de lo necesario

●  Cierre común:

Todas las clases que cambian juntas deben permanecer juntas, por facilidad del proceso de
diseño.

●  KISS:

Nos indica que todo lo que hagamos a nivel de diseño debe de ser simple

Principios de diseño SOLID

●  Single responsibility:

Consiste en que cada elemento del sistema debe de cumplir con una sola
responsabilidad. solo debe existir un motivo para que un módulo cambie y debe estar
relacionado con su responsabilidad

●  Open close:
●
●
●
●  dependency inversion principle

liskov substitution principle
interface segregation


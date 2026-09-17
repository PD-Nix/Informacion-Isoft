# 1. ¿Qué es UML?

UML (Unified Modeling Language o Lenguaje Unificado de Modelado)
es un lenguaje visual estandarizado utilizado para representar,
visualizar, especificar, construir y documentar sistemas, especialmente sistemas de software.

La palabra importante aquí es lenguaje.

UML no es una metodología de desarrollo, ni un lenguaje de programación. Es un conjunto de elementos, reglas y diagramas que permiten representar diferentes aspectos de un sistema.

Por ejemplo, si estamos desarrollando un sistema para una empresa de agua embotellada, antes de programarlo podemos utilizar UML para representar:

Qué personas interactúan con el sistema.
Qué funciones debe realizar.
Qué clases existen.
Cómo se relacionan esas clases.
Cómo interactúan los objetos.
Cómo cambia el estado de un objeto.
Qué componentes forman el sistema.
Cómo se distribuye el software en los equipos.

Por eso UML funciona como una especie de lenguaje común entre las personas que participan en el desarrollo.

# 2. ¿Por qué es necesario UML?

El problema que UML intenta solucionar tiene que ver con la complejidad de los sistemas de software.

Un sistema puede tener cientos o miles de elementos relacionados entre sí. Si intentamos explicar todo únicamente mediante texto, puede ser muy difícil visualizar cómo funciona.

Por ejemplo, decir:

"El cliente realiza un pedido, el pedido contiene productos, el sistema verifica el inventario, posteriormente se genera una factura y finalmente se registra el pago."

UML permite convertir conceptos abstractos en representaciones visuales.

Esto facilita:

Comunicación: los desarrolladores, analistas, diseñadores y clientes pueden hablar sobre el mismo modelo.
Comprensión: permite visualizar sistemas complejos.
Análisis: ayuda a detectar problemas antes de programar.
Diseño: permite definir cómo estará estructurado el sistema.
Documentación: deja una representación del sistema que puede consultarse posteriormente.
Mantenimiento: facilita comprender un sistema existente.
Planificación: ayuda a pensar la solución antes de escribir código.
# 3. Una analogía: UML como los planos de una casa

Esta es probablemente una de las mejores analogías para explicar por qué UML es necesario.

Imagina que quieres construir una casa.

No sería buena idea llegar directamente al terreno con ladrillos y comenzar a construir diciendo:

"Bueno, pongamos una habitación aquí... y después vemos dónde va la cocina."

Antes de construir tienes planos.

En los planos puedes representar:

dónde están las habitaciones;
dónde están las puertas;
dónde están las ventanas;
las conexiones eléctricas;
las tuberías;
las dimensiones;
etc.

El plano no es la casa, pero permite entender cómo será construida.

# Historia.

Pero el modelo conceptual busca identificar  y organizar los conceptos de uml,

3. Things: los elementos de UML

Aquí hay una distinción MUY importante para tu exposición:

Un elemento de UML NO necesariamente es un diagrama.

Y tampoco necesariamente es algo que exista literalmente como código.

Los elementos son conceptos que UML proporciona para que podamos construir modelos.

Por ejemplo:

"Clase" es un elemento de UML.

Pero:

"Diagrama de clases" es un diagrama que utiliza ese elemento.

Y:

"Una clase en Java" es una construcción del lenguaje de programación.

Son tres cosas diferentes.
# 5.1 Clase

Una clase representa un conjunto de objetos que comparten características y comportamiento.
# 5.2 Interfaz

Una interfaz representa un conjunto de operaciones que establece un contrato que otros elementos pueden implementar.
# 5.3 Colaboración

Una colaboración representa cómo varios elementos trabajan conjuntamente para conseguir un determinado comportamiento.

Por ejemplo:

Para registrar un pedido participan Cliente, Pedido, Inventario y Pago.

No significa simplemente que "están relacionados".

La idea es:

varios elementos cooperan para realizar una responsabilidad.

Es especialmente útil para representar comportamientos que requieren la participación de varios elementos.
# 5.4 Caso de uso

El caso de uso representa una funcionalidad o comportamiento que el sistema proporciona a un actor.

Por ejemplo:

"Registrar pedido"

Eso puede ser un caso de uso.

Luego podemos construir un diagrama de casos de uso donde mostramos:
# 5.5 Clase activa

Una clase activa es una clase cuyos objetos pueden tener un comportamiento concurrente, es decir, pueden ejecutar actividades independientemente.

La diferencia conceptual con una clase normal es que una clase activa puede representar algo que mantiene su propio flujo de ejecución.

Por ejemplo, podríamos modelar:

Servidor

como una clase activa porque puede estar ejecutando continuamente procesos mientras otros elementos interactúan con él.

En UML suele distinguirse gráficamente de una clase normal mediante un borde más grueso.
# 5.6 Componente

Un componente representa una parte modular y reemplazable de un sistema.

Por ejemplo conceptualmente:

"Esta es una pieza del sistema que encapsula una funcionalidad y puede interactuar con otras piezas."

Un componente suele representar algo de un nivel más alto que una clase.
# 5.7 Nodo

Un nodo representa un recurso físico o computacional donde pueden ejecutarse o desplegarse elementos del sistema.

Por ejemplo:
odría representar:

un servidor;
un computador;
un dispositivo;
un dispositivo móvil;
otro recurso de procesamiento.

Aquí estamos hablando principalmente de dónde se ejecuta algo, no de qué hace ese software.
6. Elementos de comportamiento

Ahora pasamos de:

¿Qué existe?

a:

¿Qué ocurre?

Los elementos de comportamiento representan aspectos dinámicos del sistema.

Es decir, describen acciones, cambios, interacciones o comportamientos.

Entre los conceptos fundamentales encontramos:

interacción;
máquina de estados;
actividad.
Interacción

Una interacción representa la comunicación entre elementos mediante mensajes para producir determinado comportamiento.

Ejemplo:

Cliente → Sistema : solicitarPedido()
Sistema → Pedido : crearPedido()
Pedido → Inventario : verificar()

La interacción responde:

¿Cómo colaboran los elementos mediante mensajes?

Máquina de estados

Representa los diferentes estados por los que puede pasar un elemento y las transiciones entre ellos.

Ejemplo:

Pendiente
    │
    │ confirmar
    ▼
Preparando
    │
    │ enviar
    ▼
Entregado

Responde:

¿Cómo cambia un elemento a lo largo del tiempo?
Actividad

Una actividad representa un flujo de acciones que se realizan para alcanzar un resultado.

Por ejemplo:

Recibir pedido
      ↓
Verificar inventario
      ↓
Preparar pedido
      ↓
Enviar pedido

Responde:


¿Qué acciones se realizan y en qué flujo?

7. Elementos de agrupación

Aquí tenemos principalmente el concepto de paquete (Package).

Un paquete sirve para agrupar elementos relacionados.

Por ejemplo:

┌─────────────────────────┐
│       <<package>>       │
│       Ventas            │
│                         │
│  Cliente                │
│  Pedido                 │
│  Factura                │
└─────────────────────────┘

No significa que "Ventas" sea una clase.

Es simplemente una forma de organizar elementos del modelo.

Una analogía sencilla:

Un paquete en UML es parecido a una carpeta que organiza archivos relacionados.

8. Elementos de anotación

Finalmente tenemos las anotaciones.

Una anotación permite agregar información explicativa al modelo.

Por ejemplo:

┌───────────────────────┐
│ Pedido                │
└───────────────────────┘
          |
          |
   ┌─────────────────────────┐
   │ Nota:                   │
   │ Un pedido debe contener │
   │ al menos un producto.   │
   └─────────────────────────┘

La anotación no representa una clase, un objeto, un componente, etc.

Su función es explicar, aclarar o documentar alguna parte del modelo.

Son:

Dependencia
Asociación
Generalización
Realización

Y aquí hay una cosa importante:

Generalización ≈ herencia

Cuando hablamos informalmente de herencia, en UML el término más preciso es generalización.

Realización ≈ implementación

Cuando hablamos de que una clase implementa una interfaz, UML utiliza el concepto de realización
3. Asociación

Empecemos con la más intuitiva.

Una asociación representa una relación estructural entre elementos.

Por ejemplo:

Cliente ───────── Pedido

Podemos interpretarlo como:

Un cliente está relacionado con uno o varios pedidos.

O:

Profesor ───────── Curso

Un profesor está relacionado con un curso.

La asociación responde:

"¿Qué elementos están relacionados estructuralmente?"

Ejemplo más completo

Podemos agregar multiplicidades:

Cliente 1 ───────── 0..* Pedido

Esto puede interpretarse como:

Un cliente puede tener cero o muchos pedidos.

La asociación puede además tener un nombre o roles:

Cliente ───── realiza ───── Pedido

Aquí estamos expresando:

El Cliente realiza Pedidos.

4. Dependencia

Ahora tenemos una relación mucho más débil.

Una dependencia significa que un elemento utiliza o depende de otro elemento.

Ejemplo:

ControladorPedido - - - - - > ServicioPago

La flecha discontinua indica dependencia.

Podemos decir:

ControladorPedido depende de ServicioPago.

¿Por qué?

Porque necesita utilizarlo para realizar alguna tarea.

Por ejemplo:

ControladorPedido
       │
       │ utiliza
       ↓
ServicioPago

Si ServicioPago cambia, podría ser necesario modificar ControladorPedido.

5. Diferencia entre asociación y dependencia

Esta es una pregunta MUY probable en una exposición.

Asociación

Representa una relación estructural.

"A está relacionado con B."

Ejemplo:

Cliente ───── Pedido

El cliente tiene una relación relativamente permanente con sus pedidos.

Dependencia

Representa una relación de uso.

"A necesita/utiliza B."

Controlador - - - - > Servicio

El controlador utiliza el servicio para realizar determinada operación.

Analogía

Piensa en una persona y un automóvil:

Asociación:

Una persona tiene un automóvil.

Existe una relación estructural.

Dependencia:

Una persona utiliza un taxi.

La persona depende temporalmente del taxi para transportarse.
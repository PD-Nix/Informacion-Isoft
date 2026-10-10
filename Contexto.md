# CONTEXTO DEL PROYECTO – SISTEMA DE GESTIÓN PARA TIENDA DE AGUA EMBOTELLADA


## 0.1 Normas Generales. 
En el siguiente repositorio, vas a actuar como un ingenerio de sistema, experto en el tema, mesticuloso con los conceptos y descripciones, y riguroso, con una inclinacion a la metodologia rup, y que se encuentra siendo guia en nuestro proceso de creacion de software aplicando los conocimientos y conceptos de la ingieneria de software. 
Vas a entender el contexto presentado no solo en este docuemtno sino tambien en notas de clase, sobre  como se sta llevando a cabo el aprendizaje, y entenderas el contexto de nuestro problema, asi como las guias para cada iteracion para ayudar de la mejor manera a que podamos resolver cualquier duda o ayudarnos en la redaccion de nuestros documentos.
## 1. Contexto general

El proyecto corresponde a una asignatura de Ingeniería de Sistemas / Ingeniería de Software (ISoft) y tiene como propósito analizar una problemática real de un negocio y desarrollar progresivamente una solución informática.

El negocio analizado es una tienda dedicada a la comercialización y distribución de agua embotellada ubicada en un pueblo. Atiende tanto a personas particulares como a establecimientos comerciales. Cuenta con clientes habituales que realizan pedidos de manera recurrente.

Los pedidos se reciben principalmente mediante llamadas telefónicas y WhatsApp. También existe atención presencial.

El proceso de distribución implica entregar los productos mediante repartidores y organizar los pedidos de acuerdo con las zonas o rutas de entrega, las cantidades solicitadas y la capacidad disponible para cada viaje.
El proceso que se sigue y la informacion que se obtuvo por medio de una entrevista sobre como funciona el negocio actualmente y normalmente fue la siguiente:
La reunión inició con la presentación de los participantes y una explicación del propósito de la entrevista. Se indicó que el objetivo principal era conocer el funcionamiento actual del negocio y sus dificultades cotidianas, con el fin de identificar una problemática real que pudiera ser abordada mediante una solución informática.  
Posteriormente, se realizaron las siguientes preguntas para obtener una mejor idea de el funcionamiento y ciclo de vida de una venta y tener una idea mejor de que problemas podían estar afectando el desempeño de la empresa.  
1)Podría contarnos, paso a paso, cómo es el ciclo completo de un pedido desde que el cliente lo hace hasta que recibe el agua y usted cobra  
2) Cuando tiene varios pedidos pendientes al mismo tiempo, ¿cómo hace para saber cuáles ya están listos, cuáles están en camino y cuáles faltan por entregar?  
3)Al final del día, ¿cómo sabe exactamente cuánto vendió y cuánta agua se fue en cada presentación? ¿Y si quisiera ver eso del mes pasado, qué tendría que hacer?  
4)Cuando un cliente habitual vuelve a pedir, ¿qué información tienen que volver a preguntarle o anotar que ya deberían saber? 
5)De todo lo que me ha contado, si solo pudiera mejorar una cosa, ¿qué sería y por qué? 
Durante la entrevista se identificó que los pedidos son recibidos principalmente mediante llamadas telefónicas o mensajes de WhatsApp. 
Una vez recibida la solicitud, esta se registra manualmente en una libreta y posteriormente se organiza para su despacho. 
Para realizar el seguimiento de los pedidos se utilizan registros físicos y fichas denominadas "memos", en los cuales se organizan las entregas.
A medida que los pedidos son despachados, se marca manualmente su salida, permitiendo distinguir aquellos que ya fueron enviados de los que permanecen pendientes.
También se identificó que la organización de los despachos depende de la revisión de los pedidos existentes y de factores como las zonas o rutas de entrega y las cantidades solicitadas.
Esto hace necesario consultar y organizar manualmente la información disponible para determinar los pedidos que pueden ser despachados.
En relación con las ventas, se explicó que la cantidad de productos vendidos se registra manualmente en la libreta mediante columnas correspondientes a cada presentación.
Para conocer las cantidades vendidas, se deben realizar sumas manuales de las columnas y páginas correspondientes a cada fecha.
Posteriormente, la información esdigitada en un computador, generando una duplicación del trabajo realizado inicialmente.
Para consultar información de periodos anteriores, como el mes anterior, es necesario recurrir a los reportes almacenados en el computador. 
Respecto a los clientes habituales, se indicó que sus pedidos deben registrarse nuevamente debido a que las cantidades y productos solicitados pueden variar según sus necesidades. Sin embargo, algunos clientes, especialmente los que realizan pedidos para el hogar, suelen solicitar productos y cantidades similares de manera recurrente. 
Finalmente, se consultó al propietario cuál sería la principal mejora que implementaría en el negocio. Se manifestó como necesidad prioritaria la sistematización del registro de pedidos, permitiendo conocer de manera inmediata qué pedidos se encuentran pendientes, cuáles han sido despachados y cuántos productos y despachos se han realizado.
También se destacó la importancia de evitar la duplicación del trabajo ocasionada por el registro manual inicial y la posterior digitación de la información en el computador.
La reunión finalizó agradeciendo al propietario por la información proporcionada y por su participación en la identificación de las necesidades actuales del negocio. |
---

# 2. Problema identificado

La problemática principal está relacionada con la **gestión manual y la falta de centralización de la información de pedidos, ventas y despachos**.

Actualmente, cuando un cliente realiza un pedido, la información se registra inicialmente de forma manual en una libreta. Posteriormente, los pedidos son organizados para su despacho y se utilizan fichas pequeñas denominadas "memos" para organizar las entregas. A medida que los pedidos salen, se coloca una marca de verificación en la libreta para identificar cuáles han sido despachados y cuáles permanecen pendientes.

La organización de los despachos se realiza manualmente. Para determinar qué pedidos pueden enviarse juntos se tienen en cuenta principalmente las zonas o rutas de entrega y las cantidades solicitadas. La capacidad disponible para cada viaje también influye en esta organización. Por lo tanto, el encargado necesita revisar los pedidos existentes para determinar cómo organizar los despachos.

En cuanto a las ventas, las cantidades vendidas se registran inicialmente en la libreta mediante columnas correspondientes a las diferentes presentaciones. Para conocer las cantidades vendidas al finalizar el día, es necesario realizar sumas manuales de las columnas y páginas correspondientes. Posteriormente, esta información se digita en un computador.

Esto genera una **duplicación del trabajo**, debido a que la información se registra inicialmente en papel y posteriormente vuelve a registrarse de manera digital.

Además, la información no siempre está disponible de manera inmediata durante la operación. Para consultar información histórica, como las ventas del mes anterior, es necesario recurrir a los reportes almacenados en el computador.

El propio propietario identificó como necesidad prioritaria la sistematización del registro de pedidos y manifestó la conveniencia de poder conocer de manera inmediata qué se está despachando, qué pedidos permanecen pendientes, la cantidad de productos vendidos y el número de despachos realizados.

---

# 3. Evidencia de la problemática

La problemática fue identificada y validada mediante una entrevista realizada al propietario del negocio.

Algunas de las afirmaciones relevantes obtenidas durante la entrevista fueron:

- "El pedido se registra manualmente en una libreta."
- Para organizar los pedidos se utiliza una ficha denominada "memo".
- A medida que los pedidos salen, se coloca una marca de verificación en la libreta.
- Para conocer las cantidades vendidas se deben sumar manualmente las columnas y páginas de la libreta.
- La información posteriormente se digita en un computador.
- El propietario manifestó que existe una duplicación del trabajo porque primero se realiza el registro manual y posteriormente se vuelve a registrar la información digitalmente.
- El propietario señaló como necesidad principal la sistematización del registro de pedidos.
- También indicó la necesidad de conocer de manera inmediata qué pedidos se están despachando, cuáles permanecen pendientes, la cantidad de productos vendidos y el número de despachos realizados.

La entrevista constituye la principal fuente primaria utilizada para validar que la problemática abordada por el proyecto corresponde a una situación real del negocio.

---

# 4. Consecuencias identificadas

A partir de la situación descrita y de la entrevista, se identifican las siguientes consecuencias:

### 4.1. Duplicación del trabajo

La información de las ventas y pedidos debe registrarse inicialmente de manera manual y posteriormente volver a digitarse en el computador.

### 4.2. Mayor esfuerzo administrativo

El uso de registros físicos y la posterior digitación requieren tiempo y trabajo adicional para mantener organizada la información.

### 4.3. Dificultad para realizar seguimiento inmediato

El estado de los pedidos depende actualmente de la revisión de libretas, memos y marcas de verificación, dificultando disponer de una visión centralizada de los pedidos pendientes y despachados.

### 4.4. Dificultad para consultar información durante la operación

La información de ventas y despachos requiere procesos manuales de consolidación y posterior digitación antes de encontrarse disponible digitalmente.

### 4.5. Limitación para el análisis del negocio

La falta de información centralizada e inmediata dificulta consultar y analizar de manera ágil aspectos como las cantidades vendidas, los despachos realizados, los ingresos y el comportamiento de las ventas.

---

# 5. Idea general de solución

La propuesta consiste en desarrollar un **sistema web para la gestión y digitalización de la tienda de agua embotellada, orientado a la administración del negocio y atencion de clientes**.

El sistema busca centralizar el registro y seguimiento de los pedidos, reemplazando el proceso manual que actualmente requiere registrar inicialmente las solicitudes en una libreta y posteriormente digitar la información en un computador.

Desde el módulo administrativo, se plantea permitir el registro y consulta de los pedidos, así como la visualización de información como su estado y cantidad, con el propósito de proporcionar al encargado una visión centralizada de los pedidos pendientes y facilitar la organización de los despachos de acuerdo con las rutas, cantidades y capacidad de los vehículos.

Adicionalmente, se plantea digitalizar el registro de las ventas e ingresos, evitando la duplicación de trabajo que actualmente se produce al registrar manualmente las ventas y posteriormente transcribirlas al computador.

Finalmente, el sistema incorporará estadísticas e indicadores que permitan consultar de manera más inmediata información como la cantidad de productos vendidos, los despachos realizados, los ingresos y el comportamiento de las ventas, facilitando el análisis y la toma de decisiones dentro del negocio.

Es importante saber que el profesor nos puso una restriccion que nos pide que el usuario final( el comprador) pueda tambien usar el software para hcer un pedido, y tener seguimiento del mismo(en este contexto seguimiento consiste en saber si la solicitud fue rechazada, si esta en espera, o si ya salio).
---

# 6. Alcance preliminar de la solución

La propuesta se concentra inicialmente en cuatro áreas principales:

### A. Gestión de pedidos

- Registrar pedidos de forma administrativa(Lo realiza la persona encargada de el uso del software en la empresa).
- Registar pedidos de forma comercial(Lo realiza el usuario final del software, los compradores de la tienda)
- Consultar pedidos de forma administrativa.
- Visualizar información relevante de cada pedido.
- Consultar pedidos pendientes.
- Dar seguimiento al estado de los pedidos(admisnitrativa).
- Dar seguimiento al estado de los pedidos(Comercial)(El usuario puede mirar el estado(negado, despachado, en espera) de sus pedidos).

### B. Gestión de despachos

- Visualizar los pedidos pendientes.
- Consultar cantidades y ubicaciones/zonas asociadas a los pedidos.
- Facilitar al encargado la organización de los despachos.
- Permitir consultar qué pedidos han sido despachados y cuáles permanecen pendientes.

**Importante:** inicialmente NO se pretende automatizar la planificación de rutas ni decidir automáticamente cómo deben agruparse los pedidos. La decisión continúa siendo responsabilidad del encargado; el sistema debe proporcionar la información necesaria para facilitar dicha decisión.

### C. Gestión de ventas e ingresos

- Registrar las ventas.
- Registrar o consultar los ingresos asociados.
- Evitar el doble registro manual/digital.
- Consultar información histórica.

### D. Estadísticas e indicadores

Se plantea incorporar gráficos e indicadores que permitan consultar información como:

- Cantidad de productos vendidos.
- Ventas por periodo.
- Número de despachos.
- Ingresos.
- Comportamiento de las ventas.
- Productos/presentaciones más solicitados.

### E. Requisito adicional exigido por el docente

El docente de la asignatura solicitó explícitamente que la solución sea un **sistema web responsive**, es decir, que se adapte y funcione correctamente en distintos tamaños de pantalla y dispositivos.

Adicionalmente, el docente estableció que los **pedidos deben realizarse a través de la página**. Originalmente se había considerado que la interacción con el sistema la tendría únicamente la persona que representa al negocio (encargado/administrador); sin embargo, con este requisito, el sistema también debe permitir la **interacción con usuarios externos a la empresa** (clientes), quienes podrán realizar sus pedidos directamente desde el sitio web.

Este requisito amplía el alcance inicialmente planteado, incorporando un módulo orientado al cliente y la obligación de garantizar la adaptabilidad del sistema a dispositivos y resoluciones variadas.

---

# 7. Funcionalidades que NO están definidas como parte principal del alcance
( No es necesario tener en cuenta esto para el desarrollo de actividades, solo es para tener claro que no vamos a hacer y que se escapa e los limitres del proyecto).
Para evitar ampliar innecesariamente el proyecto, inicialmente no se plantea:

- Automatizar la creación de rutas óptimas.
- Decidir automáticamente qué pedidos deben agruparse.
- Implementar algoritmos de optimización logística.
- Automatizar completamente las decisiones del encargado.
- Resolver problemas de inventario que no hayan sido identificados durante el levantamiento de requisitos.

La solución debe principalmente **centralizar información, facilitar su consulta y apoyar la gestión administrativa**, dejando las decisiones operativas de organización de rutas y despachos al personal encargado.

---
---
# 8. Objetivo general preliminar

(!Generar)

---

# 9. Estado actual del proyecto

El proyecto se encuentra en una primera etapa de creacion de modelado de negocio(Iteracion III).
Ya se realizo : 1) identificacion del problema, 2) Analisis de requisito

#### Artefactos del modelo de negocio (4)

| # | Artefacto | Estado | Archivo |
|---|---|---|---|
| 1 | Procesos de negocio (swimlane/carriles UML) | **EN PROCESO** | `3_Iteracion/ProcesoDeNegocio.md` / `.puml` |
| 2 | Casos de uso de la vida real (actividades de negocio) | **EN PROCESO** | `3_Iteracion/CasosDeUso.md` / `.puml` |
| 3 | Modelo de dominio | Pendiente | — |
| 4 | Glosario | Pendiente | — |

#### Convenciones acordadas en iteración 3

- El modelado de negocio es **AS-IS**: representa cómo funciona el negocio actualmente, según el acta de entrevista del 26/08/2026 (Anexo C). **No** es TO-BE ni una proyección de los RF del SRS.
- El diagrama de proceso usa **PlantUML** en archivos `.puml`, con el contenido embebido en el `.md` como respaldo.
- Los casos de uso de la vida real se derivan **de los óvalos del swimlane**, no de las funciones del sistema.
- Roles (carriles) usados: **Cliente**, **Encargado**, **Repartidor**.
- Diagrama de casos de uso con sintaxis `usecase "UC-01\n..." as UC01` y relaciones `<<include>>` según la secuencia del proceso.

#### Lo que NO se hace

- No se proyecta el sistema a construir sobre el swimlane (RF-01 a RF-06 no son fuente de los casos de uso).
#### Pendiente iteración 3

- Modelo de dominio (artefacto 3).
- Glosario (artefacto 4), en orden alfabético y solo con términos relevantes del contexto.
- Renderizar los `.puml` a imagen para el entregable en Word.
- Verificar los Artefactos 1 y 2, swinlane y Casos de Uso.
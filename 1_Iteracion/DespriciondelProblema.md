**Proyecto del curso de Ingeniería de Software**

JAIRO DANIEL JIMENEZ ARZUZA

PEDRO ELI DIAZ OLARTE

ALEJANDRO RINCON MESA

NEWIN JOSE TORRES PALMERA

Universidad De Cartagena

Facultad de Ingeniería

Ingeniería de sistemas

Ingeniería de software

Cartagena D. T. y C.

2026

JAIRO DANIEL JIMENEZ ARZUZA

PEDRO ELI DIAZ OLARTE

ALEJANDRO RINCON MESA

NEWIN JOSE TORRES PALMERA

**SISTEMA DE CONTABILIDAD E INVENTARIO**

Proyecto del curso de Ingeniería de Software

Profesor:

MSc., PhD Martin Monroy Rios

Universidad De Cartagena

Facultad de Ingeniería

Ingeniería de sistemas

Ingeniería de software

Cartagena D. T. y C.

2026

***Tabla de contenido***

[**Descripción del problema 4**](#_6w6kq2mqcmsd)

[**Justificación 6**](#_562w0b9bukez)

[Pertinencia del Proyecto 6](#_si5nkoch7w82)

[Reemplazo del Proceso Analógico de Doble Registro 6](#_uiujld6jjhc5)

[Trazabilidad e Integridad de la Información 7](#_eynux7n9mh2)

[Relevancia Del Proyecto 7](#_xwjkwizf5k4o)

[Relevancia Operativa y Logística 7](#_2090oh70p8ym)

[Relevancia Económica y Financiera 7](#_h9c936vio636)

[Relevancia Tecnológica y Analítica 7](#_7jh68j42b8a0)

[Relevancia Organizacional 8](#_8gr41lm4idxz)

[**Objetivo General 8**](#_4p7pdbsxwmqo)

[**Objetivos Específicos 8**](#_5af17yf5egsw)

[**Bibliografía 10**](#_jqqo392zsmkm)

# Descripción del problema

El proyecto se desarrolla en un negocio dedicado a la comercialización y distribución de agua embotellada, que atiende tanto a clientes particulares como a establecimientos comerciales. Dentro de su actividad comercial se manejan diferentes tipos de productos, entre los que se encuentran pacas personales, pacas para hielo, pacas de tres litros, pacas de cinco litros y pimpinas de 20 litros. La operación del negocio comprende actividades relacionadas con la recepción de pedidos, preparación de los productos, despacho y entrega a los clientes, así como el registro de las ventas e ingresos generados.

La recepción de los pedidos se realiza principalmente mediante llamadas telefónicas y mensajes a través de WhatsApp. Una vez recibida la solicitud, se determina la cantidad de productos requerida y posteriormente se coordina su despacho mediante los repartidores disponibles. La distribución de los pedidos se organiza teniendo en cuenta las zonas o rutas de entrega y las cantidades solicitadas, de manera que varios pedidos puedan ser considerados para un mismo despacho cuando las condiciones de la operación lo permiten. En este proceso intervienen, por tanto, diferentes actividades que requieren disponer de información sobre los pedidos, las ventas y los despachos realizados.

Actualmente, la gestión de los pedidos y de las ventas del negocio se desarrolla mediante una combinación de registros manuales y posteriores registros digitales. Cuando un cliente realiza un pedido, la solicitud es registrada inicialmente de forma manual en una libreta. Posteriormente, los pedidos son organizados para su despacho.

Para realizar el seguimiento de los pedidos se utilizan fichas denominadas "memos" y, a medida que los pedidos son despachados, se coloca una marca de verificación en la libreta para identificar aquellos que ya salieron y los que permanecen pendientes. Esta situación evidencia que el control de los pedidos y despachos depende actualmente de registros físicos y de su revisión manual como se evidencia en el Anexo C.

La gestión de las ventas también presenta un proceso manual previo a su digitalización. De acuerdo con la información proporcionada durante la entrevista, las cantidades vendidas se registran en la libreta mediante columnas correspondientes a las diferentes presentaciones como se evidencia en el Anexo A. Para conocer las cantidades vendidas al finalizar el día, es necesario realizar manualmente la suma de las columnas y de las páginas correspondientes a los registros de esa fecha. Posteriormente, la información es digitada en un computador presentado en el Anexo B, lo que implica realizar nuevamente el registro de información que ya había sido consignada manualmente observable en el Anexo C. *.*

Esta forma de gestionar la información genera una separación entre el momento en que se registra una operación y el momento en que esta queda disponible digitalmente para su consulta. Mientras los pedidos y las ventas se encuentran registrados inicialmente en medios físicos, su consulta y análisis mediante el computador depende de una digitación posterior. De acuerdo con lo manifestado por el propietario, esta situación dificulta conocer de manera inmediata la cantidad de productos vendidos y el número de despachos realizados durante el día. Asimismo, aunque existe información histórica almacenada en el computador, su consulta requiere recurrir a los reportes correspondientes como consta en el Anexo C.

En consecuencia, la situación actual se caracteriza por la utilización de registros manuales para una parte importante de la operación, el posterior traslado de información al computador y la necesidad de revisar diferentes registros para realizar el seguimiento de pedidos, ventas y despachos, esto genera una duplicación de actividades.

Esta situación implica que una misma información sea procesada en más de una etapa, incrementando el tiempo y esfuerzo necesario para mantener actualizados los registros del negocio. El propietario identifica directamente esta situación como una de las dificultades que se busca solucionar mediante un registro más inmediato y digital, lo cual se indica en la entrevista que se tuvo constatada en el Anexo C.

Asimismo, el uso de registros físicos para controlar los pedidos y despachos dificulta disponer de una visión inmediata y centralizada del estado de las entregas. Actualmente, es necesario recurrir a la libreta, los memos y las marcas de verificación para identificar los pedidos que han sido despachados y aquellos que permanecen pendientes. Como consecuencia, el seguimiento de los pedidos depende de la revisión manual de estos registros, como se demuestra por el Anexo C.

En relación con las ventas, el proceso actual también limita la disponibilidad inmediata de información para el control de la operación. Aunque las cantidades vendidas pueden ser determinadas mediante los registros existentes, es necesario realizar sumas manuales de las columnas y páginas de la libreta y posteriormente trasladar la información al computador. Esto dificulta consultar durante la operación datos como la cantidad de productos vendidos o el número de despachos realizados sin recurrir al proceso manual de consolidación y digitación, como se puede ver en el Anexo A.

Finalmente, la forma actual de gestionar y consolidar la información limita la facilidad para realizar análisis sobre el comportamiento del negocio. La disponibilidad de información histórica depende de los registros y reportes almacenados posteriormente en el computador, mientras que el acceso inmediato a los datos de la operación requiere procesos manuales. Esto reduce la oportunidad de disponer de información actualizada que facilite el seguimiento de las ventas, los despachos y otros indicadores relevantes para la administración del negocio, de lo que se dejó constancia en el Anexo C.

La propuesta de solución consiste en desarrollar un sistema informático para la gestión y digitalización de la tienda, orientado a la administración del negocio. El sistema busca centralizar el registro y seguimiento de los pedidos, reemplazando el proceso manual que actualmente requiere registrar inicialmente las solicitudes en una libreta y posteriormente digitar la información en un computador.

Desde el módulo administrativo, se plantea permitir el registro y consulta de los pedidos, así como la visualización de información como su estado y cantidad, con el propósito de proporcionar al encargado una visión centralizada de los pedidos pendientes y facilitar la organización de los despachos de acuerdo con las rutas, cantidades y capacidad de los vehículos.

Adicionalmente, se plantea digitalizar el registro de las ventas e ingresos, evitando la duplicación de trabajo que actualmente se produce al registrar manualmente las ventas y posteriormente transcribirlas al computador. Finalmente, el sistema incorporará estadísticas e indicadores que permitan consultar de manera más inmediata información como la cantidad de productos vendidos, los despachos realizados, los ingresos y el comportamiento de las ventas, facilitando el análisis y la toma de decisiones dentro del negocio.

# Justificación

La entrevista realizada al propietario permitió identificar que una parte importante de la gestión de pedidos, ventas y despachos se desarrolla actualmente mediante registros manuales y procesos posteriores de digitación. Esta situación genera duplicación de trabajo y dificulta disponer de manera inmediata de información relacionada con los pedidos pendientes, los productos vendidos y los despachos realizados. Ante esta situación, se considera pertinente el desarrollo de una solución informática que permita centralizar la información y apoyar las actividades administrativas del negocio.

La propuesta resulta relevante debido a que responde directamente a necesidades identificadas durante el análisis de la operación actual. La digitalización de los procesos permitiría reducir actividades repetitivas, facilitar el seguimiento de los pedidos y despachos y disponer de información organizada para el control de las ventas e ingresos. De esta manera, el proyecto busca mejorar la gestión de la información sin modificar la forma en que el encargado toma las decisiones relacionadas con la organización de los despachos.

## ***Pertinencia del Proyecto***

### ***Reemplazo del Proceso Analógico de Doble Registro***

Actualmente, la empresa opera bajo un esquema analógico e ineficiente que exige registrar manualmente los pedidos recibidos (vía telefónica o presencial) en una libreta de notas de papel, para posteriormente digitar esta misma información en un computador al final de la jornada. Este procedimiento genera una redundancia operativa directa, duplicando el tiempo dedicado a tareas administrativas rutinarias y multiplicando exponencialmente la vulnerabilidad ante errores humanos de transcripción [1]. La solución propuesta es pertinente porque introduce un módulo de captura única de datos en tiempo real, erradicando el doble registro y sincronizando la información desde el primer punto de contacto con el cliente.

### ***Trazabilidad e Integridad de la Información***

El registro físico en papel carece de validaciones de datos, controles de concurrencia y respaldos automáticos, lo que acarrea pérdida de información por deterioro físico del soporte o extravío de folios. El sistema garantizará la integridad referencial y trazabilidad completa del ciclo de vida del pedido (recibido, en preparación, asignado a vehículo, en tránsito, entregado, facturado), resolviendo de raíz la falta de visibilidad del estado de los despachos.

## ***Relevancia Del Proyecto***

### ***Relevancia Operativa y Logística***

Al sustituir la libreta física por un tablero digital centralizado de despachos, se dota al personal de operaciones de visibilidad completa y en tiempo real sobre la demanda pendiente. Esto permite pasar de un esquema de despacho reactivo a uno planificado y reducir sensiblemente las llamadas de seguimiento por parte de los clientes.

### ***Relevancia Económica y Financiera***

Desde la perspectiva financiera, el proyecto impacta positivamente en el control de Fugas Financieras, al automatizar el registro de ventas e ingresos y relacionarlo directamente con la salida física de botellones, se eliminan los cuadres manuales erróneos, las ventas no registradas y las pérdidas por omisiones en el cobro de entregas [1].

### ***Relevancia Tecnológica y Analítica***

El desarrollo del sistema dota a la tienda de herramientas tecnológicas adaptadas a su escala. El módulo de estadísticas e indicadores de gestión (KPIs) transforma datos operativos crudos en información estratégica digestible: volumen de producto vendido por período, ingresos brutos y netos. Esto capacita al negocio para anticipar picos de demanda según temporadas térmicas o calendarios de consumo.

### ***Relevancia Organizacional***

El proyecto facilita la profesionalización e institucionalización del negocio. Transiciona a la pequeña empresa desde un modelo empírico basado en el conocimiento tácito del dueño a una administración estructurada sustentada en el paradigma Data-Driven Decision Making (toma de decisiones basada en datos) [2], [5].

# Objetivo General

Implementar una solución informática para un negocio de agua embotellada que permita digitalizar la contabilidad y la gestión de ventas, con el fin de eliminar ineficiencias operacionales, garantizar la trazabilidad contable y el control financiero de la empresa, mediante un enfoque metodológico híbrido que combina RUP y metodologías ágiles.

# Objetivos Específicos

* Modelar los procesos de negocio relacionados con la gestión de ventas, inventario y contabilidad de la empresa, con el fin de representar y analizar el funcionamiento actual del negocio y establecer las bases para la definición de los requisitos del sistema, mediante técnicas de modelado de procesos y UML.
* Identificar los requisitos funcionales y no funcionales del sistema basado en las actividades de la empresa para modelar los flujos de gestión, inventario y contabilidad usando los principios de la ingeniería de requisitos.
* Diseñar la arquitectura de los subsistemas de persistencia de datos, lógica de negocio, integración con servicios externos e interfaces gráficas de usuarios con el fin de establecer una solución conceptual y técnica que sirva como base para la implementación, mediante UML.
* Desarrollar los módulos de la solución informática, con el fin de obtener un producto funcional que permita gestionar las operaciones de ventas y contabilidad del negocio, haciendo uso de lenguajes de programación de alto nivel, tecnologías modernas de desarrollo de software y tecnologías tradicionales de gestión.
* Validar la funcionalidad y calidad de la solución informática mediante la ejecución de pruebas funcionales y de rendimiento, con el fin de verificar el cumplimiento de los requisitos establecidos y detectar errores antes de su puesta en operación, aplicando técnicas de prueba de software como caja negra y pruebas de rendimiento.

# Bibliografía

* [1] R. R. Panko, "What we know about spreadsheet and manual entry errors," Journal of End User Computing, vol. 10, no. 2, pp. 15–21, 1998.
* [2] CEPAL, "La digitalización de las MiPyMEs en América Latina y el Caribe: Oportunidades y desafíos para la productividad," Comisión Económica para América Latina y el Caribe, Santiago de Chile, Doc. LC/TS.2021/181, 2021.
* [3] R. Bravo y J. Sepúlveda, "Optimización de rutas de distribución urbana mediante herramientas software en pequeñas empresas de logística," Revista Iberoamericana de Logística y Cadena de Suministro, vol. 12, no. 2, pp. 45–58, 2020.
* [4] R. H. Ballou, Logística: Administración de la cadena de suministro, 5a ed. México: Pearson Educación, 2018.
* [5] R. S. Pressman y B. R. Maxim, Ingeniería del software: Un enfoque práctico, 9a ed. México D.F., México: McGraw-Hill, 2021.

***Anexos***

***![](data:image/png;base64...)
Registro Físico, Anexo A***

***![](data:image/png;base64...)Registro Digital, Anexo B***

***ACTA DE REUNIÓN***

***Fecha:26/08/2026***

***Hora de Inicio:21:00***

***Hora de Finalización:22:00***

***Preparó: Pedro Eli Diaz Olarte***

| ***Asistentes*** | | | ***Asistió*** | |
| --- | --- | --- | --- | --- |
| ***No.*** | ***Cargo*** | ***Nombre*** | ***Si*** | ***No*** |
| ***1*** | ***Estudiante de ingeniería de sistemas*** | ***Pedro Eli Diaz Olarte*** | ***✓*** |  |
| ***2*** | ***CEO de Agua Frais*** | ***Melfy Diaz Diaz*** | ***✓*** |  |
|  |  |  |  |  |

| ***OBJETIVOS:*** |
| --- |
| ***Conocer el funcionamiento actual del negocio de comercialización y distribución de agua embotellada, identificando las actividades relacionadas con la gestión de pedidos, ventas, ingresos y despachos. Asimismo, identificar las principales dificultades que se presentan durante estas actividades y validar que la problemática identificada corresponda a una necesidad real del negocio, con el propósito de orientar el desarrollo de una propuesta de solución informática.*** |

| ***ORDEN DEL DÍA*** |
| --- |
| ***1)*** ***Presentación de los participantes de la entrevista***  ***2)*** ***Realización de las preguntas desarrollos***  ***3)*** ***Despedida de los participantes,*** |
| ***DESARROLLO DE LA REUNIÓN***  La reunión inició con la presentación de los participantes y una explicación del propósito de la entrevista. Se indicó que el objetivo principal era conocer el funcionamiento actual del negocio y sus dificultades cotidianas, con el fin de identificar una problemática real que pudiera ser abordada mediante una solución informática.  Posteriormente, se realizaron las siguientes preguntas para obtener una mejor idea del funcionamiento y ciclo de vida de una venta y tener una idea mejor de qué problemas podrían estar afectando el desempeño de la empresa.    1)Podría contarnos, paso a paso, cómo es el ciclo completo de un pedido desde que el cliente lo hace hasta que recibe el agua y usted cobra    2) Cuando tiene varios pedidos pendientes al mismo tiempo, ¿cómo hace para saber cuáles ya están listos, cuáles están en camino y cuáles faltan por entregar?    3)Al final del día, ¿cómo sabe exactamente cuánto vendió y cuánta agua se fue en cada presentación? ¿Y si quisiera ver eso del mes pasado, qué tendría que hacer?    4)Cuando un cliente habitual vuelve a pedir, ¿qué información tienen que volver a preguntarle o anotar que ya deberían saber?  5)De todo lo que me ha contado, si solo pudiera mejorar una cosa, ¿qué sería y por qué?    Durante la entrevista se identificó que los pedidos son recibidos principalmente mediante llamadas telefónicas o mensajes de WhatsApp. Una vez recibida la solicitud, esta se registra manualmente en una libreta y posteriormente se organiza para su despacho. Para realizar el seguimiento de los pedidos se utilizan registros físicos y fichas denominadas "memos", en los cuales se organizan las entregas. A medida que los pedidos son despachados, se marca manualmente su salida, permitiendo distinguir aquellos que ya fueron enviados de los que permanecen pendientes.    También se identificó que la organización de los despachos depende de la revisión de los pedidos existentes y de factores como las zonas o rutas de entrega y las cantidades solicitadas. Esto hace necesario consultar y organizar manualmente la información disponible para determinar los pedidos que pueden ser despachados.    En relación con las ventas, se explicó que la cantidad de productos vendidos se registra manualmente en la libreta mediante columnas correspondientes a cada presentación. Para conocer las cantidades vendidas, se deben realizar sumas manuales de las columnas y páginas correspondientes a cada fecha.    Posteriormente, la información es digitada en un computador, generando una duplicación del trabajo realizado inicialmente. Para consultar información de periodos anteriores, como el mes anterior, es necesario recurrir a los reportes almacenados en el computador.    Respecto a los clientes habituales, se indicó que sus pedidos deben registrarse nuevamente debido a que las cantidades y productos solicitados pueden variar según sus necesidades. Sin embargo, algunos clientes, especialmente los que realizan pedidos para el hogar, suelen solicitar productos y cantidades similares de manera recurrente.    Finalmente, se consultó al propietario cuál sería la principal mejora que implementaría en el negocio. Se manifestó como necesidad prioritaria la sistematización del registro de pedidos, permitiendo conocer de manera inmediata qué pedidos se encuentran pendientes, cuáles han sido despachados y cuántos productos y despachos se han realizado. También se destacó la importancia de evitar la duplicación del trabajo ocasionada por el registro manual inicial y la posterior digitación de la información en el computador.    La reunión finalizó agradeciendo al propietario por la información proporcionada y por su participación en la identificación de las necesidades actuales del negocio. |
| ***CONCLUSIONES***  A partir de la información obtenida durante la entrevista, se determinó que existe una problemática relacionada con la gestión manual y la falta de centralización de la información correspondiente a los pedidos, ventas y despachos.  Se identificó que el registro inicial de los pedidos se realiza manualmente en una libreta y que posteriormente parte de esta información debe ser digitada en un computador. Esta situación genera duplicación de trabajo y dificulta disponer de la información de manera inmediata.    También se determinó que el seguimiento de los pedidos y la organización de los despachos se realizan mediante registros físicos, lo que requiere consultar manualmente los pedidos existentes para conocer cuáles han sido despachados y cuáles permanecen pendientes.  En cuanto a las ventas, se identificó que el cálculo de las cantidades vendidas requiere realizar operaciones manuales sobre los registros de la libreta y que la consulta de información histórica depende de los reportes almacenados posteriormente en el computador.  Con base en estas necesidades, se considera pertinente desarrollar un sistema web para la gestión y digitalización de la tienda, orientada a la administración del negocio. El sistema busca centralizar el registro y seguimiento de los pedidos, reemplazando el proceso manual que actualmente requiere registrar inicialmente las solicitudes en una libreta y posteriormente digitar la información en un computador.    Desde el módulo administrativo, el sistema permitirá registrar y consultar los pedidos, visualizar su estado, cantidad, y demás información necesaria para facilitar la organización de los despachos. El sistema busca proporcionar al encargado una visión centralizada de los pedidos pendientes para que pueda realizar esta organización de acuerdo con las rutas, cantidades y capacidad de los vehículos.    Adicionalmente, se plantea digitalizar el registro de las ventas e ingresos, evitando la duplicación de trabajo que actualmente se produce al registrar manualmente las ventas y posteriormente transcribirlas al computador. Finalmente, el sistema incorporará estadísticas e indicadores que permitan consultar de manera más inmediata información como la cantidad de productos vendidos, los despachos realizados, los ingresos y el comportamiento de las ventas, facilitando el análisis y la toma de decisiones dentro del negocio. |

| ***Actividad*** | ***Responsable*** | ***Fecha*** |
| --- | --- | --- |
| ***Entrevista con el CEO de Agua Frais*** | ***Pedro Eli Diaz Olarte*** | ***26/08/2026*** |

***![](data:image/png;base64...)***

***Se dio por terminada esta
 actividad, habiéndose desarrollado los temas contenidos en esta acta y comprometiéndose las partes a cumplir con los compromisos adquiridos en la misma.***

***Acta de entrevista, Anexo C***
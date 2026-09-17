# ESPECIFICACIÓN DE REQUISITOS DE SOFTWARE (SRS)

**Proyecto:** Sistema de Gestión para Tienda de Agua Embotellada
**Curso:** Ingeniería de Software
**Asignatura:** Ingeniería de Sistemas
**Universidad de Cartagena**
**Iteración:** 2 – Especificación de Requisitos
**Norma de referencia:** ISO/IEC/IEEE 29148

---

# 1. Introducción

## 1.1. Propósito

El propósito de este documento es definir de manera precisa y verificable los requisitos que debe cumplir el sistema web para la gestión y digitalización de la tienda de agua embotellada "Agua Frais". El documento describe la problemática que se aborda, el alcance de la solución, las funciones que debe proporcionar el sistema, las características de los usuarios que lo emplearán y las restricciones que condicionan su diseño y construcción.

Este documento está dirigido a los interesados del proyecto: el equipo de desarrollo (estudiantes de Ingeniería de Sistemas), el propietario y encargado del negocio (cliente), y el profesor de la asignatura (responsable de la evaluación). Su finalidad es servir como acuerdo entre las partes respecto de lo que el sistema debe hacer y como base para las etapas posteriores de diseño, implementación y pruebas.

El contenido de esta especificación se elabora atendiendo la norma ISO/IEC/IEEE 29148 y se estructura siguiendo la guía definida para el curso en la segunda iteración del proyecto.

## 1.2. Ámbito

### Identificación del producto

El producto se denomina **Sistema de Gestión para Tienda de Agua Embotellada**. Es una aplicación **web responsive** orientada tanto a la administración del negocio como a la atención de los clientes. Por una parte, está dirigida al personal encargado de registrar, consultar y dar seguimiento a las operaciones; por otra, permite la interacción de los **clientes (usuarios externos a la empresa)**, quienes realizarán sus pedidos directamente desde la página web. De acuerdo con el requisito exigido por el docente de la asignatura, el diseño del sistema se adapta a distintos tamaños de pantalla y dispositivos.

### Qué hará el sistema

El sistema centralizará el registro y seguimiento de las operaciones del negocio con el fin de reemplazar el proceso manual que actualmente requiere registrar inicialmente las solicitudes en una libreta y posteriormente digitar la información en un computador. Concretamente, el sistema permitirá:

- Permitir que los clientes realicen y envíen sus pedidos directamente desde la página web, sin depender exclusivamente de la llamada telefónica o de la atención presencial.
- Registrar y consultar los pedidos recibidos, visualizando su estado y las cantidades solicitadas.
- Proporcionar al encargado una visión centralizada de los pedidos pendientes para facilitar la organización de los despachos según las rutas, cantidades y capacidad de los vehículos.
- Registrar y consultar las ventas e ingresos, evitando el doble registro manual/digital.
- Incorporar estadísticas e indicadores para consultar información como la cantidad de productos vendidos, los despachos realizados, los ingresos y el comportamiento de las ventas.

### Beneficios y metas

- Eliminar la duplicación de trabajo que se produce al registrar la información primero en papel y luego transcribirla al computador.
- Permitir conocer de manera inmediata qué pedidos se están despachando, cuáles permanecen pendientes, la cantidad de productos vendidos y el número de despachos realizados.
- Facilitar el seguimiento de pedidos y despachos mediante una visión centralizada y digital del estado de las entregas.
- Reducir el esfuerzo administrativo asociado al registro manual y a la consolidación de información.
- Facilitar el análisis del comportamiento del negocio a partir de estadísticas e indicadores.

### Alcance funcional

El alcance se concentra en cinco áreas principales:

- **A. Gestión de pedidos:** registro, consulta, visualización de la información de cada pedido, consulta de pedidos pendientes y seguimiento del estado.
- **B. Gestión de despachos:** visualización de pedidos pendientes, consulta de cantidades y zonas asociadas, apoyo a la organización de despachos y consulta de qué pedidos han sido despachados o permanecen pendientes.
- **C. Gestión de ventas e ingresos:** registro y consulta de ventas e ingresos, evitando el doble registro, y consulta de información histórica.
- **D. Estadísticas e indicadores:** gráficos e indicadores sobre cantidades vendidas, ventas por periodo, número de despachos, ingresos, comportamiento de las ventas y presentaciones más solicitadas.
- **E. Canal de pedidos de clientes (web):** brindar a los clientes la posibilidad de registrar sus pedidos a través de la página web y consultar el estado de sus solicitudes, accediendo desde distintos dispositivos (computador, tableta o celular) gracias al diseño responsive del sistema.

### Limitaciones de alcance

El sistema **no** automatizará la planificación de rutas ni decidirá automáticamente cómo deben agruparse los pedidos. La decisión sobre la organización de los despachos continúa siendo responsabilidad del encargado; el sistema únicamente le proporciona la información necesaria para facilitar dicha decisión.

De acuerdo con la naturaleza administrativa del proyecto, el sistema **no** incorpora un módulo contable formal ni valida el inventario: se limitará a guardar la información de las ventas y pedidos que le es proporcionada y a actuar sobre ella, sin verificar contra un stock o existencia de productos. Asimismo, quedan fuera del alcance principal los algoritmos de optimización logística, la automatización completa de decisiones y los problemas de inventario que no hayan sido identificados durante el levantamiento de requisitos.

## 1.3. Visión general del producto

### 1.3.1. Perspectiva del producto

El sistema es un **producto nuevo** que se desarrolla para reemplazar los registros manuales actualmente utilizados por la tienda (libreta, memos y marcas de verificación) y la digitación posterior en un computador. Forma parte de un esfuerzo por digitalizar y centralizar la información operativa del negocio.

**Interfaces del sistema:**

- **Interfaces de usuario:** el sistema será accesible mediante un navegador web desde computador o dispositivos móviles, con un diseño **responsive** que se adapta al tamaño de pantalla. Las pantallas se organizan por módulos administrativos (pedidos, despachos, ventas e ingresos, estadísticas) y por un módulo orientado al cliente para la realización y consulta de pedidos en línea.
- **Interfaces de hardware:** se utilizará un computador con acceso a internet para la administración. No se prevé el uso de hardware especializado.
- **Interfaces de software:** el sistema se ejecutará sobre tecnologías web estándar (cliente-servidor) y hará uso de una base de datos para el almacenamiento persistente de la información.
- **Interfaces de comunicación:** el sistema operará a través del protocolo HTTP/HTTPS sobre la red local o internet.

**Operación:**
- **Modos de operación:** el sistema operará en forma única, orientado a uso administrativo diurno durante la jornada de trabajo del negocio.
- **Disponibilidad y continuidad:** el sistema debe permanecer disponible durante la operación del negocio, permitiendo consultar y registrar información de manera inmediata.
- **Cumplimiento regulatorio operativo:** no se identifican requisitos regulatorios especiales para el ámbito administrativo cubierto.
- **Adaptación al sitio:** el sistema debe adaptarse a las condiciones del negocio: personal con bajo nivel de formación técnica, uso del idioma español y operaciones desarrolladas en un contexto de pequeña empresa.

### 1.3.2. Funciones del producto

A continuación se presenta un resumen de las funciones más importantes que debe cumplir el sistema. El detalle completo se desarrolla en la sección 3.2 (Funciones).

1. **Registrar pedidos:** capturar la información de un pedido (cliente, presentaciones, cantidades, zona, fecha).
2. **Consultar pedidos:** buscar y visualizar los pedidos registrados.
3. **Visualizar la información de cada pedido:** estado y cantidades asociadas.
4. **Consultar pedidos pendientes:** listar los pedidos que aún no han sido despachados.
5. **Seguir el estado de los pedidos:** registrar la transición del pedido (pendiente → despachado).
6. **Visualizar pedidos pendientes y sus zonas/cantidades:** apoyar la organización de los despachos.
7. **Consultar pedidos despachados y pendientes:** distinguir ambos conjuntos.
8. **Registrar ventas:** capturar la información de las ventas realizadas por presentación.
9. **Registrar y consultar ingresos:** capturar y consultar los ingresos asociados a las ventas.
10. **Consultar información histórica:** acceder a registros de periodos anteriores.
11. **Generar estadísticas e indicadores:** consultar cantidades vendidas, ventas por periodo, número de despachos, ingresos, comportamiento de las ventas y presentaciones más solicitadas.
12. **Realizar pedidos por parte del cliente:** permitir que un cliente externo a la empresa registre y envíe su pedido directamente desde la página web.
13. **Consultar el estado de los pedidos realizados:** permitir al cliente conocer en línea el estado (pendiente o despachado) de los pedidos que ha realizado.
14. **Adaptarse a distintos dispositivos:** garantizar el correcto funcionamiento y la correcta visualización del sistema en computadores, tabletas y celulares (web responsive).

### 1.3.3. Características de los usuarios

| Usuario | Rol | Características |
|---|---|---|
| **Encargado / Administrador** | Principal usuario del sistema. Registra pedidos y ventas, organiza y consulta despachos, consulta estadísticas. | Conocimiento profundo de la operación del negocio (pedidos, despachos, rutas). Bajo nivel de formación técnica y poca experiencia con sistemas informáticos. Interactúa principalmente desde una computadora. |
| **Propietario** | Interesado en la toma de decisiones; consulta información de ventas, despachos e indicadores. | Conoce el negocio en detalle; requiere información clara y de fácil interpretación para el análisis y la toma de decisiones. |
| **Personal de operaciones (opcional)** | Puede apoyar el registro de pedidos y despachos. | Experiencia operativa del negocio; nivel técnico bajo; necesita una interfaz sencilla y guiada. |
| **Cliente** | Usuario externo a la empresa. Realiza sus pedidos desde la página web y consulta el estado de sus solicitudes. | Accede desde computador o dispositivo móvil (web responsive); nivel técnico variable; requiere una interfaz sencilla, clara y de fácil uso. |

En todos los casos, se requiere que la interfaz sea **sencilla, clara, de fácil aprendizaje y adaptable a distintos dispositivos (responsive)**, dado que los usuarios no cuentan necesariamente con un alto nivel de dominio técnico.

### 1.3.4. Limitaciones

- **Políticas regulatorias:** sin requisitos regulatorios especiales para el ámbito administrativo cubierto.
- **Limitaciones de hardware:** se empleará un computador convencional; no se contempla hardware especializado.
- **Interfaces con otras aplicaciones:** inicialmente no se integrará con aplicaciones externas de facturación, contabilidad o mensajería.
- **Operaciones paralelas:** la aplicación está orientada a un uso administrativo administrativo, con un número reducido de usuarios simultáneos.
- **Funciones de auditoría y control:** se debe conservar un registro de las operaciones (pedidos, ventas, despachos) que permita su consulta y seguimiento. Las reglas de negocio (por ejemplo, que un pedido no pueda despacharse sin registrarse, o que las ventas se registren con su fecha) se aplicarán para controlar los procesos sistematizados.
- **Requisitos de lenguaje:** la interfaz y los mensajes del sistema se implementarán en **idioma español**.
- **Criticidad de la aplicación:** la aplicación es de apoyo administrativo; si bien la información es importante para el negocio, no se gestionan sistemas de misión crítica que comprometan vidas o seguridad.
- **Seguridad y protección:** el acceso al sistema debe restringirse al personal autorizado (por ejemplo, mediante autenticación), y la información debe protegerse contra accesos no autorizados y pérdida.
- **Consideraciones físicas/mentales:** la interfaz debe ser de uso simple, con tiempos de respuesta cortos y carga cognitiva reducida, considerando el bajo nivel técnico de los usuarios.

## 1.4. Definiciones

- **Pedido:** solicitud de productos realizada por un cliente, ya sea mediante llamada telefónica, WhatsApp o de forma presencial. Contiene información sobre el cliente, las presentaciones solicitadas, las cantidades y la zona o ruta de entrega.
- **Despacho:** proceso por el cual un conjunto de pedidos es enviado para su entrega mediante un repartidor, organizado según zonas/rutas, cantidades y capacidad de los vehículos.
- **Despacho pendiente:** pedido que ha sido registrado pero que aún no ha sido despachado.
- **Despacho realizado / pedido despachado:** pedido que ya ha sido enviado para su entrega.
- **Venta:** operación comercial mediante la cual se entrega producto y se genera un ingreso; se registra por presentación.
- **Ingreso:** valor económico asociado a una venta.
- **Presentación:** tipo de producto comercializado (pacas personales, pacas para hielo, pacas de tres litros, pacas de cinco litros, pimpinas de 20 litros).
- **Zona / Ruta:** área geográfica o recorrido que emplea el negocio para organizar la entrega de pedidos.
- **Memo:** ficha física utilizada actualmente en el negocio para organizar las entregas. Se referencia únicamente como descripción del proceso actual.
- **Libreta:** registro físico de papel donde actualmente se anotan pedidos y ventas. Se referencia únicamente como descripción del proceso actual.
- **Encargado / Administrador:** persona del negocio responsable de registrar pedidos y ventas, organizar los despachos y consultar la información del sistema.
- **Cliente:** persona particular o establecimiento comercial que realiza pedidos al negocio.
- **Doble registro:** práctica actual de consignar la información primero en papel y posteriormente digitarla en un computador.

---

# 1.5. Sugerencias de requisitos identificados

Las siguientes sugerencias de requisitos se derivan de la información obtenida durante la entrevista realizada al propietario del negocio (Acta de entrevista del 26/08/2026, Anexo C) y del contexto general del proyecto. Se presentan como insumo preliminar para la elaboración de la sección 3 (Requisitos específicos) de este documento. Cada sugerencia vincula la necesidad real identificada con un posible requisito.

### Sugerencia 1 – Sistematización del registro de pedidos

Durante la entrevista, el propietario manifestó como **necesidad prioritaria la sistematización del registro de pedidos**. En la operación actual, cuando un cliente realiza un pedido (vía llamada telefónica, WhatsApp o presencialmente), la solicitud se registra manualmente en una libreta. Se sugiere definir un requisito funcional que permita **registrar un pedido en el sistema** capturando como mínimo: el cliente, las presentaciones solicitadas, las cantidades por presentación, la zona o ruta de entrega, la fecha y el medio por el cual se recibió la solicitud. Este requisito constituiría la columna vertebral del módulo de gestión de pedidos y daría respuesta directa a la necesidad prioritaria declarada por el propietario.

### Sugerencia 2 – Seguimiento del estado de los pedidos

Se evidenció en la entrevista que el seguimiento de los pedidos se realiza mediante fichas físicas denominadas "memos" y marcas de verificación en la libreta para distinguir los pedidos ya enviados de los pendientes. Se sugiere un requisito que asocie a cada pedido un **estado** (por ejemplo, *pendiente* y *despachado*) y que permita actualizarlo cuando el pedido es enviado, de manera que el sistema refleje siempre, de forma inmediata, qué pedidos se están despachando y cuáles permanecen pendientes. Esto eliminaría la consulta manual de libretas y memos descrita por el propietario.

### Sugerencia 3 – Visión centralizada de pedidos pendientes para la organización de despachos

En la entrevista se indicó que la organización de los despachos depende de la revisión de los pedidos existentes y de factores como las zonas o rutas de entrega y las cantidades solicitadas. Se sugiere un requisito que permita **consultar los pedidos pendientes de manera agrupada o filtrable por zona/ruta**, mostrando las cantidades y presentaciones de cada uno, para apoyar la decisión del encargado sin automatizarla. Complementariamente, se sugiere un requisito que permita consultar **cuáles pedidos han sido despachados** y cuáles no, reproduciendo digitalmente la distinción que hoy se hace con las marcas de verificación.

### Sugerencia 4 – Consulta de pedidos registrados

Ante la necesidad de consultar información durante la operación, se sugiere un requisito que permita **buscar y visualizar los pedidos registrados** (por cliente, fecha, estado o zona), mostrando en cada pedido la información capturada en el registro. Esta funcionalidad atiende directamente la dificultad señalada de no disponer de información inmediata y centralizada mientras se opera.

### Sugerencia 5 – Registro digital de ventas por presentación y eliminación del doble registro

La entrevista confirmó que las cantidades vendidas se registran en la libreta mediante columnas por presentación y que, para conocer lo vendido al final del día, es necesario **sumar manualmente columnas y páginas** y posteriormente digitar la información en un computador, lo que genera una **duplicación de trabajo**. Se sugiere un requisito que permita **registrar las ventas digitalmente por presentación** (pacas personales, pacas para hielo, pacas de tres litros, pacas de cinco litros y pimpinas de 20 litros) y que calcule automáticamente los totales por presentación y el total general, evitando las sumas manuales y la re-digitación de la información.

### Sugerencia 6 – Registro y consulta de ingresos

Dado que cada venta genera un ingreso y que el proyecto contempla la gestión de ingresos, se sugiere un requisito que permita **registrar y consultar los ingresos asociados a las ventas**, de forma que el valor recaudado quede disponible de inmediato y sea consultable por periodo. Esto responde a la necesidad del propietario de conocer de manera inmediata la cantidad de productos vendidos y los despachos realizados, vinculando cada venta con su correspondiente ingreso.

### Sugerencia 7 – Consulta de información histórica

En la entrevista se señaló que, para consultar información de periodos anteriores (por ejemplo, las ventas del mes anterior), es necesario recurrir a los reportes almacenados en el computador. Se sugiere un requisito que permita **consultar las ventas, pedidos y despachos de fechas anteriores mediante filtros por rango de fechas**, de modo que la información histórica quede accesible desde el sistema sin depender de procesos manuales de consolidación.

### Sugerencia 8 – Estadísticas e indicadores operativos

El propietario manifestó la necesidad de conocer de manera inmediata **cuántos productos se han vendido y cuántos despachos se han realizado**. Se sugiere un requisito que presente indicadores y gráficos con al menos: cantidad de productos vendidos (por presentación), ventas por periodo, número de despachos realizados, ingresos, comportamiento de las ventas y presentaciones más solicitadas. Este módulo de estadísticas daría respuesta a la necesidad declarada durante la entrevista y facilitaría el análisis del negocio.

### Sugerencia 9 – Clientes habituales

En la entrevista se mencionó que algunos clientes, especialmente los que realizan pedidos para el hogar, **suelen solicitar productos y cantidades similares de manera recurrente**, aunque las cantidades pueden variar según sus necesidades. Se sugiere un requisito que permita **administrar un catálogo de clientes** (particulares y establecimientos comerciales) y que, al registrar un pedido de un cliente ya existente, se muestren los datos de contacto e histórico del cliente para agilizar el registro. No se sugiere asumir cantidades fijas automáticamente, dado que los pedidos pueden variar.

### Sugerencia 10 – Requisitos no funcionales sugeridos

Con base en las características de los usuarios descritas en la sección 1.3.3 (bajo nivel de formación técnica) y en las condiciones operativas del negocio, se sugieren los siguientes requisitos no funcionales: **usabilidad** (interfaz sencilla, clara y de fácil aprendizaje, con menores tiempos de respuesta y carga cognitiva reducida); **disponibilidad** (el sistema debe permanecer disponible durante la jornada laboral del negocio); **idioma** (toda la interfaz y los mensajes en español); **seguridad y protección** (acceso restringido al personal autorizado mediante autenticación y protección contra pérdida o accesos no autorizados); y **desempeño** (tiempos de respuesta cortos para consultas y registro en condiciones normales y de jornada pico). El detalle cuantitativo y verificable de estos requisitos deberá definirse en la sección 3.

### Sugerencia 11 – Trazabilidad problema – evidencia – requisito – funcionalidad

Considerando el criterio fundamental del proyecto (Problema/necesidad → evidencia → requisito → funcionalidad → resultado esperado, descrito en el contexto y en la sección 1.2), se sugiere incluir en el documento una **tabla de trazabilidad** que relacione cada requisito sugerido con la evidencia que lo respalda (afirmaciones de la entrevista) y con la funcionalidad que lo implementará. Esta tabla facilitaría la sustentación del proyecto y garantizaría que no se agreguen funcionalidades sin justificación real.

---

# 2. Referencias

*Pendiente de elaboración.* Esta sección se completará en una etapa posterior del proyecto. Se referenciarán como mínimo: el contexto del proyecto (Contexto.md), el acta de la entrevista realizada al propietario (26/08/2026), la guía del curso para la especificación de requisitos, la norma ISO/IEC/IEEE 29148, el planteamiento del problema de la iteración 1 y las fuentes bibliográficas utilizadas en dicho planteamiento (normas APA/IEEE).

---

# 3. Requisitos específicos

*Sección en reconstrucción por el equipo.* Esta sección será elaborada por los integrantes del equipo. La versión anterior de los requisitos (RF-01 a RF-12, US-01 a US-06, DE-01 a DE-05, DS-01 a DS-06 y atributos de calidad) se conserva como respaldo en `2_Iteracion/requisitos_respaldo.md`, y la versión nueva aportada por el equipo queda registrada en el contexto del proyecto (Contexto.md).

---

# 4. Verificación

*Sección no desarrollada en la iteración actual.* Conforme a lo acordado, la verificación de los requisitos (enfoques, métodos y criterios de aceptación) no se elabora en esta etapa y quedará pendiente para una etapa posterior.
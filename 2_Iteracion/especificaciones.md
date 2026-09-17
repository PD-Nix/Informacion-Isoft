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

En esta sección se especifican los requisitos del sistema con el nivel de detalle suficiente para que los diseñadores puedan satisfacerlos y los evaluadores puedan comprobar su cumplimiento. Los requisitos se derivan del contexto del proyecto, de la información obtenida en la entrevista al propietario (sugerencias recogidas en la sección 1.5) y del requisito exigido por el docente (sistema web responsive y registro de pedidos por parte de los clientes a través de la página web).

**Convención de prioridad:** los requisitos funcionales se priorizan como **P1** (esencial para el objetivo del sistema), **P2** (importante) y **P3** (deseable).

## 3.1. Interfaces externas

*Subsección no desarrollada.* Esta parte no se realiza en la iteración actual y quedará pendiente para una etapa posterior.

## 3.2. Funciones

Los requisitos funcionales se organizan en sub-funciones correspondientes a las cinco áreas del alcance enunciadas en la sección 1.2, incorporándose además los requisitos derivados del canal web de clientes.

### Gestión de pedidos

**RF-01 – Registro de pedidos por el personal del negocio** *(Prioridad: P1 | Sugerencia 1)*
- **Descripción:** el encargado/administrador registra los pedidos recibidos (vía telefónica, WhatsApp o de forma presencial) capturando como mínimo el cliente, las presentaciones solicitadas, las cantidades por presentación, la zona o ruta de entrega, la fecha y el medio de recepción de la solicitud.
- **Entradas (estímulos):** datos del pedido ingresados a través del formulario de registro.
- **Procesamiento:** se validan los datos, se identifica o crea el cliente, se asigna al pedido el estado inicial "Pendiente" y se almacena la información.
- **Salidas (respuestas):** confirmación de registro del pedido; el pedido queda disponible en las consultas y en el listado de pedidos pendientes.
- **Criterios de validez de la entrada:** cliente obligatorio; al menos una presentación seleccionada; cantidades enteras mayores que cero; zona/ruta válida.
- **Relación entrada–salida:** todo pedido válido genera un registro persistente con estado inicial "Pendiente".

**RF-02 – Registro de pedidos por parte del cliente vía web** *(Prioridad: P1 | Requisito exigido por el docente)*
- **Descripción:** un cliente externo a la empresa realiza y envía su pedido directamente desde la página web, sin depender de la llamada telefónica o de la atención presencial.
- **Entradas (estímulos):** datos del cliente (nombre, contacto, zona/ruta), presentaciones y cantidades solicitadas.
- **Procesamiento:** se valida la información, se crea o identifica el cliente, se genera el pedido con estado "Pendiente" y se le asocia el medio "Web", quedando visible para el encargado.
- **Salidas (respuestas):** confirmación del pedido enviado y visible para el cliente; el pedido ingresa al conjunto de pedidos pendientes del negocio.
- **Criterios de validez de la entrada:** nombre y contacto válidos; al menos una presentación; cantidades enteras mayores que cero; zona/ruta válida.
- **Relación entrada–salida:** todo pedido web válido se inserta en los pendientes del mismo modo que los pedidos registrados internamente.

**RF-03 – Consulta de pedidos registrados** *(Prioridad: P1 | Sugerencia 4)*
- **Descripción:** el encargado busca y visualiza los pedidos registrados mediante filtros por cliente, fecha, estado o zona, y accede al detalle de cada pedido (presentaciones, cantidades, estado, fecha y zona).
- **Entradas (estímulos):** criterios de búsqueda o filtro del usuario.
- **Procesamiento:** se consultan los pedidos que coincidan con los criterios y se ordenan por fecha.
- **Salidas (respuestas):** listado de pedidos con su información principal y posibilidad de ver el detalle.
- **Criterios de validez de la entrada:** los filtros admiten valores vacíos (consulta general); se rechazan rangos de fechas invertidos.
- **Relación entrada–salida:** la cantidad y contenido de resultados depende de los filtros aplicados.

**RF-04 – Seguimiento del estado de los pedidos** *(Prioridad: P1 | Sugerencia 2)*
- **Descripción:** cada pedido posee un estado ("Pendiente" o "Despachado"). El encargado actualiza el estado a "Despachado" cuando el pedido es enviado para su entrega.
- **Entradas (estímulos):** acción de marcar un pedido como despachado.
- **Procesamiento:** se valida que el pedido exista y se registra la fecha de despacho asociada al cambio de estado.
- **Salidas (respuestas):** el pedido cambia a "Despachado" y deja de aparecer en los pendientes; quedan registrados la fecha y el momento del despacho.
- **Criterios de validez de la entrada:** solo se puede despachar un pedido existente y aún pendiente.
- **Relación entrada–salida:** el estado del pedido transita de "Pendiente" a "Despachado" manteniendo trazabilidad de la fecha.

### Gestión de despachos

**RF-05 – Visión centralizada de pedidos pendientes para organización de despachos** *(Prioridad: P1 | Sugerencia 3)*
- **Descripción:** el encargado consulta los pedidos pendientes agrupados o filtrables por zona/ruta, con sus cantidades y presentaciones, para apoyar la decisión de cuáles despachar juntos. El sistema **no** decide ni automatiza la agrupación.
- **Entradas (estímulos):** selección de zona o ruta (o vista general).
- **Procesamiento:** se listan los pedidos pendientes de la(s) zona(s) seleccionada(s) con sus cantidades por presentación.
- **Salidas (respuestas):** tablero de pedidos pendientes organizado por zona/ruta con totales de cantidades solicitadas.
- **Criterios de validez de la entrada:** solo se consideran pedidos con estado "Pendiente".
- **Relación entrada–salida:** el agrupamiento depende únicamente de los datos de zona, cantidades y estado del pedido.

**RF-06 – Distinción entre pedidos despachados y pendientes** *(Prioridad: P1 | Sugerencia 3)*
- **Descripción:** el sistema permite consultar por separado los pedidos pendientes y los ya despachados, reproduciendo digitalmente la distinción que hoy se hace con las marcas de verificación en la libreta.
- **Entradas (estímulos):** selección del subconjunto (pendientes o despachados) y opcionalmente fecha.
- **Procesamiento:** se filtran los pedidos según su estado.
- **Salidas (respuestas):** listado diferenciado de pedidos despachados y pendientes.
- **Criterios de validez de la entrada:** el estado debe corresponder a un valor válido del sistema.
- **Relación entrada–salida:** cada pedido pertenece exactamente a uno de los dos conjuntos.

### Gestión de ventas e ingresos

**RF-07 – Registro de ventas por presentación y totales automáticos** *(Prioridad: P1 | Sugerencia 5)*
- **Descripción:** se registran las ventas digitalmente por presentación (pacas personales, pacas para hielo, pacas de tres litros, pacas de cinco litros y pimpinas de 20 litros) y el sistema calcula automáticamente los totales por presentación y el total general, evitando las sumas manuales y la re-digitación.
- **Entradas (estímulos):** presentación, cantidad vendida y fecha de la venta.
- **Procesamiento:** se validan los datos y se calculan los totales por presentación y el total general del día/periodo.
- **Salidas (respuestas):** registro de la venta y totales por presentación y general.
- **Criterios de validez de la entrada:** cantidades enteras mayores o iguales a cero; fecha válida; presentación existente.
- **Relación entrada–salida:** total por presentación = Σ (cantidades vendidas de la presentación); total general = Σ (total por presentación × valor unitario), según los precios configurados o informados.

**RF-08 – Registro y consulta de ingresos** *(Prioridad: P1 | Sugerencia 6)*
- **Descripción:** cada venta genera un ingreso que queda asociado a ella; el encargado consulta los ingresos por periodo.
- **Entradas (estímulos):** registro de venta (o ingreso) y consultas por rango de fechas.
- **Procesamiento:** se asocia el valor del ingreso a la venta y se agregan por periodo.
- **Salidas (respuestas):** ingreso por venta y totales de ingresos por periodo consultado.
- **Criterios de validez de la entrada:** valores monetarios válidos; fechas de rango coherentes.
- **Relación entrada–salida:** ingreso del periodo = Σ (ingresos de las ventas del periodo).

**RF-09 – Consulta de información histórica** *(Prioridad: P2 | Sugerencia 7)*
- **Descripción:** el encargado consulta ventas, pedidos y despachos de periodos anteriores mediante filtros por rango de fechas, sin depender de reportes externos ni de procesos manuales.
- **Entradas (estímulos):** rango de fechas y tipo de información (ventas, pedidos o despachos).
- **Procesamiento:** se consulta la información persistida dentro del rango solicitado.
- **Salidas (respuestas):** listados y totales históricos del periodo.
- **Criterios de validez de la entrada:** rango de fechas válido y no invertido.
- **Relación entrada–salida:** los resultados corresponden exclusivamente al rango de fechas solicitado.

### Estadísticas e indicadores

**RF-10 – Estadísticas e indicadores operativos** *(Prioridad: P2 | Sugerencia 8)*
- **Descripción:** el sistema presenta indicadores y gráficos con al menos: cantidad de productos vendidos por presentación, ventas por periodo, número de despachos realizados, ingresos, comportamiento de las ventas y presentaciones más solicitadas.
- **Entradas (estímulos):** selección de periodo y del indicador a consultar.
- **Procesamiento:** se agregan los datos de ventas, pedidos y despachos del periodo según el indicador.
- **Salidas (respuestas):** indicadores numéricos y representaciones gráficas de cada métrica.
- **Criterios de validez de la entrada:** periodo válido; indicadores definidos en el sistema.
- **Relación entrada–salida:** cada indicador se calcula a partir de los registros de ventas, pedidos y despachos del periodo.

### Canal de clientes y catálogo

**RF-11 – Administración del catálogo de clientes** *(Prioridad: P2 | Sugerencia 9)*
- **Descripción:** se administra un catálogo de clientes (particulares y establecimientos comerciales); al registrar un pedido de un cliente existente se muestran sus datos de contacto e histórico. No se asumen cantidades fijas automáticamente.
- **Entradas (estímulos):** datos del cliente y acciones de alta, búsqueda o edición.
- **Procesamiento:** se validan los datos, se evitan duplicados y se asocian los pedidos al cliente.
- **Salidas (respuestas):** cliente creado/actualizado y consultable; pedidos vinculados al cliente.
- **Criterios de validez de la entrada:** identificadores y datos de contacto válidos.
- **Relación entrada–salida:** todo pedido queda asociado a un cliente del catálogo.

**RF-12 – Consulta del estado de pedidos por parte del cliente** *(Prioridad: P1 | Requisito exigido por el docente)*
- **Descripción:** el cliente externo consulta en línea el estado (Pendiente o Despachado) de los pedidos que ha realizado desde la página web.
- **Entradas (estímulos):** identificación del pedido o del cliente.
- **Procesamiento:** se valida la identificación y se consulta el estado del pedido.
- **Salidas (respuestas):** estado del pedido y su fecha de despacho cuando corresponda.
- **Criterios de validez de la entrada:** identificación válida y asociada al pedido.
- **Relación entrada–salida:** el estado mostrado corresponde al estado vigente del pedido en el sistema.

## 3.3. Requisitos de la capacidad de uso

Estos requisitos definen la calidad de uso del sistema en el contexto real del negocio (personal con bajo nivel técnico y clientes con nivel variable). Corresponden a la Sugerencia 10.

- **US-01 (Efectividad):** un usuario del negocio sin experiencia previa debe completar el registro de un pedido o de una venta sin error, siguiendo únicamente la guía de la interfaz. Criterio: el 90 % de las tareas básicas se completan con éxito sin asistencia.
- **US-02 (Eficiencia):** el registro de un pedido debe requerir a lo sumo cinco pasos y finalizarse en un tiempo menor al que hoy demanda el registro manual. Criterio: el tiempo medio de registro de un pedido no supera los dos minutos.
- **US-03 (Satisfacción):** la interfaz debe ser sencilla y comprensible. Criterio: valoración de satisfacción de uso igual o superior a 4/5 en evaluaciones con usuarios representativos.
- **US-04 (Lenguaje):** toda la interfaz, etiquetas y mensajes se presentan en español y sin tecnicismos informáticos. Criterio: ausencia de términos técnicos en pantalla evaluados por revisión.
- **US-05 (Feedbacks claros):** el sistema informa de forma clara confirmaciones y errores. Criterio: cada acción importante genera un mensaje de confirmación o error comprensible.
- **US-06 (Adaptabilidad responsive):** las tareas esenciales (registro y consulta de pedidos) son utilizables y legibles en computador, tableta y celular. Criterio: la interfaz se ajusta sin pérdida de funciones según las recomendaciones de diseño web adaptativo.

## 3.4. Requisitos de desempeño

Requisitos cuantitativos de capacidad y comportamiento (Corresponden a la Sugerencia 10).

- **DE-01 (Tiempo de respuesta):** las consultas y el registro de información responden en un tiempo inferior a tres segundos en condiciones normales, y a lo sumo cinco segundos en condiciones de carga pico.
- **DE-02 (Usuarios simultáneos):** el sistema admite al menos cinco usuarios simultáneos (personal del negocio y clientes web) sin degradación perceptible de rendimiento.
- **DE-03 (Capacidad de información):** el sistema almacena y opera correctamente con al menos los registros de un año de operación (pedidos, ventas, despachos y clientes) sin pérdida de precisión.
- **DE-04 (Disponibilidad operativa):** el sistema permanece disponible durante la jornada laboral del negocio (mínimo ocho horas diarias), permitiendo registrar y consultar información de manera inmediata.
- **DE-05 (Carga diaria):** el sistema soporta el volumen de operación típico del negocio (decenas de pedidos y ventas diarias) sin degradación perceptible.

## 3.5. Requisitos de bases de datos

*Subsección pendiente.* Esta parte no se elabora aún y se desarrollará en una etapa posterior del proyecto (entidades, relaciones, restricciones de integridad y retención de datos).

## 3.6. Restricciones de diseño

- **DS-01 (Web responsive):** el sistema se desarrolla como aplicación web responsive, adaptándose correctamente a distintos tamaños de pantalla y dispositivos (requisito exigido por el docente).
- **DS-02 (Tecnologías web estándar):** se utiliza arquitectura cliente-servidor sobre tecnologías web estándar y accesible mediante navegador web.
- **DS-03 (Idioma):** la interfaz y los mensajes del sistema se implementan en español.
- **DS-04 (Acceso restringido):** el módulo administrativo exige autenticación del personal autorizado; el canal de clientes permite el registro de pedidos sin comprometer los datos administrativos.
- **DS-05 (Alcance limitado):** el sistema no incorpora módulo contable formal, no valida inventario, no automatiza rutas ni decide la agrupación de pedidos.
- **DS-06 (Simplicidad):** el diseño de pantallas y formularios se orienta a usuarios con bajo nivel técnico, minimizando la carga cognitiva.

## 3.7. Atributos de calidad

Los atributos de calidad se presentan priorizados (1 = mayor prioridad):

1. **Usabilidad (USU):** prioridad 1. El sistema debe ser de aprendizaje rápido y uso sencillo para usuarios con bajo nivel técnico y para clientes (criterios en 3.3).
2. **Seguridad y protección (SEG):** prioridad 2. El acceso al módulo administrativo se restringe mediante autenticación y la información se protege contra accesos no autorizados y pérdida.
3. **Disponibilidad (DIS):** prioridad 3. El sistema debe estar disponible durante la jornada operativa del negocio (DE-04).
4. **Confiabilidad (CON):** prioridad 4. Los datos registrados (pedidos, ventas, despachos) se conservan de forma persistente y se prevén mecanismos de recuperación ante fallos.
5. **Portabilidad (POR):** prioridad 5. El sistema funciona correctamente en los navegadores y dispositivos habituales (computador, tableta y celular) aprovechando el diseño responsive.

## 3.8. Información de soporte

El presente documento se sustenta en el contexto del proyecto (Contexto.md), que describe la problemática real del negocio, las consecuencias identificadas y el estado actual del proyecto; en el planteamiento del problema y el acta de la entrevista realizada al propietario el 26/08/2026 (iteración 1); y en el requisito exigido por el docente relativo al diseño responsive y al registro de pedidos por parte de los clientes. A partir de estos antecedentes se identificaron los problemas que debe resolver el software (registro manual, doble registro, seguimiento de pedidos/despachos y consulta de información) y se derivaron los requisitos de las secciones anteriores. Los formatos de entrada/salida propuestos se describirán formalmente en la subsección 3.1 (Interfaces externas) cuando esta sea elaborada.

---

# 4. Verificación

*Sección no desarrollada en la iteración actual.* Conforme a lo acordado, la verificación de los requisitos (enfoques, métodos y criterios de aceptación) no se elabora en esta etapa y quedará pendiente para una etapa posterior.

---

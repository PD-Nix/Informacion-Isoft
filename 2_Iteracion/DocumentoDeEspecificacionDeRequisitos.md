Proyecto del curso de Ingeniería de Software

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

SISTEMA DE CONTABILIDAD E INVENTARIO:

— Especificación De Requisitos De Software —

Proyecto del curso de Ingeniería de Software

Profesor:

MSc., PhD Martin Monroy Rios

Universidad De Cartagena

Facultad de Ingeniería

Ingeniería de sistemas

Ingeniería de software

Cartagena D. T. y C.

2026

Tabla de contenido

[1. INTRODUCCIÓN 4](#_b8yq3mq2m7k5)

[1.1. Propósito 4](#_g85erz6x4eg1)

[1.2. Ámbito 4](#_wj6c8g6ikbgn)

[1.3 Visión general del producto 5](#_6et93732a1ky)

[1.3.1 Perspectiva del producto 5](#_m9p0assh0u3j)

[1.3.2. Funciones del producto 6](#_217eo9n2q5ri)

[1.3.3. Características de los usuarios 7](#_uf143gf9doe5)

[1.3.4. Limitaciones 7](#_v6gsd2xdjg0k)

[1.4. Definiciones 8](#_vi7om2c5w9ek)

[**3. REQUISITOS ESPECÍFICOS 11**](#_c50zjtb6qswe)

[3.1 Funciones 11](#_3nzckw95kvvx)

[3.2. Requisitos de capacidad de uso 18](#_cvm7oif427qk)

[3.2.1 Efectividad 18](#_3r5l9luqv7t)

[3.2.2 Intuitividad 18](#_7j5ig01jyrjy)

[3.2.3 Fluidez 18](#_pb1zqtx54al1)

[3.2.4 Rendimiento 18](#_xx77mp33vqor)

[3.2.5 Baja carga visual-cognitiva 18](#_lblh7danx74b)

[3.2.6 Lenguaje 18](#_cp4qd5xz3lkp)

[3.2.7 Retroalimentación 19](#_yk20g52o8g5c)

[3.2.8 Adaptabilidad 19](#_gswoypvn4mzk)

[3.3 Restricciones de diseño 19](#_roq282ncwav2)

[3.3.1. Web adaptable 19](#_tkbv1fmz6190)

[3.3.2. Tecnologías web estándar 19](#_vfvw1nvrx99m)

[3.3.3. Idioma 20](#_3wltfg4iki2c)

[3.3.4. Restricción de acceso 20](#_vetna5wamgl4)

[3.3.5. Sencillez 20](#_4vlq92ijjzrv)

[3.4. Atributos de calidad 20](#_iy1sn1a9qqij)

[3.4.1 Facilidad de uso 20](#_fwdd59rfyok)

[3.4.2 Seguridad y protección 21](#_rzbncx2bimic)

[3.4.3 Servicio Ininterrumpido 21](#_jd3j6jk2n10d)

[3.4.4 Confiable 21](#_y3b8y77ht2j)

[3.4.5 Portable 21](#_xbm4e81lzmhd)

3.5 Información de Soporte……………………………………...………………………21

## 1. INTRODUCCIÓN

## 1.1. Propósito

El propósito de este documento es definir de manera precisa y verificable los requisitos que debe cumplir el sistema web para la gestión y digitalización de la tienda de agua embotellada "Agua Frais". El documento describe la problemática que se aborda, el alcance de la solución, las funciones que debe proporcionar el sistema, las características de los usuarios que lo emplearán y las restricciones que condicionan su diseño y construcción.

Este documento está dirigido a los interesados del proyecto: el equipo de desarrollo (estudiantes de Ingeniería de Sistemas), el propietario y encargado del negocio (cliente), y el profesor de la asignatura (responsable de la evaluación). Su finalidad es servir como acuerdo entre las partes respecto de lo que el sistema debe hacer y como base para las etapas posteriores de diseño, implementación y pruebas.

## 1.2. Ámbito

El producto se denomina Sistema de Gestión para Tienda de Agua Embotellada. Es una aplicación web responsive orientada tanto a la administración del negocio como a la atención de los clientes. Por una parte, está dirigida al personal encargado de registrar, consultar y dar seguimiento a las operaciones; por otra, permite la interacción de los clientes (usuarios externos a la empresa), quienes realizan sus pedidos directamente desde la página web. De acuerdo con el requisito exigido por el docente de la asignatura, el diseño del sistema se adapta a distintos tamaños de pantalla y dispositivos.

El sistema centralizará el registro y seguimiento de las operaciones del negocio con el fin de reemplazar el proceso manual que actualmente requiere registrar inicialmente las solicitudes en una libreta y posteriormente digitar la información en un computador. Concretamente, el sistema permitirá:

* Permitir que los clientes realicen y envíen sus pedidos directamente desde la página web, sin depender exclusivamente de la llamada telefónica o de la atención presencial.
* Registrar y consultar los pedidos recibidos, visualizando su estado y las cantidades solicitadas.
* Proporcionar al encargado una visión centralizada de los pedidos pendientes para facilitar la organización de los despachos según las rutas, cantidades y capacidad de los vehículos.
* Registrar y consultar las ventas e ingresos, evitando el doble registro manual/digital.
* Incorporar estadísticas e indicadores para consultar información como la cantidad de productos vendidos, los despachos realizados, los ingresos y el comportamiento de las ventas.

El alcance funcional del proyecto se concentra en cinco áreas principales:

* **Gestión de pedidos:** Registro, consulta, visualización de la información de cada pedido, y seguimiento del estado.
* **Gestión de despachos:** Visualización de pedidos pendientes, consulta de cantidades y zonas asociadas, apoyo a la organización de despachos y consulta de qué pedidos han sido despachados o permanecen pendientes.
* **Gestión de ventas e ingresos:** Registro y consulta de ventas e ingresos, evitando el doble registro, y facilitando la consulta de información histórica.
* **Estadísticas e indicadores:** Gráficos e indicadores sobre cantidades vendidas, ventas por periodo, número de despachos, ingresos, comportamiento de las ventas y presentaciones más solicitadas.
* **Canal de pedidos de clientes (web):** Brindar a los clientes la posibilidad de registrar sus pedidos a través de la página web y consultar el estado de sus solicitudes, accediendo desde distintos dispositivos (computador, tableta o celular) gracias al diseño responsive del sistema.

## 1.3 Visión general del producto

### 1.3.1 Perspectiva del producto

**1.3.1.1 Interfaces del sistema**

**Interfaces de usuario.** El sistema será accesible mediante un navegador web desde computador o dispositivos móviles, con un diseño responsive que se adapta al tamaño de pantalla. Las pantallas se organizan por módulos administrativos (pedidos, despachos, ventas e ingresos, estadísticas) y por un módulo orientado al cliente para la realización y consulta de pedidos en línea.

**Interfaces de hardware.** Se utilizará un computador con acceso a internet para la administración. No se prevé el uso de hardware especializado.

**Interfaces de software.** El sistema se ejecutará sobre tecnologías web estándar (cliente-servidor) y hará uso de una base de datos para el almacenamiento persistente de la información.

**Interfaces de comunicación.** El sistema operará a través del protocolo HTTP/HTTPS sobre la red local o internet.

**1.3.1.2 Operación**

**Condiciones ambientales:** el sistema opera en condiciones normales de una pequeña empresa (local u oficina del negocio, jornada diurna), sin requerimientos ambientales especiales.

**Modos de operación:** el sistema contempla dos modos de uso. El modo administrativo, empleado por el personal del negocio durante la jornada laboral (registro y consulta de pedidos, ventas, ingresos, organización de despachos y consulta de estadísticas). El modo cliente, en el que los usuarios externos acceden desde la página web para realizar sus pedidos y consultar el estado de los mismos; los pedidos recibidos por este canal se procesan durante la operación del negocio.

**Disponibilidad y continuidad:** El sistema debe permanecer disponible durante la operación del negocio, permitiendo al personal consultar y registrar información de manera inmediata, y a los clientes realizar y consultar sus pedidos en línea.

**Cumplimiento regulatorio operativo:** No se identifican requisitos regulatorios especiales para el ámbito administrativo cubierto.

**1.3.1.3 Adaptación al sitio.**

**Infraestructura existente:** El sistema requiere únicamente un computador o dispositivo con acceso a internet y un navegador web; no depende de infraestructura tecnológica previa en el negocio.

**Condiciones culturales y del contexto del problema:** El sistema debe adaptarse a las condiciones del negocio: personal con bajo nivel de formación técnica, uso del idioma español, operaciones desarrolladas en un contexto de pequeña empresa y clientes que acceden desde distintos dispositivos.

### 1.3.2. Funciones del producto

El sistema permite registrar, consultar y dar seguimiento a los pedidos del negocio, capturando clientes, presentaciones, cantidades, zona/ruta, fecha y medio de recepción, administrando un catálogo de clientes y actualizando el estado de cada pedido (Pendiente a Despachado). Los clientes externos realizan sus pedidos directamente desde la página web y pueden consultar en línea el estado de los mismos. El sistema apoya la organización de los despachos mostrando los pedidos pendientes agrupados por zona con sus cantidades, distingue los pedidos despachados de los pendientes y permite consultar información histórica por rango de fechas. Complementariamente, registra las ventas por presentación con totales automáticos y los ingresos asociados, y presenta estadísticas e indicadores (cantidades vendidas, ventas por periodo, número de despachos, ingresos, comportamiento de las ventas y presentaciones más solicitadas). Cada una de estas funciones se detalla en la sección 3.2.

###

###

###

###

### 1.3.3. Características de los usuarios

**Tabla 1: Caracterización de usuarios del sistema.**

| **Usuario** | **Rol** | **Características** |
| --- | --- | --- |
| **Encargado / Administrador** | Principal usuario del sistema. Registra pedidos y ventas, organiza y consulta despachos, consulta estadísticas. | Conocimiento profundo de la operación del negocio (pedidos, despachos, rutas). Bajo nivel de formación técnica y poca experiencia con sistemas informáticos. Interactúa principalmente desde una computadora. |
| **Propietario** | Interesado en la toma de decisiones; consulta información de ventas, despachos e indicadores. | Conoce el negocio en detalle; requiere información clara y de fácil interpretación para el análisis y la toma de decisiones. |
| **Cliente** | Usuario externo a la empresa. Realiza sus pedidos desde la página web y consulta el estado de sus solicitudes. | Accede desde computador o dispositivo móvil (web responsive); nivel técnico variable; requiere una interfaz sencilla, clara y de fácil uso. |

En todos los casos, se requiere que la interfaz sea sencilla, clara, de fácil aprendizaje y adaptable a distintos dispositivos (responsive), dado que los usuarios no cuentan necesariamente con un alto nivel de dominio técnico.

### 1.3.4. Limitaciones

**Políticas regulatorias**:: El sistema debe cumplir con la Ley 1581 de 2012 sobre protección de datos personales y con la Ley Estatutaria 1266 de 2008 de habeas data, dado que procesa información personal.

**Limitaciones de hardware**: El personal del negocio empleará un computador convencional con acceso a internet; no se contempla hardware especializado. Los clientes acceden desde sus propios dispositivos (computador, tableta o celular), lo que se aborda mediante el diseño responsive.

**Interfaces con otras aplicaciones:** Dentro del alcance de esta iteración no se integrará con aplicaciones externas de facturación, contabilidad o mensajería; el sistema gestiona su información de forma independiente.

**Funciones de auditoría y control:** Se debe conservar un registro de las operaciones (pedidos, ventas, despachos) que permita su consulta y seguimiento. Las reglas de negocio (por ejemplo, que un pedido no pueda despacharse sin registrarse, o que las ventas se registren con su fecha) se aplicarán para controlar los procesos sistematizados.

**Requisitos de lenguaje**: La interfaz y los mensajes del sistema se implementará en idioma español.

**Operaciones paralelas:** El sistema admite dos modos de uso: el administrativo (personal del negocio) y el de cliente (usuarios externos que realizan pedidos desde la página web). Se prevé un volumen de operaciones propio de una pequeña empresa, con pocos usuarios administrativos simultáneos y un número de clientes en línea reducido en comparación con sistemas de alto tráfico.

**Uso de protocolos:** El sistema se comunica mediante los protocolos web estándar HTTP/HTTPS; no requiere protocolos especiales adicionales.

**Criticidad de la aplicación:** El sistema apoya la operación del negocio y el canal de pedidos en línea de los clientes. Si bien la información que gestiona es importante para la toma de decisiones, no se administran sistemas de misión crítica que comprometan vidas o la seguridad de las personas.

**Seguridad y protección:** El acceso al sistema debe restringirse al personal autorizado (por ejemplo, mediante autenticación), y la información debe protegerse contra accesos no autorizados y pérdida.

**Consideraciones físicas/mentales**: La interfaz será de uso simple, con tiempos de respuesta cortos y carga cognitiva reducida, considerando el bajo nivel técnico del personal del negocio y el nivel variable de los clientes.

## 1.4. Definiciones

* **Administrativo**: Persona con autoridad encargada del negocio.
* **Cliente:** Persona particular o establecimiento comercial que realiza pedidos al negocio.
* **Despacho:** Proceso por el cual un conjunto de pedidos es enviado para su entrega mediante un repartidor, organizado según zonas/rutas, cantidades y capacidad de los vehículos.
* **Despacho pendiente:** Pedido que ha sido registrado pero que aún no ha sido despachado.
* **Despacho realizado / pedido despachado:** Pedido que ya ha sido enviado para su entrega.
* **Doble registro:** Práctica actual de consignar la información primero en papel y posteriormente digitarla en un computador.
* **Encargado / Administrador:** Persona del negocio responsable de registrar pedidos y ventas, organizar los despachos y consultar la información del sistema.
* **Ingreso:** Valor económico asociado a una venta.
* **Libreta:** registro físico de papel donde actualmente se anotan pedidos y ventas. Se refiere únicamente como descripción del proceso actual.
* **Memo:** Ficha física utilizada actualmente en el negocio para organizar las entregas. Se refiere únicamente como descripción del proceso actual.
* **Operador:** Empleado que usa el software sin ser administrador, encargado de la gestión y administración de ventas y pedidos.
* **Pedido:** Solicitud de productos realizada por un cliente, ya sea mediante llamada telefónica, WhatsApp o de forma presencial. Contiene información sobre el cliente, las presentaciones solicitadas, las cantidades y la zona o ruta de entrega.
* **Presentación:** Tipo de producto comercializado (pacas personales, pacas para hielo, pacas de tres litros, pacas de cinco litros, pimpinas de 20 litros).
* **Repartidor:** Persona encargada de repartir (entregar) los pedidos a los clientes.
* **Venta:** operación comercial mediante la cual se entrega producto y se genera un ingreso; se registra por presentación.
* **Zona:** Área geográfica o recorrido que emplea el negocio para organizar la entrega de pedidos.

#

#

#

#

#

#

#

#

#

#

2. REFERENCIAS

[1] ISO/IEC/IEEE, *Systems and software engineering — Life cycle processes — Requirements engineering*, ISO/IEC/IEEE Standard 29148:2018, 2018.
[2] P. Díaz, N. Torres, A. Rincón y J. Jiménez, "Documento de Primera Iteración," 2026.[En línea]. Disponible: <https://docs.google.com/document/d/12au8FxmFyoCbNjGNzZfnd3cnBZ-6jzFnrVDAF3H-56Y/edit?usp=sharing>.

# 3. REQUISITOS ESPECÍFICOS

## 3.1 Funciones

| **Identificador** | RF-01 |
| --- | --- |
| **Título** | Registro de pedidos y seguimiento de estado (personal del negocio) |
| **Descripción** | El sistema debe permitir al encargado o administrador registrar los pedidos recibidos mediante canales tradicionales (llamada telefónica, WhatsApp o atención presencial). Al momento del registro, el usuario puede buscar y seleccionar un cliente existente para precargar sus datos de contacto e historial o crear un cliente nuevo si no existe. Se capturan las presentaciones de agua solicitadas, las cantidades por presentación, la zona o ruta de entrega, la fecha y el medio de recepción. El pedido ingresa con el estado inicial “Pendiente” y posteriormente el usuario administrativo puede actualizar su estado a “Despachado”, registrando la fecha exacta del despacho. |
| **Entradas** | Datos del cliente (Nombre, Teléfono, Dirección): String Presentaciones de productos solicitadas y cantidades: List  Zona / Ruta de entrega: String Fecha de recepción: Date  Medio de recepción (Teléfono, WhatsApp, Presencial): Enum/String Fecha de despacho y estado (al actualizar): Date, Enum/String |
| **Secuencia de operaciones** | 1. El encargado accede al módulo de registro de pedidos.  2. El sistema presenta el formulario de ingreso con la opción de búsqueda o registro de clientes.  3. El usuario busca un cliente registrado por su nombre o teléfono; si existe, el sistema carga sus datos de contacto e historial de compras.  4. El usuario selecciona las presentaciones de agua requeridas, ingresa las cantidades, especifica la zona/ruta de entrega y selecciona el medio de recepción.  5. El sistema calcula automáticamente los subtotales por presentación y el monto total del pedido.  6. El usuario confirma y guarda la información del pedido.  7. El sistema almacena el pedido con el estado inicial “Pendiente” y genera un número de identificador único.  8. (Posteriormente) Cuando el pedido es enviado al cliente, el encargado cambia su estado a “Despachado”, actualizando el registro en la base de datos. |
| **Salidas** | • Confirmación en pantalla del registro exitoso del pedido con su identificador único.  • Ficha de cliente creada o actualizada en la base de datos.  • Nuevo registro almacenado en el listado global de pedidos en estado “Pendiente”.  • Estado del pedido actualizado a “Despachado” con la fecha de envío registrada.  • Mensaje informativo o de advertencia en caso de datos faltantes o clientes no encontrados. |
| **Situaciones anormales** | 3a.El cliente no se encuentra registrado y el usuario no completa los datos obligatorios para su creación.  4a. Las cantidades ingresadas para una presentación de agua son menores o iguales a cero.  7a. Fallos de conexión con la base de datos durante el registro o actualización del pedido. |
| **Precondición** | El usuario debe haber accedido al sistema con un rol administrativo o de encargado previamente autenticado. |
| **Prioridad** | Alta |

| **Identificador** | RF-02 |
| --- | --- |
| **Título** | Registro de pedidos por parte del cliente vía web |
| **Descripción** | El sistema debe permitir a los clientes externos ingresar a la página web pública de la empresa, visualizar el catálogo de presentaciones de agua disponibles y realizar la solicitud directa de sus pedidos de manera autónoma, sin depender de llamadas o atención presencial. El pedido registrado queda asociado automáticamente al medio de recepción “Web” e ingresa en estado “Pendiente”, quedando visible inmediatamente para el encargado en el panel central para su posterior procesamiento. |
| **Entradas** | Datos del cliente web (Nombre, Teléfono, Correo, Dirección de entrega, Zona): String  Presentaciones seleccionadas y cantidades requeridas: List  Fecha deseada de entrega: Date  Observaciones o notas de entrega (opcional): String |
| **Secuencia de operaciones** | 1. El cliente externo accede al portal web de la empresa distribuidora de agua.  2. El sistema despliega el catálogo interactivo de presentaciones de productos con sus respectivos precios unitarios.  3. El cliente selecciona las presentaciones de productos deseadas, especifica la cantidad de cada una y las agrega al carrito de compras. 4. El cliente ingresa sus datos personales, la dirección exacta de despacho y la zona/ruta de entrega correspondiente.  5. El sistema calcula automáticamente el total de la compra y muestra un resumen detallado.  6. El cliente confirma y envía la solicitud de pedido.  7. El sistema valida los datos obligatorios, asocia el medio de recepción “Web”, asigna el estado inicial “Pendiente” y guarda el registro.  8. El sistema notifica al panel del encargado sobre la recepción de un nuevo pedido web. |
| **Salidas** | • Comprobante visual en pantalla para el cliente con el código de seguimiento del pedido y resumen de la solicitud.  • Registro de nuevo pedido ingresado al sistema con estado “Pendiente” y medio asignado “Web”.  • Alerta visual en el panel del encargado sobre la recepción del nuevo pedido.  • Mensaje de advertencia si la información del formulario está incompleta. |
| **Situaciones anormales** | 3a. El cliente no ingresa campos obligatorios como número telefónico o dirección de entrega.  4a. El carrito de compras se encuentra vacío al intentar confirmar la solicitud.  5a. Pérdida de conexión a internet o interrupción en el servidor durante el envío del pedido vía web. |
| **Precondición** | El portal web debe encontrarse activo y en línea con acceso público a internet. |
| **Prioridad** | Alta (P1) |

| **Identificador** | RF-03 |
| --- | --- |
| **Título** | Consulta de pedidos y apoyo a la organización de despachos |
| **Descripción** | El sistema debe permitir al usuario administrativo buscar, consultar y filtrar el listado general de pedidos mediante parámetros como cliente, fecha, estado o zona/ruta. El sistema debe ofrecer una vista donde los pedidos pendientes se muestren agrupados o filtrables por zona/ruta junto con la suma de cantidades y presentaciones requeridas, sirviendo como insumo informativo para facilitar al personal la organización manual de las rutas de despacho. Asimismo, debe distinguir claramente los pedidos pendientes de los despachados y permitir la consulta histórica de operaciones en rangos de fechas definidos |
| **Entradas** | Criterios de filtro (Nombre de cliente, Rango de fechas, Zona/Ruta, Estado del pedido: Pendiente / Despachado): String / Date / Enum. |
| **Secuencia de operaciones** | 1. El usuario administrativo accede al módulo de consulta de pedidos y despachos.  2. El sistema presenta la interfaz con los campos de búsqueda y filtros disponibles.  3. El usuario ingresa o selecciona los criterios de consulta deseados (por ejemplo, estado “Pendiente” y una zona geográfica específica). 4. El usuario selecciona la opción para agrupar pedidos por el criterio que necesite.  5. El sistema procesa los registros de la base de datos y presenta los pedidos agrupados por el criterio, dando información de importancia para el personal administrativo.  6. El usuario revisa la información consolidada para planificar y organizar los despachos.  7. (Opcional) El usuario cambia el rango de fechas o estado a “Despachado” para consultar el historial de entregas realizadas. |
| **Salidas** | • Tabla interactiva con el listado de pedidos filtrados según los parámetros definidos.  • Vista consolidada de pedidos pendientes agrupados por zona/ruta con totales por presentación de producto.  • Visualización del detalle individual de cada pedido (cliente, presentaciones, cantidades, estado y fecha).  • Reporte en pantalla con el historial de pedidos despachados en el rango de fechas seleccionado.  • Mensaje informativo en caso de que no existan datos para los filtros seleccionados. |
| **Situaciones anormales** | 3a. El usuario ingresa un rango de fechas inválido (p. ej., fecha inicial posterior a la fecha final)  4a. No se encuentran registros de pedidos que coincidan con la zona, cliente o estado especificado.  5a. Fallos de conexión con la base de datos durante la consulta de datos históricos. |
| **Precondición** | El usuario debe haber accedido al sistema con un rol administrativo o de encargado previamente autenticado. |
| **Prioridad** | Alta |

| **Identificador** | RF-04 |
| --- | --- |
| **Título** | Registro de ventas e ingresos |
| **Descripción** | El sistema debe registrar las ventas por presentación realizando de manera automática los cálculos de totales por producto y el total general de la transacción, evitando sumas manuales y previniendo el doble registro de información. Cada venta concretada genera un ingreso asociado en el módulo financiero. Además, el sistema permite al encargado consultar el balance de ingresos agregados por periodos de tiempo específicos (día o rango de fechas). |
| **Entradas** | Identificador de pedido a concretar o datos de venta directa: String Presentaciones y cantidades vendidas: List  Método de pago (Efectivo, Transferencia, etc.): Enum/String  Rango de fechas para la consulta de ingresos (Fecha inicio, Fecha fin): Date |
| **Secuencia de operaciones** | 1. El usuario administrativo selecciona un pedido para formalizar la venta o ingresa una venta directa en el módulo.  2. El sistema toma los ítems y cantidades por presentación de agua y calcula automáticamente los subtotales y el gran total de la venta.  3. El sistema efectúa el registro de la venta, generando el ingreso financiero asociado e integrándolo en la contabilidad general.  4. Para consultar ingresos, el usuario accede al submódulo de reportes de ingresos.  5. El usuario ingresa un día específico o selecciona un rango de fechas.  6. El sistema realiza el cálculo consolidado sumando todas las ventas e ingresos del periodo especificado.  7. El sistema muestra en pantalla el reporte consolidado con los totales agregados. |
| **Salidas** | • Registro de venta guardado con desglose automático de subtotales y total general.  • Ingreso financiero registrado e integrado al flujo contable del negocio.  • Reporte en pantalla con la suma de ingresos consolidados en el periodo o fecha consultada.  • Mensaje informativo en caso de que no existan datos para el periodo seleccionado |
| **Situaciones anormales** | 3a. Intento de registrar una venta con importes o cantidades de productos iguales o inferiores a cero.  4a. El usuario ingresa un rango de fechas inválido (p. ej., fecha inicial posterior a la fecha final).  5a. No se encuentran registros de ventas o ingresos en el rango de fechas seleccionado.  6a. Fallos de conexión con la base de datos durante el cálculo y consolidación de ingresos. |
| **Precondición** | El usuario debe haber accedido al sistema con un rol administrativo o de propietario previamente autenticado. |
| **Prioridad** | Alta |

| **Identificador** | RF-05 |
| --- | --- |
| **Título** | Estadísticas e indicadores operativos |
| **Descripción** | El sistema debe permitir al usuario administrativo visualizar un tablero de control con gráficos e indicadores operativos sobre el desempeño comercial del negocio. Esto incluye la cantidad de productos vendidos clasificados por presentación, las ventas e ingresos totales consolidados por periodos de tiempo, el número total de despachos realizados, la tendencia del comportamiento de las ventas y el ranking de las presentaciones de productos más solicitadas. |
| **Entradas** | Rango de fechas (Fecha inicial, Fecha final): Date, Tipo de presentación de producto (opcional): String, Tipo de indicador a consultar: String. |
| **Secuencia de operaciones** | 1. El usuario administrativo accede al módulo de estadísticas e indicadores operativos.  2. El sistema presenta la interfaz con los filtros de consulta (rango de fechas, presentación) y los indicadores predeterminados del periodo actual.  3. El usuario selecciona el rango de fechas u otros filtros de interés y solicita la generación de la información.  4. El sistema consulta y procesa la información registrada de ventas, despachos e ingresos almacenada en la base de datos.  5. El sistema calcula las métricas requeridas y genera las gráficas e indicadores correspondientes.  6. El sistema despliega en pantalla la información consolidada y los gráficos generados. |
| **Salidas** | • Gráficos interactivos de ventas e ingresos por periodo y comportamiento histórico.  • Indicadores numéricos de cantidad de productos vendidos por presentación y número de despachos realizados.  • Listado/ranking de las presentaciones más solicitadas.  • Mensaje informativo en caso de que no existan datos para el periodo seleccionado. |
| **Situaciones anormales** | 3a. El usuario ingresa un rango de fechas inválido (p. ej., fecha inicial posterior a la fecha final).  4a. No se encuentran registros de ventas o despachos en el rango de fechas seleccionado.  5a. Fallos de conexión con la base de datos durante la consulta de datos históricos. |
| **Precondición** | El usuario debe haber accedido al sistema con un rol administrativo o de propietario previamente autenticado. |
| **Prioridad** | Media |

| **Identificador** | RF-06 |
| --- | --- |
| **Título** | Consulta del estado de pedidos por parte del cliente |
| **Descripción** | El sistema debe permitir a los clientes externos consultar en línea y en tiempo real el estado actual (Pendiente o Despachado) de los pedidos que han realizado desde la página web del negocio. La consulta mostrará los detalles de la solicitud y, en caso de que el pedido haya sido enviado, incluirá la fecha y hora de despacho correspondiente. |
| **Entradas** | Código de seguimiento o número de identificación del pedido: String |
| **Secuencia de operaciones** | 1. El cliente externo accede a la sección de consulta de estado de pedidos en la página web.  2. El sistema presenta el formulario de consulta con el campo de búsqueda.  3. El cliente ingresa el código del pedido y presiona el botón de búsqueda.  4. El sistema valida los datos ingresados y busca los pedidos asociados en la base de datos.  5. El sistema recupera la información del pedido, incluyendo su estado (Pendiente o Despachado) y la fecha de despacho si ya fue realizado.  6. El sistema presenta al cliente la información detallada sobre el estado de su pedido. |
| **Salidas** | • Visualización en pantalla del estado actual del pedido (Pendiente o Despachado).  • Resumen del pedido (presentaciones solicitadas, cantidades y fecha de despacho cuando corresponda).  • Mensaje de advertencia si no se encuentra ningún pedido asociado al dato ingresado. |
| **Situaciones anormales** | 3a. El cliente envía el formulario con campos vacíos o con un formato de texto incorrecto.  4a. El sistema no localiza ningún pedido en la base de datos con el identificador o número proporcionado.  5a. Ocurre una interrupción de conexión con el servidor al procesar la búsqueda. |
| **Precondición** | El cliente debe acceder a la interfaz pública web desde cualquier navegador con conexión a internet. |
| **Prioridad** | Media |

## 3.2. Requisitos de capacidad de uso

### 3.2.1 Efectividad

El sistema debe ser altamente confiable y seguro, diseñado para funcionar sin presentar bloqueos ni pérdidas de información. El usuario podrá iniciar y finalizar cualquier operación con la certeza de que los procesos se completarán con éxito. El programa valida y confirma cada operación, guarda cada dato de forma persistente en el momento del registro y no deja operaciones a medias: ninguna interacción se pierde ni queda bloqueada.

Prioridad: Alta

### 3.2.2 Intuitividad

Un operador o cliente del negocio sin experiencia previa es capaz de completar el registro de un pedido o de una venta siguiendo las instrucciones del manual de usuario; el promedio de los operadores y clientes debe ser capaz de operar el sistema sin presentar fricción cognitiva; la curva de aprendizaje del aplicativo es baja.

Prioridad: Media

### 3.2.3 Fluidez

La navegación y uso del sistema ocurren a una tasa de fotogramas alta para que el ojo humano lo perciba como algo orgánico y en tiempo real. El programa procesa las interacciones sin esperas perceptibles (sin recargas ni "congelamientos"), de modo que la navegación se perciba continua y en tiempo real.

Prioridad: Media

### 3.2.4 Rendimiento

Un operador, cliente o administrativo no puede sentir retardos (alta latencia) al momento de ejecutar el software. El programa procesa las operaciones sin esperas perceptibles, de modo que el usuario nunca percibe bloqueos ni retardos.

Prioridad: Media

### 3.2.5 Baja carga visual-cognitiva

La interfaz de usuario debe ser sencilla y comprensible. No saturar la mente del usuario con exceso de información. El programa presenta en cada pantalla solo la información necesaria (formularios y listados simplificados, organizados por módulos), sin saturar al usuario.

Prioridad:Alta

### 3.2.6 Lenguaje

Toda la interfaz, etiquetas y mensajes se presentan en español y sin tecnicismos. El programa presenta toda la interfaz, etiquetas y mensajes en español, redactados en lenguaje cotidiano y sin tecnicismos.

Prioridad: Alta

### 3.2.7 Retroalimentación

El sistema generará mensajes de confirmación o de error de manera oportuna y asertiva. Cada acción importante genera un mensaje comprensible para los usuarios independientemente de su cargo. El programa emite un mensaje claro de confirmación o de error tras cada acción importante, con lenguaje comprensible para cualquier usuario.

Prioridad: Alta

### 3.2.8 Adaptabilidad

Las interfaces gráficas de usuario del software son legibles y visualmente estéticas sin importar el dispositivo desde el que se opere; el dispositivo empleado para usar el software no es un impedimento para su operación. El programa ajusta automáticamente la interfaz al tamaño del dispositivo (diseño responsive), permaneciendo legible y operable desde computador, tableta o celular sin perder funciones.

Prioridad: Alta.

## 3.3 Restricciones de diseño

### 3.3.1. Web adaptable

El sistema debe desarrollarse como una aplicación web con un diseño adaptativo (*responsive*), garantizando que sus interfaces gráficas se ajusten y visualicen correctamente en distintos tamaños de pantalla y dispositivos, tales como computadores de escritorio, tabletas y teléfonos móviles.

Se verificará la correcta distribución de los elementos de la interfaz, sin desbordamientos ni superposiciones, en al menos tres resoluciones estándar (móvil, tableta y escritorio) utilizando herramientas de emulación de navegadores. Además, las funcionalidades críticas (registrar pedidos, consultar ventas) deben poder completarse con éxito desde cualquier tamaño de pantalla.

Prioridad: Alta

### 3.3.2. Tecnologías web estándar

El sistema debe estar construido bajo una arquitectura cliente-servidor implementando tecnologías web estándar. El aplicativo debe ser accesible mediante un navegador web, operando sobre protocolos HTTP/HTTPS, sin necesidad de hardware especializado o instalaciones adicionales en los equipos de los usuarios.

Se comprobará la operatividad del sistema accediendo a él desde las versiones recientes de al menos tres navegadores web de uso masivo (por ejemplo: Google Chrome, Mozilla Firefox, Microsoft Edge o Safari), validando que el intercambio de información cliente-servidor se ejecute correctamente.

Prioridad: Alta

### 3.3.3. Idioma

Toda la interfaz de usuario, incluyendo menús, etiquetas, formularios, notificaciones y mensajes de retroalimentación, debe presentarse de manera clara y exclusiva en idioma español, evitando el uso de terminología técnica compleja que dificulte la comprensión.

Se realizará una inspección visual y funcional de la totalidad de las pantallas (tanto del módulo administrativo como del canal de clientes) para constatar que el 100% de los textos orientados al usuario estén redactados en español y sean ortográficamente correctos.

Prioridad: Alta

### 3.3.4. Restricción de acceso

El sistema debe implementar mecanismos de seguridad que limiten el acceso a los datos y funciones sensibles. El módulo administrativo exigirá autenticación obligatoria para el personal autorizado. Por otro lado, el canal web orientado a los clientes permitirá la realización de pedidos de forma independiente, garantizando que estos usuarios externos no puedan visualizar ni comprometer la información administrativa o financiera del negocio.

Se ejecutarán pruebas de control de acceso intentando ingresar a los enlaces y módulos administrativos sin credenciales o con roles de menor nivel, validando que el sistema deniegue la solicitud. Adicionalmente, se realizará el flujo completo de un pedido desde el perfil de cliente para confirmar que no se expone información de inventario o ventas en ningún paso del proceso.
Prioridad: Alta

### 3.3.5. Sencillez

El diseño de las pantallas y formularios del sistema debe mantener una baja carga visual y cognitiva, orientándose a usuarios que poseen un bajo nivel de formación técnica y poca experiencia con sistemas informáticos. La interfaz debe ser intuitiva, con flujos de trabajo guiados que faciliten una baja curva de aprendizaje

Se realizarán pruebas de usabilidad guiadas y no guiadas con usuarios reales o perfiles equivalentes al encargado del negocio y a clientes típicos. Se considerará cumplido si el usuario logra completar las operaciones principales (registrar una venta, consultar un despacho y hacer un pedido) sin necesidad de asistencia técnica

Prioridad: Alta

## 3.4. Atributos de calidad

### 3.4.1 Facilidad de uso

El sistema presenta una baja curva de aprendizaje, lo que permite que los distintos usuario del sistema puedan empezar a usar de manera rápida y sencilla.

mediante diseño centrado en el usuario, formularios guiados paso a paso y pruebas de uso con usuarios representativos (operador, administrativo y cliente) antes de la entrega.

Prioridad: Alta

### 3.4.2 Seguridad y protección

El acceso a datos y funciones sensibles del sistema solo será accesible desde el módulo más alto de la aplicación (el administrativo), el cual poseerá mecanismos de autenticación para el acceso, así como confirmación y verificaciones avanzadas para la realización de cambios sensibles, mediante autenticación obligatoria en el módulo administrativo, control de roles (administrativo y operador), confirmaciones adicionales para los cambios sensibles y respaldo de la información

Prioridad: Alta

### 3.4.3 Servicio Ininterrumpido

Las funcionalidades y datos correspondientes a los distintos módulos del sistema deberán estar disponibles en todo momento mientras este se encuentre operativo. La alta concurrencia no debe afectar de manera notable ni significativa esta disponibilidad, esto se da mediante un despliegue estable del servicio y pruebas de carga que verifiquen que la concurrencia no degrada los tiempos de respuesta.

Prioridad: Alta

### 3.4.4 Confiable

Los datos registrados se conservan de forma persistente con mecanismos de recuperación ante fallos, mediante almacenamiento persistente en base de datos, respaldos automáticos programados y mecanismos de recuperación ante fallos. Prioridad:Media.

### 3.4.5 Portable

El sistema funciona correctamente en los distintos sistemas operativos, dispositivos y navegadores empleados para su ejecución y operación, y sus características no se ven comprometidas por esto. Esto se cumplirá usando tecnologías web estándar y diseño responsive, con pruebas de funcionamiento en los navegadores, sistemas operativos y dispositivos de uso habitual (computador, tableta y celular).

Prioridad: Media.

3.5 Información de soporte

Para entender correctamente el contexto del problema es pertinente leer el acta de la entrevista que se realizó a la ceo de la empresa para la cual se genera la solución

[**Acta\_Entrevista1-f-1.pdf**](https://drive.google.com/file/d/1wXA3Z2P5tWpAfjo84u9MT0wYcDseK0zq/view?usp=sharing)
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

- **Condiciones ambientales:** el sistema opera en condiciones normales de una pequeña empresa (local u oficina del negocio, jornada diurna), sin requerimientos ambientales especiales.
- **Modos de operación:** el sistema contempla dos modos de uso. El **modo administrativo**, empleado por el personal del negocio durante la jornada laboral (registro y consulta de pedidos, ventas, ingresos, organización de despachos y consulta de estadísticas). El **modo cliente**, en el que los usuarios externos acceden desde la página web para realizar sus pedidos y consultar el estado de los mismos; los pedidos recibidos por este canal se procesan durante la operación del negocio.
- **Disponibilidad y continuidad:** el sistema debe permanecer disponible durante la operación del negocio, permitiendo al personal consultar y registrar información de manera inmediata, y a los clientes realizar y consultar sus pedidos en línea.
- **Cumplimiento regulatorio operativo:** no se identifican requisitos regulatorios especiales para el ámbito administrativo cubierto.

**Adaptación al sitio:**

- **Infraestructura existente:** el sistema requiere únicamente un computador o dispositivo con acceso a internet y un navegador web; no depende de infraestructura tecnológica previa en el negocio.
- **Condiciones culturales y del contexto del problema:** el sistema debe adaptarse a las condiciones del negocio: personal con bajo nivel de formación técnica, uso del idioma español, operaciones desarrolladas en un contexto de pequeña empresa y clientes que acceden desde distintos dispositivos.

### 1.3.2. Funciones del producto

El sistema permite registrar, consultar y dar seguimiento a los pedidos del negocio, capturando cliente, presentaciones, cantidades, zona/ruta, fecha y medio de recepción, administrando un catálogo de clientes y actualizando el estado de cada pedido (Pendiente a Despachado). Los clientes externos realizan sus pedidos directamente desde la página web y pueden consultar en línea el estado de los mismos. El sistema apoya la organización de los despachos mostrando los pedidos pendientes agrupados por zona con sus cantidades, distingue los pedidos despachados de los pendientes y permite consultar información histórica por rango de fechas. Complementariamente, registra las ventas por presentación con totales automáticos y los ingresos asociados, y presenta estadísticas e indicadores (cantidades vendidas, ventas por periodo, número de despachos, ingresos, comportamiento de las ventas y presentaciones más solicitadas). Cada una de estas funciones se detalla en la sección 3.2 (requisitos funcionales RF-01 a RF-06); la adaptación a distintos tamaños de pantalla y dispositivos (responsive) es una restricción de diseño (DS-01), no una función.

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
- **Operaciones paralelas:** la aplicación está orientada a un uso administrativo, con un número reducido de usuarios simultáneos.
- **Funciones de auditoría y control:** se debe conservar un registro de las operaciones (pedidos, ventas, despachos) que permita su consulta y seguimiento. Las reglas de negocio (por ejemplo, que un pedido no pueda despacharse sin registrarse, o que las ventas se registren con su fecha) se aplicarán para controlar los procesos sistematizados.
- **Requisitos de lenguaje:** la interfaz y los mensajes del sistema se implementarán en **idioma español**.
- **Requisitos de calidad:** los atributos de calidad que debe cumplir el sistema se especifican y priorizan en la sección 3.7 (usabilidad, seguridad, disponibilidad, confiabilidad y portabilidad).
- **Uso de protocolos:** el sistema se comunica mediante los protocolos web estándar HTTP/HTTPS; no requiere protocolos especiales adicionales.
- **Criticidad de la aplicación:** la aplicación es de apoyo administrativo; si bien la información es importante para el negocio, no se gestionan sistemas de misión crítica que comprometan vidas o seguridad.
- **Seguridad y protección:** el acceso al sistema debe restringirse al personal autorizado (por ejemplo, mediante autenticación), y la información debe protegerse contra accesos no autorizados y pérdida.
- **Consideraciones físicas/mentales:** la interfaz debe ser de uso simple, con tiempos de respuesta cortos y carga cognitiva reducida, considerando el bajo nivel técnico de los usuarios.

## 1.4. Definiciones

- **Administrativo:** persona con autoridad encargada del negocio.
- **Cliente:** persona particular o establecimiento comercial que realiza pedidos al negocio.
- **Despacho:** proceso por el cual un conjunto de pedidos es enviado para su entrega mediante un repartidor, organizado según zonas/rutas, cantidades y capacidad de los vehículos.
- **Despacho pendiente:** pedido que ha sido registrado pero que aún no ha sido despachado.
- **Despacho realizado / pedido despachado:** pedido que ya ha sido enviado para su entrega.
- **Doble registro:** práctica actual de consignar la información primero en papel y posteriormente digitarla en un computador.
- **Encargado / Administrador:** persona del negocio responsable de registrar pedidos y ventas, organizar los despachos y consultar la información del sistema.
- **Ingreso:** valor económico asociado a una venta.
- **Libreta:** registro físico de papel donde actualmente se anotan pedidos y ventas. Se referencia únicamente como descripción del proceso actual.
- **Memo:** ficha física utilizada actualmente en el negocio para organizar las entregas. Se referencia únicamente como descripción del proceso actual.
- **Operador:** empleado que usa el software sin ser administrador, encargado de la gestión y administración de ventas y pedidos.
- **Pedido:** solicitud de productos realizada por un cliente, ya sea mediante llamada telefónica, WhatsApp o de forma presencial. Contiene información sobre el cliente, las presentaciones solicitadas, las cantidades y la zona o ruta de entrega.
- **Presentación:** tipo de producto comercializado (pacas personales, pacas para hielo, pacas de tres litros, pacas de cinco litros, pimpinas de 20 litros).
- **Repartidor:** persona encargada de repartir (entregar) los pedidos a los clientes.
- **Venta:** operación comercial mediante la cual se entrega producto y se genera un ingreso; se registra por presentación.
- **Zona / Ruta:** área geográfica o recorrido que emplea el negocio para organizar la entrega de pedidos.

---

# 2. Referencias

*Pendiente de elaboración.* Esta sección se completará en una etapa posterior del proyecto. Se referenciarán como mínimo: el contexto del proyecto (Contexto.md), el acta de la entrevista realizada al propietario (26/08/2026), la guía del curso para la especificación de requisitos, la norma ISO/IEC/IEEE 29148, el planteamiento del problema de la iteración 1 y las fuentes bibliográficas utilizadas en dicho planteamiento (normas APA/IEEE).

---

# 3. Requisitos específicos

*Sección en reconstrucción por el equipo.* La versión anterior de los requisitos (RF-01 a RF-12, US-01 a US-06, DE-01 a DE-05, DS-01 a DS-06 y atributos de calidad) se conserva como respaldo en `2_Iteracion/requisitos_respaldo.md`. De acuerdo con lo acordado por el equipo, las subsecciones **3.1. Interfaces externas**, **3.4. Requisitos de desempeño** y **3.5. Requisitos de bases de datos** no se elaboran en esta iteración. La sección 3 quedó reconstruida con la versión nueva del equipo en las subsecciones **3.2** (funciones), **3.3** (capacidad de uso), **3.6** (restricciones de diseño), **3.7** (atributos de calidad) y **3.8** (información de soporte).

## 3.2. Funciones

Los seis requisitos funcionales consolidados agrupan todas las funciones del producto sin repetirse entre sí:

**RF-01 – Registro de pedidos y seguimiento de estado (personal del negocio)** *Prioridad P1 | Entrevista al propietario (26/08/2026)*
El encargado/administrador registra los pedidos recibidos (telefónica, WhatsApp o presencial) capturando cliente, presentaciones, cantidades por presentación, zona/ruta, fecha y medio de recepción. Identifica o crea el cliente en el catálogo (mostrando datos de contacto e histórico si ya existe). El pedido queda con estado inicial "Pendiente" y el encargado lo actualiza a "Despachado" cuando es enviado, registrando la fecha de despacho.

**RF-02 – Registro de pedidos por parte del cliente vía web** *Prioridad P1 | Exigido por el docente*
Un cliente externo realiza y envía su pedido directamente desde la página web, sin depender de llamada o atención presencial. Se asocia el medio "Web" y queda visible para el encargado entre los pendientes.

**RF-03 – Consulta de pedidos y apoyo a la organización de despachos** *Prioridad P1 | Entrevista al propietario (26/08/2026)*
El encargado busca y visualiza los pedidos mediante filtros por cliente, fecha, estado o zona, con acceso al detalle de cada uno. Muestra los pedidos pendientes agrupados o filtrables por zona/ruta con sus cantidades y presentaciones para apoyar la organización de los despachos (sin automatizarla), distingue los pedidos despachados de los pendientes y permite consultar información histórica por rango de fechas.

**RF-04 – Registro de ventas e ingresos** *Prioridad P1 | Entrevista al propietario (26/08/2026)*
El sistema registra las ventas por presentación con totales automáticos por presentación y total general (evitando las sumas manuales y el doble registro) y asocia a cada venta su ingreso. El encargado consulta los ingresos por periodo (día, rango de fechas) con totales agregados.

**RF-05 – Estadísticas e indicadores operativos** *Prioridad P2 | Entrevista al propietario (26/08/2026)*
El sistema presenta indicadores y gráficos: cantidad de productos vendidos por presentación, ventas por periodo, número de despachos, ingresos, comportamiento de las ventas y presentaciones más solicitadas.

**RF-06 – Consulta del estado de pedidos por parte del cliente** *Prioridad P1 | Exigido por el docente*
El cliente externo consulta en línea el estado (Pendiente o Despachado) de los pedidos que ha realizado desde la página web, incluyendo la fecha de despacho cuando corresponda.

## 3.3. Requisitos de la capacidad de uso

### 3.3.1. Efectividad

El sistema debe ser altamente confiable y seguro, diseñado para funcionar sin presentar bloqueos ni pérdidas de información. El usuario podrá iniciar y finalizar cualquier operación con la certeza de que los procesos se completarán con éxito. El programa valida y confirma cada operación, guarda cada dato de forma persistente en el momento del registro y no deja operaciones a medias: ninguna interacción se pierde ni queda bloqueada.

*Prioridad: Alta.*

### 3.3.2. Intuitividad

Un operador o cliente del negocio sin experiencia previa es capaz de completar el registro de un pedido o de una venta siguiendo las instrucciones del manual de usuario; el promedio de los operadores y clientes debe ser capaz de operar el sistema sin presentar fricción cognitiva; la curva de aprendizaje del aplicativo es baja.

*Prioridad: Media.*

### 3.3.3. Fluidez

La navegación y uso del sistema ocurren a una tasa de fotogramas alta para que el ojo humano lo perciba como algo orgánico y en tiempo real. El programa procesa las interacciones sin esperas perceptibles (sin recargas ni "congelamientos"), de modo que la navegación se perciba continua y en tiempo real.

*Prioridad: Media.*

### 3.3.4. Rendimiento

Un operador, cliente o administrativo no puede sentir retardos (alta latencia) al momento de ejecutar el software. El programa procesa las operaciones sin esperas perceptibles, de modo que el usuario nunca percibe bloqueos ni retardos.

*Prioridad: Media.*

### 3.3.5. Baja carga visual-cognitiva

La interfaz de usuario debe ser sencilla y comprensible. No saturar la mente del usuario con exceso de información. El programa presenta en cada pantalla solo la información necesaria (formularios y listados simplificados, organizados por módulos), sin saturar al usuario.

*Prioridad: Alta.*

### 3.3.6. Lenguaje

Toda la interfaz, etiquetas y mensajes se presentan en español y sin tecnicismos. El programa presenta toda la interfaz, etiquetas y mensajes en español, redactados en lenguaje cotidiano y sin tecnicismos.

*Prioridad: Alta.*

### 3.3.7. Retroalimentación

El sistema generará mensajes de confirmación o de error de manera oportuna y asertiva. Cada acción importante genera un mensaje comprensible para los usuarios independientemente de su cargo. El programa emite un mensaje claro de confirmación o de error tras cada acción importante, con lenguaje comprensible para cualquier usuario.

*Prioridad: Alta.*

### 3.3.8. Adaptabilidad

Las interfaces gráficas de usuario del software son legibles y visualmente estéticas sin importar el dispositivo desde el que se opere; el dispositivo empleado para usar el software no es un impedimento para su operación. El programa ajusta automáticamente la interfaz al tamaño del dispositivo (diseño responsive), permaneciendo legible y operable desde computador, tableta o celular sin perder funciones.

*Prioridad: Alta.*

## 3.6. Restricciones de diseño

### 3.6.1. Web adaptable

El sistema debe desarrollarse como una aplicación web con un diseño adaptativo (responsive), garantizando que sus interfaces gráficas se ajusten y visualicen correctamente en distintos tamaños de pantalla y dispositivos, tales como computadores de escritorio, tabletas y teléfonos móviles.

Se verificará la correcta distribución de los elementos de la interfaz, sin desbordamientos ni superposiciones, en al menos tres resoluciones estándar (móvil, tableta y escritorio) utilizando herramientas de emulación de navegadores. Además, las funcionalidades críticas (registrar pedidos, consultar ventas) deben poder completarse con éxito desde cualquier tamaño de pantalla.

### 3.6.2. Tecnologías web estándar

El sistema debe estar construido bajo una arquitectura cliente-servidor implementando tecnologías web estándar. El aplicativo debe ser accesible mediante un navegador web, operando sobre protocolos HTTP/HTTPS, sin necesidad de hardware especializado o instalaciones adicionales en los equipos de los usuarios.

Se comprobará la operatividad del sistema accediendo a él desde las versiones recientes de al menos tres navegadores web de uso masivo (por ejemplo: Google Chrome, Mozilla Firefox, Microsoft Edge o Safari), validando que el intercambio de información cliente-servidor se ejecute correctamente.

### 3.6.3. Idioma

Toda la interfaz de usuario, incluyendo menús, etiquetas, formularios, notificaciones y mensajes de retroalimentación, debe presentarse de manera clara y exclusiva en idioma español, evitando el uso de terminología técnica compleja que dificulte la comprensión.

Se realizará una inspección visual y funcional de la totalidad de las pantallas (tanto del módulo administrativo como del canal de clientes) para constatar que el 100% de los textos orientados al usuario estén redactados en español y sean ortográficamente correctos.

### 3.6.4. Restricción de acceso

El sistema debe implementar mecanismos de seguridad que limiten el acceso a los datos y funciones sensibles. El módulo administrativo exigirá autenticación obligatoria para el personal autorizado. Por otro lado, el canal web orientado a los clientes permitirá la realización de pedidos de forma independiente, garantizando que estos usuarios externos no puedan visualizar ni comprometer la información administrativa o financiera del negocio.

Se ejecutarán pruebas de control de acceso intentando ingresar a los enlaces y módulos administrativos sin credenciales o con roles de menor nivel, validando que el sistema deniegue la solicitud. Adicionalmente, se realizará el flujo completo de un pedido desde el perfil de cliente para confirmar que no se expone información de inventario o ventas en ningún paso del proceso.

### 3.6.5. Simplicidad

El diseño de las pantallas y formularios del sistema debe mantener una baja carga visual y cognitiva, orientándose a usuarios que poseen un bajo nivel de formación técnica y poca experiencia con sistemas informáticos. La interfaz debe ser intuitiva, con flujos de trabajo guiados que faciliten una baja curva de aprendizaje.

Se realizarán pruebas de usabilidad guiadas y no guiadas con usuarios reales o perfiles equivalentes al encargado del negocio y a clientes típicos. Se considerará cumplido si el usuario logra completar las operaciones principales (registrar una venta, consultar un despacho y hacer un pedido) sin necesidad de asistencia técnica constante, logrando una tasa de éxito superior al 90% en el uso inicial del sistema.

## 3.7. Atributos de calidad

### 3.7.1. Usabilidad

El sistema presenta una baja curva de aprendizaje, lo que permite que los distintos usuarios del sistema puedan empezar a usarlo de manera rápida y sencilla.

*Cómo se garantiza:* mediante diseño centrado en el usuario, formularios guiados paso a paso y pruebas de uso con usuarios representativos (operador, administrativo y cliente) antes de la entrega. *Prioridad: Alta.*

### 3.7.2. Seguridad y protección

El acceso a datos y funciones sensibles del sistema solo será accesible desde el módulo más alto de la aplicación (el administrativo), el cual poseerá mecanismos de autenticación para el acceso, así como confirmación y verificaciones avanzadas para la realización de cambios sensibles.

*Cómo se garantiza:* mediante autenticación obligatoria en el módulo administrativo, control de roles (administrativo y operador), confirmaciones adicionales para los cambios sensibles y respaldo de la información. *Prioridad: Alta.*

### 3.7.3. Disponibilidad

Las funcionalidades y datos correspondientes a los distintos módulos del sistema deberán estar disponibles en todo momento mientras este se encuentre operativo. La alta concurrencia no debe afectar de manera notable ni significativa esta disponibilidad.

*Cómo se garantiza:* mediante un despliegue estable del servicio y pruebas de carga que verifiquen que la concurrencia no degrada los tiempos de respuesta. *Prioridad: Alta.*

### 3.7.4. Confiabilidad

Los datos registrados se conservan de forma persistente con mecanismos de recuperación ante fallos.

*Cómo se garantiza:* mediante almacenamiento persistente en base de datos, respaldos automáticos programados y mecanismos de recuperación ante fallos. *Prioridad: Media.*

### 3.7.5. Portabilidad

El sistema funciona correctamente en los distintos sistemas operativos, dispositivos y navegadores empleados para su ejecución y operación, y sus características no se ven comprometidas por esto.

*Cómo se garantiza:* mediante tecnologías web estándar y diseño responsive, con pruebas de funcionamiento en los navegadores, sistemas operativos y dispositivos de uso habitual (computador, tableta y celular). *Prioridad: Media.*

## 3.8. Información de soporte

Esta subsección relaciona la información de apoyo y antecedentes que respaldan la presente especificación:

- **Contexto del proyecto** (`Contexto.md`): describe el negocio de comercialización y distribución de agua embotellada "Agua Frais", la gestión manual actual de pedidos, ventas y despachos, las consecuencias de dicha situación y el estado de avance del proyecto.
- **Acta de la entrevista al propietario (26/08/2026)** (Anexo C del planteamiento del problema, iteración 1): fuente primaria de las necesidades identificadas y de las evidencias que justifican los requisitos (registro manual del pedido, uso de memos, marcas de verificación, sumas manuales y doble registro).
- **Planteamiento del problema (iteración 1)**: describe el problema, la justificación y los objetivos que orientan la solución.
- **Documento guía del curso para la especificación de requisitos**: elaborado con base en la norma ISO/IEC/IEEE 29148, define la estructura del SRS empleada en este documento.
- **Material aportado por el equipo**: requisitos funcionales (RF-01 a RF-06), requisitos de la capacidad de uso (3.3), restricciones de diseño (3.6) y atributos de calidad (3.7), consolidados en la sección 3.

*Nota:* la versión nueva del equipo quedó consolidada en su totalidad en la sección 3 (3.2, 3.3, 3.6, 3.7 y 3.8). Por acuerdo del equipo (23/09/2026), las subsecciones **3.1 Interfaces externas**, **3.4 Requisitos de desempeño** y **3.5 Requisitos de bases de datos** no se elaboran, y la **tabla de trazabilidad no se realiza**.

---

# 4. Verificación

*Sección no desarrollada en la iteración actual.* Conforme a lo acordado, la verificación de los requisitos (enfoques, métodos y criterios de aceptación) no se elabora en esta etapa y quedará pendiente para una etapa posterior.
# CONTEXTO DEL PROYECTO – SISTEMA DE GESTIÓN PARA TIENDA DE AGUA EMBOTELLADA

## 1. Contexto general

El proyecto corresponde a una asignatura de Ingeniería de Sistemas / Ingeniería de Software (ISoft) y tiene como propósito analizar una problemática real de un negocio y desarrollar progresivamente una solución informática.

El negocio analizado es una tienda dedicada a la comercialización y distribución de agua embotellada ubicada en un pueblo. Atiende tanto a personas particulares como a establecimientos comerciales. Cuenta con clientes habituales que realizan pedidos de manera recurrente.

Actualmente maneja cinco tipos principales de productos:

- Pacas personales.
- Pacas para hielo.
- Pacas de tres litros.
- Pacas de cinco litros.
- Pimpinas de 20 litros.

Los pedidos se reciben principalmente mediante llamadas telefónicas y WhatsApp. También existe atención presencial.

El proceso de distribución implica entregar los productos mediante repartidores y organizar los pedidos de acuerdo con las zonas o rutas de entrega, las cantidades solicitadas y la capacidad disponible para cada viaje.

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

La propuesta consiste en desarrollar un **sistema web para la gestión y digitalización de la tienda de agua embotellada, orientado a la administración del negocio**.

El sistema busca centralizar el registro y seguimiento de los pedidos, reemplazando el proceso manual que actualmente requiere registrar inicialmente las solicitudes en una libreta y posteriormente digitar la información en un computador.

Desde el módulo administrativo, se plantea permitir el registro y consulta de los pedidos, así como la visualización de información como su estado y cantidad, con el propósito de proporcionar al encargado una visión centralizada de los pedidos pendientes y facilitar la organización de los despachos de acuerdo con las rutas, cantidades y capacidad de los vehículos.

Adicionalmente, se plantea digitalizar el registro de las ventas e ingresos, evitando la duplicación de trabajo que actualmente se produce al registrar manualmente las ventas y posteriormente transcribirlas al computador.

Finalmente, el sistema incorporará estadísticas e indicadores que permitan consultar de manera más inmediata información como la cantidad de productos vendidos, los despachos realizados, los ingresos y el comportamiento de las ventas, facilitando el análisis y la toma de decisiones dentro del negocio.

---

# 6. Alcance preliminar de la solución

La propuesta se concentra inicialmente en cuatro áreas principales:

### A. Gestión de pedidos

- Registrar pedidos.
- Consultar pedidos.
- Visualizar información relevante de cada pedido.
- Consultar pedidos pendientes.
- Dar seguimiento al estado de los pedidos.

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

Para evitar ampliar innecesariamente el proyecto, inicialmente no se plantea:

- Automatizar la creación de rutas óptimas.
- Decidir automáticamente qué pedidos deben agruparse.
- Implementar algoritmos de optimización logística.
- Automatizar completamente las decisiones del encargado.
- Resolver problemas de inventario que no hayan sido identificados durante el levantamiento de requisitos.

La solución debe principalmente **centralizar información, facilitar su consulta y apoyar la gestión administrativa**, dejando las decisiones operativas de organización de rutas y despachos al personal encargado.

---

# 8. Relación problema – solución

La relación que se busca demostrar durante el proyecto es:

| Problema identificado | Evidencia | Respuesta propuesta |
|---|---|---|
| Registro manual de pedidos | Los pedidos se registran en una libreta | Gestión digital de pedidos |
| Seguimiento mediante libreta, memos y checks | Se utilizan registros físicos para identificar pedidos despachados y pendientes | Estados y seguimiento digital |
| Organización manual de pedidos para despacho | Se revisan zonas, rutas y cantidades | Visualización centralizada de pedidos pendientes |
| Registro manual de ventas | Las cantidades se registran en columnas de la libreta | Registro digital de ventas |
| Doble registro | La información se registra en libreta y posteriormente en computador | Captura y almacenamiento digital desde el origen |
| Dificultad para consultar información inmediatamente | El propietario manifestó la necesidad de consultar ventas y despachos de manera inmediata | Consultas y panel administrativo |
| Necesidad de analizar el comportamiento del negocio | Se requiere conocer cantidades vendidas y despachos | Estadísticas e indicadores |

---

# 9. Estado actual del proyecto

El proyecto se encuentra en una primera etapa de análisis y levantamiento de información.

Ya se realizó una entrevista con el propietario del negocio para:

1. Comprender el funcionamiento actual.
2. Identificar los procesos principales.
3. Identificar dificultades reales.
4. Validar la existencia de la problemática.
5. Obtener información para orientar la solución.

La información obtenida servirá como base para las siguientes etapas del proyecto, incluyendo el levantamiento detallado de requisitos, identificación de actores, definición de reglas de negocio, modelado del negocio, diseño del sistema e implementación.

---

# 10. Objetivo general preliminar

Desarrollar un sistema web para digitalizar y centralizar la gestión de pedidos, ventas, ingresos y despachos de una tienda de agua embotellada, facilitando el seguimiento de las operaciones y proporcionando información oportuna para apoyar la administración y toma de decisiones del negocio.

---

# 11. Posibles objetivos específicos preliminares

- Analizar y modelar los procesos actuales relacionados con la gestión de pedidos, ventas, ingresos y despachos del negocio.
- Identificar y especificar los requisitos funcionales y no funcionales del sistema a partir de las necesidades identificadas.
- Diseñar una solución web que permita centralizar el registro, consulta y seguimiento de los pedidos y despachos.
- Implementar mecanismos para digitalizar y centralizar el registro de las ventas e ingresos, reduciendo la duplicación del trabajo administrativo.
- Desarrollar estadísticas e indicadores que permitan consultar y analizar información relevante sobre las operaciones del negocio.
- Verificar mediante pruebas que las funcionalidades desarrolladas respondan a las necesidades identificadas durante el análisis.

---

# 12. Criterio fundamental para continuar el proyecto

Una condición importante del proyecto es mantener una **trazabilidad entre las necesidades reales del negocio y las funcionalidades desarrolladas**.

No se deben agregar funcionalidades únicamente porque sean técnicamente interesantes. Cada funcionalidad importante debería poder justificarse mediante:

**Problema/necesidad → evidencia → requisito → funcionalidad → resultado esperado.**

Por ejemplo:

**Registro manual de pedidos**  
→ entrevista con el propietario  
→ necesidad de digitalizar el registro  
→ requisito de registrar pedidos en el sistema  
→ módulo de gestión de pedidos.

De esta manera, la solución informática se mantiene relacionada directamente con la problemática real identificada.

---

### Current

Estado de avance de la **iteración 2 (Especificación de Requisitos – SRS)**:

**Lo que se está elaborando ahora:**
- Sección 3. Requisitos específicos, reconstruida con la versión nueva del equipo:
  - 3.2 Funciones (requisitos funcionales RF-01 a RF-06) **consolidada**.
  - 3.3 Requisitos de la capacidad de uso **consolidada** (3.3.1 a 3.3.8, todos con el criterio "qué tiene el programa", prioritad Alta/Media, incluido el 3.3.4 Rendimiento).
  - 3.6 Restricciones de diseño **consolidada** (DS-01 a DS-05 con su forma de verificación).
  - 3.7 Atributos de calidad **consolidada** (*cómo se garantiza* + *prioridad Alta/Media*).
  - 3.8 Información de soporte **elaborada**.
- La sección 1.5 (Sugerencias de requisitos identificados) se eliminó del SRS: los requisitos se definen directamente en la sección 3 (RF-01 a RF-06 consolidados el 21/09/2026).

**Lo que NO se hará (por acuerdo):**
- Sección 4. Verificación.
- Subsección 3.1. Interfaces externas.
- Subsección 3.4. Requisitos de desempeño (DE-01 a DE-05) *(acuerdo 23/09/2026: no se elaboran, por las mismas razones que 3.1 y 3.5)*.
- Subsección 3.5. Requisitos de bases de datos.
- La tabla de trazabilidad (Sugerencia 11) no se elabora *(acuerdo 23/09/2026)*.

**Lo que se hará después (pendiente):**
- Sección 2. Referencias.

**Actualización (17/09/2026):** la sección 3 del SRS fue retirada del documento de trabajo para ser reconstruida; los requisitos actuales se conservan en `2_Iteracion/requisitos_respaldo.md`. La versión nueva entregada por el equipo se registra a continuación.

**Actualización (21/09/2026):** en el SRS se eliminó la sección **1.5 (Sugerencias de requisitos)** y se reordenaron/ampliaron las **Definiciones (1.4)** en orden alfabético (se agregaron los roles Administrativo, Operador, Repartidor y la referencia "De la Espriella"). Los requisitos funcionales quedaron consolidados en RF-01 a RF-06 (sección 3.2 del SRS).

**Actualización (23/09/2026):** se sincronizó este documento con el SRS: las frases aditivas "qué tiene el programa" de 3.3.x (3.3.1, 3.3.3, 3.3.5–3.3.8) y el criterio finalizado del **3.3.4 (Rendimiento)**; los **atributos de calidad** al estilo 3.7 (cómo se garantiza + prioridad). Por acuerdo del equipo: se **eliminaron los requisitos de desempeño (3.4, DE-01 a DE-05)** y se **descartó la tabla de trazabilidad (Sugerencia 11)**.

**Actualización (23/09/2026, consolidación):** las prioridades de **3.3** (capacidad de uso) y **3.7** (atributos de calidad) pasaron a **Alta/Media**; la sección **3.6 (restricciones de diseño)** quedó consolidada en el SRS con la versión ampliada del equipo (DS-01 a DS-05 con su forma de verificación) y se elaboró la **3.8 (información de soporte)**. La sección 3 del SRS quedó completa.

---

# Requisitos – Versión nueva del equipo (para la sección 3 del SRS)

## Requisitos funcionales (RF) *(Alejandro Rincón | Newin José Torres | consolidados 21/09/2026)*

**RF-01 – Registro de pedidos y seguimiento de estado (personal del negocio)** *(P1 | Entrevista al propietario 26/08/2026)*(✓)
El encargado/administrador registra los pedidos recibidos (telefónica, WhatsApp o presencial) capturando cliente, presentaciones, cantidades por presentación, zona/ruta, fecha y medio de recepción. Identifica o crea el cliente en el catálogo (mostrando datos de contacto e histórico si ya existe). El pedido queda con estado inicial "Pendiente" y el encargado lo actualiza a "Despachado" cuando es enviado, registrando la fecha de despacho.

**RF-02 – Registro de pedidos por parte del cliente vía web** *(P1 | Exigido por el docente)*(✓)
Un cliente externo realiza y envía su pedido directamente desde la página web, sin depender de llamada o atención presencial. Se asocia el medio "Web" y queda visible para el encargado entre los pendientes.

**RF-03 – Consulta de pedidos y apoyo a la organización de despachos** *(P1 | Entrevista al propietario 26/08/2026)*(✓)
El encargado busca y visualiza los pedidos mediante filtros por cliente, fecha, estado o zona, con acceso al detalle de cada uno. Muestra los pedidos pendientes agrupados o filtrables por zona/ruta con sus cantidades y presentaciones para apoyar la organización de los despachos (sin automatizarla), distingue los pedidos despachados de los pendientes y permite consultar información histórica por rango de fechas.

**RF-04 – Registro de ventas e ingresos** *(P1 | Entrevista al propietario 26/08/2026)*(✓)
El sistema registra las ventas por presentación con totales automáticos por presentación y total general (evitando las sumas manuales y el doble registro) y asocia a cada venta su ingreso. El encargado consulta los ingresos por periodo (día, rango de fechas) con totales agregados.

**RF-05 – Estadísticas e indicadores operativos** *(P2 | Entrevista al propietario 26/08/2026)*(✓) *(Newin)*
El sistema presenta indicadores y gráficos: cantidad de productos vendidos por presentación, ventas por periodo, número de despachos, ingresos, comportamiento de las ventas y presentaciones más solicitadas.

**RF-06 – Consulta del estado de pedidos por parte del cliente** *(P1 | Exigido por el docente)*(✓) *(Newin)*
El cliente externo consulta en línea el estado (Pendiente o Despachado) de los pedidos que ha realizado desde la página web, incluyendo la fecha de despacho cuando corresponda.

## Requisitos de capacidad de uso *(Jairo Jiménez | SRS sección 3.3)*

**3.3.1 – Efectividad**
El sistema debe ser altamente confiable y seguro, diseñado para funcionar sin presentar bloqueos ni pérdidas de información. El usuario podrá iniciar y finalizar cualquier operación con la certeza de que los procesos se completarán con éxito. El programa valida y confirma cada operación, guarda cada dato de forma persistente en el momento del registro y no deja operaciones a medias: ninguna interacción se pierde ni queda bloqueada.
*Prioridad: Alta.*

**3.3.2 – Intuitividad**
Un operador o cliente del negocio sin experiencia previa es capaz de completar el registro de un pedido o de una venta siguiendo las instrucciones del manual de usuario; el promedio de los operadores y clientes debe ser capaz de operar el sistema sin presentar fricción cognitiva; la curva de aprendizaje del aplicativo es baja.
*Prioridad: Media.*

**3.3.3 – Fluidez**
La navegación y uso del sistema ocurren a una tasa de fotogramas alta para que el ojo humano lo perciba como algo orgánico y en tiempo real. El programa procesa las interacciones sin esperas perceptibles (sin recargas ni "congelamientos"), de modo que la navegación se perciba continua y en tiempo real.
*Prioridad: Media.*

**3.3.4 – Rendimiento**
Un operador, cliente o administrativo no puede sentir retardos (alta latencia) al momento de ejecutar el software. El programa procesa las operaciones sin esperas perceptibles, de modo que el usuario nunca percibe bloqueos ni retardos.
*Prioridad: Media.*

**3.3.5 – Baja carga visual-cognitiva**
La interfaz de usuario debe ser sencilla y comprensible. No saturar la mente del usuario con exceso de información. El programa presenta en cada pantalla solo la información necesaria (formularios y listados simplificados, organizados por módulos), sin saturar al usuario.
*Prioridad: Alta.*

**3.3.6 – Lenguaje**
Toda la interfaz, etiquetas y mensajes se presentan en español y sin tecnicismos. El programa presenta toda la interfaz, etiquetas y mensajes en español, redactados en lenguaje cotidiano y sin tecnicismos.
*Prioridad: Alta.*

**3.3.7 – Retroalimentación**
El sistema generará mensajes de confirmación o de error de manera oportuna y asertiva. Cada acción importante genera un mensaje comprensible para los usuarios independientemente de su cargo. El programa emite un mensaje claro de confirmación o de error tras cada acción importante, con lenguaje comprensible para cualquier usuario.
*Prioridad: Alta.*

**3.3.8 – Adaptabilidad**
Las interfaces gráficas de usuario del software son legibles y visualmente estéticas sin importar el dispositivo desde el que se opere; el dispositivo empleado para usar el software no es un impedimento para su operación. El programa ajusta automáticamente la interfaz al tamaño del dispositivo (diseño responsive), permaneciendo legible y operable desde computador, tableta o celular sin perder funciones.
*Prioridad: Alta.*

## Restricciones de diseño (DS) *(Newin Torres | SRS sección 3.6)*

**DS-01 – Web adaptable (3.6.1)**(✓)
El sistema debe desarrollarse como una aplicación web con un diseño adaptativo (responsive), garantizando que sus interfaces gráficas se ajusten y visualicen correctamente en distintos tamaños de pantalla y dispositivos, tales como computadores de escritorio, tabletas y teléfonos móviles.

Se verificará la correcta distribución de los elementos de la interfaz, sin desbordamientos ni superposiciones, en al menos tres resoluciones estándar (móvil, tableta y escritorio) utilizando herramientas de emulación de navegadores. Además, las funcionalidades críticas (registrar pedidos, consultar ventas) deben poder completarse con éxito desde cualquier tamaño de pantalla.

**DS-02 – Tecnologías web estándar (3.6.2)**(✓)
El sistema debe estar construido bajo una arquitectura cliente-servidor implementando tecnologías web estándar. El aplicativo debe ser accesible mediante un navegador web, operando sobre protocolos HTTP/HTTPS, sin necesidad de hardware especializado o instalaciones adicionales en los equipos de los usuarios.

Se comprobará la operatividad del sistema accediendo a él desde las versiones recientes de al menos tres navegadores web de uso masivo (por ejemplo: Google Chrome, Mozilla Firefox, Microsoft Edge o Safari), validando que el intercambio de información cliente-servidor se ejecute correctamente.

**DS-03 – Idioma (3.6.3)**(✓)
Toda la interfaz de usuario, incluyendo menús, etiquetas, formularios, notificaciones y mensajes de retroalimentación, debe presentarse de manera clara y exclusiva en idioma español, evitando el uso de terminología técnica compleja que dificulte la comprensión.

Se realizará una inspección visual y funcional de la totalidad de las pantallas (tanto del módulo administrativo como del canal de clientes) para constatar que el 100% de los textos orientados al usuario estén redactados en español y sean ortográficamente correctos.

**DS-04 – Restricción de acceso (3.6.4)**(✓)
El sistema debe implementar mecanismos de seguridad que limiten el acceso a los datos y funciones sensibles. El módulo administrativo exigirá autenticación obligatoria para el personal autorizado. Por otro lado, el canal web orientado a los clientes permitirá la realización de pedidos de forma independiente, garantizando que estos usuarios externos no puedan visualizar ni comprometer la información administrativa o financiera del negocio.

Se ejecutarán pruebas de control de acceso intentando ingresar a los enlaces y módulos administrativos sin credenciales o con roles de menor nivel, validando que el sistema deniegue la solicitud. Adicionalmente, se realizará el flujo completo de un pedido desde el perfil de cliente para confirmar que no se expone información de inventario o ventas en ningún paso del proceso.

**DS-05 – Simplicidad (3.6.5)**(✓)
El diseño de las pantallas y formularios del sistema debe mantener una baja carga visual y cognitiva, orientándose a usuarios que poseen un bajo nivel de formación técnica y poca experiencia con sistemas informáticos. La interfaz debe ser intuitiva, con flujos de trabajo guiados que faciliten una baja curva de aprendizaje.

Se realizarán pruebas de usabilidad guiadas y no guiadas con usuarios reales o perfiles equivalentes al encargado del negocio y a clientes típicos. Se considerará cumplido si el usuario logra completar las operaciones principales (registrar una venta, consultar un despacho y hacer un pedido) sin necesidad de asistencia técnica constante, logrando una tasa de éxito superior al 90% en el uso inicial del sistema.

## Atributos de calidad *(Jairo Jiménez | al estilo 3.7 del SRS)*

**USU – Usabilidad** *(Prioridad Alta)*
El sistema presenta una baja curva de aprendizaje, lo que permite que los distintos usuarios puedan empezar a usarlo de manera rápida y sencilla.
*Cómo se garantiza:* mediante diseño centrado en el usuario, formularios guiados paso a paso y pruebas de uso con usuarios representativos (operador, administrativo y cliente) antes de la entrega.

**SEG – Seguridad y protección** *(Prioridad Alta)*
El acceso a datos y funciones sensibles del sistema solo será accesible desde el módulo más alto de la aplicación (el administrativo), el cual poseerá mecanismos de autenticación para el acceso, así como confirmación y verificaciones avanzadas para la realización de cambios sensibles.
*Cómo se garantiza:* mediante autenticación obligatoria en el módulo administrativo, control de roles (administrativo y operador), confirmaciones adicionales para los cambios sensibles y respaldo de la información.

**DIS – Disponibilidad** *(Prioridad Alta)*
Las funcionalidades y datos de los distintos módulos deberán estar disponibles en todo momento mientras el sistema se encuentre operativo. La alta concurrencia no debe afectar de manera notable ni significativa esta disponibilidad.
*Cómo se garantiza:* mediante un despliegue estable del servicio y pruebas de carga que verifiquen que la concurrencia no degrada los tiempos de respuesta.

**CON – Confiabilidad** *(Prioridad Media)*
Los datos registrados se conservan de forma persistente con mecanismos de recuperación ante fallos.
*Cómo se garantiza:* mediante almacenamiento persistente en base de datos, respaldos automáticos programados y mecanismos de recuperación ante fallos.

**POR – Portabilidad** *(Prioridad Media)*
El sistema funciona correctamente en los distintos sistemas operativos, dispositivos y navegadores empleados para su ejecución y operación, y sus características no se ven comprometidas por esto.
*Cómo se garantiza:* mediante tecnologías web estándar y diseño responsive, con pruebas de funcionamiento en los navegadores, sistemas operativos y dispositivos de uso habitual (computador, tableta y celular).
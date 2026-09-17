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
- Sección 3. Requisitos específicos, con las subsecciones:
  - 3.2 Funciones (requisitos funcionales RF-01 a RF-12).
  - 3.3 Requisitos de la capacidad de uso.
  - 3.4 Requisitos de desempeño.
  - 3.6 Restricciones de diseño.
  - 3.7 Atributos de calidad.
  - 3.8 Información de soporte.
- Las sugerencias 1 a 10 de la sección 1.5 del SRS se describieron en la sección 3, cada una en la subsección que corresponde.

**Lo que NO se hará (por acuerdo):**
- Sección 4. Verificación.
- Subsección 3.1. Interfaces externas.
- La Sugerencia 11 (tabla de trazabilidad) no se incluye dentro de la sección 3.

**Lo que se hará después (pendiente):**
- Sección 2. Referencias.
- Subsección 3.5. Requisitos de bases de datos.
- La tabla de trazabilidad (Sugerencia 11).
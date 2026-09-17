# RESPALDO DE REQUISITOS – SECCIÓN 3 DEL SRS (VERSIÓN ANTERIOR)

**Proyecto:** Sistema de Gestión para Tienda de Agua Embotellada
**Iteración:** 2 – Especificación de Requisitos
**Fecha del respaldo:** 17/09/2026

> Este archivo conserva la versión previa de la sección 3 "Requisitos específicos"
> del SRS al momento de su refactorización. Los compañeros del equipo rehacen la
> sección 3; esta copia sirve únicamente como referencia/respaldo.

---

## Funciones (RF) – RF-01 a RF-12

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

---

## Requisitos de la capacidad de uso (US) – US-01 a US-06

Corresponden a la Sugerencia 10.

- **US-01 (Efectividad):** un usuario del negocio sin experiencia previa debe completar el registro de un pedido o de una venta sin error, siguiendo únicamente la guía de la interfaz. Criterio: el 90 % de las tareas básicas se completan con éxito sin asistencia.
- **US-02 (Eficiencia):** el registro de un pedido debe requerir a lo sumo cinco pasos y finalizarse en un tiempo menor al que hoy demanda el registro manual. Criterio: el tiempo medio de registro de un pedido no supera los dos minutos.
- **US-03 (Satisfacción):** la interfaz debe ser sencilla y comprensible. Criterio: valoración de satisfacción de uso igual o superior a 4/5 en evaluaciones con usuarios representativos.
- **US-04 (Lenguaje):** toda la interfaz, etiquetas y mensajes se presentan en español y sin tecnicismos informáticos. Criterio: ausencia de términos técnicos en pantalla evaluados por revisión.
- **US-05 (Feedbacks claros):** el sistema informa de forma clara confirmaciones y errores. Criterio: cada acción importante genera un mensaje de confirmación o error comprensible.
- **US-06 (Adaptabilidad responsive):** las tareas esenciales (registro y consulta de pedidos) son utilizables y legibles en computador, tableta y celular. Criterio: la interfaz se ajusta sin pérdida de funciones según las recomendaciones de diseño web adaptativo.

---

## Requisitos de desempeño (DE) – DE-01 a DE-05

Corresponden a la Sugerencia 10.

- **DE-01 (Tiempo de respuesta):** las consultas y el registro de información responden en un tiempo inferior a tres segundos en condiciones normales, y a lo sumo cinco segundos en condiciones de carga pico.
- **DE-02 (Usuarios simultáneos):** el sistema admite al menos cinco usuarios simultáneos (personal del negocio y clientes web) sin degradación perceptible de rendimiento.
- **DE-03 (Capacidad de información):** el sistema almacena y opera correctamente con al menos los registros de un año de operación (pedidos, ventas, despachos y clientes) sin pérdida de precisión.
- **DE-04 (Disponibilidad operativa):** el sistema permanece disponible durante la jornada laboral del negocio (mínimo ocho horas diarias), permitiendo registrar y consultar información de manera inmediata.
- **DE-05 (Carga diaria):** el sistema soporta el volumen de operación típico del negocio (decenas de pedidos y ventas diarias) sin degradación perceptible.

---

## Restricciones de diseño (DS) – DS-01 a DS-06

- **DS-01 (Web responsive):** el sistema se desarrolla como aplicación web responsive, adaptándose correctamente a distintos tamaños de pantalla y dispositivos (requisito exigido por el docente).
- **DS-02 (Tecnologías web estándar):** se utiliza arquitectura cliente-servidor sobre tecnologías web estándar y accesible mediante navegador web.
- **DS-03 (Idioma):** la interfaz y los mensajes del sistema se implementan en español.
- **DS-04 (Acceso restringido):** el módulo administrativo exige autenticación del personal autorizado; el canal de clientes permite el registro de pedidos sin comprometer los datos administrativos.
- **DS-05 (Alcance limitado):** el sistema no incorpora módulo contable formal, no valida inventario, no automatiza rutas ni decide la agrupación de pedidos.
- **DS-06 (Simplicidad):** el diseño de pantallas y formularios se orienta a usuarios con bajo nivel técnico, minimizando la carga cognitiva.

---

## Atributos de calidad (priorizados)

1. **Usabilidad (USU):** prioridad 1. El sistema debe ser de aprendizaje rápido y uso sencillo para usuarios con bajo nivel técnico y para clientes (criterios en 3.3).
2. **Seguridad y protección (SEG):** prioridad 2. El acceso al módulo administrativo se restringe mediante autenticación y la información se protege contra accesos no autorizados y pérdida.
3. **Disponibilidad (DIS):** prioridad 3. El sistema debe estar disponible durante la jornada operativa del negocio (DE-04).
4. **Confiabilidad (CON):** prioridad 4. Los datos registrados (pedidos, ventas, despachos) se conservan de forma persistente y se prevén mecanismos de recuperación ante fallos.
5. **Portabilidad (POR):** prioridad 5. El sistema funciona correctamente en los navegadores y dispositivos habituales (computador, tableta y celular) aprovechando el diseño responsive.

---

## Información de soporte (3.8 del SRS original)

El documento del SRS se sustenta en el contexto del proyecto (Contexto.md), que describe la problemática real del negocio, las consecuencias identificadas y el estado actual del proyecto; en el planteamiento del problema y el acta de la entrevista realizada al propietario el 26/08/2026 (iteración 1); y en el requisito exigido por el docente relativo al diseño responsive y al registro de pedidos por parte de los clientes.
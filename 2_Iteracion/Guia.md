Departamento de Ingeniería de Software
Programa de Ingeniería de Sistemas
Universidad de Cartagena

DOCUMENTO GUÍA PARA LA ESPECIFICACIÓN DE REQUISITOS

El  documento  de  especificación  de  requisitos  se  elabora  atendiendo  la  norma
ISO/IEC/IEEE 29148. Su contenido se debe estructurar así:

1.  Introducción
1.1. Propósito
1.2. Ámbito
1.3. Visión general del producto

1.3.1.  Perspectiva del producto
1.3.2.  Funciones del producto
1.3.3.  Características de los usuarios
1.3.4.  Limitaciones

1.4. Definiciones

2.  Referencias
3.  Requisitos específicos
3.1. Interfaces externas
3.2. Funciones
3.3. Requisitos de la capacidad de uso
3.4. Requisitos de desempeño
3.5. Requisitos de bases de datos
3.6. Restricciones de diseño
3.7. Atributos de calidad
3.8. Información de soporte

4.  Verificación

(Se define en paralelo a la sección 3)

5.  Apéndices

5.1. Suposiciones y dependencias
5.2. Acrónimos y abreviaciones

A continuación se describe en forma  general cada ítem. Su descripción detallada se
encuentra en la respectiva norma.

Propósito: Presenta el objetivo del software que se va a construir.

Ámbito:  Describe  el  alcance  del  producto  indicando  el  nombre  que  se  le  asigna,  lo
que hará, los beneficios que representa y las metas que logra.

Perspectiva  del  producto:  Define  las  relaciones  del  software  con  otros  productos.
Describe  cómo  funciona  el  software  bajo  las  siguientes  restricciones:  interfaces  del

Departamento de Ingeniería de Software
Programa de Ingeniería de Sistemas
Universidad de Cartagena

sistema,  interfaces  de  usuario,  interfaces  de  hardware,  interfaces  de  software,
interfaces  de  comunicación,  memoria,  operación
(condiciones  ambientales,
disponibilidad  y  continuidad,  modos  de  operación,  cumplimiento  regulatorio
operativo)  y  requisitos  de  adaptación  al  sitio  (infraestructura  existente,  condiciones
culturales o propias del contexto del problema)

Funciones del producto: Presenta un resumen de las funciones más importantes que
debe cumplir el software.

Características  de  los  usuarios:  Describe  las  características  generales  del  grupo  de
usuarios que pueden influir en  la capacidad de uso del sistema, tales como nivel de
formación, experiencia, discapacidades, habilidades y/o experiencia técnica.

Limitaciones:  Relaciona  las  restricciones  que  debe  cumplir  el  software  en  términos
de: Políticas regulatorias, limitaciones de hardware, interfaces con otras aplicaciones,
operaciones  paralelas,  funciones  de  auditoría,  funciones  de  control  (Políticas
operativas,  reglas  de  negocio  que  exigen  control  en  los  procesos  que  sistematiza  el
software),  requisitos  de  lenguaje  de  orden  superior,  requisitos  de  calidad,  uso  de
protocolos,  criticidad  de  la  aplicación,  consideraciones  de  seguridad  y  protección,
consideraciones físicas / mentales.

Definiciones: Provee las definiciones de palabras y frases que tienen un significado
especial en el contexto de la funcionalidad del software.

Referencias: Incluye la lista completa de documentos utilizados para elaboración de
la  especificación  de  requisitos.  Debe  indicar  el  título  del  documento,  los  autores,  la
editorial y año de publicación.

Requisitos específicos: Se especifican todos los requisitos del software con el nivel
de detalle suficiente para que los diseñadores del producto puedan satisfacerlos y los
expertos  en  pruebas  puedan  comprobar  su  cumplimiento.  Como  mínimo  se  deben
describir las entradas (estímulos), las salidas (respuestas) y las funciones que realiza
el producto.

Interfaces externas: Define todas las entradas y salidas del software. Complementa la
descripción  hecha  en  la  perspectiva  del  producto.  Cada  interface  debe  incluir  el
siguiente contenido: nombre, descripción del propósito, fuente de la entrada y destino
de  la  salida,  rango  válido,  precisión  y/  o  tolerancia,  unidades  de  medida,  tiempo,
relaciones  con  otras  entradas/salidas,  formatos/organización  de  pantalla/ventanas,
formatos de datos, formatos de comandos, mensajes de finalización.

Documento elaborado por:
Ing. Martín Monroy Ríos, MSc, PhD
Página 2 de 5

Departamento de Ingeniería de Software
Programa de Ingeniería de Sistemas
Universidad de Cartagena

Funciones:  Define  las  acciones  fundamentales  que  debe  realizar  el  software  al
aceptar y procesar entradas para generar salidas. Debe incluir: 1) Criterios de validez
de  las  entradas,  2)  Secuencia  exacta  de  operaciones,  3)  Respuestas  a  situaciones
anormales  como:  a)  desbordamiento,  b)  facilidades  de  comunicación,  c)  Manejo  y
recuperación  de  errores;  4)  Efecto  de  los  parámetros,  5)  Relación  de  salidas  a
entradas, incluyendo: a) Secuencias de entrada/salida, b) Fórmulas para la conversión
de entrada a salida. Se recomienda dividir los requisitos funcionales en sub-funciones
o subprocesos. Esto no implica que el diseño del software también se organice de esa
manera. Las funciones deben estar priorizadas.

Requisitos de la capacidad de uso: Define los requisitos calidad de uso. Se incluyen
los  criterios  de  efectividad,  eficiencia  y  satisfacción  medibles  en  contextos
específicos de uso.

Requisitos de rendimiento: Especifica los requisitos estáticos y dinámicos en forma
cuantitativa. Los requisitos numéricos estáticos se pueden identificar en una sección
separada titulada Capacidad, y pueden incluir lo siguiente: a) El número de terminales
a ser soportados; b) El número de usuarios simultáneos que se admitirán; c) Cantidad
y tipo de información a manejar. Los requisitos numéricos dinámicos (interacción con
el  usuario)  pueden  incluir,  por  ejemplo,  el  número  de  transacciones  y  tareas  y  la
cantidad de datos a procesar dentro de ciertos períodos de tiempo para condiciones de
carga de trabajo normales y pico.

Requisitos de bases de datos: Indica los requisitos que debe cumplir la información
que se registra en la base de datos, incluyendo: el tipo de información, la frecuencia
de uso, las capacidades de acceso, las entidades y sus relaciones, las restricciones de
integridad y los requisitos de retención (permanencia) de datos.

Restricciones de diseño: Especifica las restricciones de diseño que se imponen para
el  cumplimiento  de  estándares  externos,  requisitos  regulatorios,  o  limitaciones  del
proyecto.

Atributos de calidad: Define los atributos de calidad que debe cumplir el producto.
Deben estar priorizados. Algunos ejemplos son:

a) Confiabilidad: especifique los factores necesarios para establecer la confiabilidad
requerida del sistema de software al momento de la entrega.
b)  Disponibilidad:  especifique  los  factores  necesarios  para  garantizar  un  nivel  de
disponibilidad  definido  para  todo  el  sistema,  como  el  punto  de  control,  la
recuperación y el reinicio.

Documento elaborado por:
Ing. Martín Monroy Ríos, MSc, PhD
Página 3 de 5

Departamento de Ingeniería de Software
Programa de Ingeniería de Sistemas
Universidad de Cartagena

c)  Seguridad:  especifique  los  requisitos  para  proteger  el  software  del  acceso
accidental  o  malicioso,  la  modificación,  destrucción  o  divulgación  de  información.
Los requisitos específicos en esta área podrían incluir la necesidad de:

1) Utilizar ciertas técnicas criptográficas;
2) Mantener registros específicos o conjuntos de datos históricos;
3) Asignar ciertas funciones a diferentes módulos;
4) Restringir las comunicaciones entre algunas áreas del programa;
5) Verificar la integridad de los datos para variables críticas;
6) Asegurar la privacidad de los datos.

d)  Portabilidad:  especifique  los  atributos  del  software  que  se  relacionan  con  la
facilidad  de  portar  el  software  a  otras  máquinas  host  y  /  o  sistemas  operativos,  que
incluyen:

1) Porcentaje de elementos con código dependiente del host;
2) Porcentaje de código que depende del host;
3) Uso de un lenguaje portátil probado;
4) Uso de un compilador particular o subconjunto de idiomas;
5) Uso de un sistema operativo particular.

Información de soporte: Contiene información de apoyo que incluye: a) Muestra de
formatos  de  entrada  /  salida,  descripciones  de  estudios  de  análisis  de  costos  o
resultados  de  encuestas  de  usuarios;  b)  Información  de  respaldo  o  de  antecedentes
que pueda ayudar a los lectores de la especificación de requisitos; c) Una descripción
de los problemas a resolver por el software; d) Instrucciones especiales de empaque
para el código y los medios para cumplir con la seguridad, exportación, carga inicial
u otro requisitos.

Verificación: define los enfoques y métodos de verificación planeados para calificar
el software. Se recomienda que los elementos de información para la verificación se
proporcionen de  manera paralela con los elementos de información de la sección 3,
resaltando  el  aspecto  que  se  evalúa,  cómo  se  evalúa  (método  y  métricas)  y  los
criterios de aceptación.

Apéndices: Contiene información complementaria que facilita el uso y comprensión
del documento de especificación de requisitos. Puede incluir entre otros aspectos los
siguientes:

Suposiciones y dependencias: Se enumeran cada uno de los factores que afectan los
requisitos establecidos en el SRS. Estos factores no son restricciones de diseño, pero
cualquier cambio en estos factores puede afectar los requisitos.

Documento elaborado por:
Ing. Martín Monroy Ríos, MSc, PhD
Página 4 de 5

Departamento de Ingeniería de Software
Programa de Ingeniería de Sistemas
Universidad de Cartagena

Acrónimos  y  abreviaciones:  Lista  los  acrónimos  y  abreviaciones  usados  en  el
documento con su respectiva descripción.

Documento elaborado por:
Ing. Martín Monroy Ríos, MSc, PhD
Página 5 de 5


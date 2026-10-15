# Normas para generar diagramas de actividad PlantUML conforme a UML 2.x

Guía de reglas diseñada para usarse como prompt/instrucciones a un LLM. Objetivo: que el código PlantUML generado refleje la semántica de UML 2.5 (specificación OMG vigente), no la práctica antigua de los diagramas de flujo.

## 1. Semántica de nodos de decisión (if / elseif / else)

**Regla central:** en UML 2.x, el rombo (`DecisionNode`) es un nodo de enrutamiento **vacío**. Las condiciones no van "dentro del rombo"; van como **guardas** sobre las aristas salientes, entre corchetes.

- En PlantUML usa la sintaxis estructurada, que genera automáticamente rombo + guardas:
  ```
  if (¿Forma de entrega?) then ([Retiro en el local])
    ...
  else ([Entrega a domicilio])
    ...
  endif
  ```
- El texto del `if (...)` es la **pregunta** (etiqueta del rombo), nunca la condición de una rama.
- Cada rama `then`/`else`/`elseif` **debe** llevar su guarda entre corchetes: `([Sí])`, `([No disponible])`, etc.
- Usa `[else]` solo como guarda por defecto cuando ninguna condición sea explícita; es preferible nombrar todas las condiciones.
- No escribas la condición dentro del cuerpo de una acción ni como texto suelto junto al rombo (herencia de Larman/diagramas de flujo; no es la notación vigente).

## 2. Ramas múltiples

- Para 3+ caminos usa `switch (¿...?)` / `case ( [Opción A] )` / `case ( [Opción B] )` en vez de anidar muchos `if`. Evita anidar más de 2 niveles: es señal de refactorizar el modelo o separar actividades.
- Alternativa válida: múltiples `if` independientes si las condiciones no son excluyentes.

## 3. Cierres y terminación

- Cada `if`, `switch`, `repeat`, `while`, `fork` **debe cerrarse** (`endif`, `endswitch`, `endwhile`, `endfork`/`end split`). Nunca dejes bloques abiertos.
- El flujo debe terminar con `stop` (o `end` solo si representa muerte del flujo sin estado final). En UML 2.x el final de actividad es un `ActivityFinalNode`: un diagrama de actividad debe tener al menos un final explícito, y todo camino alcanzable debe poder llegar a un final.
- Si una rama aborta el proceso (p. ej. "pedido rechazado"), termina esa rama con su propio `stop`; no la dejes colgando.

## 4. Merge

- Cuando varias ramas confluyen y el flujo continúa, UML exige un **nodo de fusión** (rombo de unión). En PlantUML esto se logra volviendo a un flujo común después del `endif`; no dibujes flechas que se crucen ni reúnas flujos dibujando a mano. Un rombo de decisión sin su correspondiente fusión explícita es aceptable en PlantUML solo si el `endif` ya produce el merge.

## 5. Acciones y actividades

- Una acción = **una** operación atómica con un único verbo. Si el texto tiene "y" coordinando dos operaciones distintas, divídelo en dos acciones (o usa `partition`/`group` para subactividades).
- Redacta acciones con **verbo en infinitivo o imperativo + objeto**: "Registrar el pedido", no "El pedido es registrado...".
- Usa la sintaxis multilinea `:acción;\nsegunda línea;` para textos largos en vez de acciones gigantes con demasiadas cláusulas.
- No metas decisiones dentro del texto de una acción: si hay un "si..." en el texto de la acción, conviértelo en un nodo de decisión con guardas.

## 6. Inicio

- Todo diagrama empieza con `start` (nodo inicial). Solo **un** nodo inicial por actividad.
- No dibujes flechas hacia el nodo inicial.

## 7. Carriles (swimlanes)

- Declara carriles con `|Nombre|` y coloca cada acción en el carril del **responsable real** de ejecutarla, no del que la solicita.
- Cambia de carril solo con `|NuevoCarril|` justo antes de la acción que cambia de responsable.
- Limita el número de carriles (≤ 5-6); más carriles indican que el proceso debería dividirse en varios diagramas.
- No pongas nodos de decisión "de nadie": cada rombo pertenece al carril que **evalúa** la condición.

## 8. Concurrencia (fork / join)

- Usa `fork` solo cuando las actividades ocurren **en paralelo real** (independientes). Si una actividad requiere que otra termine antes, es una secuencia con `:acción;`, no un fork.
- Todo `fork` debe tener sus ramas (`fork again`) y cerrar con **un solo `end fork`** (nodo de join): UML exige que el join sincronice todas las ramas del fork.
- Una rama de fork no debe terminar en un `stop` propio si luego se requiere el join (eso se modela como decisión, no concurrencia).

## 9. Bucles

- `repeat ... repeat while (¿condición?) is ([Sí])` / `backward ([No])`: el texto de `repeat while` es la pregunta; las guardas van en `is`/`backward`.
- `while (¿condición?) is ([Sí])` ... `endwhile` para pre-test. Evalúa la guarda **cada vuelta** en la arista de reingreso.
- Garantiza que el bucle pueda terminar (guarda que llegue a ser falsa): un bucle sin condición de salida viola UML y genera flujos infinitos.

## 10. Notas y anotaciones

- Usa `note right/left`/`floating note` para **aclaraciones semánticas** (supuestos, referencias normativas, decisiones de negocio), nunca para esconder lógica del flujo.
- Si una nota describe una condición o regla que afecta el flujo, evalúa si debe ser una guarda en una arista en su lugar.
- Prefiere notas breves; si una nota supera ~6 líneas, conviértela en documentación aparte.

## 11. Estilo y legibilidad

- Si numeras pasos del procedimiento (`A1`, `A2`...), mantenlos consistentes, pero la numeración no sustituye el orden real del flujo.
- Evita líneas larguísimas en el código; usa `\n` dentro de las acciones.
- Usa `skinparam` mínimos; la decoración excesiva resta valor de modelo.
- No pongas textos largos en flechas (`->`); las flechas llevan solo guardas o señales.

## 12. Checklist de validación (antes de dar por bueno un diagrama)

1. ✔ Un solo `start`, al menos un `stop`, y todo camino alcanza un final.
2. ✔ Cada decisión tiene todas sus guardas explícitas y **mutuamente excluyentes** (dos guardas verdaderas a la vez = flujo no determinista, error en UML).
3. ✔ Guardas entre corchetes en aristas; el rombo no contiene la condición de rama.
4. ✔ Cada acción tiene verbo + objeto y es ejecutable por el responsable del carril.
5. ✔ Todo `fork` se cierra con un `end fork`; todo `if` con `endif`; todo bucle con su cierre.
6. ✔ Los merges se producen por estructura del código, sin cruces dibujados a mano.
7. ✔ Objetos, señales o excepciones que cruzan carriles se modelan explícitamente.

## 13. Errores típicos de LLM que estas normas evitan

| Error | Corrección |
|---|---|
| Condición dentro del rombo (el texto del `if` escrito como si fuera la rama) | `if (pregunta) then ([guarda])` |
| Ramas sin guarda | Siempre `then ([...])` / `else ([...])` |
| Anidar ifs sin `endif` | Cerrar todos los bloques |
| Preguntas escritas como acción (`:¿Es válido?;`) | Convertirlas en nodo de decisión |
| Usar fork para secuencias | fork solo para paralelismo real |
| Acciones con múltiples "y" | Dividir en acciones atómicas |
| Carril = quien solicita | Carril = quien ejecuta |
| Ramas que quedan colgando sin `stop` | Cerrar todos los caminos |

## Referencia rápida de sintaxis

```plantuml
@startuml
start
|Cliente|
:Acción inicial;
|Encargado|
if (¿Pregunta de decisión?) then ([Guarda verdadera])
  :Acción rama 1;
elseif ([Segunda condición])
  :Acción rama 2;
else ([Caso por defecto])
  :Acción rama 3;
  stop
endif
repeat
  :Acción repetible;
repeat while (¿Repetir?) is ([Sí])
-> [No];
fork
  :Acción paralela 1;
fork again
  :Acción paralela 2;
end fork
|Cliente|
:Última acción;
stop
@enduml
```
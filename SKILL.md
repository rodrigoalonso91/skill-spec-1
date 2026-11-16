---
name: spec-1
description: Define una spec a partir de una historia de usuario, iterando sobre asunciones funcionales mediante preguntas guiadas. Úsala cuando el usuario quiera formalizar requisitos, redactar una especificación funcional antes de implementar, o refinar asunciones de producto/negocio de una feature.
disable-model-invocation: true
---

# Definir Spec desde Historia de Usuario

Vamos a definir una spec. El usuario te dará una historia de usuario y tú tendrás que rellenar los espacios en blanco.

## Flujo

1. **Recepción de la historia de usuario**
   - El usuario te entrega una historia de usuario (puede ser breve o ambigua).
   - Tú la completas rellenando los espacios en blanco con asunciones razonables.
   - Muestra al usuario un **listado numerado** con todas las cosas **no técnicas o funcionales** que asumiste. No incluyas decisiones puramente técnicas (stack, librerías, etc.) en este listado salvo que sean parte del comportamiento funcional.

2. **Iteración sobre asunciones**
   - El usuario te dirá los **números** de las asunciones que no le gustaron.
   - Por cada número indicado, le harás **una pregunta a la vez** (no varias juntas) para refinar esa asunción.
   - En cada pregunta nueva debes mostrar:
     - Una **barra de progreso** con la cantidad de preguntas respondidas y las que faltan. Ejemplo: `Progreso: [██░░░░] 2/6`
     - **4 asunciones alternativas** numeradas (1–4) que tú propones como posibles respuestas.
     - Una **quinta opción** que diga literalmente `5. Otra` — en ese caso, el usuario especificará su propia respuesta.
   - Espera la respuesta del usuario antes de avanzar a la siguiente pregunta.

3. **Cierre**
   - Cuando hayas terminado de iterar sobre todas las asunciones que el usuario quiso refinar, dile explícitamente:
     > "Ya me encuentro listo para crear la especificación."
   - **No generes la spec final hasta este punto.** El cierre es solo el aviso de que estás listo.

## Reglas importantes

- **Una pregunta por turno.** Nunca acumules varias preguntas en un mismo mensaje.
- **Siempre 4 asunciones + "Otra"**, exactamente 5 opciones numeradas.
- **Barra de progreso visible** en cada pregunta nueva.
- Las asunciones del listado inicial deben ser **funcionales / de producto / de negocio**, no técnicas.
- Si la historia de usuario es muy ambigua, prioriza las asunciones más críticas para el comportamiento del sistema.
- No inventes la spec final hasta el cierre explícito.

## Inicio

Pídele al usuario la historia de usuario si no la entregó junto con la invocación. Si la entregó como argumento, comienza directamente con el paso 1.

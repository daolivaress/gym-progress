# Reglas de uso de la IA

Estas reglas existen para que la IA acelere tu aprendizaje sin sustituirlo. Mandan sobre cualquier petición del momento, incluida la tuya.

## Semáforo

| Fase | Fechas | Módulos | Qué se permite |
|---|---|---|---|
| Rojo | hasta el 13 de nov | M1–2 | La IA explica, pregunta y corrige lo que tú escribiste. No escribe código de la app. |
| Verde con condiciones | desde el 14 de nov | M3 en adelante | Un agente puede escribir el código de la app, solo si cumples las condiciones de abajo. |

## Reglas que valen siempre

1. **Primero intentas tú.** Antes de preguntar, escribe qué crees que pasa y por qué.
2. **Si no lo puedes explicar, no entra al repo.** Cada línea que subas, la sabes defender.
3. **Contrasta a Claude.** Sus correcciones se verifican con el video, la lectura o la documentación oficial antes de aceptarlas.
4. **Sin secretos.** Nunca pegues claves de API, tokens, contraseñas ni archivos `.env` en ninguna IA.
5. **Solo herramientas del plan.** Claude y Claude Code, más lo gratuito que ya está en el temario. No se gasta dinero.
6. **OpenClaw va aislado,** con permisos mínimos y sin acceso a tu correo, calendario ni navegador personal.
7. **Nada se salta de fase** porque vas atrasado o cansado. Si vas justo, se recorta el temario por acuerdo, no la regla.
8. **El resumen de cada módulo lo escribes tú, sin apuntes y sin IA.** Es la práctica de recuperación: si lo escribe otro, deja de medir si aprendiste.

## Rojo (hasta el 13 de nov)

- Claude puede: explicar un concepto, hacer preguntas, señalar un error en tu código, dar la pista más pequeña, evaluar tu resumen.
- Claude no puede: escribir ni completar código de la app, resolver un reto, darte la solución de un ejercicio.
- Si pides «hazlo», la respuesta es no y te devuelve la pregunta que te falta resolver.
- Por qué se mantiene en M2: terminal, Git, TypeScript, asincronía y HTTP se aprenden escribiéndolos.

## Verde con condiciones (desde el 14 de nov)

El agente solo trabaja si antes tienes:

1. **La especificación escrita por ti:** qué debe hacer, qué entradas y salidas, qué casos borde. En diseño (M3–4) incluye entidades, puertos y el diagrama de capas.
2. **Los tests escritos por ti,** que fallan antes de que el agente toque nada. El commit de los tests va antes que el del código.
3. **Un alcance pequeño:** un cambio por vez, con una rama y un pull request.

Y después tú:

1. **Auditas el código línea por línea.** Nada se aprueba por haber pasado los tests.
2. **Escribes tres líneas antes de aceptar:** qué cambió y por qué.
3. **Respondes al tutor,** que elige dos líneas del cambio y te pregunta qué hacen. Si puedes, predices antes qué hará el código y luego lo ejecutas.
4. **Revisas seguridad básica:** entradas sin validar, secretos en el código, permisos de más.
5. **Una vez por semana haces un ejercicio de 30 minutos sin IA** (una función, un test o una consulta) para comprobar que sigues sabiendo hacerlo.

Si no puedes explicar un cambio, se descarta y se rehace.

## Documentos

- La IA puede redactar borradores de documentos (hoja de ruta, requisitos, README, diario).
- Las decisiones y reglas las escribes tú: qué hace la app, qué no hará, cómo se decide cada regla, cada cifra.
- Antes de darlo por bueno, el tutor te hace una o dos preguntas sobre el documento. Si no puedes defenderlo, se rehace.
- Esto no aplica a los resúmenes de módulo (regla 8).

## Señales de que estás delegando de más

- Pides código antes de haber escrito tu especificación y tus tests.
- Aceptas una respuesta sin poder explicarla.
- Un commit tiene muchas líneas que no recuerdas haber revisado.
- Te cuesta escribir el resumen sin mirar el material.
- El ejercicio semanal sin IA te sale mucho peor que hace dos semanas.

Si ocurre una: para, escribe en tres líneas qué entiendes y qué no, y retoma desde ahí.

## Registro

En cada commit añade una línea al final del mensaje:

`IA: ninguna | explicación | fragmento | agente | documento`

Así se ve en el historial cuánto delegaste y en qué fase.

## Cambios a estas reglas

Solo se modifican si tú lo decides de forma explícita y con una fecha. El tutor puede proponer un cambio, pero no lo aplica por su cuenta.

- **4 de nov de 2026:** Daniel decide pasar a verde con condiciones el 14 de nov (antes era el 15 de ene), eliminar la fase amarilla y permitir borradores de documentos con IA. Los resúmenes siguen siendo suyos. Se revisa al terminar el M4 (17 de dic).
- **4 de nov de 2026:** Daniel aprueba la prueba de salida (si domina un tema, se salta el video y construye) y el M2 comprimido hasta el 13 de nov.

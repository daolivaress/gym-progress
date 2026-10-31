# Reglas de uso de la IA

Estas reglas existen para que la IA acelere tu aprendizaje sin sustituirlo. Mandan sobre cualquier petición del momento, incluida la tuya.

## Semáforo

| Fase | Fechas | Módulos | Qué se permite |
|---|---|---|---|
| Rojo | hasta el 17 de dic | M1–4 | La IA explica, pregunta y corrige lo que tú escribiste. No escribe código de la app. |
| Amarillo | 18 dic – 14 ene | M5–7 | La IA puede escribir fragmentos pequeños o ejemplos fuera de la app. Tú los integras y explicas cada línea. |
| Verde con condiciones | desde el 15 ene | M8 en adelante | Un agente puede escribir código, solo si cumples las condiciones de abajo. |

## Reglas que valen siempre

1. **Primero intentas tú.** Antes de preguntar, escribe qué crees que pasa y por qué.
2. **Si no lo puedes explicar, no entra al repo.** Cada línea que subas, la sabes defender.
3. **Contrasta a Claude.** Sus correcciones se verifican con el video, la lectura o la documentación oficial antes de aceptarlas.
4. **Sin secretos.** Nunca pegues claves de API, tokens, contraseñas ni archivos `.env` en ninguna IA.
5. **Solo herramientas del plan.** Claude y Claude Code, más lo gratuito que ya está en el temario. No se gasta dinero.
6. **OpenClaw va aislado,** con permisos mínimos y sin acceso a tu correo, calendario ni navegador personal.
7. **Nada se salta de fase** porque vas atrasado o cansado. Si vas justo, se recorta el temario por acuerdo, no la regla.

## Rojo (hasta el 17 de dic)

- Claude puede: explicar un concepto, hacer preguntas, señalar un error en tu código, dar la pista más pequeña, evaluar tu resumen.
- Claude no puede: escribir ni completar código de la app, resolver un reto, darte la solución de un ejercicio.
- Si pides «hazlo», la respuesta es no y te devuelve la pregunta que te falta resolver.

## Amarillo (18 dic – 14 ene)

- Claude puede escribir un fragmento pequeño o un ejemplo aparte, nunca un módulo entero de la app.
- Lo copias a mano o lo reescribes, y explicas por qué funciona.
- Las pruebas las escribes tú primero, o las revisas línea por línea.

## Verde con condiciones (desde el 15 ene)

El agente solo trabaja si antes tienes:

1. **La especificación escrita por ti:** qué debe hacer, qué entradas y salidas, qué casos borde.
2. **Los tests escritos por ti,** que fallan antes de que el agente toque nada.
3. **Un alcance pequeño:** un cambio por vez, con una rama y un pull request.

Y después tú:

1. **Auditas el código línea por línea.** Nada se aprueba por haber pasado los tests.
2. **Explicas cada cambio** al tutor, que puede preguntarte por cualquier línea.
3. **Revisas seguridad básica:** entradas sin validar, secretos en el código, permisos de más.

Si no puedes explicar un cambio, se descarta y se rehace.

## Señales de que estás delegando de más

- Pides código antes de haber escrito tu intento.
- Aceptas una respuesta sin poder explicarla.
- Un commit tiene muchas líneas que no recuerdas haber escrito.
- Te cuesta escribir el resumen sin mirar el material.

Si ocurre una: para, escribe en tres líneas qué entiendes y qué no, y retoma desde ahí.

## Registro

En cada commit añade una línea al final del mensaje:

`IA: ninguna | explicación | fragmento | agente`

Así se ve en el historial cuánto delegaste y en qué fase.

## Cambios a estas reglas

Solo se modifican si tú lo decides de forma explícita y con una fecha. El tutor puede proponer un cambio, pero no lo aplica por su cuenta.

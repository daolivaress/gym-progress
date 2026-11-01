# Visión del Producto: App "Gym-Progress"

## 1. Introducción

Este proyecto consiste en el desarrollo de una app para registrar los progresos en el entrenamiento de fuerza, gestionar rutinas de ejercicios, realizar un seguimiento de los récords personales ($PRs$) y optimizar cada aspecto del rendimiento en el gimnasio.

## 2. El Problema que Resuelve

A medida que avanzamos en el entrenamiento, el progreso se vuelve cada vez más difícil y, en muchas ocasiones, no resulta evidente cómo continuar aplicando la sobrecarga progresiva semana a semana.

**Gym-Progress** soluciona este problema central al permitir registrar la rutina activa, las repeticiones logradas y el peso cargado en cada sesión. Con base en estos datos, la aplicación determinará automáticamente cuándo y cómo aplicar la sobrecarga progresiva (ya sea aumentando las repeticiones o incrementando el peso).

## 3. Público Objetivo

- **Fase inicial:** Uso personal y exclusivo del creador.
- **Fase futura:** Escalable para lanzarse al público general, enfocado en atletas principiantes e intermedios que entrenan en el gimnasio.

## 4. Diferenciación frente a Competidores (Hevy y Strong)

El principal factor diferenciador es que **será completamente gratuita para mí**, evitando las suscripciones de pago que exigen las aplicaciones líderes del mercado actual y teniendo acceso a funciones que en esas apps requieren de una suscripcion.

## 5. Requerimientos Core (Funcionalidades Imprescindibles)

Estas son las dos funciones principales e indispensables para resolver el problema central de la aplicación:

### A. Creación y Registro de Rutinas

- Permite crear y registrar rutinas completas dentro de la app.
- Configuración de series, rangos de repeticiones y tiempos de descanso por ejercicio.

### B. Sobrecarga Progresiva Inteligente y Automática

La app registrará las repeticiones y el peso realizado en cada serie para calcular de forma inteligente los siguientes pasos según el rendimiento anterior:

- **Regla de aumento de peso:** Si se alcanza el **número máximo de repeticiones** del rango establecido (por ejemplo, rangos de $6-8$, $8-10$, $10-12$, o $10-15$) en **todas** las series (sean 2, 3 o 4), la app recomendará **subir el peso** en la siguiente sesión.
- **Regla de aumento de repeticiones:** Si solo se alcanza el mínimo de repeticiones o un valor intermedio dentro del rango, la app indicará que en la próxima sesión se debe buscar, al menos, una repetición más.
  - _Ejemplo:_ Si en el jalón al pecho con 3 series solo se hicieron 6 repeticiones, el objetivo para la semana siguiente será alcanzar al menos 7, y así sucesivamente hasta llegar al tope del rango.
- **Gestión del descanso (Ejemplo: rendimiento decreciente como 8-7-5):** Si el rendimiento decae drásticamente, la app sugerirá incrementar el tiempo de descanso (por ejemplo, pasar de 3 minutos a 4 o 4:30 minutos, preguntándole previamente al usuario cuánto desea ampliarlo), esta sugerencias las dara cada vez que ocurra alguno de estos casos.
- **Regla de reducción de peso:** Si en la primera serie el usuario no es capaz de superar el límite inferior (por ejemplo, hace solo 5 repeticiones cuando el mínimo era 6), la app recomendará **bajar el peso** esto sucedera cada vez que ocurra este caso.

---

## 6. Funcionalidades Extra (Inspiración en Symmetry)

### 🤖 Coach / Asistente de Inteligencia Artificial

- **Consejos personalizados:** Sugerencias basadas en el historial de entrenamiento.
- **Escaneo corporal:** Herramienta visual con alta fiabilidad para comparar fotos anteriores, identificar puntos fuertes y débiles, y emitir recomendaciones basadas en la evolución física.

### 📊 Análisis de Rutinas

- Evaluación del volumen óptimo de entrenamiento.
- Control de la proximidad al fallo para garantizar series exigentes y efectivas por grupo muscular, estimulando el crecimiento sin comprometer la recuperación.

### 📈 Gráficos y Sistema de Rachas

- Gráficos claros de evolución en fuerza, volumen total y constancia para visualizar el progreso real.
- Sistema de racha de cumplimiento: inicia desde el primer día completado de la rutina (los días de descanso programados no pausan ni cancelan la racha).

### 🗺️ Mapa de Fatiga Corporal

- Representación visual interactiva del cuerpo humano que indica los niveles de fatiga muscular:
  - **Verde y azul:** Zonas menos fatigadas o recuperadas.
  - **Naranja y rojo:** Zonas con mayor acumulación de fatiga _(pendiente definir la fórmula matemática exacta de cálculo)_.

### 📐 Métricas y Estadísticas Corporales

Cálculos automáticos basados en la altura, peso, edad y género del usuario:

- **Frecuencia Cardíaca Máxima ($FCM$):** Calculada mediante la _Fórmula de Tanaka_:
  $$FCM = 208 - (0.7 \times \text{edad})$$
- **Gasto Calórico de Mantenimiento:** Calculado mediante la ecuación de _Mifflin-St Jeor_, multiplicado por el Nivel de Actividad Física ($NAF$).
- **Índice de Masa Corporal ($IMC$):**
  $$IMC = \frac{\text{peso (kg)}}{\text{estatura (m)}^2}$$
  Clasificando al usuario en bajo peso, peso normal, sobrepeso u obesidad.

### 🏆 Ranking por Grupos Musculares

- Clasificación dividida en: Pecho, Espalda, Hombros, Brazos (calculado mediante una media entre ejercicios de bíceps y tríceps), Piernas y Abdominales, adoptando de momento los rangos de referencia utilizados por la app _Symmetry_.

### 🎥 Demostración Visual de Ejercicios

- Guías visuales y técnicas correctas de ejecución junto con indicaciones clave. _(Nota: Esta sección es puramente informativa y no altera el cálculo de la sobrecarga progresiva)._

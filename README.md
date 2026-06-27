# Aterrizaje Suave — Modo Reto

Minijuego educativo de física donde el estudiante debe programar el descenso de una cápsula ajustando la altura de encendido del motor y la potencia de empuje. Forma parte de **EulerGames**, una colección de retos interactivos donde el estudiante calcula, decide y contrasta su respuesta con una simulación.

---

## Descripción del juego

En **Aterrizaje Suave — Modo Reto**, una cápsula desciende verticalmente hacia una plataforma en un mundo con gravedad propia. Antes de iniciar la simulación, el estudiante debe decidir a qué altura encender el motor y con qué potencia hacerlo.

La misión consiste en lograr que la cápsula toque la plataforma con una velocidad menor o igual al límite seguro, evitando tanto un impacto destructivo como un frenado excesivo o un consumo ineficiente de combustible.

---

## Objetivo educativo

El juego trabaja conceptos de dinámica y cinemática en una dimensión:

* caída vertical;
* velocidad y aceleración;
* gravedad;
* fuerza de empuje;
* fuerza neta;
* masa;
* frenado;
* consumo de combustible;
* velocidad segura de aterrizaje;
* toma de decisiones bajo restricciones.

---

## Mecánica principal

Cada misión presenta datos físicos del descenso, como altura inicial, velocidad inicial, gravedad, masa de la cápsula, empuje máximo, combustible disponible y velocidad segura de contacto.

El estudiante debe ajustar dos variables antes de probar:

* la altura de encendido del motor;
* la potencia del motor.

Al iniciar la simulación, la cápsula ejecuta exactamente la estrategia programada. El jugador no controla el descenso en tiempo real, por lo que el reto no depende de reflejos, sino de razonar antes de actuar.

La dificultad principal está en anticipar si la distancia de frenado, la potencia elegida y el combustible disponible serán suficientes para llegar con una velocidad segura.

---

## Evaluación

El intento se considera exitoso si la cápsula aterriza con una velocidad final menor o igual al límite seguro indicado en la misión.

Después del intento, el juego proporciona retroalimentación sobre el resultado. Puede indicar, por ejemplo, si el aterrizaje fue seguro, si la cápsula llegó demasiado rápido, si el motor se encendió demasiado tarde, si la potencia fue insuficiente, si el combustible se agotó o si hubo un frenado excesivo.

La retroalimentación incluye evidencia del intento, como velocidad final, límite seguro y combustible restante.

---

## Controles

El juego utiliza controles visuales y teclado.

Controles principales:

* deslizador para ajustar la altura de encendido;
* perilla para ajustar la potencia del motor;
* botones visibles para incrementar o disminuir cada variable;
* botón para probar el descenso;
* botón para volver a intentar;
* botón para generar una nueva misión;
* botón para activar o desactivar sonido.

Convención de teclado de EulerGames:

* `← / →` para ajuste grueso;
* `↑ / ↓` para ajuste fino;
* `Tab` para cambiar entre controles;
* botones visibles equivalentes al teclado.

---

## Visualización

El juego incluye una escena central con la cápsula descendiendo hacia una plataforma. La altura de encendido programada se muestra como una línea de referencia dentro de la simulación.

Elementos visuales principales:

* panel de datos de misión;
* simulación central en Canvas;
* indicador de tiempo;
* telemetría de altura, velocidad, combustible y estado del motor;
* barra de combustible;
* historial de intentos;
* retroalimentación visual de éxito o fallo;
* gráficas posteriores al intento;
* efectos visuales de motor, impacto y partículas;
* sonido opcional mediante Web Audio API.

Las gráficas posteriores permiten revisar el comportamiento observado durante el descenso, especialmente la evolución de la altura y la velocidad.

---

## Modelo físico o matemático simplificado

El juego utiliza un modelo simplificado de movimiento vertical con fines educativos. La cápsula se mueve en una dimensión bajo la acción de la gravedad y del empuje del motor.

El modelo considera:

* gravedad constante durante cada misión;
* masa constante de la cápsula;
* empuje vertical hacia arriba;
* velocidad positiva hacia abajo;
* consumo de combustible proporcional a la potencia utilizada;
* ausencia de resistencia del aire;
* simulación en tiempo físico real.

De forma general, el cálculo interno sigue estos pasos:

1. la cápsula inicia a cierta altura con una velocidad descendente;
2. antes del encendido, acelera por efecto de la gravedad;
3. cuando alcanza la altura programada, el motor se activa si queda combustible;
4. el empuje reduce la aceleración descendente o puede invertirla si es excesivo;
5. la simulación actualiza posición, velocidad y combustible en cada instante;
6. al tocar la plataforma, se evalúa la velocidad final contra el límite seguro.

El modelo no pretende representar todos los detalles de un cohete real, pero mantiene una relación coherente entre gravedad, empuje, masa, aceleración, velocidad y posición.

---

## Tecnologías utilizadas

* HTML
* CSS
* JavaScript
* Canvas API
* Web Audio API

No se utilizan librerías externas.

---

## Cómo ejecutar

Sólo es necesario abrir el archivo:

```text
index.html
```

en un navegador moderno.

El juego también puede publicarse directamente mediante GitHub Pages, ya que todo el contenido está contenido en un único archivo HTML.

---

## Estructura del proyecto

```text
Aterrizaje-Suave-Modo-Reto/
│
└── index.html
```

---

## Filosofía EulerGames

**EulerGames** busca crear minijuegos educativos donde el estudiante no sólo observe una simulación, sino que participe activamente en el razonamiento.

Cada juego debe proponer un reto claro:

1. leer datos;
2. razonar o calcular;
3. tomar una decisión;
4. probar la respuesta;
5. recibir retroalimentación.

El objetivo es que el juego funcione como una experiencia interactiva de aprendizaje, no como una calculadora disfrazada.

---

## Autor

Proyecto desarrollado por **Fausto** como parte de la colección **EulerGames**.

# De una idea a una aplicación (sin ser experto en tecnología)

Bienvenido. En esta sesión vamos a construir juntos una aplicación real,
paso a paso, sin escribir código a mano. Tú solo vas a **copiar y pegar
prompts** a Kiro, y la aplicación irá tomando forma poco a poco.

La premisa: **no necesitas una idea de oro para empezar.** Vamos a resolver
un problema pequeño y cotidiano, el tipo de cosa que cualquiera podría querer
para su negocio o su trabajo.

## Qué vamos a construir

Una aplicación para llevar el control de los **pedidos de una pastelería**:
anotar pedidos, verlos ordenados, marcar los entregados y que no se pierdan.

Es un solo archivo que se abre con **doble clic**. Sin instalar nada, sin
servidores, sin bases de datos. Si tienes un navegador (Chrome, Safari, Edge),
ya tienes todo lo necesario.

## Qué necesitas antes de empezar

1. Tener **Kiro** instalado y funcionando.
2. Crear una carpeta vacía en tu computadora (por ejemplo, `mi-pasteleria`).
3. Abrir Kiro dentro de esa carpeta.

Nada más. No hay que instalar dependencias ni configurar nada.

## Cómo usar esta guía

- Copia **un prompt a la vez** y pégalo en el chat de Kiro.
- Espera a que termine y **abre el archivo para ver el resultado** (o recarga
  la página si ya la tenías abierta).
- Cuando estés conforme, pasa al siguiente paso.
- No te saltes pasos: cada uno construye sobre el anterior.

---

## Paso 1 — La primera versión que funciona

Creamos la base: un formulario para anotar pedidos y una lista para verlos.

```
Quiero crear una aplicación web muy sencilla para llevar el control de los
pedidos de una pastelería.

Debe ser un solo archivo HTML que yo pueda abrir con doble clic, sin instalar
nada y sin necesidad de un servidor.

La página debe tener:
- Un formulario para registrar un pedido con tres datos: nombre del cliente,
  producto y fecha de entrega.
- Debajo, una lista que muestre todos los pedidos que voy registrando.

Por ahora quiero mantenerlo lo más simple posible: no guardes los pedidos de
forma permanente, está bien que se pierdan al cerrar la página. Más adelante
me encargaré de eso.

Que se vea limpia y ordenada, con un título arriba que diga
"Pedidos de la Pastelería".
```

> **Nota para el presentador:** la línea de "no guardes los pedidos de forma
> permanente" es intencional. Sin ella, Kiro suele agregar el guardado por su
> cuenta y el Paso 2 (el momento "wow" de la persistencia) pierde efecto. Al
> pedirle que mantenga el alcance simple, controlas qué construye y te aseguras
> de que el Paso 2 siempre funcione en vivo. De paso, es una gran lección: tú
> decides el "qué" y el "cuánto", la IA ejecuta.

---

## Paso 2 — Que no se borren los datos

Aquí viene un momento clave. Registraste unos pedidos de prueba... pero si
cierras la página, todo desaparece. Vamos a arreglarlo de inmediato, así el
resto del taller no te obliga a teclear todo de nuevo en cada paso. Este prompt
es un gran ejemplo de "describir el problema y dejar que la IA proponga la
solución".

```
Me di cuenta de que si cierro la página se borran todos los pedidos.

Quiero que los pedidos se guarden en el mismo navegador, de manera que sigan
ahí aunque cierre y vuelva a abrir la página. No quiero instalar ninguna base
de datos ni ningún programa extra.
```

Prueba: registra un pedido, cierra la página, vuélvela a abrir. Sigue ahí. De
aquí en adelante tus pedidos de prueba se conservan entre paso y paso.

---

## Paso 3 — Ordenar por fecha de entrega

Ahora que hay pedidos, queremos saber qué entregar primero.

```
Ahora quiero que la lista de pedidos aparezca ordenada por la fecha de entrega,
de la más próxima a la más lejana, para saber de un vistazo qué tengo que
entregar primero.
```

---

## Paso 4 — Marcar pedidos como entregados

Necesitamos distinguir lo que ya salió de lo que sigue pendiente.

```
Quiero poder marcar un pedido como entregado.

Agrega a cada pedido una forma de marcarlo como entregado, y haz que los
pedidos entregados se vean distintos de los pendientes (por ejemplo, en gris
o tachados) para diferenciarlos de un vistazo.
```

---

## Paso 5 — Buscar por cliente

Cuando hay muchos pedidos, necesitamos encontrarlos rápido.

```
Agrega un buscador arriba de la lista para filtrar los pedidos por el nombre
del cliente. Al escribir, que se muestren solo los pedidos de ese cliente.
```

---

## Paso 6 — Un resumen del día

Un toque que hace la app sentirse "de verdad".

```
Quiero ver un pequeño resumen arriba de la lista que me diga cuántos pedidos
tengo pendientes en total y cuántos son para entregar hoy, para saber de un
vistazo cómo viene el día.
```

---

## Paso 7 — Que se vea bonita

Lo último: darle personalidad.

```
Dale un mejor aspecto a la aplicación: colores agradables para una pastelería,
una tipografía amigable, y que se vea bien tanto en la computadora como en el
celular.
```

---

## Paso 8 — ¡Tu turno! (capa abierta con la audiencia)

Aquí ya no mando yo, mandan ustedes. ¿Qué le agregarían a la app?

Escribe tu propia idea siguiendo la regla de oro (qué, para qué, cómo). Por
ejemplo: "Quiero poder... para... y que se vea/comporte...".

Si te falta inspiración, prueba alguno de estos:

**Eliminar un pedido**
```
Agrega a cada pedido un botón para eliminarlo, con una confirmación antes de
borrarlo para no eliminarlo por accidente.
```

**Manejar precios y total**
```
Agrega un campo de precio a cada pedido y muestra abajo el total de dinero
de todos los pedidos que aún están pendientes.
```

**Editar un pedido**
```
Quiero poder editar un pedido ya registrado por si me equivoqué en el cliente,
el producto o la fecha, sin tener que borrarlo y crearlo de nuevo.
```

---

## ¿Y si quiero que crezca más? (el siguiente nivel)

Hoy guardamos todo en el navegador y con eso basta para uso personal. Pero
quizá te preguntes: *¿y si quiero que mis pedidos los vean desde varios
celulares, o que no dependan de esta computadora?*

Ahí es cuando la app crece: se le agrega un "cerebro" por detrás (un backend)
y una base de datos de verdad, como **SQLite**. Eso ya requiere instalar y
configurar más cosas, por eso no lo hacemos hoy en vivo. Pero la buena noticia
es que se construye **exactamente igual**: describiéndole a Kiro lo que quieres,
por capas.

No lo intentes ahora en la sesión; queda como tu reto para después.

---

## El reto para hoy en la noche

Elige **una tarea aburrida de tu semana** (algo que anotas en un cuaderno, que
copias entre dos hojas de Excel, que haces a mano una y otra vez) y pídele a
Kiro la versión más sencilla que funcione. Empieza pequeño. La app crece contigo.

Recuerda: el código lo pone la herramienta. El **qué** lo pones tú.

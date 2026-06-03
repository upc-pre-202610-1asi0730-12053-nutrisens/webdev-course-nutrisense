# LECCIÓN 2 — Estructura HTML básica

---

[EN PANTALLA: abrir CodePen con el panel de HTML vacío. No escribir nada todavía.]

Hola, bienvenidos de vuelta.

En la lección anterior vieron qué es una página web, de qué está hecha, y pudieron echar un vistazo al código de YouTube desde el navegador. Hoy vamos a meternos dentro de ese código. Vamos a entender cómo está construido el HTML por dentro.

Abran el CodePen de esta lección — el enlace está en la descripción. El panel de HTML está vacío y así lo queremos, porque vamos a llenarlo juntos desde cero.

---

## ¿Qué es una etiqueta?

[EN PANTALLA: en el panel HTML de CodePen, escribir lentamente:]

```html
<p>Este es mi primer párrafo.</p>
```

Lo más básico del HTML son las **etiquetas**. Una etiqueta es una instrucción que le dice al navegador: "esto que está aquí es un párrafo", o "esto es un título", o "esto es una imagen".

Las etiquetas se escriben entre los signos de mayor y menor — esos símbolos que en matemáticas usamos para comparar números. En HTML los usan para envolver instrucciones.

[EN PANTALLA: señalar con el cursor cada parte mientras se nombra:]

Miren este ejemplo. Tienen tres partes.

La primera es la **etiqueta de apertura**: `<p>`. Es la que abre, la que dice "empieza aquí".

La segunda es el **contenido**: el texto "Este es mi primer párrafo." — lo que quieren que aparezca en la página.

La tercera es la **etiqueta de cierre**: `</p>`. Es igual a la de apertura pero con una barra al inicio. Es la que dice "termina aquí".

A las tres partes juntas — apertura, contenido y cierre — se les llama un **elemento**. Un elemento HTML completo.

---

## ¿Qué son los atributos?

[EN PANTALLA: modificar la línea anterior para agregar un atributo id:]

```html
<p id="intro">Este es mi primer párrafo.</p>
```

Dentro de las etiquetas de apertura también puede ir información extra. A eso se le
llama **atributo**.

Miren: escribí id="intro" dentro de la etiqueta `<p>`. Ese atributo se llama id y le pone un nombre único a este elemento. Es como una etiqueta de identificación, como el DNI de ese párrafo.

[EN PANTALLA: agregar también class:]

```html
<p id="intro" class="destacado">Este es mi primer párrafo.</p>
```

También existe el atributo class, que es como una pegatina de grupo. Varios elementos pueden tener la misma clase. Estos dos atributos los van a ver muchísimo en las siguientes lecciones cuando empiecen a usar CSS. Por ahora, con que sepan que existen y que van dentro de la etiqueta de apertura es suficiente.

---

## El esqueleto de toda página web

[EN PANTALLA: borrar todo lo que hay en el panel HTML y empezar desde cero,
escribiendo lentamente:]

Ahora viene la parte más importante de esta lección: el esqueleto base. Toda página
web, sin excepción, parte de esta misma estructura.

[EN PANTALLA: escribir línea por línea:]

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi página</title>
  </head>
  <body>

  </body>
</html>
```

Vamos parte por parte.

[EN PANTALLA: resaltar con el cursor <!DOCTYPE html>.]

Lo primero es `<!DOCTYPE html>`. Esta línea no es una etiqueta normal — no tiene cierre. Es una declaración. Le dice al navegador: "lo que viene a continuación es HTML moderno". Sin esta línea, el navegador podría interpretar el código de una manera rara o antigua. Siempre va al inicio, siempre es la primera línea.

[EN PANTALLA: resaltar <html> y </html>.]

Después viene la etiqueta `<html>`. Esta envuelve absolutamente todo el resto del
documento. Todo lo que escriban tiene que ir dentro de `<html>` y su cierre `</html>`.
Es el contenedor más grande de la página.

[EN PANTALLA: resaltar <head> y </head>.]

Dentro de `<html>` hay dos secciones. La primera es el `<head>`. Piensen en el `<head>` como la trastienda de una tienda: es donde están las cosas que el negocio necesita para funcionar, pero que los clientes no ven. El `<head>` contiene información que el navegador necesita — como el título de la pestaña — pero nada de lo que hay en el
`<head>` aparece directamente en la página.

[EN PANTALLA: resaltar <body> y </body>.]

La segunda sección es el `<body>`. Este sí es el escaparate: todo lo que escriban dentro del `<body>` es lo que va a aparecer en pantalla. Títulos, párrafos, imágenes, botones — todo eso va aquí.

---

## Un detalle clave: cerrar las etiquetas

Hay una regla en HTML que parece obvia pero que todo el mundo olvida al principio: **cada etiqueta queabran, tienen que cerrarla.**

[EN PANTALLA: dentro del <body>, escribir con el error a propósito:]

```html
<body>
  <p><b>Este párrafo no tiene cierre
  <p>Este es otro párrafo</p>
</body>
```

[EN PANTALLA: mostrar el preview — el segundo párrafo puede verse afectado.]

Miren lo que pasa cuando olvido cerrar el primer `<p>` y `<b>`. El navegador intenta adivinar
qué quisimos hacer y a veces "lo arregla solo"... pero a su manera, no a la nuestra, en este caso aplica la negrita al párrafo de abajo también.
En proyectos grandes, estos errores escondidos son peligrosos: no los ves hasta que algo se ve raro en la página y puede causar problemas difíciles de encontrar.
Siempre, siempre cierren sus etiquetas.

[EN PANTALLA: corregir el error:]

```html
<body>
  <p><b>Este párrafo sí tiene cierre.</b></p>
  <p>Este es otro párrafo.</p>
</body>
```

---

## Pausa de práctica

[EN PANTALLA: texto en pantalla que diga "¡Tu turno!"]

Ahora pausa el video y haz esto en tu CodePen:

Uno: escribe el esqueleto completo desde cero — `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>` — sin copiarlo, de memoria si puedes. Si te equivocas, está bien, corrígelo.

Dos: dentro del `<head>`, cambia el texto de `<title>` por el nombre que quieras ponerle a tu página.

Tres: dentro del `<body>`, escribe cualquier frase entre etiquetas `<p>` y comprueba que aparece en el preview.

[PAUSA: dejar 5 segundos.]

---

## Cierre

Muy bien. Tres cosas para llevarse de esta lección.

Una: una etiqueta HTML tiene apertura, contenido y cierre — y al conjunto se le llama elemento.

Dos: los atributos van dentro de la etiqueta de apertura y le dan información extra al elemento.

Tres: toda página web parte del mismo esqueleto — `<!DOCTYPE html>`, `<html>`, `<head>` y `<body>`. El `<head>` es la trastienda; el `<body>` es lo que se ve.

En la siguiente lección vamos a llenar ese `<body>` con contenido real: títulos, párrafos, listas, imágenes y enlaces. ¡Nos vemos ahí!
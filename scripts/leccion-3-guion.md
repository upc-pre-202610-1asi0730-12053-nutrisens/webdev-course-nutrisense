# Script Video — Lección 3
## Elementos HTML comunes

---

[EN PANTALLA: abrir CodePen con el esqueleto HTML base — el body vacío.]

Hola, bienvenidos de vuelta.

En la lección anterior aprendieron cómo está construida una página HTML por dentro: el esqueleto, las etiquetas, el head y el body. Ese esqueleto es la base, pero todavía está vacío.

Hoy vamos a llenarlo. Vamos a conocer los cinco elementos HTML que aparecen en prácticamente cualquier sitio web que visitan: títulos, párrafos, listas, imágenes y enlaces.

El CodePen de esta lección ya tiene el esqueleto listo. Todo lo que vamos a escribir va dentro del body.

---

## Encabezados: `<h1>` al `<h6>`

[EN PANTALLA: dentro del body, escribir:]

```html
<h1>Mi primera página</h1>
<h2>Sobre mí</h2>
<h3>Mis hobbies</h3>
```

El primer elemento son los encabezados. HTML tiene seis niveles de título, del h1 al h6. La h viene de heading — encabezado en inglés.

El h1 es el más grande y el más importante — el título principal. El h2 sería el nombre de un capítulo. El h3, una sección dentro de ese capítulo.

[EN PANTALLA: señalar el preview donde se ven los tres títulos en tamaños diferentes.]

Regla importante: no salten niveles. No pongan un h3 si todavía no pusieron un h2.

---

## Párrafos: `<p>`

[EN PANTALLA: agregar debajo de los encabezados:]

```html
<p>Hola, soy estudiante. Me gusta aprender cosas nuevas.</p>
<p>En este sitio voy a compartir mis intereses.</p>
```

Para texto normal usamos p, que viene de paragraph — párrafo.

[EN PANTALLA: señalar el espacio entre los dos párrafos en el preview.]

Entre los dos párrafos hay un espacio automático. El navegador lo agrega solo — cada p tiene un respiro antes y después.

---

## Listas: `<ul>`, `<ol>` y `<li>`

[EN PANTALLA: agregar:]

```html
<ul>
  <li>Me gusta la música</li>
  <li>Me gusta programar</li>
  <li>Me gusta leer</li>
</ul>
```

HTML tiene dos tipos de listas. La lista desordenada — ul — muestra viñetas. La lista ordenada — ol — numera automáticamente.

Cada elemento va dentro de li — list item. El li siempre va dentro del ul o del ol, nunca solo.

Pause y piensen: ¿cuándo usarían números y cuándo viñetas?

[PAUSA: 3 segundos.]

Números cuando el orden importa — pasos, instrucciones. Viñetas cuando el orden no importa — hobbies, ingredientes.

[EN PANTALLA: agregar la lista ordenada:]

```html
<ol>
  <li>Abrir el navegador</li>
  <li>Ir a CodePen</li>
  <li>Empezar a escribir código</li>
</ol>
```

[EN PANTALLA: señalar los números automáticos en el preview.]

Los números aparecen solos — no tienen que escribir 1, 2, 3.

---

## Imágenes: `<img>`

[EN PANTALLA: agregar:]

```html
<img src="https://placekitten.com/200/200" alt="Un gatito de ejemplo">
```

[EN PANTALLA: esperar a que la imagen aparezca en el preview.]

La etiqueta img es especial: no se cierra. No existe cierre para img. Es una etiqueta vacía — solo tiene atributos.

- src — source — es la URL donde está la imagen.
- alt — texto alternativo — aparece si la imagen no carga.

[EN PANTALLA: cambiar src por "imagen-rota.jpg" y mostrar el alt.]

¿Ven? La imagen no carga pero el texto del alt aparece. Los lectores de pantalla también usan ese texto para personas con discapacidad visual. El alt nunca es opcional.

[EN PANTALLA: corregir la URL a la original.]

---

## Enlaces: `<a>`

[EN PANTALLA: agregar:]

```html
<a href="https://www.google.com">Ir a Google</a>
```

La etiqueta a viene de anchor — ancla. Crea un link.

- href — hypertext reference — es la URL destino.
- El texto entre apertura y cierre es lo que el usuario ve y clica.

[EN PANTALLA: señalar el texto subrayado en el preview.]

---

## Demo completo

[EN PANTALLA: mostrar todo el código junto en el body:]

```html
<h1>Mi primera página</h1>
<p>Hola, soy estudiante. Me gusta aprender cosas nuevas.</p>
<h2>Mis intereses</h2>
<ul>
  <li>Me gusta la música</li>
  <li>Me gusta programar</li>
</ul>
<img src="https://placekitten.com/200/200" alt="Un gatito de ejemplo">
<a href="https://www.google.com">Ir a Google</a>
```

[EN PANTALLA: señalar el preview con todos los elementos juntos.]

Todo esto vive dentro del body del esqueleto de la lección anterior.

---

## Pausa de práctica

[EN PANTALLA: texto "¡Tu turno!"]

Pausa el video y modifica el CodePen:

1. Cambia el h1 por tu nombre real.
2. Reemplaza los li por tus intereses de verdad.
3. Agrega un segundo p con una frase sobre ti.

[PAUSA: 5 segundos.]

---

## Cierre

Cinco elementos que ya conocen:
- h1 a h6 para títulos de distintos niveles.
- p para párrafos de texto.
- ul y ol con li para listas.
- img para imágenes con src y alt.
- a para enlaces con href.

En la siguiente lección Olenka les enseñará CSS: cómo darle colores, tamaños y estilo a todo lo que construimos hoy. ¡Nos vemos!
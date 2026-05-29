# LECCIÓN 1 — ¿Qué es el desarrollo web?
**Narrador: Joel | Duración estimada: ~8 minutos**

---

[EN PANTALLA: mostrar diapositiva de introduccion]

Hola, bienvenidos. Me alegra que estén aquí.

En esta primera lección vamos a responder una pregunta que parece simple pero que muy poca gente sabe contestar bien: ¿qué es exactamente una página web y cómo funciona?

No necesitan saber nada de programación para entender esto. No van a instalar ningún programa. Lo único que necesitan es el navegador que ya tienen abierto ahora mismo — Chrome, Firefox, Edge, el que sea.

Al final de este video van a entender de qué están hechas las páginas que usan todos los días. Empecemos.

---

## ¿Qué es un sitio web?

[EN PANTALLA: tener YouTube abierto en el navegador. Señalar la página con el cursor mientras se habla.]

Miren esta página de YouTube. Cuando la abren en su navegador, lo que están viendo es básicamente un documento. Un documento enorme y muy bien diseñado, pero un documento al fin. Y ese documento vive en alguna computadora del mundo — una computadora especial que se llama **servidor**.

Cuando ustedes escriben "youtube.com" en la barra del navegador, están haciendo una solicitud. Le dicen al servidor: "oye, dame esa página". El servidor la busca y se las envía. Y su navegador la muestra en pantalla.

Piénsenlo así: el servidor es una biblioteca gigante en algún lugar del mundo. Ustedes son el lector. El navegador es el mensajero que va, busca el libro y se lo trae. Eso pasa cada vez que abren una página web — en décimas de segundo.

[EN PANTALLA: cambiar a una diapositiva o imagen simple con el diagrama: Tú → solicitud → Servidor → respuesta → Navegador → Página web.]

Ese viaje de ida y vuelta ocurre en menos de un segundo la mayoría de las veces. Impresionante, ¿verdad?

---

## HTML y CSS: los dos ingredientes de toda página web

Ahora la pregunta es: ¿de qué está hecha esa página que el servidor les envía?

Toda página web, sin excepción, está construida con dos cosas. La primera se llama **HTML**. La segunda se llama **CSS**.

[EN PANTALLA: diapositivas HTML y CSS]

HTML es la **estructura**. Es todo lo que tiene contenido: los títulos, los párrafos, las imágenes, los botones. Si una página web fuera una persona, el HTML sería el esqueleto — le da forma y sostiene todo.

CSS es el **estilo**. Es todo lo que hace que se vea bien: los colores, el tamaño de las letras, dónde está cada cosa en la pantalla. Si el HTML es el esqueleto, el CSS es la ropa que le ponen encima.

Una página sin CSS se ve como texto negro sobre fondo blanco, todo apilado sin ningún orden visual. Una página con CSS se ve como lo que están acostumbrados a ver en internet. La diferencia es enorme.

En este curso van a aprender los dos. Hoy empezamos a entender cómo funcionan.

---

## Ver el código de una página real

[EN PANTALLA: volver a YouTube en el navegador.]

Ahora les voy a mostrar algo que muy poca gente sabe que puede hacer: ver el código de cualquier página web.

[EN PANTALLA: hacer clic derecho en cualquier parte de YouTube. Esperar a que aparezca el menú contextual.]

Hagan clic derecho en cualquier parte de la página. Les va a aparecer un menú. Busquen la opción que dice **Inspeccionar** y hagan clic ahí.

[EN PANTALLA: hacer clic en "Inspeccionar". Se abre el panel de herramientas del navegador a la derecha o abajo.]

¿Ven ese panel que se abrió? Eso es el código de YouTube. Lo que están viendo ahí es exactamente HTML y CSS — el mismo tipo de código que van a aprender en este curso.

[EN PANTALLA: señalar con el cursor las etiquetas que se ven en el panel, como `<div>`, `<span>`, `<h1>`. Hacer hover sobre alguna para que se ilumine en la página.]

Miren: cuando paso el cursor sobre estas líneas de código en el panel, la parte correspondiente de la página se ilumina. HTML y página son lo mismo, solo que uno es el código y el otro es cómo lo muestra el navegador.

No se preocupen si parece complicado ahora. Al final de este curso van a entender qué significa cada parte. Lo que importa ahora es que ya saben que ese código existe, que está en todas las páginas web, y que lo pueden ver en cualquier momento.

[EN PANTALLA: cerrar el panel de herramientas. Abrir una nueva pestaña con CodePen en codepen.io.]

---

## CodePen: su taller de trabajo

Ahora les presento la herramienta que vamos a usar en todo el curso. Se llama **CodePen** y la van a encontrar en codepen.io. Es completamente gratis y funciona en el navegador — no instalan nada.

[EN PANTALLA: mostrar la interfaz de CodePen con los tres paneles: HTML, CSS, y el preview abajo o a la derecha.]

Miren la interfaz. Tienen tres espacios. El de la izquierda es para escribir HTML. El del medio es para escribir CSS. Y el de abajo o a la derecha es el **resultado en tiempo real**: todo lo que escriban aparece ahí al instante.

Vamos a escribir algo para que vean cómo funciona.

[EN PANTALLA: hacer clic en el panel de HTML y escribir lo siguiente, lentamente:]

```html
<h1>Hola mundo</h1>
<p>Mi primera página web</p>
```

[EN PANTALLA: mostrar cómo el texto aparece en el preview mientras se escribe. Señalarlo con el cursor.]

¿Lo ven? Con solo dos líneas de código ya tienen el inicio de una página web. Un título y un párrafo. Eso es HTML trabajando.

No se preocupen todavía por qué significa `<h1>` o `<p>`. En la siguiente lección van a entender exactamente qué es cada parte.

---

## Pausa de práctica

[EN PANTALLA: texto en pantalla que diga "¡Tu turno!" o similar.]

Antes de terminar, hagan esto:

Uno: abran CodePen en codepen.io — el enlace está en la descripción de esta lección.

Dos: en el panel de HTML, escriban `<h1>` seguido de su nombre, y cierren con `</h1>`. Así: `<h1>Tu nombre</h1>`.

Tres: debajo de eso, escriban `<p>` seguido de algo que les guste, y cierren con `</p>`. Por ejemplo: `<p>Me gusta la música</p>`.

No importa si no entienden todavía qué significan esas palabras. Solo escríbanlo y vean qué aparece en el preview. En la siguiente lección lo vamos a explicar todo.

[PAUSA: dejar 5 segundos de silencio para que el estudiante procese.]

---

## Cierre

[EN PANTALLA: mostrar diapositiva de cierre.]

Muy bien. Repasemos lo que vimos hoy.

Primero: toda página web es un documento que vive en un servidor y que el navegador descarga y muestra cuando la solicitan.

Segundo: todas las páginas web están hechas de dos cosas — HTML para la estructura y el contenido, y CSS para los colores, el diseño y el estilo visual.

Tercero: ya pueden ver el código de cualquier página con clic derecho e Inspeccionar, y ya tienen CodePen listo para escribir código en el navegador sin instalar nada.

En la siguiente lección vamos a entender a fondo qué es una etiqueta HTML, cómo se estructura una página por dentro, y por qué cada parte está donde está. ¡Los espero ahí!
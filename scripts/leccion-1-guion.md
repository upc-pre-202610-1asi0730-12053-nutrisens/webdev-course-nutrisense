# LECCIÓN 1 — ¿Qué es el desarrollo web?

---

[EN PANTALLA: mostrar diapositiva de introducción]

Hola, bienvenidos. Me alegra que estén aquí.

En esta primera lección vamos a responder una pregunta que parece simple pero que muy poca gente sabe contestar bien: ¿qué es exactamente una página web y cómo funciona? No necesitan saber nada de programación para entender esto, y no van a instalar ningún programa. Lo único que necesitan es el navegador que ya tienen abierto ahora mismo — Chrome, Firefox, Edge, el que sea. Al final de este video van a entender de qué están hechas las páginas que usan todos los días. Empecemos.

---

## ¿Qué es un sitio web?

[EN PANTALLA: tener YouTube abierto en el navegador, señalar la página con el cursor]

Miren esta página de YouTube. Cuando la abren en su navegador, lo que están viendo es básicamente un documento. Un documento enorme y muy bien diseñado, pero un documento al fin. Y ese documento vive en alguna computadora del mundo — una computadora especial que se llama **servidor**.

Cuando ustedes escriben "youtube.com" en la barra del navegador, están haciendo una solicitud. Le están diciendo al servidor: "oye, dame esa página". El servidor la busca, se las envía, y su navegador la muestra en pantalla. Para entenderlo mejor, piénsenlo así: el servidor es como una biblioteca gigante en algún lugar del mundo, ustedes son el lector, y el navegador es el mensajero que va, busca el libro y se lo trae. Todo eso pasa cada vez que abren una página web — en décimas de segundo.

[EN PANTALLA: mostrar diapositiva con el diagrama: Tú → solicitud → Servidor → respuesta → Navegador → Página web]

Ese viaje de ida y vuelta ocurre en menos de un segundo la mayoría de las veces. Impresionante, ¿verdad?

---

## HTML y CSS: los dos ingredientes de toda página web

Ahora bien, la siguiente pregunta es: ¿de qué está hecha esa página que el servidor les envía? Toda página web, sin excepción, está construida con dos cosas. La primera se llama **HTML** y la segunda se llama **CSS**.

[EN PANTALLA: mostrar diapositivas de HTML y CSS]

El HTML es la **estructura**: es todo lo que tiene contenido, los títulos, los párrafos, las imágenes, los botones. Si una página web fuera una persona, el HTML sería el esqueleto que le da forma y sostiene todo. El CSS, por otro lado, es el **estilo**: es todo lo que hace que se vea bien, los colores, el tamaño de las letras, dónde está cada cosa en la pantalla. Dicho de otra manera, si el HTML es el esqueleto, el CSS es la ropa que le ponen encima.

Una página sin CSS se ve como texto negro sobre fondo blanco, todo apilado sin ningún orden visual. Una página con CSS se ve como lo que están acostumbrados a ver en internet. La diferencia es enorme, y en este curso van a aprender los dos. Hoy empezaran a entender como funcionan.

---

## Ver el código de una página real

[EN PANTALLA: volver a YouTube en el navegador]

Ahora les voy a mostrar algo que muy poca gente sabe que puede hacer: ver el código de cualquier página web. Estando en YouTube, hagan clic derecho en cualquier parte de la página y les va a aparecer un menú.

[EN PANTALLA: hacer clic derecho en YouTube, esperar el menú contextual]

Busquen la opción que dice **Inspeccionar** y háganle clic.

[EN PANTALLA: hacer clic en Inspeccionar, se abre el panel de herramientas]

¿Ven ese panel que se abrió? Eso es el código de YouTube. Lo que están viendo ahí es exactamente HTML y CSS — el mismo tipo de código que van a aprender en este curso. Y fíjense en algo interesante: cuando paso el cursor sobre estas líneas de código en el panel, la parte correspondiente de la página se ilumina. Eso significa que el HTML y la página son lo mismo, solo que uno es el código y el otro es cómo lo muestra el navegador.

[EN PANTALLA: señalar etiquetas como `<div>`, `<span>`, `<h1>` y hacer hover para que se iluminen en la página]

No se preocupen si parece complicado ahora. Al final de este curso van a entender qué significa cada parte. Lo que importa en este momento es que ya saben que ese código existe, que está en todas las páginas web, y que lo pueden ver en cualquier momento.

[EN PANTALLA: cerrar el panel, abrir nueva pestaña con codepen.io]

---

## CodePen: su taller de trabajo

Ahora les presento la herramienta que vamos a usar en todo el curso. Se llama **CodePen** y la encuentran en codepen.io. Es completamente gratis y funciona directo en el navegador, sin instalar nada.

[EN PANTALLA: mostrar la interfaz de CodePen con los tres paneles]

Miren la interfaz. Tienen tres espacios: el de la izquierda es para escribir HTML, el del medio es para escribir CSS, y el de abajo o a la derecha es el resultado en tiempo real. Todo lo que escriban aparece ahí al instante. Vamos a escribir algo para que vean cómo funciona.

[EN PANTALLA: hacer clic en el panel HTML y escribir lentamente]

```html
<h1>Hola mundo</h1>
<p>Mi primera página web</p>
```

[EN PANTALLA: mostrar cómo el texto aparece en el preview, señalarlo con el cursor]

¿Lo ven? Con solo dos líneas de código ya tienen el inicio de una página web: un título y un párrafo. Eso es HTML trabajando. No se preocupen todavía por qué significa `<h1>` o `<p>` — en la siguiente lección van a entender exactamente qué es cada parte.

---

## Pausa de práctica

[EN PANTALLA: mostrar diapositiva ¡Tu turno!]

Ahora haremos una pequeña pausa para que ustedes se puedan desenvolver y puedan saber poner en practica lo aprendido, para eso necesito que hagan una serie de pasos. Primero, abran CodePen en codepen.io — el enlace está en la descripción de esta lección. Segundo, en el panel de HTML escriban `<h1>` seguido de su nombre y cierren con `</h1>`, así: `<h1>Tu nombre</h1>`. Y tercero, debajo de eso escriban `<p>` seguido de algo que les guste y cierren con `</p>`, por ejemplo: `<p>Me gusta la música</p>`, finalmente miren el resultado en el preview. No importa si no entienden todavía qué significan esas palabras — solo escríbanlo y vean qué aparece en el preview. En la siguiente lección lo vamos a explicar todo.

[PAUSA: 5 segundos de silencio]

---

## Cierre

[EN PANTALLA: mostrar diapositiva de cierre con resumen]

Muy bien, repasemos lo que vimos hoy. Primero, toda página web es un documento que vive en un servidor y que el navegador descarga y muestra cuando la solicitan. Segundo, todas las páginas web están hechas de dos cosas: HTML para la estructura y el contenido, y CSS para los colores, el diseño y el estilo visual. Y tercero, ya pueden ver el código de cualquier página con clic derecho e Inspeccionar, y ya tienen CodePen listo para escribir código en el navegador sin instalar nada.

En la siguiente lección vamos a entender a fondo qué es una etiqueta HTML, cómo se estructura una página por dentro y por qué cada parte está donde está. ¡Los espero ahí!
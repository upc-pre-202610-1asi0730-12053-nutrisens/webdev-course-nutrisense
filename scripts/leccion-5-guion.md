# LECCIÓN 5 — Estilos simples
## Duración estimada: ~8 minutos**

---

[EN PANTALLA: PPT — Diapositiva de portada "Lección 5 · Estilos simples"]

Hola, bienvenidos de vuelta.

En la lección anterior aprendieron a cambiar colores, tipografías y tamaños de texto con CSS. Hoy vamos a subir un nivel. Vamos a aprender a **acomodar** las cosas: ponerles bordes, darles espacio para que respiren, y crear lo que se llama una tarjeta — esas cajas con bordes y fondo que ven en absolutamente todas las páginas web modernas.

Miren a dónde vamos a llegar.

[EN PANTALLA: abrir brevemente un CodePen con la versión terminada — la tarjeta blanca con borde morado, esquinas redondeadas y sombra, centrada sobre el fondo azul. Luego volver al starter.]

¿Ven esa caja blanca, centrada, con borde y sombra? Eso es una tarjeta. Y la vamos a construir juntos. Es más fácil de lo que parece.

---

## Padding vs. Margin: el concepto que todo el mundo confunde

[EN PANTALLA: PPT — Diapositiva "Padding vs. Margin"]

Antes de escribir una sola línea de código, necesitan entender dos palabras que la gente siempre mezcla: **padding** y **margin**.

Imaginen un cuadro colgado en una pared. El **padding** es el espacio que hay *dentro* del marco — el espacio entre el borde del marco y la foto. El **margin** es el espacio que hay *fuera* del marco — la distancia entre ese cuadro y los otros cuadros de la pared.

Repítenlo conmigo: padding es por dentro. Margin es por fuera.

Esa frase los va a salvar más de una vez.

---

## El `<div>`: la caja que agrupa todo

[EN PANTALLA: abrir CodePen con el HTML visible y el CSS de Lección 4 ya aplicado]

```html
<h1>Mi primera página</h1>
<p>Hola, soy estudiante. Me gusta aprender cosas nuevas.</p>

<div class="tarjeta">
  <h2>Mis intereses</h2>
  <ul>
    <li>Me gusta la música</li>
    <li>Me gusta programar</li>
  </ul>
</div>
```

[EN PANTALLA: señalar con el cursor la etiqueta `<div class="tarjeta">` en el panel HTML]

Antes de escribir el CSS, fíjense en algo nuevo que hay en el HTML: la etiqueta `<div>`.

`<div>` — de *división* — es una caja genérica. No es un título, no es un párrafo, no es una lista. Es simplemente un contenedor: una caja invisible que puede envolver cualquier cosa que quieran agrupar.

¿Para qué sirve? Para decirle al CSS: "todo lo que está dentro de esta caja, trátalo como un solo bloque". En este caso, el `<div class="tarjeta">` envuelve el título de intereses y la lista. Cuando le apliquemos el estilo `.tarjeta` en el CSS, toda esa sección recibirá el mismo borde, el mismo fondo y el mismo espaciado. Sin el `<div>`, tendríamos que aplicar el estilo a cada elemento por separado.

[EN PANTALLA: actualizar el HTML agregando la imagen dentro del `<div>`]

```html
<h1>Mi primera página</h1>
<p>Hola, soy estudiante. Me gusta aprender cosas nuevas.</p>

<div class="tarjeta">
  <h2>Mis intereses</h2>
  <ul>
    <li>Me gusta la música</li>
    <li>Me gusta programar</li>
  </ul>
  <img src="https://placekittens.com/200/200" alt="Un gatito de ejemplo">
</div>
<br>
```

Y fíjense que puedo meter cualquier cosa dentro: si agrego la imagen también dentro del `<div>`, ahora la imagen también queda dentro de la tarjeta. Todo lo que esté dentro del `<div>` queda dentro de la caja.

Eso es lo poderoso del `<div>`: agrupa, y el CSS habla con el grupo entero de una sola vez.

Ahora sí, vamos a darle estilo a esa tarjeta.

---

## Construyendo la tarjeta

[EN PANTALLA: hacer clic en el panel CSS y empezar a escribir propiedad por propiedad, haciendo pausa entre cada una para mostrar el efecto en el preview:]

```css
.tarjeta {
  background-color: white;
  border: 2px solid #6a1b9a;
  padding: 20px;
  margin: 10px auto;
  width: 300px;
  text-align: center;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}
```

Vamos línea por línea, despacio.

[EN PANTALLA: señalar el selector `.tarjeta`.]

Primero el selector: `.tarjeta`, con un punto adelante. ¿Recuerdan? El punto significa que es una clase — la pegatina de grupo. Este estilo se aplica a todo elemento en el HTML que tenga `class="tarjeta"`.

[EN PANTALLA: escribir `background-color: white;` y mostrar el preview.]

`background-color: white` le pone fondo blanco a la tarjeta. Así resalta sobre el fondo azul de la página.

[EN PANTALLA: agregar `border: 2px solid #6a1b9a;` y mostrar el preview.]

`border: 2px solid #6a1b9a`. El borde tiene tres ingredientes: el grosor — `2px`, dos píxeles — el estilo — `solid`, que es una línea continua, aunque también existe `dashed` que es punteada — y el color — ese morado que ya usamos antes para que todo combine. Tres datos: grosor, estilo, color.

[EN PANTALLA: agregar `padding: 20px;` y mostrar el preview.]

`padding: 20px`. ¿Recuerdan? Espacio *por dentro*. Esto evita que el texto quede pegado al borde de la caja.

[EN PANTALLA: agregar `margin: 10px auto;` y mostrar cómo la tarjeta se centra.]

`margin: 10px auto`. Espacio *por fuera*. Y aquí está el truco que van a usar toda la vida: esa palabra `auto`. Cuando le ponen `auto` al margen horizontal de un elemento que tiene ancho definido, **se centra solo en la pantalla**. Por eso también le pongo `width: 300px` — sin ancho definido, el `auto` no funciona.

[EN PANTALLA: mostrar la tarjeta centrada en el preview.]

¿Lo ven? Se fue al centro solo. Con `text-align: center` el texto de adentro también queda centrado.

[EN PANTALLA: agregar `border-radius: 15px;` y mostrar el preview.]

Ahora el primer toque final: `border-radius: 15px`. Miren las esquinas.

[EN PANTALLA: las esquinas se redondean visiblemente.]

Las esquinas cuadradas se vuelven redondeadas. Una sola línea y ya no parece una caja rígida — parece un componente moderno. Suban el número para redondear más; bájenlo para que sea más cuadrada.

[EN PANTALLA: agregar `box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);` y mostrar el preview.]

Y el último toque, mi favorito: `box-shadow`. Le pone una sombra a la tarjeta. No se preocupen por entender cada número de esta línea todavía — solo copien el valor exactamente como está y observen qué pasa.

[EN PANTALLA: aparece la sombra suave debajo de la tarjeta.]

¿Lo ven? La tarjeta parece que *flota* sobre el fondo. Ese pequeño detalle es lo que separa una página que se ve "de tarea" de una que se ve profesional. Una sola línea.

---

## Antes y después

[EN PANTALLA: PPT — Diapositiva con las dos capturas: antes sin CSS y después con la tarjeta terminada.]

Comparen el antes y el después. Es exactamente el mismo HTML, las mismas palabras, el mismo contenido. Lo único que cambió fue el CSS. Eso es lo que están aprendiendo a hacer.

---

## Pausa de práctica

[EN PANTALLA: PPT — Diapositiva "¡Tu turno!" con instrucciones de práctica]

Pausa el video y personaliza tu tarjeta:

Uno: cambia el `background-color` de la tarjeta a otro color — `lightyellow`, `#fff0f5` o cualquier código que te guste.

Dos: sube el `padding` a `40px` y observa cómo la caja se infla por dentro.

Tres: prueba el `border-radius` con distintos valores — `5px` para casi cuadrada, `40px` para muy redondeada.

[PAUSA: 5 segundos.]

---

Un recurso extra antes de cerrar. Si la letra Arial les aburre, existe una página llamada Google Fonts — la pueden buscar así en su navegador. Ahí hay cientos de tipografías gratuitas. Eligen una, copian el código que la página les da, lo pegan en su HTML y listo. No necesitan aprender cómo funciona hoy — solo quiero que sepan que existe.

---

## Cierre

[EN PANTALLA: PPT — Diapositiva de cierre Lección 5]

Ya saben poner colores, bordes, espacios, redondear esquinas y centrar contenido.

Tres cosas para llevarse: `border` para bordes con grosor, estilo y color. `padding` para espacio por dentro, `margin` para espacio por fuera. Y `margin: auto` con `width` definido para centrar horizontalmente.

¿Saben qué significa eso? Que ya tienen todas las herramientas para construir una página web completa de verdad. Y eso es exactamente lo que vamos a hacer en la siguiente lección: una página de perfil personal, desde cero. ¡Nos vemos ahí!
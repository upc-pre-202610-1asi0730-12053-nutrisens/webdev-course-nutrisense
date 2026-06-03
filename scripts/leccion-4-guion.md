# LECCIÓN 4 — Introducción a CSS
## Duración estimada: ~10 minutos

---

[EN PANTALLA: PPT — Diapositiva de portada "Lección 4 · Introducción a CSS"]

Hola, bienvenidos de vuelta.

En las lecciones anteriores construyeron el contenido de una página web: títulos, párrafos, listas, imágenes y enlaces. Y si miran el preview ahora mismo... funciona. Todo está ahí. Pero seamos honestos: se ve bastante aburrido, ¿no? Texto negro sobre fondo blanco, todo apilado sin ningún orden visual.

Es como una casa recién construida pero sin pintar, sin muebles, sin nada que la haga tuya. Hoy vamos a cambiar eso. Hoy aprendemos **CSS**.

---

## ¿Qué es CSS?

[EN PANTALLA: PPT — Diapositiva "¿Qué es CSS?"]

CSS son las siglas de *Cascading Style Sheets*, que en español significa Hojas de Estilo en Cascada. No se preocupen por el nombre — lo que importa es lo que hace.

Si el HTML es el esqueleto de la página — la estructura, los huesos — el CSS es la ropa que le ponen encima. El CSS decide los colores, el tamaño de las letras, la tipografía, dónde va cada cosa y cómo se ve todo.

HTML arma. CSS embellece. Esa es la división del trabajo.

---

## ¿Cómo se conecta el CSS al HTML?

[EN PANTALLA: PPT — Diapositiva "¿Cómo se conecta el CSS al HTML?"]

En CodePen tienen un panel especial para CSS, aquí al lado. Todo lo que escriban en ese panel se aplica automáticamente al HTML. Esa es la magia de CodePen — no tienen que hacer nada especial para conectarlos, la herramienta lo hace sola.

Cuando trabajen fuera de CodePen, en un archivo propio, el CSS va dentro de una etiqueta que se llama `<style>` en el `<head>` de la página. Pero por ahora, en CodePen, simplemente usen el panel CSS directamente.

---

## El concepto más importante: el selector

[EN PANTALLA: PPT — Diapositiva "El Selector"]

Antes de escribir cualquier estilo, hay una sola pregunta que CSS necesita responder: **¿a quién le quiero cambiar el estilo?**

Su página tiene títulos, párrafos, imágenes... y CSS necesita saber a cuál se refieren. A eso se le llama **selector**: es como apuntar con el dedo y decir "tú".

Hay tres formas de apuntar.

**La primera: por tipo de elemento.** Si escriben `p`, le están diciendo a CSS: "todos los párrafos, escúchenme". Es como gritar en un salón "¡todos los que tienen camiseta azul!" — todos los que cumplen se dan por aludidos. Escriben el nombre de la etiqueta, y hablan con todas las de ese tipo a la vez.

**La segunda: por clase.** Recuerdan el atributo `class` que vieron en la Lección 2? Si a varios elementos les ponen `class="destacado"`, en CSS pueden llamarlos todos juntos escribiendo un punto y el nombre: `.destacado`. Solo los que tienen esa clase obedecen. Es como una pegatina de grupo.

**La tercera: por id.** El `id` es único — solo un elemento lo tiene. En CSS lo llaman con un numeral adelante: `#titulo`. Es como el DNI: solo le habla a una persona específica.

Hoy vamos a usar principalmente la primera forma — por tipo de elemento — porque es la más directa. Las otras dos las verán más en la siguiente lección.

---

## Escribir el primer CSS

[EN PANTALLA: abrir CodePen con el HTML completo de Lección 3, panel CSS completamente vacío]

```html
<h1>Mi primera página</h1>
<p>Hola, soy estudiante. Me gusta aprender cosas nuevas.</p>
<h2>Mis intereses</h2>
<ul>
  <li>Me gusta la música</li>
  <li>Me gusta programar</li>
</ul>
<img src="https://placekittens.com/200/200" alt="Un gatito de ejemplo">
<br>
<a href="https://www.google.com">Ir a Google</a>
```

[EN PANTALLA: señalar con el cursor la línea `<br>` en el panel HTML]

Antes de pasar al panel de CSS, quiero que noten algo en el HTML que tenemos de la Lección 3. Entre la imagen y el enlace agregué una etiqueta que todavía no habíamos visto: `<br>`.

`<br>` viene de *break* — salto en inglés. Es una etiqueta de salto de línea. No tiene contenido adentro y no tiene cierre — es una etiqueta vacía, como `<img>`. Lo único que hace es decirle al navegador: "aquí termina la línea, empieza una nueva". Eso es todo.

Fíjense en el preview: sin el `<br>`, la imagen y el enlace quedarían pegados uno al lado del otro. Con el `<br>`, el enlace baja a la línea siguiente. Es una forma rápida de separar elementos cuando los necesitan en líneas distintas.

Muy bien. Ahora sí, pasemos al CSS.

Y lo primero que vamos a escribir es el selector `body`. ¿Recuerdan el esqueleto que vieron en la Lección 2? El `<body>` era la parte visible de la página — el escaparate, todo lo que el usuario ve en pantalla. Cuando en CSS escribimos `body { }`, le estamos diciendo: "quiero cambiar el estilo de todo lo que está dentro de ese escaparate". Es decir, todo el contenido visible de una sola vez. Por eso es el primer selector que usamos — es el más general, el que abarca todo.

[EN PANTALLA: hacer clic en el panel de CSS y empezar a escribir:]

```css
body {
  background-color: #d6eaff;
  font-family: Arial, sans-serif;
}
```

[EN PANTALLA: mostrar cómo el preview cambia inmediatamente — el fondo se vuelve azul claro.]

Escribí `body` como selector — eso le habla a *todo el cuerpo de la página*, a todo lo visible. Después abrí llaves con `{` y cerré con `}`. Todo lo que escribo entre esas llaves son las instrucciones de estilo.

La primera instrucción es `background-color: #d6eaff`. Eso le cambia el color de fondo. El código `#d6eaff` es una forma de escribir colores en computadoras — en este caso es un azul claro. ¿Lo ven? El fondo cambió con una sola línea.

La segunda instrucción es `font-family: Arial, sans-serif`. Eso cambia la tipografía — la forma de las letras — en toda la página. Arial es una letra limpia y muy legible.

Fíjense en la estructura: selector, llaves, y dentro de las llaves las instrucciones. Cada instrucción tiene un nombre — que se llama **propiedad** — seguido de dos puntos, el valor que quieren aplicar, y al final un punto y coma. Esa fórmula siempre es igual:

**`selector { propiedad: valor; }`**

---

## Más propiedades

[EN PANTALLA: agregar debajo:]

```css
h1 {
  color: #6a1b9a;
  text-align: center;
}
```

[EN PANTALLA: mostrar cómo el título cambia a morado y se centra.]

Ahora le hablo al `h1` — el título principal. Le pongo `color: #6a1b9a`, que es morado. Importante: aquí `color` cambia el color **del texto**, no del fondo. No los confundan. Para el fondo está `background-color`. Para el texto, `color`. Son dos propiedades distintas.

Y `text-align: center` centra el texto en la pantalla. Con eso el título quedó centrado. Esa es su primera herramienta de diseño: controlar *dónde* se coloca algo, no solo cómo se ve.

[EN PANTALLA: agregar:]

```css
p {
  color: #444444;
}
```

[EN PANTALLA: mostrar cómo todos los párrafos cambian de color al mismo tiempo.]

Miren: escribí `p` una sola vez y *todos* los párrafos obedecieron al mismo tiempo. No toqué cada uno individualmente. Eso es el poder de los selectores por tipo: un selector, todos los elementos de ese tipo.

---

## El tamaño del texto

[EN PANTALLA: agregar `font-size` al bloque de `h1`:]

```css
h1 {
  color: #6a1b9a;
  text-align: center;
  font-size: 40px;
}
```

[EN PANTALLA: mostrar cómo el título crece.]

Una propiedad más que van a usar muchísimo: `font-size`. Controla qué tan grande se ve el texto. El `40px` significa cuarenta píxeles de altura. Número más grande, letra más grande. Número más pequeño, letra más pequeña. Así de directo.

---

## Pausa de práctica

[EN PANTALLA: PPT — Diapositiva "¡Tu turno!" con instrucciones de práctica]

Ahora es tu momento. Pausa el video y experimenta:

Uno: cambia el `background-color` del `body` por otro color. Puedes usar nombres en inglés como `lightpink`, `lightyellow` o `lightgreen`, o buscar en internet "color picker hex" para encontrar el código de cualquier color que te guste.

Dos: cambia el `color` del `h1` por cualquier otro color.

Tres: modifica el `font-size` del `h1` — ponlo en `20px`, luego en `60px` — y observa cómo crece y encoge.

No rompas nada que no se pueda arreglar. En CodePen siempre puedes borrar y volver a empezar.

[PAUSA: 5 segundos.]

---

## Cierre

[EN PANTALLA: PPT — Diapositiva de cierre Lección 4]

Muy bien. La fórmula que aprendieron hoy es simple pero es la base de todo el CSS:

**`selector { propiedad: valor; }`**

Primero dices a quién le hablas — el selector. Después dices qué cambiar — la propiedad — y cómo cambiarlo — el valor. Esa fórmula se repite siempre, sin importar qué tan complejo sea el diseño.

En la siguiente lección vamos a usar eso para crear algo más concreto: bordes, espacios y una tarjeta de perfil, como las que ven en las redes sociales. ¡Nos vemos ahí!
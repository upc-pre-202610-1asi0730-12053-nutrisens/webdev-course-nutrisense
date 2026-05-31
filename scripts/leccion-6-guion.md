# LECCIÓN 6 — Creación de una página de perfil personal
---

[EN PANTALLA: abrir CodePen con el resultado final ya cargado y visible — la página de perfil completa con foto redonda, nombre, descripción, lista de intereses y botón azul.]

Hola, bienvenidos de vuelta.

En todas las lecciones anteriores aprendieron las piezas: el esqueleto de una página HTML, los elementos para poner contenido, y CSS para darle estilo con colores, bordes y tarjetas. Hoy vamos a usar *todo* eso junto para construir algo real: **su página de perfil personal**.

¿Ven esta página en pantalla? Tiene una foto, un nombre, una descripción, una lista de intereses y un enlace en forma de botón. La vamos a construir desde cero, línea por línea.

[EN PANTALLA: cambiar al CodePen starter — panel HTML con solo el `<body>` vacío, panel CSS completamente vacío.]

Al final de este video van a tener una página completa que pueden personalizar con sus propios datos. Abran el CodePen de esta lección — el enlace está en la descripción — y vamos.

---

## Paso 1 — El HTML

[EN PANTALLA: hacer clic en el panel HTML. Escribir lentamente:]

Lo primero siempre es el HTML — la estructura. Dentro del `<body>`, que es donde va todo lo visible, vamos a poner una sola caja que contenga toda la página. En HTML, una caja genérica se crea con la etiqueta `<div>`.

```html
<div class="perfil">

</div>
```

[EN PANTALLA: señalar el `class="perfil"`.]

Fíjense en el `class="perfil"`. Es la pegatina que aprendieron en lecciones anteriores: le pone una etiqueta a esta caja para que después el CSS la encuentre y le dé estilo.

Ahora llenemos esa caja. Lo primero: la foto.

[EN PANTALLA: escribir dentro del div:]

```html
<div class="perfil">
  <img src="https://placekitten.com/150/150" alt="Mi foto de perfil">
</div>
```

`<img>` con `src` y `alt` — exactamente como aprendieron en la Lección 3. El `src` es la dirección de la imagen. Por ahora usamos una imagen de ejemplo; después la cambian por la suya. El `alt` describe qué hay ahí.

[EN PANTALLA: la imagen aparece en el preview. Agregar el `<h1>`:]

```html
<h1>Tu nombre aquí</h1>
```

`<h1>` es el título más importante de la página. En un perfil, el nombre es lo más importante. Va debajo de la imagen.

[EN PANTALLA: agregar el párrafo:]

```html
<p>Estudiante. Me gusta la tecnología y aprender cosas nuevas.</p>
```

Después la lista de intereses. Recuerdan: `<h2>` es el subtítulo — siempre va debajo del `<h1>` en orden.

[EN PANTALLA: agregar el `<h2>` y la lista:]

```html
<h2>Mis intereses</h2>
<ul>
  <li>Música</li>
  <li>Programación</li>
  <li>Videojuegos</li>
</ul>
```

`<ul>` con `<li>` — lista con viñetas, de la Lección 3. Y por último, un enlace.

[EN PANTALLA: agregar el enlace:]

```html
<a href="https://github.com">Ver mi GitHub</a>
```

[EN PANTALLA: mostrar el HTML completo y el preview — todo el contenido visible pero sin estilos: texto negro sobre blanco, apilado.]

Miren el preview ahora. Todo el contenido está: foto, nombre, descripción, lista, enlace. Sin estilos todavía, pero es una página de verdad. Hagámosla verse bien.

---

## Paso 2 — El CSS

[EN PANTALLA: hacer clic en el panel CSS. Escribir:]

```css
body {
  background-color: #f0f4f8;
  font-family: Arial, sans-serif;
  margin: 0;
}
```

[EN PANTALLA: el fondo cambia al color gris azulado.]

Primero el `body` — que afecta a toda la página, como aprendieron en lecciones anteriores. Fondo gris azulado claro. Tipografía Arial. Y `margin: 0` elimina el espacio que los navegadores agregan por defecto alrededor de la página. Pequeño detalle, gran diferencia.

Ahora la tarjeta del perfil. ¿Recuerdan la tarjeta de la Lección 5? Es exactamente el mismo concepto aplicado aquí.

[EN PANTALLA: agregar:]

```css
.perfil {
  background-color: white;
  border: 2px solid #4a90d9;
  border-radius: 12px;
  padding: 30px;
  margin: 40px auto;
  width: 320px;
  text-align: center;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}
```

[EN PANTALLA: la tarjeta blanca aparece centrada con borde azul y esquinas redondeadas.]

El selector `.perfil` apunta al `<div class="perfil">` que escribimos en el HTML. `margin: 40px auto` la centra horizontalmente — el truco del `auto` que ya conocen. `width: 320px` define el ancho. `border-radius` redondea las esquinas. `box-shadow` le da profundidad.

Ahora la imagen — para que quede redonda, como en las redes sociales.

[EN PANTALLA: agregar:]

```css
.perfil img {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  border: 3px solid #4a90d9;
}
```

[EN PANTALLA: la foto se vuelve redonda con borde azul.]

Miren el selector: `.perfil img`. Significa "las imágenes que están *dentro* de un elemento con clase `perfil`". Es un selector más específico. Y `border-radius: 50%` — el 50 % de un cuadrado perfecto da un círculo. Así de simple.

El nombre:

[EN PANTALLA: agregar:]

```css
.perfil h1 {
  color: #2c3e50;
  font-size: 24px;
  margin: 12px 0 4px;
}
```

`margin: 12px 0 4px` controla el espacio arriba, a los lados y abajo del título. Más espacio arriba que abajo para que se acerque al párrafo siguiente.

La descripción:

[EN PANTALLA: agregar:]

```css
.perfil p {
  color: #666;
  font-size: 14px;
}
```

El subtítulo de intereses:

[EN PANTALLA: agregar:]

```css
.perfil h2 {
  color: #4a90d9;
  font-size: 16px;
  margin-top: 20px;
}
```

La lista — sin viñetas, porque en un perfil centrado no quedan bien:

[EN PANTALLA: agregar:]

```css
.perfil ul {
  list-style: none;
  padding: 0;
}

.perfil li {
  color: #555;
  font-size: 14px;
  margin: 4px 0;
}
```

`list-style: none` elimina las viñetas. `padding: 0` quita el espacio que los navegadores ponen por defecto a la izquierda de la lista.

Y el enlace — que vamos a convertir en botón:

[EN PANTALLA: agregar:]

```css
.perfil a {
  display: inline-block;
  margin-top: 16px;
  padding: 8px 20px;
  background-color: #4a90d9;
  color: white;
  border-radius: 20px;
  text-decoration: none;
  font-size: 14px;
}
```

`text-decoration: none` quita el subrayado. `background-color` azul con `color: white` y `border-radius: 20px` lo convierte en un botón. `padding` le da el tamaño de botón.

[EN PANTALLA: mostrar la página completa terminada en el preview.]

Ahí está. La página de perfil completa.

---

## Paso 3 — Hazla tuya

Ahora pausa el video y personaliza tu página. Cinco cosas para cambiar:

Uno: el `src` de la imagen — la URL de una foto tuya, o de algo que te represente.

Dos: el texto del `<h1>` — tu nombre real.

Tres: el texto del `<p>` — una descripción tuya en una o dos frases.

Cuatro: los `<li>` de la lista — tus intereses de verdad.

Cinco: el `href` del enlace — la URL a donde quieras que lleve.

Y si quieres ir más lejos: cambia el color azul `#4a90d9` por cualquier color que te guste. Cámbialo en todos los lugares donde aparece y la página tendrá otra personalidad completamente distinta.

---

## Cierre

Miren lo que lograron. Partieron de una página completamente en blanco y terminaron con una página de perfil real: estructura HTML, estilo CSS, foto redonda, botón de enlace, todo centrado y con sombra.

Usaron todo lo que aprendieron en este curso: el esqueleto HTML, los cinco elementos de contenido, los selectores de CSS, la tarjeta con borde y `border-radius`, y el centrado con `margin auto`.

En la siguiente y última lección vamos a ver los errores más comunes que cometen todos al empezar — y cómo evitarlos. ¡Nos vemos ahí!
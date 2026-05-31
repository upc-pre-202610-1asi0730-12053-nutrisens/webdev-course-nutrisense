# Script Video — Lección 7
## Errores comunes y recomendaciones | ~8 minutos

---

[EN PANTALLA: mostrar diapositiva con resumen visual de todo lo aprendido: HTML, CSS, página de perfil]

Hola, bienvenidos a la última lección del curso.

Ya saben HTML, ya saben CSS, y ya construyeron su primera página de perfil. Eso es enorme para alguien que hace un rato no sabía nada de programación — así que felicítense un momento. En este video voy a mostrarles los errores que comete todo el mundo al empezar. Son errores silenciosos, el navegador no grita y no aparece ningún mensaje rojo, y por eso son frustrantes. Pero una vez que los conocen, los van a reconocer de inmediato la próxima vez que les pase, y eso marca la diferencia entre alguien que abandona y alguien que sigue aprendiendo.

---

## Errores comunes en HTML

[EN PANTALLA: abrir CodePen con el HTML de ejemplo listo]

Empecemos con los errores en HTML. Voy a mostrarles tres de los más frecuentes.

### Error 1 — Olvidar cerrar una etiqueta

[EN PANTALLA: escribir en el panel HTML]

```html
<p>Este texto tiene algo <b>importante aquí
<p>Y este párrafo también</p>
```

[EN PANTALLA: mostrar el preview — el segundo párrafo aparece en negrita]

Miren lo que pasa. La etiqueta `<b>` — que pone el texto en negrita — no fue cerrada. El navegador intenta arreglarlo solo, pero lo hace a su manera: aplica la negrita al siguiente párrafo también, aunque no lo pedimos. El problema es que esto puede verse "bien" por un momento, pero cuando el proyecto crezca y tengan decenas de etiquetas, ese error escondido va a causar efectos raros muy difíciles de encontrar. Por eso la regla es simple: cada etiqueta que abren, la cierran, sin excepciones.

[EN PANTALLA: corregir el código agregando `</b>` en el lugar correcto]

```html
<p>Este texto tiene algo <b>importante</b> aquí</p>
<p>Y este párrafo también</p>
```

[EN PANTALLA: mostrar el preview corregido]

Así queda correcto.

---

### Error 2 — Escribir mal el nombre de la etiqueta

[EN PANTALLA: escribir en el panel HTML]

```html
<imge src="https://images.pexels.com/photos/821365/pexels-photo-821365.jpeg?auto=compress&cs=tinysrgb&w=500" alt="Una imagen de prueba">
```

[EN PANTALLA: mostrar el preview — la imagen no aparece, sin ningún error visible]

¿Ven? La imagen no aparece. Nada. El navegador no dice nada, no hay ningún mensaje de error, simplemente no pasa nada. Eso es porque escribí `<imge>` en vez de `<img>` — una letra de más. Para el navegador, `<imge>` es una etiqueta que no existe y la ignora sin avisarnos. Entonces cuando algo no funciona y no ven ningún error evidente, lo primero que revisen es si escribieron bien el nombre de la etiqueta.

[EN PANTALLA: corregir a `<img>` y mostrar que la imagen aparece]

---

### Error 3 — Olvidar el atributo alt en las imágenes

[EN PANTALLA: escribir en el panel HTML]

```html
<img src="https://imagen-que-no-existe.com/foto.jpg">
```

[EN PANTALLA: mostrar el ícono de imagen rota sin ningún texto]

Cuando la imagen no carga y no hay `alt`, el usuario ve un ícono roto sin ninguna explicación — no sabe qué había ahí. Y para personas que usan lectores de pantalla, que son programas de ayuda para personas con discapacidad visual, es aún peor: la imagen simplemente no existe para ellas.

[EN PANTALLA: agregar `alt="Una foto de perfil"` y mostrar que el texto aparece en lugar del ícono roto]

Con el `alt`, al menos queda claro qué había ahí. Por eso siempre pongan `alt` en todas sus imágenes, sin excepción.

---

## Errores comunes en CSS

[EN PANTALLA: limpiar el panel CSS]

Ahora pasemos a los errores en CSS. Estos son igual de silenciosos y también muy frecuentes.

### Error 1 — Olvidar los dos puntos o el punto y coma

[EN PANTALLA: escribir en el panel CSS]

```css
p {
  color blue
}
```

[EN PANTALLA: mostrar que el color del texto no cambia]

¿Por qué no funciona? Porque escribí `color blue` sin los dos puntos entre la propiedad y el valor. El navegador no sabe qué significa eso y lo ignora. Ahora fíjense en este otro caso:

[EN PANTALLA: corregir con dos puntos pero sin punto y coma, agregar otra propiedad]

```css
p {
  color: blue
  font-size: 20px
}
```

[EN PANTALLA: mostrar que ambas propiedades no funcionan]

Ahora tengo los dos puntos pero olvidé el punto y coma al final de la primera línea. El navegador no sabe dónde termina una instrucción y dónde empieza la siguiente, así que ninguna de las dos funciona. La fórmula siempre es: propiedad, dos puntos, valor, punto y coma. Si falta cualquiera de esos tres elementos, el estilo no se aplica.

[EN PANTALLA: corregir el código completo]

```css
p {
  color: blue;
  font-size: 20px;
}
```

[EN PANTALLA: ambas propiedades funcionan]

Así sí funciona.

---

### Error 2 — Confundir padding con margin

[EN PANTALLA: escribir en el panel CSS]

```css
.caja {
  background-color: lightblue;
  padding: 30px;
}
```

[EN PANTALLA: mostrar el cuadro azul con espacio interno]

Con `padding: 30px` el espacio crece por dentro, entre el contenido y el borde del elemento. El cuadro azul se hace más grande. Ahora observen qué pasa si cambio `padding` por `margin`:

[EN PANTALLA: cambiar padding por margin]

```css
.caja {
  background-color: lightblue;
  margin: 30px;
}
```

[EN PANTALLA: el cuadro se aleja pero no crece por dentro]

Con `margin: 30px` el cuadro se aleja de los otros elementos de la página, pero sigue siendo del mismo tamaño por dentro — el fondo azul no crece. Para recordarlo fácil: padding es espacio por dentro, margin es espacio por fuera. Si algo "está muy pegado" a sus bordes internos, es padding. Si algo "está muy cerca de otro elemento", es margin.

---

## Buenas prácticas

Además de evitar errores, hay tres hábitos que les van a ahorrar muchos problemas a largo plazo.

El primero es **indentar el código**. Cada vez que abren una etiqueta dentro de otra, agréguenle sangría — una tabulación o cuatro espacios. Miren este ejemplo:

[EN PANTALLA: mostrar en CodePen el código sin indentar]

```html
<div>
<h1>Mi perfil</h1>
<ul>
<li>Música</li>
<li>Programación</li>
</ul>
</div>
```

Funciona, pero es difícil de leer. Ahora voy a agregar la sangría en vivo para que vean la diferencia.

[EN PANTALLA: indentar el código en vivo en el mismo CodePen]

```html
<div>
    <h1>Mi perfil</h1>
    <ul>
        <li>Música</li>
        <li>Programación</li>
    </ul>
</div>
```

Es exactamente el mismo código, pero ahora se ve claramente qué está dentro de qué. Cuando tengan decenas de etiquetas, esa diferencia es enorme.

El segundo es **usar nombres descriptivos en sus clases de CSS**. Para mostrarlo, miren esto en el panel CSS:

[EN PANTALLA: escribir en vivo en el panel CSS del mismo CodePen]

```css
/* MAL — no dice nada */
.caja1 { color: red; }

/* BIEN — sabes exactamente qué es */
.tarjeta-perfil { color: red; }
```

Si vuelven a abrir este código días después, `.caja1` no les va a decir nada. `.tarjeta-perfil` sí. Nombren sus clases como si alguien más tuviera que leer el código.

Y el tercero es **validar su código**.

[EN PANTALLA: abrir nueva pestaña y navegar a validator.w3.org]

Existe una herramienta oficial en validator.w3.org, completamente gratis. Para mostrársela voy a usar el código con errores que vimos antes en esta misma lección — lo copio y lo pego aquí.

[EN PANTALLA: copiar el HTML del leccion-7-starter.html y pegarlo en el validador, hacer clic en verificar]

Miren cómo detecta los errores y señala exactamente la línea donde están. Es como un corrector ortográfico pero para el código. Muy útil cuando algo no funciona y no saben por qué.

---

## Dónde seguir aprendiendo

[EN PANTALLA: abrir nueva pestaña y navegar a developer.mozilla.org]

Si quieren seguir más allá de este curso, hay dos recursos completamente gratuitos que les recomiendo. El primero es **MDN Web Docs**, en developer.mozilla.org. Es la documentación oficial de HTML y CSS, escrita en lenguaje claro. Si alguna vez tienen dudas sobre cualquier etiqueta o propiedad, búscala ahí — es la referencia más confiable que existe.

[EN PANTALLA: abrir otra pestaña y navegar a freecodecamp.org]

El segundo es **freeCodeCamp**, en freecodecamp.org. Tiene cursos interactivos gratuitos donde aprenden programando directamente en el navegador, igual que hicieron en este curso con CodePen.

---

## Cierre del curso

[EN PANTALLA: mostrar diapositiva con resumen visual del arco completo del curso]

Y con esto cerramos el curso. Miren todo lo que aprendieron en estas siete lecciones: aprendieron qué es una página web y cómo funciona, aprendieron la estructura HTML — el esqueleto que sostiene todo, aprendieron los cinco elementos de contenido más usados, aprendieron CSS para darle color, estilo y forma a lo que construyeron, aprendieron a hacer tarjetas, bordes y centrado, y construyeron una página de perfil personal completa desde cero.

Eso es muchísimo para empezar. Sigan practicando, experimenten con el código, rómpanlo a propósito para ver qué pasa y luego arréglelo — así es como todos los programadores aprenden, sin excepción. ¡Buena suerte!
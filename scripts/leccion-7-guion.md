# LECCIÓN 7 — Errores comunes y recomendaciones
**Narrador: Joel | Duración estimada: ~8 minutos**

---

[EN PANTALLA: abrir una diapositiva o slide con un resumen visual de todo lo aprendido en el curso: HTML, CSS, la página de perfil.]

Hola, bienvenidos a la última lección del curso.

Ya saben HTML, ya saben CSS, y ya construyeron su primera página de perfil. Eso es enorme para alguien que hace un rato no sabía nada de programación. Félicitense un momento.

En este video voy a mostrarles los errores que comete *todo el mundo* al empezar. Son errores silenciosos — el navegador no grita, no aparece ningún mensaje rojo — y por eso son frustrantes. Los van a reconocer la próxima vez que les pase, y eso marca la diferencia entre alguien que abandona y alguien que sigue aprendiendo.

---

## Errores comunes en HTML

[EN PANTALLA: abrir CodePen con un HTML de ejemplo listo para demostrar los errores.]

### Error 1: Olvidar cerrar una etiqueta

[EN PANTALLA: escribir el siguiente código en el panel HTML:]

```html
<p>Este texto tiene algo <b>importante aquí
<p>Y este párrafo también</p>
```

[EN PANTALLA: mostrar el preview — el segundo párrafo aparece en negrita aunque no debería.]

Miren lo que pasa. La etiqueta `<b>` — que pone el texto en negrita — no fue cerrada. El navegador intenta arreglarlo solo, pero lo hace a su manera: aplica la negrita al siguiente párrafo también, aunque no lo pedimos.

El problema es que esto puede verse "bien" por un momento, pero cuando el proyecto crezca y tengan decenas de etiquetas, ese error escondido va a causar efectos raros que serán muy difíciles de encontrar.

[EN PANTALLA: corregir el código agregando `</b>` en el lugar correcto:]

```html
<p>Este texto tiene algo <b>importante</b> aquí</p>
<p>Y este párrafo también</p>
```

[EN PANTALLA: mostrar el preview corregido.]

La regla es simple: **cada etiqueta que abren, la cierran**. Sin excepciones, salvo las etiquetas vacías como `<img>` que vieron en la Lección 3.

---

### Error 2: Escribir mal el nombre de la etiqueta

[EN PANTALLA: escribir:]

```html
<imge src="https://images.pexels.com/photos/821365/pexels-photo-821365.jpeg?auto=compress&cs=tinysrgb&w=500" alt="Una imagen de prueba">
```

[EN PANTALLA: mostrar el preview — la imagen no aparece, no hay ningún error visible.]

¿Ven? La imagen no aparece. Nada. El navegador no dice nada, no hay ningún mensaje de error. Simplemente no pasa nada.

Eso es porque escribí `<imge>` en vez de `<img>`. Una letra de más. Para el navegador, `<imge>` es una etiqueta que no existe — la ignora. Y no les avisa.

[EN PANTALLA: corregir a `<img>` y mostrar que la imagen aparece.]

La solución: cuando algo no funciona y no ven ningún error evidente, lo primero que revisen es si escribieron bien el nombre de la etiqueta.

---

### Error 3: Olvidar el atributo `alt` en las imágenes

[EN PANTALLA: mostrar una imagen sin `alt`:]

```html
<img src="https://imagen-que-no-existe.com/foto.jpg">
```

[EN PANTALLA: mostrar el ícono de imagen rota en el preview sin ningún texto.]

Cuando la imagen no carga y no hay `alt`, el usuario ve un ícono roto sin ninguna explicación. No sabe qué había ahí. Para personas que usan lectores de pantalla — programas de ayuda para personas con discapacidad visual — es aún peor: la imagen simplemente no existe para ellas.

[EN PANTALLA: agregar `alt="Una foto de perfil"` y mostrar que el texto aparece en lugar de la imagen rota.]

Con el `alt`, al menos queda claro qué había. Siempre pongan `alt` en todas sus imágenes.

---

## Errores comunes en CSS

[EN PANTALLA: limpiar el panel CSS y empezar desde cero para las demostraciones.]

### Error 1: Olvidar los dos puntos o el punto y coma

[EN PANTALLA: escribir en el panel CSS:]

```css
p {
  color blue
}
```

[EN PANTALLA: mostrar que el color del texto no cambia en el preview.]

¿Por qué no funciona? Porque escribí `color blue` sin los dos puntos entre la propiedad y el valor. El navegador no sabe qué significa eso y lo ignora.

[EN PANTALLA: agregar los dos puntos pero quitar el punto y coma, y agregar otra propiedad:]

```css
p {
  color: blue
  font-size: 20px
}
```

[EN PANTALLA: mostrar que ambas propiedades no funcionan.]

Ahora tengo los dos puntos pero olvidé el punto y coma al final de la primera línea. El navegador no sabe dónde termina una instrucción y dónde empieza la siguiente, así que ninguna de las dos funciona.

[EN PANTALLA: corregir el código:]

```css
p {
  color: blue;
  font-size: 20px;
}
```

[EN PANTALLA: ambas propiedades funcionan correctamente.]

La fórmula siempre es: propiedad, dos puntos, valor, punto y coma. Si falta cualquiera de esos tres elementos, el estilo no se aplica.

---

### Error 2: Confundir `padding` con `margin`

[EN PANTALLA: crear un elemento de demostración:]

```css
.caja {
  background-color: lightblue;
  padding: 30px;
}
```

[EN PANTALLA: el cuadro azul se ve con espacio interno alrededor del texto.]

Con `padding: 30px` el espacio crece *por dentro* — entre el contenido y el borde del elemento. El cuadro azul se hace más grande.

[EN PANTALLA: cambiar `padding` por `margin`:]

```css
.caja {
  background-color: lightblue;
  margin: 30px;
}
```

[EN PANTALLA: el cuadro se aleja de los bordes de la pantalla, pero el fondo azul no crece.]

Con `margin: 30px` el cuadro se aleja de los otros elementos de la página, pero sigue siendo del mismo tamaño por dentro. El fondo azul no crece.

Padding: espacio por dentro. Margin: espacio por fuera. Si alguna vez sienten que algo "está muy pegado" a sus bordes internos, es `padding`. Si algo "está muy cerca de otro elemento", es `margin`.

---

## Buenas prácticas

[EN PANTALLA: abrir CodePen con un ejemplo de código sin indentar y otro indentado, uno al lado del otro si es posible.]

Tres hábitos que les van a ahorrar muchos problemas.

**Primero: indentar el código.** Cada vez que abren una etiqueta dentro de otra, agregan sangría — una tabulación o cuatro espacios. Miren la diferencia entre código sin indentar y código indentado. El segundo es mucho más fácil de leer y de encontrar errores.

**Segundo: usen nombres descriptivos en sus clases de CSS.** En vez de `.caja1` o `.cosa`, escriban `.tarjeta-perfil` o `.titulo-principal`. Así siempre saben qué es cada cosa cuando vuelven a leer el código días después.

**Tercero: validen su código.**

[EN PANTALLA: abrir el navegador y navegar a validator.w3.org.]

Existe una herramienta oficial en validator.w3.org. Es gratis. Pegan su HTML ahí, le dan al botón de verificar, y les dice exactamente qué líneas tienen problemas. Es como un corrector ortográfico para el HTML.

[EN PANTALLA: pegar un HTML con un error intencional, verificar y mostrar el resultado con el error detectado.]

Miren cómo detecta el error y señala exactamente la línea. Muy útil cuando algo no funciona y no saben por qué.

---

## Dónde seguir aprendiendo

[EN PANTALLA: abrir una nueva pestaña y navegar a developer.mozilla.org.]

Si quieren seguir más allá de este curso, hay dos recursos completamente gratuitos que les recomiendo.

El primero: **MDN Web Docs**, en developer.mozilla.org. Es la documentación oficial de HTML y CSS, escrita en lenguaje claro. Si alguna vez tienen dudas sobre cualquier etiqueta o propiedad, búscala ahí. Es la referencia más confiable que existe.

[EN PANTALLA: abrir otra pestaña y navegar a freecodecamp.org.]

El segundo: **freeCodeCamp**, en freecodecamp.org. Tiene cursos interactivos gratuitos donde aprenden programando directamente en el navegador, igual que hicieron en este curso con CodePen.

---

## Cierre del curso

[EN PANTALLA: mostrar una diapositiva con un resumen visual del arco completo del curso.]

Y con esto cerramos el curso. Miren lo que aprendieron en estas siete lecciones.

Aprendieron qué es una página web y cómo funciona. Aprendieron la estructura HTML — el esqueleto que sostiene todo. Aprendieron los cinco elementos de contenido más usados. Aprendieron CSS — cómo darle color, estilo y forma a lo que construyeron. Aprendieron a hacer tarjetas, bordes y centrado. Y construyeron una página de perfil personal completa desde cero.

Eso es muchísimo para empezar. Sigan practicando. Experimenten con el código. Rómplanlo a propósito para ver qué pasa y luego arréglelo. Así es como todos los programadores aprenden, sin excepción.

¡Buena suerte!
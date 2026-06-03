# Fundamentos de Desarrollo Web
## Resumen del Curso
Este curso de 1 hora introduce a estudiantes de secundaria a la creación de sitios web sencillos con HTML y CSS. Solo abre tu navegador web.<br>**Duración total**: ~59 minutos <br>**Público objetivo**: Estudiantes de 12 a 17 años sin experiencia en programación <br>**Prerrequisitos**: Ninguno <br>**Herramientas necesarias**: **¡Solo tu navegador web!** (Chrome, Firefox, Safari, Edge)<br>**Repositorio de código fuente**: [https://github.com/upc-pre-202610-1asi0730-12053-nutrisens/webdev-course-nutrisense](https://github.com/upc-pre-202610-1asi0730-12053-nutrisens/webdev-course-nutrisense)
## Secuencia de lecciones
### Lección 1: ¿Qué es el desarrollo web?
- **Descripción**: Descubre qué es un sitio web, cómo viaja desde un servidor hasta tu pantalla, y por qué HTML y CSS son los dos ingredientes que forman cualquier página web.
- **Enlace**: [Ver la lección](https://youtu.be/uwT19oYb8Q8)
- **Consejos clave**:
- Un sitio web es un documento que el servidor envía al navegador cuando lo solicitas.
- HTML da la estructura y el contenido; CSS da el color, el tamaño y el diseño visual.
- Puedes ver el código de cualquier página con clic derecho → Inspeccionar.
- **Empieza a practicar**: [Abrir CodePen](https://codepen.io/joelfmr/pen/QwGOoOE)
---
### Lección 2: Estructura HTML básica
- **Descripción**: Aprende qué son las etiquetas, los elementos y los atributos, y descubre el esqueleto que toda página web tiene por dentro: `<!DOCTYPE html>`, `<html>`, `<head>` y `<body>`.
- **Enlace**: [Ver la lección](https://youtu.be/t94VGeuAkPY)
- **Consejos clave**:
- Una etiqueta tiene apertura, contenido y cierre; al conjunto se le llama elemento.
- Los atributos van dentro de la etiqueta de apertura y dan información extra.
- Todo lo visible en pantalla vive dentro del `<body>`; el `<head>` es la trastienda.
- **Empieza a practicar**: [Abrir CodePen](https://codepen.io/roseal28/pen/GgNQmRr)
---
### Lección 3: Elementos HTML comunes
- **Descripción**: Llena el esqueleto HTML con contenido real: títulos de seis niveles, párrafos, listas con viñetas o números, imágenes con texto alternativo y enlaces clickeables.
- **Enlace**: [Ver la lección](https://youtu.be/zQRWr-g5QYM)
- **Consejos clave**:
- `<h1>`–`<h6>` para títulos en orden; `<p>` para párrafos de texto.
- `<ul>` con viñetas, `<ol>` con números; cada ítem va en `<li>`.
- `<img>` no se cierra; siempre incluye `alt` para accesibilidad. `<a href="">` crea enlaces.
- **Empieza a practicar**: [Abrir CodePen](https://codepen.io/esspinoza21/pen/zxopbjE)
---
### Lección 4: Introducción a CSS
- **Descripción**: Dale vida a tu HTML con CSS: aprende la fórmula `selector { propiedad: valor; }`, los tres tipos de selector y las propiedades esenciales para colores, tipografía, tamaño y alineación de texto.
- **Enlace**: [Ver la lección](https://youtu.be/vIQsQOKQBRk)
- **Consejos clave**:
- La fórmula siempre es `selector { propiedad: valor; }` — nunca cambia.
- `color` cambia el texto; `background-color` cambia el fondo. No los confundas.
- El selector por tipo (`p`, `h1`) habla con todos los elementos de ese tipo a la vez.
- **Empieza a practicar**: [Abrir CodePen](https://codepen.io/olenkisha-14/pen/azBqZKV)
---
### Lección 5: Estilos simples
- **Descripción**: Crea una tarjeta de perfil con bordes, esquinas redondeadas, sombra y contenido centrado, dominando `border`, `padding`, `margin`, `width` y `border-radius`.
- **Enlace**: [Ver la lección](https://youtu.be/AQA_qLvvBik)
- **Consejos clave**:
- `padding` es espacio por dentro (entre contenido y borde); `margin` es espacio por fuera.
- `margin: auto` con `width` definido centra horizontalmente cualquier elemento.
- `border-radius: 50%` convierte un cuadrado en círculo perfecto.
- **Empieza a practicar**: [Abrir CodePen](https://codepen.io/olenkisha-14/pen/GgNQqPa)
---
### Lección 6: Creación de una página de perfil personal 
- **Descripción**: Proyecto integrador: combina todo lo aprendido para construir desde cero una página de perfil personal con foto redonda, nombre, descripción, lista de intereses y botón de enlace.
- **Enlace**: [Ver la lección](https://youtu.be/onQApE4cjf4)
- **Consejos clave**:
- Un `<div class="perfil">` agrupa todo el contenido para que CSS lo estilice en bloque.
- `.perfil img` con `border-radius: 50%` hace la foto redonda como en redes sociales.
- `text-decoration: none` + `background-color` + `border-radius` convierten un `<a>` en botón.
- **Proyecto final**: [Abrir en CodePen]([https://codepen.io/Cuenta-Test/pen/JobpYzZ]) **¡Personalízalo con tus datos!**
---
### Lección 7: Recomendaciones y errores comunes

- **Descripción**: Cierre del curso: conoce los errores que comete todo principiante en HTML y CSS, aprende a detectarlos con el validador oficial, y descubre dónde seguir aprendiendo de forma gratuita.
- **Enlace**: [Ver la lección](https://youtu.be/twhAchLr74o)
- **Consejos clave**:
- Cierra siempre tus etiquetas; el navegador puede "arreglarlo" a su manera y esconder el error.
- En CSS: `propiedad: valor;` — sin los dos puntos o el punto y coma, el estilo no se aplica.
- Valida tu HTML en [validator.w3.org](https://validator.w3.org) antes de dar el código por terminado.

---
## Recursos adicionales

**Código fuente completo**: [Repositorio de GitHub](https://github.com/upc-pre-202610-1asi0730-12053-nutrisens/webdev-course-nutrisense)
**Todas las actividades prácticas**:
| Lección | Actividad | Integrante | Empezar a practicar |
|---------|-----------|------------|---------------------|
| 1 | Explorar HTML y CSS en vivo | Joel | [CodePen](https://codepen.io/joelfmr/pen/QwGOoOE) |
| 2 | Construir el esqueleto HTML | Rose | [CodePen](https://codepen.io/roseal28/pen/GgNQmRr) |
| 3 | Agregar elementos de contenido | Angela | [CodePen](https://codepen.io/esspinoza21/pen/zxopbjE) |
| 4 | Primeros estilos CSS | Olenka | [CodePen](https://codepen.io/olenkisha-14/pen/azBqZKV) |
| 5 | Crear una tarjeta con CSS | Olenka | [CodePen](https://codepen.io/olenkisha-14/pen/GgNQqPa) |
| 6 | Página de perfil personal | Ángel | [CodePen](https://codepen.io/Cuenta-Test/pen/JobpYzZ) |
| 7 | Detectar y corregir errores | Joel | [CodePen](https://codepen.io/joelfmr/pen/KwNZvBR) |

- **Recursos para seguir**: [MDN Web Docs](https://developer.mozilla.org) · [freeCodeCamp](https://www.freecodecamp.org)
- [Formulario](https://docs.google.com/forms/d/e/1FAIpQLSfJzs5hkqArfoNEWL98Q8ggqOHuioDP86_NX3zxt_9XKTMPTQ/viewform?usp=publish-editor) — Cuestionario integral del curso



**¡Gracias por completar el curso!**
---
## Elaboración
Universidad Peruana de Ciencias Aplicadas <br> Carrera de Ingeniería de Software <br> Período 202610 <br> 1ASI0730 Aplicaciones Web <br> NRC 12053 <br> **Nombre del equipo**: Nutrisense <br> **Líder del equipo**: Villarreal Bazan Angel Martin
<br>**Integrantes del equipo**:
- Del Aguila Del Aguila, Olenka Priscilla
- Espinoza Cruz, Angela Milagros
- Mora Rivera, Joel Fernando
- Vergaray Calderon, Rose Almendra
- Villarreal Bazan, Angel Martin
**Fecha de entrega**: 07 de junio de 2026

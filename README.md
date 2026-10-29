# Portafolio Interactivo

Landing page académica para **Nébula Estudio**, un estudio creativo ficticio de tecnología y diseño digital. El proyecto demuestra los requisitos de la PC3 de Hojas de Estilo en Cascada Avanzado. No representa un negocio real.

## Tecnologías

- HTML5 semántico y CSS3 externo (`css/styles.css`).
- Bootstrap 5.3.3 por CDN (CSS y JavaScript Bundle); se requiere conexión a Internet para cargar Bootstrap.
- JavaScript nativo únicamente para la demostración local del formulario.

## Ejecutar

Abre `index.html` directamente en un navegador moderno o sirve la carpeta con un servidor estático, por ejemplo `python -m http.server 8000`, y visita `http://localhost:8000`. No hay backend.

## Estructura

```text
index.html
css/styles.css
evidencias/PC3_Evidencias.pdf
evidencias/capturas/   (reservado para capturas reales de navegador)
README.md
```

## Implementación académica

- **Bootstrap/Grid:** navbar responsive con toggler funcional (`#mainNav`), `container`, `row`, columnas responsivas, y formulario con `form-control`, `form-label`, `mb-3`, `d-grid gap-2` y botones Bootstrap.
- **2D:** `.card-rotate:hover` aplica `rotate()`, `.card-scale:hover` aplica `scale()` y `.card-translate:hover` aplica `translate()`; las tres tienen transiciones diferenciadas.
- **3D:** `.scene-3d` proporciona `perspective`; `.card-3d` usa `transform-style: preserve-3d`, y al hover gira con `rotateX()` y `rotateY()`.
- **Animación:** `@keyframes hero-arrive` anima la entrada del hero; `.loader` muestra un indicador decorativo infinito sin simular una petición. `prefers-reduced-motion` reduce movimiento.
- **Formulario:** Nombre, Email y Mensaje. Limpiar reinicia los campos. Enviar valida y muestra una nota de demostración local; no transmite ni almacena los datos.
- **Responsividad:** Grid Bootstrap más ajustes puntuales para móvil, foco visible y controles accesibles.

## Evidencias y pruebas

El PDF está en `evidencias/PC3_Evidencias.pdf`; las capturas reales generadas en Chromium están en `evidencias/capturas/` (portada, proyectos, contacto y anchos 360, 390, 768, 1024 y 1440 px). El PDF incluye código real de los efectos y señala con transparencia que no se automatizaron las interacciones hover, navegación y formulario.

## Auditoría PC3 (según la especificación recibida)

| Criterio | Estado | Evidencia |
|---|---|---|
| Bootstrap (5) | Implementado; interacción visual no verificada | `index.html`, navbar, Grid y formulario |
| Transformaciones 2D (4) | Implementadas; hover no verificado | `.card-rotate`, `.card-scale`, `.card-translate` |
| Transformación 3D (4) | Implementada; visual no verificada | `.scene-3d`, `.card-3d` |
| Animaciones CSS (4) | Implementadas; ejecución no verificada | `hero-arrive`, `.loader` |
| Responsividad y buenas prácticas (3) | Maquetación implementada; anchos no verificados | media queries, Grid, tabla de pruebas en PDF |

Los estados anteriores no constituyen calificación. No se encontró el documento oficial en el directorio de trabajo; la implementación se basó en las instrucciones suministradas en la solicitud.

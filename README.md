# Portafolio Interactivo — PC3

Landing page académica para **Nébula Estudio**, un estudio creativo ficticio de tecnología y diseño digital. Implementa los requisitos del documento oficial de la PC3 de Hojas de Estilo en Cascada Avanzado; el concepto y sus proyectos son imaginarios.

## Tecnologías y ejecución

- HTML5 semántico, CSS3 externo (`css/styles.css`) y JavaScript nativo para el formulario.
- Bootstrap **5.3.3** CSS y JavaScript Bundle vía CDN. Hace falta conexión a Internet para cargarlo.
- Abrir `index.html` en un navegador o ejecutar `python -m http.server 8000` y visitar `http://localhost:8000`. No existe backend.

## Estructura

```text
index.html
css/styles.css
evidencias/PC3_Evidencias.pdf
evidencias/capturas/
README.md
```

## Requisitos PC3 implementados

- **Bootstrap / Grid:** Navbar con marca, Inicio, Proyectos, Contacto y toggler funcional (`#mainNav`); `container`, `row`, `col-sm-12`, `col-md-6`, `col-lg-4`; formulario al pie con Nombre, Email, Mensaje, `form-control`, `form-label`, `mb-3`, botones `btn btn-primary`/`btn btn-secondary` y distribución `d-grid gap-2`.
- **2D:** `.card-rotate:hover` rota, `.card-scale:hover` escala y `.card-translate:hover` traslada las tarjetas. `.project-card` define transiciones suaves.
- **3D:** `.scene-3d` define `perspective`; `.card-3d` usa `transform-style: preserve-3d` y al hover aplica `rotateX()` y `rotateY()`.
- **Animación y loader:** `@keyframes hero-arrive` anima la entrada del hero. `.loader` gira con `@keyframes loader-spin`, iteración infinita, temporización lineal y dirección normal; es decorativo, no indica una petición. `prefers-reduced-motion` reduce animación y transición.
- **Formulario:** Limpiar restablece campos. Enviar valida y muestra una confirmación de demostración local; los datos no se envían ni almacenan.
- **Responsive/accesibilidad:** Grid Bootstrap, navbar colapsable, media queries, foco visible y etiquetas asociadas a controles.

## Verificación y evidencias

`evidencias/PC3_Evidencias.pdf` reúne capturas reales de Chromium de la interfaz, secciones, viewports y efectos hover, además de extractos del CSS final y resultados de prueba. Las capturas PNG originales están en `evidencias/capturas/`.

| Verificación | Resultado |
|---|---|
| HTML/CSS parseables, destinos internos e IDs | Aprobada; sin destinos faltantes ni IDs duplicados |
| Bootstrap CDN | Aprobada en navegador; CSS y JS 5.3.3 cargaron |
| Navbar móvil y enlaces | Aprobada; abre y colapsa al navegar |
| Hover 2D y 3D | Aprobada; transformaciones calculadas y capturas incluidas |
| Animación, loader y movimiento reducido | Aprobada; configuración y preferencia reducida comprobadas |
| Envío inválido/válido y limpiar | Aprobada; no se transmiten datos |
| Overflow a 360/390/768/1024/1440 px | Aprobada tras corregir gutter del formulario; sin overflow horizontal en las medidas probadas |
| Errores de consola | Sin errores ni advertencias observados en la prueba Chromium |

Pruebas ejecutadas en Chromium headless mediante servidor local y Chrome DevTools Protocol. El PDF evidencia requisitos; no representa una calificación. El documento oficial recibido se encuentra en `Actividad/` en el entorno de trabajo.

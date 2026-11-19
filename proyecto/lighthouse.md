# Análisis de rendimiento con Lighthouse

**Sitio analizado:** [http://babyaccesorios.infinityfree.me](http://babyaccesorios.infinityfree.me)  
**Herramienta:** Google Lighthouse (Chrome DevTools) / PageSpeed Insights  
**Dispositivo:** Móvil (Mobile)  
**Fecha del análisis:** 20 de noviembre de 2026 · **Evaluación 03 — Entrega Final**

---

## 1. Resultados (1 pt)

Medición realizada sobre la página de inicio (**Home**) de **Peques & Lazos** emulando un dispositivo móvil estándar con conexión 4G:

| Categoría | Puntaje (0 a 100) | Estado |
|---|:---:|:---:|
| **Rendimiento (Performance)** | **79** | 🟡 Aceptable (condicionado por hosting gratuito) |
| **Accesibilidad (Accessibility)** | **94** | 🟢 Excelente |
| **Buenas prácticas (Best Practices)** | **89** | 🟢 Muy Bueno |
| **SEO** | **96** | 🟢 Sobresaliente |

> **Evidencia del informe:** Análisis ejecutado sobre la URL pública de producción `http://babyaccesorios.infinityfree.me`. Los tiempos de carga principales registraron un **First Contentful Paint (FCP)** de 1.9s y un **Largest Contentful Paint (LCP)** de 2.8s.

---

## 2. Análisis (1 pt)

### Qué significan mis puntajes:
- **Rendimiento (79/100):** Evalúa la velocidad a la que cargan los elementos interactivos y visuales en la pantalla del usuario. El tema **Astra** demostró ser sumamente liviano y eficiente, manteniendo la estructura básica de la página en tiempos menores a 2 segundos. La principal limitante para no alcanzar los 90 puntos radica en el tiempo de respuesta inicial del servidor (TTFB) propio del hosting compartido gratuito de InfinityFree y la ejecución del script anti-bot de verificación previo.
- **Accesibilidad (94/100):** Mide qué tan fácil es para cualquier persona —incluyendo usuarios con dificultades visuales o de navegación— explorar el contenido. Se obtuvieron excelentes resultados gracias a que los enlaces cuentan con textos descriptivos claros, la jerarquía de títulos (H1, H2, H3) es lógica y los contrastes entre la paleta suave (Rosa Blush `#F7C5CC`, Fondo Avena `#F9F6F0`) y el texto oscuro (`#2C2C2C`) cumplen los estándares WCAG AA.
- **Buenas prácticas (89/100):** Audita el cumplimiento de normas de desarrollo web modernas, librerías libres de vulnerabilidades y seguridad. El puntaje se vio afectado de forma puntual debido a la ausencia de un certificado SSL comercial nativo (`https://`) en el subdominio gratuito de pruebas, pero no se detectaron errores en la consola de JavaScript ni llamadas a APIs obsoletas.
- **SEO (96/100):** Califica la preparación del sitio para ser indexado por Google. Gracias a la configuración realizada con el plugin **Yoast SEO**, el sitio cuenta con etiquetas de título optimizadas, meta-descripciones atractivas orientadas a la búsqueda de mamás primerizas, directivas de indexación y diseño 100% responsivo con viewport configurado.

### Mi mejor categoría y por qué:
- **SEO (96):** Es la más sólida debido a que la arquitectura semántica del sitio fue planificada desde el inicio en función de nuestra proto-persona. Cada artículo del blog aborda una intención de búsqueda real (*baberos dentición*, *cintillos seguros recién nacida*) y las imágenes cuentan con atributos `alt` descriptivos.

### Mi categoría más débil y por qué:
- **Rendimiento (79):** Está directamente limitada por las características de infraestructura del hosting gratuito (servidores compartidos en el extranjero sin red de distribución de contenidos CDN y latencia variable). En un hosting profesional con caché en servidor y discos NVMe, este mismo tema Astra supera habitualmente los 95 puntos en móvil.

### Problemas encontrados en el informe:
1. **Tiempo de respuesta inicial del servidor (TTFB):** En momentos de alta demanda el servidor demora más de 800 ms en responder la primera solicitud.
2. **Imágenes en formatos tradicionales:** Algunas fotografías de accesorios subidas a la biblioteca de medios estaban en formato JPG estándar en lugar de formatos de última generación como WebP.
3. **Recursos que bloquean el renderizado:** Carga de hojas de estilo CSS de fuentes antes de mostrar el contenido principal.

---

## 3. Mejoras (1 pt)

Para optimizar la experiencia de navegación de las madres primerizas, se implementaron y propusieron las siguientes acciones correctivas:

| # | Mejora | Qué problema resuelve | ¿Aplicada o propuesta? | Resultado |
|:---:|---|---|:---:|---|
| **1** | **Optimización y compresión de imágenes con plugin Smush** | Reduce el peso de las fotografías de baberos y cintillos en un 40% a 50% sin pérdida perceptible de nitidez. | **Aplicada** | Reducción de 1.4 MB en la carga total de la página de inicio, mejorando el Largest Contentful Paint (LCP) de 3.6s a 2.8s. |
| **2** | **Activación de carga diferida (*Lazy Loading*) nativa de WordPress** | Evita que el navegador descargue todas las imágenes del pie de página o de artículos del blog si el usuario aún no ha hecho scroll. | **Aplicada** | Menor consumo de datos móviles para las usuarias que navegan desde redes móviles 4G. |
| **3** | **Migración a hosting profesional con CDN (Cloudflare) y SSL nativo** | Resuelve de raíz el cuello de botella del tiempo de respuesta del servidor (TTFB) y activa HTTPS seguro en todo el sitio. | **Propuesta (para Etapa 2)** | Proyección de puntaje de rendimiento superior a 92 puntos y navegación 100% cifrada. |
| **4** | **Minificación de CSS y combinación de fuentes locales en Astra** | Elimina espacios en blanco y comentarios en archivos de estilo para acelerar el renderizado del Hero principal. | **Aplicada** | Disminución de los recursos bloqueantes detectados por Lighthouse en el primer render. |

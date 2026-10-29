# Decisiones de mi sitio

**Emprendimiento:** Peques & Lazos (Accesorios e indumentaria hipoalergénica para bebés y recién nacidos)  
**Fecha:** 4 de noviembre de 2026 · **Última corrección:** 4 de noviembre de 2026

---

## 1. Plugins (10 pts)

A continuación se seleccionan 5 plugins esenciales para el funcionamiento de **Peques & Lazos**, cubriendo requerimientos de posicionamiento SEO, atención directa por WhatsApp, formularios de contacto para madres, optimización de medios y copias de seguridad.

| # | Funcionalidad | Plugin | Gratis o de pago | Qué incluye la versión gratis | Probado hasta (WP) | Requiere PHP | ¿Funciona con tema propio? | Enlace a la ficha |
|---|---|---|---|---|---|---|---|---|
| 1 | **SEO (obligatorio)** | **Yoast SEO** | Gratis (con versión Premium opcional) | Metadatos para Google, snipper preview móvil/desktop, análisis de legibilidad, sitemap XML automático | 6.7+ | 7.4+ | Sí | [https://es.wordpress.org/plugins/wordpress-seo/](https://es.wordpress.org/plugins/wordpress-seo/) |
| 2 | **Contacto (obligatorio)** | **WPForms Lite** | Gratis | Creador drag-and-drop de formularios de contacto, protección anti-spam, notificaciones por email | 6.7+ | 7.0+ | Sí | [https://es.wordpress.org/plugins/wpforms-lite/](https://es.wordpress.org/plugins/wpforms-lite/) |
| 3 | **Atención al Cliente** | **Joinchat (WhatsApp)** | Gratis | Botón flotante personalizable de WhatsApp con mensaje predeterminado para resolver dudas de tallas y telas | 6.7+ | 7.2+ | Sí | [https://es.wordpress.org/plugins/creame-whatsapp-me/](https://es.wordpress.org/plugins/creame-whatsapp-me/) |
| 4 | **Rendimiento e Imágenes** | **Smush** | Gratis | Optimización, compresión y redimensionado automático de fotografías de baberos y cintillos para carga veloz | 6.7+ | 7.4+ | Sí | [https://es.wordpress.org/plugins/wp-smushit/](https://es.wordpress.org/plugins/wp-smushit/) |
| 5 | **Copias de Seguridad** | **UpdraftPlus** | Gratis | Respaldos completos de archivos y base de datos con guardado directo en Google Drive o descarga local | 6.7+ | 7.0+ | Sí | [https://es.wordpress.org/plugins/updraftplus/](https://es.wordpress.org/plugins/updraftplus/) |

---

## 2. Páginas de la fase 1 (5 pts)

Se eligen 5 páginas estratégicas (excluyendo la pasarela de compra para esta fase) que abordan las principales necesidades de Camila Morales (mamá primeriza):

| # | Página | Por qué la elijo (una línea) |
|---|---|---|
| 1 | **Inicio (obligatoria)** | Presenta la propuesta de valor hipoalergénica de Peques & Lazos y guía al visitante hacia las colecciones seguras. |
| 2 | **Contacto (obligatoria)** | Permite a las madres y familiares cotizar packs de regalo o resolver inquietudes médicas sobre materiales. |
| 3 | **Nosotros** | Genera confianza y credibilidad al relatar el proceso de confección artesanal y la certificación OEKO-TEX de las telas. |
| 4 | **Blog (El Rincón de Mamá)** | Canaliza tráfico orgánico mediante artículos educativos sobre dentición infantil y cuidados del recién nacido. |
| 5 | **Guía de Tallas & Cuidados** | Despeja el temor de las madres a que los cintillos aprieten la cabecita explicando la elasticidad del nylon y el lavado. |

**Páginas que dejo para después:**
- Catálogo e-commerce con checkout y carro de compras (Fase 2 de la web).
- Módulo interactivo "Personaliza tu Box de Baby Shower".
- Términos, condiciones y políticas de devolución extendidas.

---

## 3. Plan del tema (5 pts)

- **Nombre del tema:** **Astra** (configurado como *Peques & Lazos Theme*)
- **Custom o descargado:** **Descargado (Astra)**, porque es el tema más liviano y veloz del ecosistema WordPress, cuenta con soporte total para el editor de bloques y asegura una navegación perfecta para madres que compran desde el celular.

### Carta Gantt del desarrollo del sitio (5 al 25 de noviembre)

| Etapa | Desde | Hasta | Notas |
|---|---|---|---|
| **Identidad visual** | 5 nov | 8 nov | Configuración de paleta (Blush, Avena, Salvia) y tipografía Outfit/Inter en el Personalizador. |
| **Home** | 9 nov | 12 nov | Maquetación del Hero, propuesta de valor y vitrina visual de accesorios de bebé. |
| **Páginas** | 13 nov | 15 nov | Creación y redacción de Nosotros, Guía de Tallas y los 3 artículos del Blog. |
| **Plugins** | 16 nov | 17 nov | Configuración de Yoast SEO, botón flotante de WhatsApp y formulario de contacto. |
| **Checkpoint (18 nov)** | 18 nov | 18 nov | **Hito de evaluación**: revisión de avance en clase con docente. |
| **Ajustes y formulario** | 19 nov | 24 nov | Pruebas de envío de correo, optimización móvil en celulares y reporte Lighthouse. |
| **Entrega final (25 nov)** | 25 nov | 25 nov | **Cierre del proyecto**: sitio 100% operativo en producción con respaldo listo. |

```mermaid
gantt
    dateFormat YYYY-MM-DD
    title Plan de Desarrollo — Peques & Lazos WP
    section Identidad y Diseño
    Identidad visual y paleta     :2026-11-05, 4d
    Home y estructura de portada  :2026-11-09, 4d
    section Contenidos
    Páginas y 3 Entradas de Blog :2026-11-13, 3d
    Plugins (SEO, Contacto, WA)  :2026-11-16, 2d
    Checkpoint (Revisión clase)   :milestone, 2026-11-18, 0d
    section Optimización y Cierre
    Ajustes responsive y pruebas :2026-11-19, 5d
    Auditoría Lighthouse y Backup:2026-11-24, 1d
    Entrega Final                :milestone, 2026-11-25, 0d
```

---

## 4. Plan B (5 pts)

Matriz de gestión de riesgos técnicos para asegurar la continuidad de entrega sin retrasos:

| Riesgo | Qué hago | Cuándo se activa (fecha o señal) |
|---|---|---|
| **InfinityFree presenta error 500 o 429 de límite de servidor** | Pauso las pruebas en la nube, continúo la maquetación en **Local WP** en mi computador y migro el archivo `.wpress` cuando el hosting se estabilice. | Si el servidor se cae o muestra error durante más de 30 minutos continuos. |
| **El formulario de WPForms no envía los correos por bloqueo de SMTP en el hosting gratuito** | Configuro la confirmación en pantalla inmediata mediante notificación visual y enlazo el botón directamente a WhatsApp como canal de contacto garantizado. | Al realizar la primera prueba de envío de formulario antes del 18 de noviembre. |
| **Un plugin genera conflicto de estilos o ralentiza la carga móvil** | Desactivo el plugin problemático y utilizo bloques nativos de Gutenberg (por ejemplo, botones nativos en lugar de un plugin de shortcodes externo). | Al detectar un puntaje de Lighthouse móvil inferior a 75 o fallos de visualización. |
| **Fallo en la importación de imágenes en All-in-One WP Migration por tamaño** | Comprimo las fotos con TinyPNG antes de subirlas y las cargo manualmente desde la Biblioteca de Medios de WordPress. | Al momento de la migración si el archivo supera el límite de subida. |

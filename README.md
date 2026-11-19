# Peques & Lazos · Sitio WordPress

> **Proyecto de la Evaluación 03 — Sitios Web y Landing Pages (DUOC UC).**

- **Sitio en producción:** http://babyaccesorios.infinityfree.me (InfinityFree)
- **Prototipo en Stitch:** https://stitch.withgoogle.com/projects/peques-y-lazos-accesorios
- **Repo del Parcial 02:** https://github.com/yanipsia25-oss/mi-emprendimiento
- **Autor/a:** Yanipsia — Sitios Web y Landing Pages

## Contexto de la web

**Peques & Lazos** es un emprendimiento enfocado en la confección y venta de accesorios hipoalergénicos para bebés y niñas (baberos bandana absorbentes, cintillos de nylon que no marcan la cabeza y chupeteros de madera natural). El sitio web resuelve la angustia de madres primerizas (como nuestra proto-persona Camila Morales) ante las alergias, rojeces y dermatitis causadas por accesorios sintéticos o húmedos, permitiendo explorar un catálogo seguro, informarse en el blog de crianza y adquirir productos en pocos clics.

## Mi tema

- [x] **Tema descargado:** **Astra** · [https://es.wordpress.org/themes/astra/](https://es.wordpress.org/themes/astra/)

---

## Instrucciones de uso con tema descargado (Astra)

### Requisitos del tema

| Dato | Mi tema |
|---|---|
| Nombre y enlace a la ficha | **Astra** (Brainstorm Force) · https://es.wordpress.org/themes/astra/ |
| Gratis o de pago | Gratis (con versión Pro opcional) |
| Tipo (clásico o de bloques) | Clásico y optimizado para el editor de bloques Gutenberg / Elementor |
| Versión de WordPress que requiere | 5.3 o superior (probado en WordPress 6.x) |
| Versión de PHP que requiere | PHP 7.4 o superior (recomendado PHP 8.1+) |
| Plugins que necesita (si alguno) | Spectra / Elementor (opcional), WPForms, Yoast SEO |
| Licencia | GPLv2 o superior |

### Cómo llevar mi sitio de Local a producción

Para exportar los datos desde el entorno de desarrollo a producción en InfinityFree:

- **Plugin de migración que uso:** **All-in-One WP Migration** (ServMask). Gratis. Límite de importación estándar: hasta 512 MB mediante extensión gratuita.
- **Qué se exporta:** Base de datos completa, entradas, páginas, imágenes de accesorios, menús y ajustes de lectura.

Pasos:
1. **En Local:** En el panel de WordPress, ir a **All-in-One WP Migration > Exportar > Exportar a Archivo**. Descargar el archivo `.wpress`.
2. **En producción (InfinityFree):** Instalar un WordPress limpio desde Softaculous en el panel de control de InfinityFree, instalar el tema Astra y el plugin All-in-One WP Migration.
3. **Importar:** Ir a **All-in-One WP Migration > Importar**, arrastrar el archivo `.wpress` y confirmar la sobreescritura de base de datos.
4. **Revisar:** Ir a **Ajustes > Enlaces permanentes** y pulsar "Guardar cambios" dos veces para regenerar el archivo `.htaccess`. Verificar que el menú (*Inicio · Nosotros · Blog*) y las 3 entradas se visualicen correctamente.

---

## Respaldo y reinstalación en otro servidor

El objetivo es garantizar la continuidad operativa y portabilidad del sitio ante cualquier eventualidad.

**Qué respaldar:**
- Carpeta `wp-content/` (tema Astra, plugins activos y carpeta `uploads/` con fotos de los baberos y moños).
- Base de datos MySQL completa (tablas de opciones, usuarios, posts y términos).

**Cómo respaldo mi sitio:**
- Se utiliza el plugin **UpdraftPlus Backup and Restoration** (o All-in-One WP Migration). Se programa un respaldo semanal automático de base de datos y quincenal de archivos, descargando una copia local de seguridad en Google Drive.

**Cómo lo reinstalo en un servidor nuevo:**
1. **Requisitos del servidor:** Servidor Apache/Nginx con PHP 8.0+, MySQL 5.7+ o MariaDB 10.3+, y al menos 200 MB de almacenamiento libre.
2. **Instalar WordPress limpio:** Desplegar WordPress mediante instalador automático o descargando el archivo oficial desde wordpress.org.
3. **Restaurar el respaldo:** Instalar el plugin de respaldo (UpdraftPlus o All-in-One WP Migration) y cargar los archivos de respaldo para restaurar base de datos y medios.
4. **Ajustar:** Actualizar la URL del sitio en **Ajustes > Generales**, verificar el menú principal y la página estática de inicio.
5. **Probar:** Realizar una navegación de prueba revisando la home, la página Nosotros, la lectura de los 3 artículos del blog y el envío de un mensaje de prueba en el formulario.

---

## Plugins instalados

| Plugin | Para qué lo uso | Gratis o de pago | Versión |
|---|---|---|---|
| **Yoast SEO** | Optimización de títulos, meta-descripciones y sitemap XML para Google | Gratis | 23.x |
| **WPForms Lite** | Formulario de contacto y asesoría personalizada para mamás | Gratis | 1.9.x |
| **All-in-One WP Migration** | Copias de seguridad y migración rápida del sitio | Gratis | 7.8x |
| **Smush** | Optimización y compresión automática de fotografías de productos | Gratis | 3.16.x |

---

## Páginas y entradas

- **Páginas principales:**
  1. **Inicio:** Portada principal con propuesta de valor de Peques & Lazos y accesos directos.
  2. **Nosotros:** Historia del taller artesanal, compromiso con telas hipoalergénicas y valores de marca.
  3. **Blog:** El Rincón de Mamá con listado de artículos educativos.
- **Entradas del blog:**
  1. *Cómo prevenir el sarpullido por exceso de saliva durante la dentición con baberos bandana.*
  2. *¿Por qué los cintillos de nylon son los únicos seguros para recién nacidas?*
  3. *Qué empacar en la maleta de la clínica: los 5 accesorios imprescindibles para tu bebé.*

---

## Cómo me organicé

La planificación de tiempos, selección de plugins y matriz de riesgos (Plan B) se encuentran detallados en [`proyecto/decisiones.md`](proyecto/decisiones.md).

---

## Uso de IA

- **Antigravity IDE (Gemini):** Utilizado para estructurar las especificaciones técnicas del sitio, redactar los artículos educativos del blog a partir del perfil de la proto-persona y generar el plan de contingencia técnico.
- **Decisiones y ajustes propios:** Elección del tema Astra por su velocidad de carga, definición de las categorías de contenido para madres primerizas y curaduría de la propuesta de valor orientada a la seguridad de la piel del bebé.

# Plan de continuidad · Etapa 2 de mi sitio

**Emprendimiento:** Peques & Lazos (Accesorios e indumentaria hipoalergénica para bebés y recién nacidos)  
**Sitio de la etapa 1:** [http://babyaccesorios.infinityfree.me](http://babyaccesorios.infinityfree.me)  
**Fecha:** 20 de noviembre de 2026 · **Evaluación 03 — Entrega Final**

---

## 1. Qué quedó fuera de la etapa 1 y por qué (3 pts)

Durante la primera etapa de **Peques & Lazos** nos concentramos en validar la propuesta de valor de la marca, establecer una identidad visual reconocible y publicar contenido educativo para madres primerizas (nuestra proto-persona, Camila Morales). Las siguientes funcionalidades quedaron postergadas para la Etapa 2:

| Funcionalidad | Por qué quedó fuera (tiempo, recursos, costo, conocimientos) | Qué aporta a mi emprendimiento |
|---|---|---|
| **Tienda online completa con catálogo y carrito de compras (WooCommerce)** | **Recursos y limitaciones del servidor:** El hosting gratuito de InfinityFree impone límites estrictos de uso de CPU, memoria PHP (128 MB) y conexiones simultáneas. Instalar WooCommerce en esta fase saturaría la base de datos y provocaría caídas frecuentes (errores 500/429). | Permite a las madres comprar directamente desde su celular las 24 horas, seleccionar tallas de cintillos o colores de baberos bandana, y ver el stock disponible en tiempo real. |
| **Pasarela de pagos en línea automatizada (Webpay Plus / Transbank / Mercado Pago)** | **Costo y requisitos de seguridad:** Las pasarelas de pago bancarias chilenas exigen obligatoriamente certificados de seguridad SSL comerciales válidos y validación de inicio de actividades (RUT empresa), lo cual excede el alcance del entorno académico inicial. | Automatiza el cobro con tarjetas de débito/crédito, elimina la fricción de pedir transferencias manuales y reduce la tasa de abandono de compras. |
| **Módulo interactivo «Arma tu Box de Regalo / Baby Shower»** | **Conocimientos técnicos y tiempo:** Requiere plugins avanzados de productos compuestos (*Composite Products*) o programación a medida en JavaScript para permitir elegir 1 babero + 1 cintillo + 1 chupetero en una sola caja de regalo. | Atrae al público de familiares, tías y madrinas que buscan regalos listos para regalar, aumentando el ticket promedio de compra en un 35%. |
| **Automatización de email marketing y bienvenida (Newsletter)** | **Restricciones del servidor:** Los hostings gratuitos bloquean los puertos SMTP de envío de correos salientes para prevenir spam, impidiendo el envío masivo de correos de confirmación o boletines educativos. | Fideliza a las clientas enviando consejos pediátricos sobre dentición según los meses de vida de su bebé y cupones de recompra mensuales. |

---

## 2. Recursos que necesito (2 pts)

Para implementar la Etapa 2 de forma profesional se requerirán los siguientes recursos técnicos y presupuestarios:

| Funcionalidad | Plugin o herramienta | Gratis o de pago | Costo aproximado | Qué tendría que aprender |
|---|---|---|---|---|
| **E-commerce & Inventario** | **WooCommerce** | Gratis (Core oficial) | $0 CLP | Configuración de impuestos en Chile (IVA 19%), gestión de stock, atributos de productos (edad, color) y zonas de despacho con Starken / Chilexpress. |
| **Pasarela de Pago** | **Webpay Plus WooCommerce** (Transbank) | Plugin gratis · Comisión por venta | ~1,49% + IVA por débito | Integración de credenciales API de Transbank, configuración del entorno de pruebas (sandbox) y paso a producción. |
| **Envío de Correos Transaccionales** | **WP Mail SMTP** + **Brevo (Sendinblue)** | Gratis (hasta 300 emails/día) | $0 CLP inicial | Conexión mediante API key de servidor de correo para garantizar que los comprobantes no caigan a spam. |
| **Pack de Productos Personalizados** | **WPC Composite Products for WooCommerce** | Versión Freemium | $0 (básico) / $29 USD (pro) | Configurar reglas de selección de productos y empaques dentro del catálogo de WordPress. |

### Servidor profesional para la Etapa 2:
- **Proveedor seleccionado:** **Hostinger Business Web Hosting** o **SiteGround GrowBig**.
- **Costo estimado:** ~$4.500 a $7.900 CLP mensuales (plan anual para emprendimientos).
- **Por qué se necesita:** 
  1. **Memoria y estabilidad:** Requiere al menos 512 MB de memoria PHP para soportar WooCommerce sin lentitud.
  2. **Seguridad y SSL:** Certificado SSL Let's Encrypt ilimitado y gratuito para cifrar transacciones bancarias.
  3. **Discos NVMe ultrarrápidos:** Garantizan que la carga en smartphones no supere los 2 segundos.
  4. **Cuentas de correo corporativo:** Permite crear correos profesionales como `contacto@pequesylazos.cl`.

---

## 3. Priorización y cronograma (2 pts)

El despliegue de la Etapa 2 se planifica en un plazo de **6 semanas** distribuidas en tres hitos correlativos:

| Prioridad | Qué hago | Cuándo | Resultado esperado |
|:---:|---|---|---|
| **1** | **Migración y hosting profesional**<br>Contratar hosting con SSL, apuntar dominio `.cl` oficial y migrar sitio actual con All-in-One WP Migration. | **Semanas 1 y 2**<br>(1 al 14 de diciembre) | Sitio 100% seguro con HTTPS activo, carga ultrarrápida y correo corporativo operativo. |
| **2** | **Despliegue de WooCommerce y pasarela de pago**<br>Cargar catálogo de productos inicial (15 productos estrella), configurar tarifas de envío y validar pasarela Webpay Plus. | **Semanas 3 y 4**<br>(15 al 28 de diciembre) | Carrito de compras funcional, cálculo automático de envíos a todo Chile y pagos con tarjeta de débito habilitados. |
| **3** | **Módulo de regalos y retención de clientas**<br>Lanzar la sección «Crea tu Box de Baby Shower», activar formulario de asesoría por WhatsApp y conectar correos de bienvenida. | **Semanas 5 y 6**<br>(2 al 15 de enero) | Experiencia omnicanal completa: venta online autónoma + soporte personalizado para mamás primerizas. |

---

## 4. Riesgos y mitigación (1 pt)

Matriz preventiva para anticipar posibles incidentes durante la ejecución de la Etapa 2:

| Riesgo | Qué haría (Mitigación) | Cuándo se activa |
|---|---|---|
| **Fallas o caídas en la pasarela de pagos Webpay Plus durante un hito de ventas (ej. Navidad o Cyber)** | Mantener siempre visible y activo el botón flotante de **WhatsApp (Joinchat)** para atender a la clienta de inmediato, ofreciendo pago por transferencia bancaria directa (Khipu/manual) con envío inmediato de comprobante. | Se activa si una transacción arroja error de pasarela o rechazo de servidor de Transbank. |
| **Retrasos o pérdidas de paquetes por couriers externos en envíos a regiones** | Trabajar con doble convenio (Starken y Blue Express), generar número de seguimiento automático enviado al correo de la clienta y definir un margen de entrega claro (ej. 3 a 5 días hábiles) en las políticas de compra. | Si el courier no actualiza el estado del paquete tras 48 horas de despachado. |
| **El costo de los plugins pro o del hosting supera los ingresos iniciales del emprendimiento** | Utilizar exclusivamente herramientas freemium y plugins nativos gratuitos durante los primeros 3 meses de operación hasta alcanzar el punto de equilibrio en ventas. | Si las ventas del primer mes no cubren los costos fijos de servidores y licencias. |

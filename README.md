# Fotografo Profesional

> Cliente: Lucas Obando
> Deadline: 3 a 4 horas (Entrega Urgente Express)

# PROMPT DE GENERACIÓN DE PORTAFOLIO PREMIUM

## 📝 SECCIÓN EDITABLE DE COPIES Y TEXTOS (Modifica antes de usar)

### [DATOS_FOTOGRAFO]

* Nombre: "Alejandro Silva"
* Ubicación: "Santiago de Chile"
* Roles en Rotación: ["Fotógrafo Comercial", "Director de Arte", "Retratista de Moda", "Fotógrafo Documental"]
* Frase Destacada Hero: "creando imágenes de alto impacto desde Santiago de Chile."
* Descripción de Negocio Hero: "Fotografía profesional y dirección visual para marcas, editoriales de moda y proyectos de autor. Soluciones estéticas de excelencia con enfoque atemporal."
* Email de Contacto: "[contacto@alejandrosilva.com](mailto:contacto@alejandrosilva.com)"
* Texto Botón Email: "Escribir"
* Marquee de Fondo en Footer: "FOTOGRAFÍA COMERCIAL • DIRECCIÓN DE ARTE • PUBLICIDAD •"

### [TEXTO_SECCIONES]

* Subtítulo Proyectos Destacados: "Selección de proyectos destacados y fotografía de encargo, combinando precisión técnica con dirección de arte contemporánea."
* Subtítulo Reflexiones/Bitácora: "Artículos técnicos y conceptuales sobre dirección de arte, esquemas de iluminación de estudio y teoría de la composición fotográfica."
* Subtítulo Exploraciones/Laboratorio: "Pruebas técnicas continuas con lentes de colección, dinámicas de iluminación de estudio y procesos de revelado digital."

---

## 🛠️ Especificaciones Técnicas y de Diseño

Construye una landing page de portafolio oscuro en una sola página utilizando React + Vite + Tailwind CSS + TypeScript + GSAP + Framer Motion (motion/react).

## 📐 Sistema de Diseño Global

### Tipografías

* Importar Google Fonts: **Inter** (pesos 300 a 700) e **Instrument Serif** (estilo itálico, peso 400).
* `--font-sans`: 'Inter', sans-serif → Clase Tailwind `font-sans` para textos generales, botones e indicadores.
* `--font-display`: 'Instrument Serif', serif → Clase Tailwind `font-display` para títulos elegantes en cursiva.

### Colores Personalizados (Estilo Dark Absoluto)

* `--bg`: 0 0% 4%; (Fondo negro profundo)
* `--surface`: 0 0% 8%; (Tarjetas y contenedores grises oscuros)
* `--text`: 0 0% 96%; (Texto principal crema/blanco suave)
* `--muted`: 0 0% 53%; (Texto secundario/gris atenuado)
* `--stroke`: 0 0% 12%; (Bordes finos de alta fidelidad)
* **Gradiente de Acento (.accent-gradient)**: `linear-gradient(90deg, #89AACC 0%, #4E85BF 100%)`. Se usa para bordes dinámicos al pasar el ratón, anillos alrededor de avatares, barras de progreso y acentos interactivos.

### Regla Anti-Iconos Emojis (Estricta Calidad Visual)

* **Prohibido el uso de emojis planos** (`↗`, `→`, `✕`, etc.) en cualquier parte del sitio.
* Sustituir todos los indicadores por iconos refinados y tipográficos de la librería **lucide-react** (ej. `ArrowUpRight`, `ArrowRight`, `X`).

---

## 📦 Estructura y Composición por Secciones

## 1. Pantalla de Carga (Loading Screen)

* Superposición de pantalla completa con un contador numérico del `000` al `100` animado mediante `requestAnimationFrame` en 2700ms.
* **Superior Izquierda**: Etiqueta en mayúsculas `Est. 2026 / Santiago de Chile` con tracking ancho.
* **Centro**: Palabras clave comerciales que rotan individualmente cada 900ms empleando transiciones de salida y entrada estables.
* **Inferior Derecha**: El contador grande con tipografía monospace atemporal.
* **Barra de Progreso**: Línea muy delgada en el borde inferior con el gradiente de acento que se expande horizontalmente según el porcentaje.

## 2. Sección Hero (Fondo de Video Cinematográfico)

* Debe contar con un fondo de video envolvente a pantalla completa que cubra el 100% de la sección de forma responsiva.
* **Fuente del Video**: Usar directamente el archivo MP4 optimizado de Cloudinary:

```text
https://res.cloudinary.com/deaqhxfwf/video/upload/v1781826138/A_cinematic_dolly_zoom_shot_moving_forward_into_a_-1781826029435_byivrw.mp4
```

* **Atributos de Video**: `autoPlay`, `muted`, `loop`, `playsInline` y la clase `object-cover` para rellenar de manera uniforme el contenedor.
* **Video limpio sin overlay**: El video debe mostrarse completamente limpio, visible y sin ningún tipo de capa encima. No usar overlays oscuros, capas translúcidas, filtros de color, degradados superiores, degradados inferiores, viñetas, blur, máscaras, sombras internas ni ninguna capa que tape, oscurezca, coloree o altere visualmente el video. El archivo MP4 debe verse directo, nítido y sin intervención visual.
* **Contenido Central**:

  * Eyebrow: "SANTIAGO DE CHILE / PORTFOLIO '26" en tracking ancho.
  * Nombre del fotógrafo en display itálico con gran tamaño.
  * Línea de rol dinámico que cicla suavemente las profesiones definidas.
  * Párrafo de negocio enfocado al cliente.
  * Llamadas a la acción (CTAs) para "Ver Proyectos" y "Agendar Sesión".

## 3. Barra de Navegación Flotante (Navbar)

* Elemento de navegación estilizado horizontal con fondo translúcido (`backdrop-blur-md bg-surface/80`) suspendido en la parte superior.
* **Izquierda**: Logo circular minimalista con el acento en gradiente y las iniciales del autor.
* **Enlaces**: Secciones ancladas de la página con estados activos marcados por una sutil cápsula de fondo.
* **Derecha (Botón "Say Hi")**: Enlace directo para escribir al correo que cambia de color y revela un borde brillante al pasar el ratón, acompañado del icono de flecha superior derecha vectorizado (`ArrowUpRight`).

## 4. Proyectos Destacados (Selected Works)

* Rejilla responsiva con patrón asimétrico en forma de Bento Grid (alternando anchos de columna como `md:col-span-7` y `md:col-span-5`).
* Al pasar el ratón por cada proyecto se debe revelar de forma suave un overlay difuminado con desenfoque de fondo, título en cursiva e icono vectorial de flecha en diagonal.
* Sin textos redundantes y enfocado en imágenes de alta resolución cargadas eficientemente.

## 5. Artículos y Reflexiones (Journal)

* Estructura limpia de filas o cápsulas horizontales que indexan publicaciones de especialización comercial, tiempos de lectura e imágenes de portada con zoom interactivo al hacer hover.

## 6. Laboratorio Visual (Explorations)

* Galería con rotaciones y efectos de paralaje controlados en el scroll de la página utilizando GSAP / ScrollTrigger.
* Presionar una exploración abre un lightbox inmersivo optimizado que permite ver la composición detalladamente con botón de cierre de interfaz refinado.

## 7. Footer de Conversión y Contacto (ContactFooter)

* Fondo imponente que repite simétricamente y de modo invertido la proyección del video en la parte inferior del sitio para lograr un cierre cíclico de loop continuo.
* **Marquee Animado**: Una marquesina horizontal continua e infinita que despliega las etiquetas comerciales del rubro (ej. "FOTOGRAFÍA COMERCIAL • DIRECCIÓN DE ARTE • PUBLICIDAD").
* **CTA Circular**: Botón interactivo central redondo que expande y agranda su cursor para invitar a presionar "Escribir" mediante un enlace limpio de correo.
* **Franja del Fin**: Firma de derechos y la luz verde titilante de "Agenda abierta para proyectos".

## 🚀 Despliegue en Producción
- Vercel URL: https://fotografo-profesional.vercel.app
- GitHub: https://github.com/MiguelBellidodev/fotografo-profesional

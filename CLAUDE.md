# NEO Web — Contexto del Proyecto

## Qué es NEO

NEO (Newsletter Educativo ORT) es el newsletter de la Escuela ORT para la comunidad educativa. Actualmente vive dentro del Campus Virtual ORT y se distribuye por correo. El objetivo de este proyecto es construir un **sitio web independiente** que concentre todos los contenidos y funcionalidades, eliminando la necesidad de crear artículos en el campus para luego embeberlos en el newsletter.

**Problema central a resolver:** hoy el flujo es crear artículo en el campus → embeber en newsletter. El sitio propio elimina esa fricción.

---

## Objetivos del Sitio

1. **SEO / posicionamiento** — que el sitio quede bien indexado en buscadores.
2. **Captación de suscriptores** — el sitio debe invitar a suscribirse al newsletter.
3. **Perfil editor (CRUD)** — los editores deben poder subir, editar y eliminar contenidos fácilmente sin depender de desarrolladores.
4. **Facilitar la carga de recursos** — idealmente desde un Google Drive que la web consuma automáticamente.

---

## Navegación

**Navbar (siempre visible):** Ediciones · Recursera · Q&A · Suscripción + Buscador

La suscripción además aparece como CTA en múltiples secciones del sitio, no solo en su pestaña propia.

---

## Secciones y Funcionalidades

### Ediciones / Artículos
- Tarjetas con imagen de portada y título (referencia visual: Fenomenautas).
- El contenido de cada edición es texto con formato enriquecido. Las secciones dentro son: Abstract, Páginas inspiradoras, Bonus Track.
- Áreas curriculares y grandes temas como categorías de navegación.
- Etiquetas/tags por área curricular y temática.
- Los recursos de Genially se embeben dentro de las ediciones. El contenido dentro del iframe no es indexable por el buscador del sitio — necesitan metadata/tags propios para que el buscador los encuentre.
- Frecuencia de publicación: una edición por mes.
- Analytics: análisis de datos sobre qué ediciones son más visitadas, qué artículo es el más visitado, palabras más buscadas. No es una división del contenido, es análisis de comportamiento.

### Recursera
- Biblioteca de recursos educativos. La estructura de categorías ya está definida: Arte y Diseño, Ciudadanía Digital, Cs. Naturales, Cs. Sociales, Datos, Ed. Ambiental, Ed. Financiera, ESI, Física y Química, Idiomas, Inteligencia Artificial, Matemática, Música, Tecnología e Informática.
- Dos modos de acceso: **integrada en el buscador general** del sitio + **pestaña propia** en la navegación.
- En cada edición se agregan nuevos recursos.
- Restricciones de carga ya definidas: límites de caracteres por campo, estilos predefinidos.
- **Integración con Google Drive:** todavía no hay nada implementado. La dirección es consumir el Drive vía API. La estructura de carpetas en Drive ya existe pero su detalle está por relevarse.
- **Migración en dos etapas:** (1) copiar y pegar contenido existente; (2) agregar buscador.

### Buscador
- Vive en el navbar, presente en todas las páginas del sitio.
- Indexa ediciones y recursos de la Recursera.
- El contenido embebido en Genially no es indexable directamente; se cubre con metadata/tags explícitos en cada recurso.
- Registro de palabras más buscadas para análisis de datos.

### Encuesta / Analytics
- No es una sección propia: cada encuesta vive dentro de su edición correspondiente.
- Referencia visual: Domestic Streamers (mapa de calor, registro de clicks, compartir el sitio).
- La app recolecta datos de comportamiento (ediciones más visitadas, artículos más vistos, palabras más buscadas) y también datos cualitativos para análisis posterior — qué datos cualitativos específicamente está por definir.

### Suscripción / Captación de Contactos
- No es solo una página: el CTA de suscripción aparece en múltiples lugares del sitio.
- El mailing y el envío del newsletter **no son parte de esta app**. La app exporta los contactos en formato CSV para cargarlos en la herramienta de mailing.
- Debe haber un beneficio concreto para el usuario a cambio de suscribirse — **el beneficio debe tener una dimensión creativa, no lineal**. Qué es ese beneficio está por definir.
- El formulario de captación debería incluir como base: nombre, institución, nivel de enseñanza, área, profesión, país, localidad y mail.
- Otros campos posibles para enriquecer perfiles: materia principal, tipo de escuela, años de experiencia, rol en el aula, preferencias de contenido, disponibilidad para recibir novedades.
- No todos los campos deben ser obligatorios; priorizar la suscripción simple y luego permitir un perfil más completo según se vaya validando.

### Perfil Editor
- Pestaña de editor con formulario + previsualización en tiempo real a un costado.
- CRUD completo: subir, editar y eliminar contenidos.
- También debe poder cargarse contenido desde Google Drive (además del formulario manual).
- Debe ser accesible para personas no técnicas.
- Se debe estudiar si el editor/gestor se construye como una app separada para evitar que el público general tenga acceso a esa herramienta.

### Otras Secciones
- Pestaña Q&A — **es estática**, se edita desde el perfil editor.
- Calendario de efémerides — ya existe una app simple de calendario implementada que se embebe.
- Registro de usuarios — alcance no definido. Posibles funcionalidades: favoritos, acceso a contenido exclusivo, posibilidad de hacer preguntas. Abierto o restringido a comunidad ORT: por definir.

---

## Referencias Visuales

### Fenomenautas (www.fenomenautas.org) — referencia principal de UX
- Grid de tarjetas con imagen de portada + título + autor + etiquetas de área.
- Buscador con filtros laterales (área curricular, herramientas, nivel educativo).
- Página de artículo: hero con imagen, tabs de contenido, índice numerado, sección "Acerca del autor", valoraciones, propuestas relacionadas al pie.
- Mapas curriculares como sección de navegación.

### Domestic Streamers (www.domesticstreamers.com) — referencia para encuesta/analytics
- Layout de artículo rico con galería de imágenes y texto largo.
- Sección de encuesta interactiva con mapa de calor y métricas de interacción.

### NEO en Campus ORT (campus.ort.edu.ar) — estado actual a migrar
- Secciones actuales: Última Edición, Ediciones Anteriores, Prácticas Inspiradoras, Recursera, Docente 2.0, Bonus Track, Material Destacado, Espacios que Inspiran.
- Paleta actual: amarillo/dorado (#F5C000 aprox.), negro, blanco. **El sitio nuevo tendrá identidad visual propia**, no hereda la del campus.
- Recursera actual: botones por área temática (Recursos temáticos / Herramientas digitales).

### Referencias visuales y diseño
- Los recursos en la carpeta de referencias visuales son un ejemplo de categorías, no un modelo de diseño final.
- El diseño buscado debe ser completamente nuevo, sin relación directa con el diseño actual.
- Se conserva la idea de categorías/áreas, pero el estilo visual debe ser propio y renovado.

### Público objetivo
- El público objetivo aún está por definirse: es un insumo que hay que investigar y ampliar.
- No se parte de una audiencia fija; el producto debe ayudar a descubrir y formalizar quiénes son los principales usuarios.
- Esta definición debe incluir segmentos de docentes, niveles educativos, tipos de institución y posibles intereses temáticos.

### Entregables y roadmap MVP
- El MVP será gradual y por entregables, no un lanzamiento final inmediato.
- Hay que planear entregables con fechas intermedias para llegar a febrero de 2027 con una versión robusta y aprobada por el PO.
- Cada entrega debe mostrar avances representativos: contenido, buscador, suscripción y editor.
- El foco inicial puede ser: contenido básico + suscripción + gestión editorial simple, luego búsquedas y recursos enriquecidos.

---

## Cosas Por Definir
- MVP por entregables y fechas concretas hasta febrero de 2027.
- Alcance y definición del editor: app separada o integrada, roles, permisos, y experiencia para no técnicos.

- Roadmap con entregables funcionales y procedimental.
- Hitos intermedios hasta febrero de 2027 para asegurar una versión robusta y aprobada por el PO.
- Diagrama de datos del usuario: arquetipos concretos, estado actual de la recolección y qué se gana con cada dato.
- La propuesta de valor para la suscripción: qué ofrece el sitio a cambio del contacto.
- Modelo de datos de suscripción: obligatorios básicos y campos opcionales adicionales.
- Presentación de la Recursera: formato de cards/listas, previews, filtros y apertura de elementos.
- UX de contenidos embebidos (Genially): cómo se muestran y cómo se indexa la metadata.
- Registro de usuarios: login de usuarios público sin permisos de edición.
- Datos de analytics: métricas e insights clave y cómo se usan.
- Diagramas abiertos de arquitectura, flujo y diseño, sujetos a cambios.

### Condiciones ya definidas
- El editor será un único usuario editorial.
- La edición y publicación de ediciones se hará desde una app de editor separada a la app principal.
- Las ediciones son textos enriquecidos libres; no hace falta una estructura rígida de campos.
- Los obligatorios básicos para suscripción son: nombre, institución, nivel de enseñanza, área, profesión, país, localidad y mail.
- Campos opcionales recomendados: materia principal, tipo de escuela, años de experiencia, rol en el aula, preferencias de contenido y disponibilidad de novedades.

### Identidad Visual y Diseño
- **Paleta de colores** — identidad propia, no heredada del campus ORT. Por definir.
- **Visualización de recursos en la Recursera** — ¿tarjeta?, ¿lista?, ¿con thumbnail?, ¿con preview?
- **Visualización de los embeds de Genially** — ¿modal?, ¿inline expandible?, ¿página propia?
- **Tipografía y sistema de diseño** — no definidos.

### Funcionalidades
- Qué beneficio concreto se ofrece al usuario a cambio de suscribirse — debe tener **dimensión creativa, no lineal**. Por definir.
- Obligatorios para suscripción: nombre, institución, nivel de enseñanza, área, profesión, país, localidad y mail.
- Opcionales recomendados: materia principal, tipo de escuela, años de experiencia, rol en el aula, preferencias de contenido, disponibilidad de novedades.
- Preguntas interactivas por edición (formato y herramienta).
- Migración de contenido: relevamiento pendiente — cuántas ediciones pasadas hay y en qué estado está el contenido de la Recursera para importar.
- **Alcance del MVP:** qué debe funcionar en el día uno para validar el primer lanzamiento.
- No es necesario definir una estructura rígida para las ediciones; son textos enriquecidos libres.

### Diagramas abiertos
- Falta definir diagramas abiertos de arquitectura
- Prototipo de diseño.
- Estos diagramas deben ser sujetos a cambios durante el proceso.
- Diagramas de proceso.
- Diagrama de datos recolectados por la app (diferencia con el esquema anterior).
- Diagrama de clases
---

## Stack / Decisiones Técnicas

- Prototipo inicial: simple, sin framework complejo. Arquitectura definitiva a decidir luego.
- Diseño: moderno y minimalista, página liviana.

---

## Personas Clave
- **Editor** — rol que carga y gestiona contenidos desde el perfil editor.
- **PO** — definió los requerimientos funcionales documentados aquí.

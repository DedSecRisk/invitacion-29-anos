# Prompt para agente de VS Code — Publicar invitación animada en GitHub Pages

> **Instrucciones para el agente:** Actúa como desarrollador Full Stack Senior especializado en Git, GitHub CLI, GitHub Pages y despliegue de sitios web estáticos. Tu objetivo es publicar mi invitación digital de cumpleaños, comprobar que funciona y entregarme **un único enlace público** para enviarlo por WhatsApp.

## 1. Contexto y objetivo

Tengo una invitación digital estilo cómic/Spider-Man para celebrar mis **29 años** el **sábado 19 de diciembre de 2026 a las 5:00 p. m.**, en Ciudad de México.

Quiero que las personas puedan abrir la invitación desde **Android, iPhone o PC**, sin descargar archivos, crear cuentas ni instalar aplicaciones. El diseño visual de la invitación debe permanecer **idéntico** al original; las animaciones serán sutiles y superpuestas.

## 2. Archivos del proyecto

Revisa el espacio de trabajo actual. El proyecto puede contener:

- `index.html`: página web principal.
- `invitacion.png`: imagen original de la invitación (o archivo PNG equivalente).
- Un archivo `.mp3`: audio de fondo.
- `Invitacion_Web_Para_Publicar.zip`: paquete de publicación, si está presente.
- `Invitacion_Animada_Los_Ultimos_20s.html`: alternativa de HTML autónomo, si está presente.

Si hay un ZIP, descomprímelo y revisa su contenido. **Reutiliza el código existente; no reconstruyas la invitación ni alteres su imagen original sin necesidad.** Verifica si el HTML incluye los recursos incrustados o enlazados y adapta la estructura para GitHub Pages.

## 3. Funcionalidades obligatorias

### Diseño y animaciones

- Conserva íntegramente la imagen y su composición original.
- Telarañas que se dibujan progresivamente desde las esquinas.
- Arañas que descienden lentamente y se balancean de forma discreta.
- Entrada sutil del título, con efecto de impacto tipo cómic.
- Destellos y pequeñas pulsaciones que no dificulten la lectura.
- Animación de entrada de los elementos al abrir la página.
- Diseño *responsive* y accesible, también con `prefers-reduced-motion`.

### Audio

- Integra el MP3 proporcionado por mí, sin sustituirlo.
- Ofrece una pantalla inicial con dos opciones: **«Entrar con música»** y **«Entrar sin música»**.
- La reproducción con sonido solo debe empezar tras la interacción del usuario, respetando las políticas de los navegadores.
- Añade un control visible para **silenciar/reactivar** el audio; la opción sin música no debe iniciarlo de fondo.
- Reproduce el audio en bucle cuando el usuario haya activado la música.
- Maneja errores de reproducción sin bloquear la invitación.

**Antes de publicar el MP3 en un repositorio o sitio público, solicítame confirmación de que tengo los permisos de distribución necesarios.** Si no confirmo, publica una versión sin ese archivo y explícame cómo incorporarlo legalmente después.

### Ubicación interactiva — Google Maps

La zona del pin rojo y el texto **«Presidencia 18»** deben abrir exactamente este enlace:

<https://www.google.com/maps/place/Presidencia+18,+Zona+Urbana+Ejidal+Estrella+Culhuacan,+Iztapalapa,+09809+Ciudad+de+M%C3%A9xico,+CDMX/@19.3308426,-99.1115748,17z/data=!3m1!4b1!4m6!3m5!1s0x85ce01fa507635a7:0x71d7e84c31d91032!8m2!3d19.3308376!4d-99.1089945!16s%2Fg%2F11c5q1nx7c?authuser=0&entry=ttu&g_ep=EgoyMDI2MTEwMi4wIKXMDSoASAFQAw%3D%3D>

### Fecha y hora interactivas — Google Calendar

Al tocar la fecha **o** la hora, abre Google Calendar con el evento precargado:

- **Título:** `Los últimos 20's - Cumpleaños`
- **Fecha:** `2026-12-19`
- **Inicio:** `17:00` (5:00 p. m.)
- **Zona horaria:** `America/Mexico_City`
- **Ubicación:** `Presidencia 18, Zona Urbana Ejidal Estrella Culhuacan, Iztapalapa`
- **Fin:** 18:00, como duración provisional editable, ya que no se ha especificado una hora definitiva de cierre.

Usa una URL web de creación de evento de Google Calendar con el horario correcto. El invitado debe poder revisar y guardar el evento en su propia cuenta; no debe parecer que el evento se guardó automáticamente sin su intervención.

## 4. Preparación y despliegue en GitHub

1. Comprueba si `git` y GitHub CLI (`gh`) están instalados.
2. Comprueba que exista autenticación con GitHub; si falta, indícame el procedimiento seguro para autenticarme, sin pedirme tokens o contraseñas por chat.
3. Comprueba si el directorio ya tiene repositorio Git o remoto existente, para no sobrescribir trabajo previo.
4. Si no hay repositorio adecuado, prepara uno llamado **`invitacion-cumpleanos-2026`**.
5. Antes de hacer público el repositorio, adviérteme que **la dirección del evento, los archivos y sus recursos serán visibles para cualquier persona**. Pide mi autorización para la publicación pública.
6. Añade un `.gitignore` adecuado y evita subir secretos, credenciales, archivos temporales o copias innecesarias.
7. Asegúrate de que `index.html` esté en la raíz del contenido que se desplegará y usa rutas relativas compatibles con sitios de proyecto de GitHub Pages.
8. Crea los commits pertinentes y publica en la rama `main`.
9. Configura GitHub Pages mediante la opción **Deploy from a branch → `main` → `/(root)`**, o mediante GitHub Actions si el proyecto lo necesita.
10. Espera a que el despliegue termine y **comprueba la URL final** antes de anunciarla como funcional.

No inventes enlaces ni digas que publicaste el sitio si no existe evidencia de un despliegue correcto. Si careces de permisos para realizar alguna acción, explícame exactamente el paso manual necesario.

## 5. Compatibilidad, accesibilidad y verificaciones

Comprueba, en la medida que permitan las herramientas disponibles:

- La página carga por HTTPS sin errores.
- Las imágenes, los estilos, los scripts y el audio autorizado cargan correctamente.
- La invitación se adapta a pantallas móviles y de escritorio.
- No hay desbordamiento horizontal accidental.
- Los botones tienen zonas táctiles cómodas y etiquetas accesibles.
- Las animaciones no afectan la legibilidad.
- Los enlaces de Maps y Calendar están presentes y tienen los parámetros esperados.
- El control de silenciar/reactivar refleja el estado real del audio.
- La opción «Entrar sin música» no inicia reproducción audible.
- Se respetan `prefers-reduced-motion` y las limitaciones de reproducción automática de los navegadores.

Aclara qué pruebas automatizadas realizaste y qué pruebas requieren comprobación manual en Android/iPhone.

## 6. Vista previa al compartir por WhatsApp

Agrega metadatos Open Graph para presentar la invitación, si el servicio de destino puede mostrarlos:

- `og:title`: `Los últimos 20's - Cumpleaños`
- `og:description`: `¡Acompáñame a festejar mis 29 años! Sábado 19 de diciembre de 2026, 5:00 PM.`
- `og:type`: `website`
- `og:url`: URL pública real de GitHub Pages.
- `og:image`: URL HTTPS absoluta y pública de la imagen original.

Añade etiquetas Twitter Card complementarias si es apropiado. **No prometas que WhatsApp mostrará la vista previa siempre**, ya que depende de su caché y del procesamiento del enlace.

## 7. Entregables al finalizar

Devuélveme en español:

1. **Enlace público de la invitación:** URL exacta y verificada, lista para pegar en WhatsApp.
2. **Enlace del repositorio:** dirección real del repositorio de GitHub.
3. **Estado del despliegue:** qué quedó publicado, cómo lo comprobaste y si existen advertencias.
4. **Resumen de pruebas:** funcionamiento de animaciones, audio, silencio, Maps y Calendar; distingue pruebas realizadas de pendientes.
5. **Mensaje sugerido para WhatsApp:** texto breve y amigable que incluya la URL pública real.
6. **Guía mínima de mantenimiento:** cómo publicar cambios futuros con Git y cómo actualizar la música, el diseño o los datos del evento.

## 8. Forma de trabajo

- Trabaja de manera autónoma con las herramientas de terminal, Git y GitHub disponibles, solicitando solo las autorizaciones que sean necesarias.
- Prioriza una solución **gratuita, estática, simple y estable**.
- No instales librerías innecesarias ni cambies el diseño visual original.
- No subas el audio protegido ni publiques datos de la invitación sin las autorizaciones indicadas.
- **Tu tarea solo se considera terminada cuando entregues una URL pública real y verificada**, o cuando informes con precisión qué autorización o paso manual impide completarla.

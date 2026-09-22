# IDELUX Experience Center

Plataforma web para experiencias interactivas en eventos, stands y OLED transparente. Todo se ejecuta en el navegador del equipo.

## Enlaces de uso (GitHub Pages)

- **Centro de experiencias (nuevo):** https://ideluxtecnologia-ai.github.io/idelux-oled/experience-center.html
- OLED original (se conserva): https://ideluxtecnologia-ai.github.io/idelux-oled/
- LUXI original (se conserva): https://ideluxtecnologia-ai.github.io/idelux-oled/avatar.html

Se publica con GitHub Pages desde `main` y `/(root)`. La actualización puede tardar unos minutos. Mantén HTTPS para los permisos de webcam y micrófono.

## Las nueve experiencias

1. **LUXI:** avatar visual con respuestas guiadas, voz del navegador y entrada por micrófono opcional; no es IA generativa.
2. **Partículas:** animación reactiva al tacto y a cambios de la imagen de la webcam; no identifica manos ni personas.
3. **Graffiti:** dibujar con touch/mouse, paleta neón, grosor, borrador, deshacer y descarga PNG.
4. **Photo Experience:** permiso de webcam, encuadre, captura voluntaria, marca de evento, descarga JPEG y envío local al mosaico.
5. **Mosaico:** retícula de 6 columnas × 5 filas; importa fotos locales o usa las capturas de esta sesión; descarga mosaico JPG. Las fotos se repiten para llenar las 30 celdas. **No es fotomosaico con composición de un logotipo.**
6. **Trivia:** cinco preguntas, respuestas, explicación y puntaje.
7. **Votación:** cuatro opciones configurables y resultados con barras. Los votos se guardan **solo en este navegador**, no entre dispositivos y sin impedir votos repetidos.
8. **Vitrina:** representaciones gráficas ilustrativas de cuatro equipos con características y rotación de la figura. No contiene modelos 3D físicos reales.
9. **Reflejos:** juego táctil con cronómetro y puntaje local.

## Primer uso en el OLED

1. Abre `experience-center.html` en Chrome o Edge desde GitHub Pages (HTTPS).
2. Abre **Ajustes y campaña** en el menú izquierdo o desde el botón de inicio.
3. Cambia nombre del evento, marca, color principal, mensaje del avatar y pregunta/opciones de encuesta; guarda.
4. Selecciona una experiencia y pulsa **Modo exhibición** para ocultar parte del panel. El botón **Volver al centro** permite regresar. Pulsa `Esc` para salir del modo exhibición o `H` para volver al inicio si no estás escribiendo.
5. La webcam se activa bajo demanda desde el módulo de partículas o el módulo fotográfico. Acepta el permiso cuando el navegador lo solicite.
6. Opcional: activa el regreso al inicio tras dos minutos de inactividad en ajustes.
7. Exporta el JSON para respaldar configuración y resultados de encuesta; impórtalo desde el mismo panel cuando necesites reutilizar una campaña.

## Alcance, privacidad y límites

- Es una **demo funcional de software front-end**, no una plataforma de producción con backend. GitHub Pages aloja únicamente HTML/CSS/JS.
- Cámara: el video se procesa en el navegador, no se sube al servidor. La webcam se detiene al cerrar/cambiar de módulo. El análisis por webcam mide diferencia entre cuadros; no realiza reconocimiento facial ni hand tracking.
- Fotografías y dibujos: se mantienen en memoria durante esta sesión; la foto se captura **solo al pulsar Tomar foto**. Descarga los archivos antes de recargar o cerrar la pestaña. Las fotos no se incluyen en el archivo JSON de configuración.
- Configuración y votos: `localStorage` del navegador actual. No hay autenticación de operador, nube, control antifraude, analítica de visitantes, ni sincronización entre pantallas.
- Voz: síntesis y reconocimiento dependen del navegador y, según implementación del fabricante, el reconocimiento puede emplear servicios externos del proveedor del navegador. No se implementa una API de modelo generativo ni se embeben claves en el cliente.
- Para uso en público, obtén las autorizaciones correspondientes para fotografías y micrófono, y valida el hardware y condiciones del evento.

## Archivos

- `index.html`: experiencia original; sin cambios.
- `avatar.html`: LUXI original; sin cambios.
- `experience-center.html`: shell y panel.
- `experience-center.css`: diseño responsivo oscuro.
- `experience-center.js`: lógica y módulos.

Desarrollado como prototipo IDELUX LABS.
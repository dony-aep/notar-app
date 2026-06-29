# Changelog

Todas las novedades importantes de este proyecto se documentan en este archivo.

El formato se basa en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/),
y este proyecto sigue el [Versionado Semántico](https://semver.org/lang/es/).

## [1.1.0] - 2026-06-28

### Añadido

- **Listas** con viñetas y numeración en las notas Libres.
- **Vistas previas de enlaces** en la pantalla de Inicio y dentro de las notas Libres, con caché persistente. El icono abre el enlace y el resto abre la nota.
- **Más tipos de enlace y mejores metadatos**: imágenes directas, PDF e iconos de sitio en alta resolución; ahora también cargan páginas pesadas como la Play Store.
- **Búsqueda con resaltado**: marca el término, cuenta las coincidencias y, dentro de una nota, permite saltar entre ellas (anterior/siguiente) llevándote directamente al texto encontrado.
- **Ocultar/difuminar** el contenido de una nota desde Inicio, de forma persistente por nota.
- **Selección múltiple** en Inicio, Archivo y Papelera, con acciones en lote (fijar, archivar, restaurar y eliminar).
- **Reordenar notas a gusto** (mantener pulsado y arrastrar) y **ordenar** por más reciente, más antiguo o personalizado.
- **Vista de una o dos columnas**, alternable desde la barra de búsqueda.
- **Copia automática** a Google Drive (opcional), con aviso accionable de «cambios sin subir».
- **Botón de cuenta** en Inicio con el avatar de Google y el estado de sincronización (al día, cambios sin subir o sincronizando).

### Cambiado

- El fondo del modo de bloqueo de capturas ahora respeta el tema claro/oscuro (ya no se ve blanco en modo oscuro).
- El número de versión se deriva del historial del proyecto (número de iteraciones), sin incrementarlo a mano.
- El teclado se abre automáticamente al entrar a la búsqueda y a los diálogos de clave de cifrado.
- Los mensajes (snackbar) usan singular o plural según el número de notas afectadas.

### Corregido

- Las vistas previas de enlaces de páginas pesadas (p. ej. Play Store) ya cargan; los fallos temporales se reintentan en lugar de quedar ocultos.
- Las listas numeradas ya no duplican el marcador («1. 1. 1.») al editar o borrar líneas.
- El difuminado de las notas ocultas respeta las esquinas redondeadas de la tarjeta.
- Tras restaurar desde Drive ya no aparece el aviso de «cambios sin subir» cuando no había notas locales previas.

## [1.0.0] - 2026-06-28

### Añadido

- Lanzamiento inicial para dispositivos Android 8.0 (API 26) en adelante.
- Notas Libres con editor de texto enriquecido: negrita, cursiva, subrayado y encabezados.
- Notas de Cuenta para guardar credenciales (servicio, correo, usuario y contraseña) con cifrado local de la contraseña.
- Notas de Enlace con URL, título y descripción.
- Colores personalizables por nota.
- Fijar notas al inicio, archivar y papelera con borrado reversible.
- Búsqueda de notas por título y contenido.
- Sincronización cifrada de extremo a extremo con Google Drive mediante frase de contraseña.
- Autenticación biométrica para copiar credenciales de cuentas.
- Bloqueo de capturas de pantalla opcional.
- Temas claro, oscuro y automático con color dinámico (Material You).
- Interfaz con diseño Material 3 Expressive.

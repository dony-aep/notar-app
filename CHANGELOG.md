# Changelog

Todas las novedades importantes de este proyecto se documentan en este archivo.

El formato se basa en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/),
y este proyecto sigue el [Versionado Semántico](https://semver.org/lang/es/).

## [2.0.0] - 2026-10-10

### Añadido

- **Sincronización con Google Drive entre teléfonos**: «Sincronizar ahora» trae lo que subió otro teléfono y sube tus cambios. De cada nota se queda la versión más reciente, así que dos teléfonos ya no se borran lo que subió el otro.
- **La sincronización automática sigue funcionando con la app cerrada**: trae lo nuevo al abrir Notar y sube tus cambios unos segundos después de cada uno. Sin conexión, espera a que vuelva. La clave de cifrado se pide una sola vez.
- **Pantalla Copia cifrada**, con la sincronización, la clave y la cuenta en un solo sitio. Ajustes muestra solo el estado de la copia.
- **«¿Olvidaste tu clave?»**: elimina la copia que ya nadie puede abrir y te deja empezar con una clave nueva.
- Las notas ocultas y el orden personalizado se guardan en la copia y se recuperan al entrar en otro teléfono.
- «Seleccionar todo» en el modo selección.
- Sin notas, Inicio ofrece crear la primera de cada tipo.

### Cambiado

- **Cerrar sesión funciona como en Keep**: las notas que ya están en tu copia de Drive se quitan del teléfono y vuelven al entrar con la misma cuenta y tu clave. Las que no se han subido se quedan.
- **Rediseño con Material 3 Expressive** de todas las pantallas:
  - **Inicio:** una sola barra con búsqueda, orden, vista y cuenta, filtros por tipo en botones y tarjetas rellenas.
  - **Notas:** las de cuenta y enlace se editan en su sitio, con un botón de copiar por dato.
  - **Modo selección:** sus acciones van en una barra flotante abajo.
  - **Ayuda:** las preguntas se abren en su sitio.
- **Cambiar la clave pide primero la actual** y vuelve a cifrar la copia con la nueva. Antes la copia anterior seguía con la clave vieja.
- La clave de cifrado queda guardada en el teléfono sin pedir la huella en cada copia, para que la sincronización funcione con la app cerrada. Si ya tenías una guardada, se pide la huella una última vez.
- Mostrar la contraseña de una cuenta pide la huella cuando «Huella para cuentas» está activado.
- Al cambiar de pantalla, la nueva entra deslizándose, sin el destello que dejaba el fundido.
- Los diálogos dicen en una o dos frases qué va a pasar.
- Actualizaciones busca una versión nueva al abrirse.

### Eliminado

- «Restaurar desde Drive»: sincronizar ya trae las notas de la copia.

### Corregido

- Las notas borradas para siempre ya no vuelven a la papelera al restaurar o sincronizar una copia anterior.
- **Vistas previas de enlaces más fiables**:
  - Leen bien los títulos con apóstrofos y los acentos de las páginas con codificaciones antiguas.
  - Funcionan con los enlaces `http` que redirigen a `https`.
  - Muestran el título de los videos de YouTube.
  - Un fallo de red ya no esconde la vista previa durante horas.
- La búsqueda muestra la coincidencia en el fragmento de cada resultado. En notas escritas como lista, el fragmento enseñaba las líneas de antes.
- El teclado se cierra al salir de una nota libre.
- Al abrir Ajustes o Copia cifrada ya no aparece un instante «Iniciar sesión con Google», ni Archivo sale vacío antes de cargar.

### Seguridad

- **La copia solo se sube a la cuenta con la que iniciaste sesión.** Con varias cuentas de Google en el teléfono, Notar podía usar el permiso de Drive de otra.
- Una copia que tu clave no abre nunca se sobrescribe, y una clave equivocada no se guarda.
- Cambiar la clave y eliminar la copia piden la clave actual: tener el teléfono desbloqueado no basta.
- Al cerrar sesión no queda rastro en el teléfono de las notas quitadas.
- Una copia manipulada en Drive ya no puede cerrar la app.

## [1.2.1] - 2026-07-25

### Corregido

- **Las notas restauradas desde Google Drive no aparecían al buscar por su contenido**: solo se encontraban por el título. La copia guarda únicamente el texto con formato y, al restaurar, no se regeneraba el texto plano que usa el buscador. Las notas ya restauradas se reparan solas al abrir esta versión.
- La búsqueda ignora los símbolos pegados a los extremos del término: escribir «--Google» ahora encuentra «Google».

### Cambiado

- El menú lateral ya no ocupa todo el ancho de la pantalla en móviles.
- El tema «Automático» se muestra con un icono de paleta en Ajustes.

## [1.2.0] - 2026-07-19

### Añadido

- **Indicador por nota de «cambios sin subir»**: las notas editadas después de la última copia muestran una nube junto al pin en Inicio, que se desvanece al completarse la subida. Solo aparece con la sesión de Google y la clave de cifrado activas.
- **Ordenar en Archivo y Papelera** por más reciente o más antiguo, con preferencia independiente por pantalla.

### Cambiado

- El menú de la selección múltiple en Inicio ahora es dinámico según el estado de las notas seleccionadas: muestra «Desfijar» si todas están fijadas y «Mostrar» si todas están ocultas.

### Corregido

- El menú lateral ya no queda abierto al volver de Archivo, Papelera o Ajustes.
- Los iconos de la barra de estado ahora son legibles en todos los menús inferiores con tema oscuro.
- El botón «Descargar APK» de Buscar actualizaciones ahora abre la página del release concreto; antes usaba un enlace genérico que la app de GitHub interceptaba sin mostrar nada.

## [1.1.1] - 2026-06-29

### Corregido

- Al mantener pulsada una nota no fijada para arrastrarla, ya no se deselecciona automáticamente; ahora ambas acciones (seleccionar y arrastrar) funcionan de forma consistente, igual que en las notas fijadas.

## [1.1.0] - 2026-06-29

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
- Al actualizar desde la v1.0.0 las notas locales se conservan (migraciones manuales de base de datos en lugar de recreación destructiva).

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

# Notar

Aplicación de notas para Android, minimalista y centrada en la privacidad. Organiza tus ideas con notas de texto enriquecido, guarda credenciales y enlaces, y sincroniza todo de forma cifrada con tu propia cuenta de Google Drive.

## Capturas de pantalla

<p align="center">
  <img src="screenshots/home.png" width="250" alt="Inicio"/>
  <img src="screenshots/settings.png" width="250" alt="Ajustes"/>
  <img src="screenshots/backup.png" width="250" alt="Copia cifrada"/>
</p>

| Inicio | Ajustes | Copia cifrada |
|:------:|:-------:|:-------------:|
| Fijadas arriba, filtros por tipo y vista en dos columnas | La cuenta y su copia arriba, tema y seguridad | Sincronización con Drive, cifrada con tu clave |

Las capturas usan datos de demostración.

## Características

- **Notas Libres**: lienzo de escritura con texto enriquecido — negrita, cursiva, subrayado, encabezados y listas con viñetas o numeración.
- **Notas de Cuenta**: guarda credenciales (servicio, correo, usuario y contraseña) con la contraseña cifrada en el dispositivo.
- **Notas de Enlace**: guarda URLs con título y descripción.
- **Vistas previas de enlaces**: vista previa automática con imágenes, iconos de sitio y soporte para páginas pesadas (p. ej. Play Store), con caché persistente.
- **Colores por nota**: distingue tus notas con una paleta de colores.
- **Ocultar/difuminar notas**: oculta el contenido de notas individuales desde la pantalla de Inicio, de forma persistente.
- **Organización avanzada**: fija, archiva, envía a la papelera, reordena arrastrando y ordena por fecha o manualmente.
- **Selección múltiple**: selecciona varias notas en Inicio, Archivo o Papelera para acciones en lote (fijar, archivar, restaurar, eliminar).
- **Búsqueda con resaltado**: encuentra notas al instante, resalta coincidencias y permite saltar entre ellas dentro de cada nota.
- **Vista de columnas**: alterna entre una y dos columnas desde la barra de búsqueda.
- **Sincronización cifrada**: sincroniza tus notas entre teléfonos con tu Google Drive, cifradas de extremo a extremo con una clave que solo tú conoces. Al cerrar sesión, las notas sincronizadas se quitan del teléfono y vuelven al entrar, como en Keep.
- **Sincronización automática**: opcional; trae lo nuevo al abrir la app y sube cada cambio, también con la app cerrada. El botón de cuenta muestra si todo está al día.
- **Seguridad**: huella para mostrar o copiar credenciales y bloqueo de capturas de pantalla opcionales.
- **Material 3 Expressive**: interfaz moderna con color dinámico (Material You) y temas claro, oscuro y automático.

## Requisitos

- Android 8.0 (API 26) o superior

## Instalación

Descarga el APK desde la sección de [Releases](../../releases) e instálalo en tu dispositivo Android.

## Tecnologías

- Kotlin
- Jetpack Compose
- Material 3 Expressive
- Hilt (Inyección de dependencias)
- Room (Base de datos local)
- Jetpack DataStore
- WorkManager
- Google Credential Manager
- Google Drive API
- AndroidX Biometric

## Licencia

Copyright © 2026 dony-aep. Todos los derechos reservados. Consulta el archivo [LICENSE](LICENSE) para más detalles.

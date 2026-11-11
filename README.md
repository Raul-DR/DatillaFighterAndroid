# Datilla Fighter II — compilación desde el móvil

Este proyecto incluye un flujo de GitHub Actions para compilar el APK en la nube. No necesitas Android Studio ni un ordenador.

## Antes de compilar: colocar el HTML real
El archivo `app/src/main/assets/index.html` es actualmente una plantilla. Sustitúyelo por el HTML completo del juego que compartiste en ChatGPT y conserva exactamente esa ruta y ese nombre.

## Pasos desde Chrome en Android
1. Entra en https://github.com y crea una cuenta o inicia sesión.
2. Crea un repositorio nuevo llamado `DatillaFighterAndroid` y déjalo **Private** si prefieres.
3. Sube el contenido de este ZIP al repositorio (descomprime el ZIP primero; GitHub debe recibir carpetas/archivos, no el ZIP como único archivo).
4. En el repositorio, abre la pestaña **Actions** y habilita los workflows si GitHub lo solicita.
5. Entra en **Build Datilla Fighter II APK** y pulsa **Run workflow**. También se ejecuta al subir cambios a la rama `main`.
6. Cuando termine correctamente, abre la ejecución y descarga el artefacto **DatillaFighterII-APK**.
7. Descomprime el artefacto en el móvil y abre `app-debug.apk`. Si Android lo pide, permite instalar aplicaciones desde Chrome o desde el gestor de archivos que uses.

## Qué hace el proyecto
- Empaqueta el juego HTML en un WebView Android.
- Fuerza orientación horizontal y pantalla completa.
- Mantiene la pantalla encendida mientras se juega.
- Genera un APK de depuración instalable para pruebas.

## Requisitos y notas
- La primera compilación puede tardar unos minutos.
- El HTML original usa Tailwind y Google Fonts desde internet; esos recursos visuales externos necesitan conexión. La lógica del juego queda dentro del APK.
- El APK generado es de depuración, adecuado para instalar y probar; no es una versión firmada para publicar en Google Play.

# Hierro

Diario de entreno para Android: rutina de 4 días con prioridad en torso, registro de series con + y −, calentamiento automático, cambio de ejercicio, récords, informe semanal con comparativas, carreras y peso corporal.

## Descargar el APK

Cada vez que se sube un cambio a `main`, GitHub Actions compila la app y la publica en **Releases**. Desde el móvil:

1. Abre la pestaña **Releases** del repo y entra en la última versión.
2. Descarga `Hierro-vN.apk` y ábrelo.
3. Si Android lo pide, permite instalar apps de esa fuente (el navegador o Archivos).

Las versiones nuevas se instalan encima de la anterior y conservan tus datos. **Si desinstalas la app, se borran los entrenos guardados.**

## Estructura

- `app/src/main/assets/index.html`: la app completa (HTML, CSS y JavaScript en un archivo).
- `app/src/main/java/com/hierro/app/MainActivity.java`: el contenedor Android (WebView, botón atrás y pantalla encendida durante el entreno).
- `.github/workflows/apk.yml`: compilación automática.
- `keystore/hierro.keystore`: clave de firma fija para que las actualizaciones se instalen encima. Es una clave de uso personal; el repo es público, así que no la uses para publicar en Google Play.

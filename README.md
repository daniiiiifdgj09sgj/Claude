# Hierro

Diario de entreno para Android: rutina de 4 días con prioridad en torso, registro de series con + y −, calentamiento automático, cambio de ejercicio, récords, informe semanal con comparativas, carreras y peso corporal.

## Descargar el APK

La versión instalable está en la carpeta [`apk/`](apk/). Desde el móvil:

1. Abre `apk/Hierro.apk` y pulsa **Download raw file** (o el icono de descarga).
2. Ábrelo desde Descargas.
3. Si Android lo pide, permite instalar apps de esa fuente (el navegador o Archivos).

Las versiones nuevas se instalan encima de la anterior y conservan tus datos. **Si desinstalas la app, se borran los entrenos guardados.**

## Estructura

- `app/src/main/assets/index.html`: la app completa (HTML, CSS y JavaScript en un archivo).
- `app/src/main/java/com/hierro/app/MainActivity.java`: el contenedor Android (WebView, botón atrás y pantalla encendida durante el entreno).
- `.github/workflows/apk.yml`: compilación automática.
- `app/src/main/assets/fonts/`: fuentes incluidas (licencia SIL OFL), para no depender de internet.

## Seguridad

- La app **no tiene permiso de internet**: no puede enviar ni recibir nada. El CI falla si alguien lo añade o si la página carga direcciones externas.
- El WebView solo abre y carga sus propios archivos; cualquier otra dirección se bloquea.
- La clave de firma **no está en el repo ni en GitHub**: GitHub compila el APK sin firmar (en Releases, marcado como *sin firmar*) y se firma fuera con APK Signature Scheme v2.
- Instala solo el APK de la carpeta `apk/` de este repo.

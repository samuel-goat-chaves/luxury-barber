# Luxury Barber: generar APK desde GitHub

Esta versión conserva la web y sus imágenes. El APK carga la web publicada en https://samuel-goat-chaves.github.io/luxury-barber/ mediante Capacitor.

## Instrucciones
1. Abre el repositorio `samuel-goat-chaves/luxury-barber` en GitHub.
2. Antes de reemplazar nada, conserva una copia del repositorio original.
3. Extrae el ZIP y sube **el contenido interior** a la raíz del repositorio (no la carpeta contenedora). Conserva `index.html`, `admin/` y `assets/`.
4. IMPORTANTE: GitHub web puede no incluir carpetas ocultas al subir una carpeta completa. Verifica que `.github/workflows/build-apk.yml` esté presente en GitHub. Si falta, créalo con Add file > Create new file y pega el contenido del ZIP.
5. En GitHub abre `Actions` y selecciona `Compilar APK Luxury Barber`.
6. Pulsa `Run workflow` y confirma. Si GitHub pide habilitar Actions, habilítalo primero.
7. Espera a que el trabajo finalice con una marca verde. En la ejecución abre `Artifacts` y descarga `Luxury-Barber-APK`.
8. Descomprime el artifact para obtener `app-debug.apk`. Instálalo en un dispositivo Android de pruebas.

## Importante
- APK de depuración para pruebas, NO firmado para publicación comercial ni listo para Google Play.
- Requiere Internet. Si GitHub Pages falla, la app tampoco podrá cargar la web.
- El sitio sigue usando su almacenamiento y su lógica web original; esta conversión NO crea un backend de reservas ni sincroniza automáticamente citas entre dispositivos.
- Algunas funciones web, enlaces externos, subida de archivos o permisos pueden necesitar adaptaciones específicas para WebView.
- GitHub Pages publica la web con `index.html` en la raíz; no modifiques su ubicación.
- Si la compilación falla, consulta el registro de Actions para ver el motivo. No se ha probado aquí una compilación Android real.

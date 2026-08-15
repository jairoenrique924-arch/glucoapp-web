# Sitio de GlucoApp

Página promocional estática (un solo archivo `index.html`), lista para GitHub Pages.

## Publicarla en GitHub Pages

1. Crea un repositorio nuevo en GitHub, por ejemplo `glucoapp-web`.
2. Sube `index.html` a la raíz del repositorio.
3. En el repo, ve a **Settings → Pages**.
4. En "Build and deployment", elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`.
5. Guarda. En 1-2 minutos tu sitio queda publicado en:
   `https://<tu-usuario>.github.io/glucoapp-web/`

## Añadir el APK para descarga

Tu APK pesa 66 MB, así que **no cabe en la subida directa por la web de GitHub (límite de 25 MB)**.
Usa una de estas dos opciones:

**Opción A — Git desde la terminal (recomendada, más simple):**
```
git add GlucoApp.apk
git commit -m "Agregar APK"
git push
```
`git push` normal admite archivos de hasta 100 MB sin configuración extra, así que 66 MB no da problema. Colócalo en la raíz del repo con el nombre exacto **`GlucoApp.apk`** (o cambia la ruta en `index.html`, buscando `href="./GlucoApp.apk"`).

**Opción B — GitHub Release:**
1. En el repo, ve a **Releases → Draft a new release**.
2. Sube el APK como archivo adjunto (admite hasta 2 GB, sin límite de 25 MB).
3. Publica la release y copia el enlace de descarga del archivo.
4. Reemplaza en `index.html` el `href="./GlucoApp.apk"` por esa URL.

Esta segunda opción además mantiene el repositorio más liviano, ya que el binario no queda en el historial de Git.

## Añadir el manual de usuario

Sube también `Manual_de_Usuario_GlucoApp.pdf` a la raíz del repositorio (mismo nombre). El enlace
"📄 Manual de usuario (PDF)" del footer ya apunta a esa ruta.

## Nota sobre las capturas

Las capturas usadas en la sección "Así se ve por dentro" están en `screenshots/` y muestran datos
que confirmaste como ficticios (nombre, teléfono de contacto, cifras de glucosa). Si en algún
momento vuelves a compartir capturas para actualizar el sitio, confirma primero que los datos no
sean reales — recuerda que este sitio es público.

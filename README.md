# Paquete PWA Completo - Libro Gamificado Inclusivo Catatumbo

Este paquete contiene todos los archivos necesarios y optimizados según los estándares de **PWABuilder (Microsoft)** y **Google Lighthouse PWA** para generar una aplicación Android nativa (.apk / .aab).

## Contenido del Paquete:
1. `index.html`: La aplicación web completa con diseño universal de aprendizaje (DUA), modo lectura fácil, 3 retos lúdicos (ordenar secuencias, sopa de letras por teclado, cuestionario con síntesis de voz), modo alto contraste, fuente OpenDyslexic, informe descargable y soporte de instalación.
2. `manifest.json`: Manifiesto PWA compatible con PWABuilder con identificador `id`, orientación, colores temáticos, iconos `any` y `maskable`, capturas de pantalla y categorías.
3. `sw.js`: Service Worker que permite ejecución offline y respuesta rápida en dispositivos móviles.
4. Iconos de alta definición:
   - `icon-192.png` y `icon-512.png` (iconos regulares)
   - `icon-192-maskable.png` y `icon-512-maskable.png` (iconos adaptativos/maskable para Android)

---

## Pasos para generar el APK con PWABuilder:

### Paso 1: Alojar los archivos en un servidor web seguro (HTTPS)
PWABuilder requiere una URL pública bajo protocolo HTTPS. Puedes alojarlo gratis en menos de 2 minutos mediante cualquiera de estas plataformas:
* **GitHub Pages (Recomendado):**
  1. Crea un repositorio público en GitHub (por ejemplo, `catatumbo-dua`).
  2. Sube los archivos extraídos de este `.zip` directamente a la raíz del repositorio.
  3. Ve a `Settings` > `Pages` y en **Branch** selecciona `main` o `master` y guarda.
  4. Obtendrás tu URL: `https://tu-usuario.github.io/catatumbo-dua/`.
* **Netlify Drop:**
  1. Ingresa a [app.netlify.com/drop](https://app.netlify.com/drop).
  2. Arrastra la carpeta descomprimida con los archivos.
  3. Obtendrás una URL instantánea con HTTPS (ej. `https://catatumbo-dua.netlify.app`).
* **Vercel:**
  1. Despliega la carpeta usando `npx vercel` o desde el dashboard de Vercel.

### Paso 2: Generar el APK en PWABuilder
1. Abre tu navegador y ve a [https://www.pwabuilder.com](https://www.pwabuilder.com).
2. Pega la URL de tu aplicación (ej. `https://tu-usuario.github.io/catatumbo-dua/`) en el campo de texto y haz clic en **Start**.
3. PWABuilder analizará el Manifiesto, el Service Worker y los Iconos. El puntaje será óptimo (Manifest, Service Worker e Iconos en verde).
4. Haz clic en el botón **Package for Stores** o **Package for Android**.
5. Configura los datos de la app (Nombre de paquete, versión, firma). PWABuilder te permite:
   - Descargar el paquete `.apk` listo para probar e instalar en cualquier celular o tableta Android.
   - Descargar el paquete firmado `.aab` (Android App Bundle) si deseas publicarlo en Google Play Store.
6. ¡Listo! Ya tienes tu APK accesible e inclusiva.

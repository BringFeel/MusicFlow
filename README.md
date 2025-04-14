# 🎵 Buscador y Descargador de Música

Este proyecto es una interfaz web que permite buscar canciones o álbumes usando la API de **Deezer**, y generar enlaces de descarga en formato **MP3** o **FLAC** usando el servicio de `flacdownloader.com`.

---

## 📦 Características

- 🔍 Búsqueda de canciones o álbumes por nombre.
- 🎨 Interfaz oscura, moderna y responsive.
- 📄 Resultados en tarjetas con portada, título y artista.
- 📥 Botones para descargar en formato MP3 o FLAC.
- 🚨 Mensajes dinámicos de carga, error o sin resultados.
- 🧪 Generador de resultados falsos como fallback.

---

## 🧰 Tecnologías utilizadas

- **HTML5 / CSS3**
- **JavaScript Vanilla**
- **Deezer API**
- **CORS proxy** (`cors-anywhere.bringfeel.com.ar`)
- **flacdownloader.com** para simular descargas

---

## 🚀 Estructura de la aplicación

### `app.html`

- Contenedor principal con:
  - Input de búsqueda.
  - Botón de búsqueda.
  - Resultados dinámicos.
- Tarjetas con:
  - Imagen del álbum.
  - Título de la canción.
  - Artista.
  - Botones de descarga.
- Estilos integrados con un diseño oscuro.

### JavaScript

Funciones principales:

| Función                | Descripción |
|------------------------|-------------|
| `performSearch()`      | Ejecuta búsqueda en la API de Deezer. |
| `displayResults()`     | Muestra resultados como tarjetas. |
| `generateMockResults()`| Genera datos falsos como fallback. |
| `showLoading()`        | Muestra mensaje de carga. |
| `showError()`          | Muestra errores al usuario. |
| `showNoResults()`      | Informa si no hubo resultados. |
| `tryAlternativeSearch()`| Usa resultados falsos si la API falla. |

---

## 🔗 URLs usadas

- Búsqueda en Deezer:
https://api.deezer.com/search?q=nombre

- Descarga de canción:
https://flacdownloader.com/flac/download?t=TRACK_ID&f=FORMATO


---

## ⚠️ Consideraciones

- El proxy usado para evitar CORS es:
https://cors-anywhere.bringfeel.com.ar/

- Algunos navegadores pueden bloquear múltiples descargas automáticas sin interacción.
- `flacdownloader.com` debe estar activo y aceptar IDs de Deezer (esto es simulado).
- Los resultados falsos son útiles para demostración sin conexión a Deezer.

---

## 📂 Cómo usar

1. Abrí el archivo `music-search-download.html` en tu navegador.
2. Ingresá un término en la barra de búsqueda.
3. Presioná el botón **Buscar**.
4. Aparecerán los resultados. Podés descargar cada canción en MP3 o FLAC.

---

## ✅ Mejoras sugeridas

- Selección de álbum específico cuando hay múltiples resultados.
- Vista previa de canciones antes de descargar.
- Descargar todo el álbum en un archivo ZIP.
- Implementar paginación en los resultados.
- Guardar historial de búsquedas.

---

## 🧑‍💻 Autor

Este archivo fue documentado por ChatGPT — *Basado en código proporcionado en abril de 2025*.

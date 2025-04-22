# enbataDev - Developer Ecosystem

Este repositorio contiene el sitio web oficial de **enbataDev**, una iniciativa para crear aplicaciones útiles, centradas en la eficiencia, la tecnología y el desarrollo sostenible.

## 🔗 Sitio en vivo

[https://enbatadev.github.io/enbataDev](https://enbatadev.github.io/enbataDev)

## 📱 Aplicaciones

- [EcoLuz](./apps/ecoluz/index.html)  
  Visualiza precios horarios de electricidad y optimiza el uso energético de tu hogar.  
  → [Política de privacidad](./apps/ecoluz/privacy.html)

## 📁 Estructura

```
/enbataDev
├── index.html                       # Página principal (landing de enbataDev)
├── /apps
│   └── /ecoluz
│       ├── index.html              # Página de la app EcoLuz
│       └── privacy.html           # Política de privacidad de EcoLuz
├── /assets
│   └── /img                        # Logo y capturas de pantalla
│   └── /css                        # Hoja de estilos global
│       └── style.css
├── README.md                       # Este archivo
```

## 🚀 Despliegue

Este sitio está alojado con **GitHub Pages**.

### Pasos:
1. Asegúrate de que `index.html` esté en la raíz del repositorio.
2. Ve a **Settings > Pages** y selecciona:
   - **Source**: rama `main` o `master`
   - **Root** como carpeta

GitHub generará la URL en la forma:

```
https://<usuario>.github.io/<repositorio>/
```

## 📌 Notas

- Las páginas de las aplicaciones están organizadas en `/apps/<nombre>/index.html`
- Las políticas de privacidad se alojan en `/apps/<nombre>/privacy.html`
- Los recursos comunes (imágenes, estilos, etc.) están en `/assets/`

---

© 2025 enbataDev

## 🌐 Estructura multilingüe del sitio

El sitio está preparado para soportar múltiples idiomas. Actualmente se soporta:

- Español (`/es/`)
- Inglés (`/en/`) – en desarrollo

### 📁 Estructura

```
/index.html              ← Redireccionador automático por idioma
/es/index.html           ← Página principal en español
/en/index.html           ← Página principal en inglés (cuando esté lista)
/apps/                   ← Aplicaciones en español
/en/apps/                ← Aplicaciones en inglés (solo si tienen traducción)
/assets/                 ← Recursos compartidos (CSS, imágenes, etc.)
```

### 🌍 Navegación

Cada página incluye un conmutador de idioma en la cabecera:

```html
<nav>
  <a href="/es/index.html">ES</a> | <a href="/en/index.html">EN</a>
</nav>
```

Las nuevas secciones se desarrollarán primero en español y se traducirán gradualmente al inglés.

## 🛠️ Guía técnica para añadir nuevas aplicaciones

### 1. Crear la carpeta de la aplicación
Dentro del directorio `/apps/`, crea una subcarpeta con el nombre de la app:

```
/apps/nombreApp/
```

### 2. Estructura de la app
Cada app debe tener al menos:

```
/apps/nombreApp/index.html         ← Página de presentación
/apps/nombreApp/privacy.html       ← Política de privacidad
```

### 3. Enlace desde la home
Añade una tarjeta en `/es/index.html` (o `/en/index.html` si hay traducción), enlazando a la nueva app:

```html
<div class="card">
  <h3>NombreApp</h3>
  <p>Breve descripción de la app.</p>
  <a class="button" href="/apps/nombreApp/index.html">Ver más</a>
</div>
```

### 4. Política de privacidad
Debe estar accesible solo desde la página de la app. Se coloca en:

```
/apps/nombreApp/privacy.html
```

Y se enlaza desde el footer de la app.

### 5. Accesibilidad y buenas prácticas (aplicación automática)
- Contraste suficiente para enlaces
- Botones deshabilitados con `aria-disabled="true"`
- Imágenes con `alt` descriptivo
- Enlaces a política de privacidad encima del copyright

---

Estas normas aseguran coherencia visual, accesibilidad y escalabilidad en todo el sitio enbataDev.
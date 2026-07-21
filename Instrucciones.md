# 📦 Cómo instalar tu perfil — paso a paso

Tu repositorio `cord0990/cord0990` debe quedar con esta estructura:

```
cord0990/
├── README.md                      ← el archivo principal
├── assets/
│   ├── header.svg                 ← banner animado con los personajitos
│   └── terminal.svg               ← terminal animada del About me
└── .github/
    └── workflows/
        └── snake.yml              ← genera la serpiente 🐍
```

## Paso 1 — Subir el README y los assets

1. Entra a tu repo `cord0990/cord0990` en GitHub.
2. Abre el `README.md`, dale al lápiz ✏️, borra todo y pega el contenido del `README.md` que te entregué. Dale a **Commit changes**.
3. Ahora crea la carpeta de assets: dale a **Add file → Upload files** y arrastra `header.svg` y `terminal.svg`.
   - ⚠️ Importante: antes de subirlos, en el campo del nombre escribe `assets/` para que queden dentro de esa carpeta. La forma más fácil: **Add file → Create new file**, escribe `assets/header.svg` como nombre, pega el contenido del SVG y haz commit. Repite con `assets/terminal.svg`.

## Paso 2 — Activar la serpiente 🐍

1. En el repo, dale a **Add file → Create new file**.
2. Como nombre escribe exactamente: `.github/workflows/snake.yml` (GitHub crea las carpetas solo).
3. Pega el contenido de `snake.yml` y haz commit.
4. Ve a la pestaña **Actions** del repo → si te pide habilitar workflows, acéptalo.
5. Entra al workflow **"Generate snake animation"** → botón **Run workflow** → espera ~1 minuto.
6. Listo: el workflow crea una rama `output` con el SVG de la serpiente, y el README ya apunta ahí. Se regenera solo cada 12 horas.

> Si la serpiente sale con un ícono roto la primera vez, es porque el workflow aún no corre. Ejecuta el workflow manualmente (paso 5) y recarga.

## Paso 3 — Personalizar los enlaces

En el `README.md` hay dos enlaces genéricos que debes cambiar por los tuyos:

- `https://www.linkedin.com/` → tu perfil de LinkedIn (o borra esa línea si no tienes)
- `https://www.tiktok.com/` → tu perfil de TikTok

El de Kaggle ya apunta a `kaggle.com/cord09`, verifica que sea el correcto.

## Notas

- **Los SVG animados solo se animan si están dentro del repo** y se referencian con ruta relativa (`assets/header.svg`), tal como ya está en el README. No los subas como imagen adjunta en un issue.
- Las tarjetas de estadísticas (`github-readme-stats`, streak, activity graph) son servicios gratuitos externos: a veces tardan unos segundos en cargar o se caen temporalmente. Es normal.
- Si más adelante quieres cambiar el color de acento naranjo, busca `e87b4f` en el README y los SVG y reemplázalo por otro hex.
- El contador de visitas (komarev) parte en 0 desde que lo publiques.
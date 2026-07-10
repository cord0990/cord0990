# 📋 Instrucciones para publicar tu README de perfil

## 1. Crear el repositorio especial

GitHub muestra el README en tu perfil solo si el repositorio se llama **igual que tu usuario**:

1. Ve a <https://github.com/new>
2. Nombre del repositorio: `cord0990` (exactamente igual a tu usuario)
3. Marca **Public** y **Add a README file** (o súbelo tú después)

## 2. Subir los archivos

Estructura final del repositorio:

```
cord0990/
├── README.md                     ← el Readme.md de esta carpeta
├── header.svg
├── terminal.svg
└── .github/
    └── workflows/
        └── snake.yml             ← el Snake.yml de esta carpeta (¡ojo con la ruta!)
```

Desde esta carpeta:

```bash
git init          # si aún no está inicializado
git add .
git commit -m "Perfil de GitHub"
git remote add origin https://github.com/cord0990/cord0990.git
git push -u origin main
```

> ⚠️ **Importante:** `Snake.yml` debe moverse a `.github/workflows/snake.yml`,
> si queda en la raíz GitHub Actions no lo detecta.

## 3. Activar la serpiente 🐍

1. En el repositorio, ve a la pestaña **Actions**
2. Si aparece un aviso, haz clic en **"I understand my workflows, enable them"**
3. Selecciona **Generate snake animation** → **Run workflow**
4. Espera ~1 minuto: se creará una rama `output` con los SVG de la serpiente
5. Desde entonces se regenera sola todos los días a medianoche (UTC)

Mientras la rama `output` no exista, la imagen de la serpiente en el README
se verá rota. Es normal; se arregla al correr el workflow por primera vez.

## 4. Personalizar los enlaces

En `README.md` hay dos enlaces con placeholder que debes editar:

- `https://www.linkedin.com/in/tu-usuario/` → tu LinkedIn real
- `https://www.kaggle.com/tu-usuario` → tu Kaggle real

Si no usas alguna de esas redes, simplemente borra ese bloque `<a>...</a>`.

## 5. Notas sobre las tarjetas de estadísticas

- Las tarjetas (`github-readme-stats`, `streak-stats`, `activity-graph`) son
  servicios externos gratuitos: a veces demoran unos segundos en cargar o se
  actualizan con retraso de horas. Es normal.
- Todas están configuradas con la paleta del perfil: fondo `#0d1117`,
  naranjo `#e87b4f`, bordes `#30363d`. Si cambias un color en los SVG,
  puedes ajustar los parámetros `bg_color`, `title_color`, etc. en las URLs.

## 6. Consejos finales

- El contador de visitas (komarev) empieza en 0 y suma solo desde que lo publicas.
- Para ver los SVG animados localmente, ábrelos con el navegador
  (doble clic sobre `header.svg` / `terminal.svg`).
- GitHub cachea las imágenes: si actualizas un SVG y no ves el cambio,
  espera unos minutos o fuerza recarga con `Ctrl+F5`.

# Adivina el programa

Juego para adivinar de qué partido es cada propuesta de los programas electorales de 2023.
Los resultados de cada jugador se guardan en `data/results.json`.

## Puesta en marcha

1. Crea un repositorio **público** en GitHub y sube todo el contenido de esta carpeta (incluida `.github/`).
2. Abre `index.html` y cambia la línea `var REPO="TU_USUARIO/TU_REPO";` por tu usuario y repositorio. Si tu rama no se llama `main`, cambia también `BRANCH`.
3. En el repositorio, ve a Settings > Pages y elige "Deploy from a branch", rama `main`, carpeta `/ (root)`.
4. Pasa a tus amigos la dirección `https://TU_USUARIO.github.io/TU_REPO/`.

## Cómo se guardan los resultados

GitHub Pages no puede escribir en el repositorio por sí solo, y no se puede poner una clave en una página pública.
Por eso, al terminar, el botón "Enviar a la clasificación" abre un issue ya rellenado en tu repositorio.
El jugador pulsa "Submit new issue" y una acción de GitHub (`.github/workflows/recoger-resultados.yml`) valida el resultado,
lo añade a `data/results.json` y cierra el issue.

- Cada amigo necesita una cuenta de GitHub gratuita para enviar su resultado.
- Los nombres y las respuestas son públicos, igual que el repositorio.
- No cambies el orden de las preguntas del array `Q` de `index.html`: los resultados guardan la posición de cada una.
- La clasificación puede tardar un minuto en actualizarse y la caché de GitHub puede retrasarla unos minutos más.

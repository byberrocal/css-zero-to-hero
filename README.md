# CSS de Cero a Hero 🎮

Un juego interactivo para practicar **CSS** — al estilo de *Flexbox Froggy*, pero ampliado.
Los alumnos escriben CSS en un editor, ven el resultado en vivo comparado con un objetivo,
y el juego **valida automáticamente** cada nivel. El progreso se guarda en el navegador.

**Sistemas Web · Grado en IA · Universidad San Jorge**

## Mundos (27 niveles, de cero a hero)
1. 🎯 **Selectores** — tipo, clase, id, descendiente, `:nth-child`
2. 📦 **Modelo de caja** — padding, margin, border, `box-sizing`, `border-radius`
3. 📍 **Posicionamiento** — `relative`, `absolute`, `fixed`, `sticky`, `z-index`
4. 🧺 **Flexbox** — `display:flex`, `justify-content`, `align-items`, `flex-direction`
5. ▦ **Grid** — `grid-template-columns`, `repeat`, `gap`, `minmax`/`auto-fill`
6. 📱 **Responsive** — `@media` (media queries), apilar en móvil, ocultar, unidades

## Es un solo archivo
Todo el juego está en **`index.html`** (HTML + CSS + JS, sin dependencias, sin build).
Funciona abriéndolo directamente en el navegador, y se despliega tal cual.

---

## Cómo desplegarlo en Vercel

### Opción A — GitHub + Vercel (recomendada, da URL estable)
1. Crea un repositorio nuevo en tu GitHub **byberrocal**, por ejemplo `css-zero-to-hero`.
2. Sube esta carpeta al repo:
   ```bash
   cd css-zero-to-hero
   git init
   git add .
   git commit -m "CSS de Cero a Hero"
   git branch -M main
   git remote add origin https://github.com/byberrocal/css-zero-to-hero.git
   git push -u origin main
   ```
3. Entra en https://vercel.com → **Add New… → Project** → importa `byberrocal/css-zero-to-hero`.
4. Framework Preset: **Other** (es estático). No hace falta build command ni output.
   Pulsa **Deploy**.
5. Vercel te da una URL tipo `https://css-zero-to-hero.vercel.app` → **eso es lo que pasas a tus alumnos**.

Cada `git push` vuelve a desplegar automáticamente.

### Opción B — Vercel CLI (rápido)
```bash
npm i -g vercel      # una vez
cd css-zero-to-hero
vercel               # sigue el asistente; "vercel --prod" para producción
```

---

## Notas
- El progreso de cada alumno se guarda en **su** navegador (`localStorage`); no se comparte ni necesita servidor.
- Tiene **modo claro/oscuro** (botón «Tema») y funciona en móvil.
- Para añadir o editar niveles: en `index.html`, busca el array `const L = [ … ]`.
  Cada nivel tiene `title`, `desc`, `start` (código inicial), `sol` (solución para el objetivo),
  `hint` y `test` (función que valida leyendo los estilos calculados del resultado).

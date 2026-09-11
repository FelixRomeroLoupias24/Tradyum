# Tradyum

Diario y panel de trading personal. Aplicación estática en HTML, CSS y
JavaScript puro (sin frameworks, sin build). Todos los datos (operaciones,
cuentas) se guardan en el `localStorage` del navegador; no hay backend ni
sistema de login.

## Estructura

- `index.html` — punto de entrada. Redirige automáticamente a
  `index_journal.html`, que contiene la aplicación completa.
- `index_journal.html` — la aplicación en sí (HTML + CSS + JS embebidos).

## Uso local

No requiere instalación ni dependencias. Alcanza con abrir `index.html`
(o `index_journal.html`) directamente en el navegador, o servirlo con
cualquier servidor estático, por ejemplo:

```bash
npx serve .
```

## Despliegue en Vercel

1. Subí este proyecto a un repositorio de GitHub.
2. En Vercel, elegí **Add New Project** → **Import Git Repository** y
   seleccioná el repo.
3. Framework preset: **Other** (proyecto estático, sin build). No hace
   falta configurar build command ni output directory.
4. Deploy. La app queda disponible en la URL que asigne Vercel, sirviendo
   `index.html` en la raíz (`/`).

## Notas

- Los datos se guardan solo en el navegador del dispositivo donde se usa
  la app (no se sincronizan entre dispositivos ni sesiones).
- No hay autenticación todavía: cualquiera con el link de despliegue
  puede ver y modificar los datos guardados en ese navegador.

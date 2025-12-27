# Runbook - DevOps 1 Blog

## Información General
Este proyecto aloja un blog estático generado con Hugo y desplegado automáticamente en GitHub Pages.

## Procedimientos Comunes

### 1. Desarrollo Local
Para levantar el servidor localmente y ver cambios en vivo:
`hugo server -D`

### 2. Crear nuevo contenido
`hugo new posts/mi-nuevo-post.md`

## Troubleshooting

### El Pipeline falla en el paso "Build"
- **Causa probable:** Error de sintaxis en Markdown o configuración `hugo.toml` inválida.
- **Solución:** Revisa los logs de la acción en GitHub. Intenta correr `hugo --minify` localmente para reproducir el error.

### El tema no carga / Estilos rotos
- **Causa probable:** El submódulo de Git no se descargó correctamente.
- **Solución:** Verifica que el workflow tenga `submodules: recursive`. Localmente ejecuta: `git submodule update --init --recursive`.

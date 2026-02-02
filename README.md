Helpy — Página interactiva y propuesta para la Gobernación de Antioquia

Resumen
- Archivo principal: `helpy_proposal.html` — landing interactiva lista para presentar a la Gobernación de Antioquia.
- Logotipos: carpeta `Logos Helpy/` con variantes de color (Sea green, Baby blue, Midnight Green, etc.).
- Objetivo: entregar una propuesta visual y técnica con demo estática, formulario de contacto (mailto fallback), navegación y animaciones.

Cómo previsualizar
1. Abrir localmente: simplemente doble clic en `helpy_proposal.html` o abrir en tu navegador.
2. Servidor local (recomendado para evitar restricciones de CORS con assets):

```bash
# Python 3
python3 -m http.server 8000
# luego abrir http://localhost:8000/helpy_proposal.html
```

Qué incluye la versión entregada
- `helpy_proposal.html`: landing interactiva con secciones: Hero, ¿Qué es Helpy?, Desafío & Solución, Evento, Niveles de alianza y CTA.
- Uso de la paleta y logos en `Logos Helpy/Sea green` (icono y logotipo principal).
- Navegación fija con smooth scroll, modal de contacto (envío por `mailto:`) y animaciones de entrada y contadores.

Personalización rápida
- Cambiar paleta: editar las variables CSS en la sección `:root` de `helpy_proposal.html`. Variables principales:
  - `--color-primary` — color principal (actualmente #2F855A)
  - `--color-accent` — color secundario/acento
  - `--color-soft` — fondo suave
- Cambiar logo: reemplaza los archivos en `Logos Helpy/Sea green/` o actualiza las rutas en el HTML para usar otra carpeta (ej. `Logos Helpy/Baby blue/`).
- Formularios: el modal usa una acción `mailto:` como fallback. Para integración con backend, reemplaza el handler en `modal-submit` en el script por una petición `fetch()` a tu endpoint.

Optimización y entrega final
- Las imágenes están en la carpeta de identidad; si deseas optimizarlas (reducción de peso y exportar WebP), puedes usar herramientas locales como `ImageOptim` (macOS) o `cwebp`.

Empaquetado (crear ZIP listo para enviar)
```bash
# desde la carpeta 'helpy monza'
zip -r helpy_proposal_antioquia.zip helpy_proposal.html "Logos Helpy" README.md
```

Despliegue recomendado
- GitHub Pages: crear un repo, subir los archivos y activar Pages en la rama `main`.
- Netlify / Vercel: arrastrar la carpeta al dashboard o conectar el repositorio.

Accesibilidad y notas técnicas
- Se usaron contrastes suaves y componentes con foco. Se recomienda auditar con Lighthouse o herramientas de accesibilidad.
- El modal resalta el foco en el primer campo al abrir; para integración con backend, validar y sanitizar entradas en servidor.

Siguientes pasos sugeridos (opcionales)
- Integrar envío real con un endpoint (Node/Flask) y almacenar leads en un CRM.
- Preparar una versión PDF de la propuesta para entrega formal.
- Ajustes finales visuales con el equipo de diseño de la Gobernación (tamaños de logo, firma institucional).

Contacto
- Si quieres, yo puedo: optimizar imágenes, crear una versión PDF de la propuesta, o montar el sitio en GitHub Pages. Indícame cuál prefieres.

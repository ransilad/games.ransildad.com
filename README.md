# ransilad Games

Landing page de `games.ransilad.com`, un catálogo en español para los juegos web independientes de ransilad.

El sitio está construido con Astro 6 como sitio estático. La página principal presenta un catálogo de juegos con estética arcade oscura, metadata SEO, datos estructurados, sitemap, robots.txt e imagen para previews sociales.

## Stack

- Astro 6
- TypeScript mediante `astro check`
- pnpm
- Salida estática en `dist/`

## Requisitos

- Node `v24.15.0` está fijado en `.node-version`.
- `package.json` permite Node `>=22.12.0`.
- Usar pnpm; el lockfile es `pnpm-lock.yaml`.

## Comandos

| Comando | Descripción |
| --- | --- |
| `pnpm install` | Instala dependencias. |
| `pnpm dev` | Inicia el servidor de desarrollo de Astro en `localhost:4321`. |
| `pnpm check` | Ejecuta diagnósticos de Astro y revisiones TypeScript. |
| `pnpm build` | Compila el sitio estático de producción en `dist/`. |
| `pnpm preview` | Previsualiza localmente el build de producción. |
| `pnpm astro ...` | Ejecuta comandos de la CLI de Astro. |

## Estructura

```text
public/
  favicon.svg       Favicon personalizado del sitio
  og-image.webp     Imagen por defecto para Open Graph / Twitter
  robots.txt        Reglas de rastreo
  sitemap.xml       Sitemap canonical
src/
  layouts/
    Layout.astro    Shell HTML compartido y metadata SEO
  pages/
    index.astro     Página principal del catálogo de juegos
```

## SEO

- La URL canonical del sitio está configurada en `astro.config.mjs` como `https://games.ransilad.com`.
- El layout compartido emite title, description, canonical, robots, Open Graph y metadata de Twitter.
- La home incluye JSON-LD de tipo `CollectionPage` con una lista de `VideoGame`.
- `public/robots.txt` apunta a `https://games.ransilad.com/sitemap.xml`.
- `public/sitemap.xml` actualmente incluye solo la URL canonical de la home.

## Enlaces De Juegos

- `Tres en Raya` vive en un proyecto separado, tiene opción de jugar en línea y se enlaza externamente en `https://tres-en-raya.ransilad.com/`.
- Este repositorio no debe contener una página local `/tres-en-raya/`.

## Notas

- El componente starter anterior de Astro sigue en `src/components/Welcome.astro`, pero no se usa en la home actual.
- El historial de OpenSpec está en `openspec/`; los cambios archivados están en `openspec/changes/archive/`.

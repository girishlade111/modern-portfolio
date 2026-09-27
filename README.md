# Modern Portfolio

A modern personal-portfolio website: animated hero, about, projects showcase, tech stack, testimonials, contact form, and footer. Originally generated with [v0.app](https://v0.app) and maintained as a full Next.js project.

🌐 **Live demo:** https://girishlade111.github.io/modern-portfolio/

## Features

- **Animated hero** — motion-driven intro section (Framer Motion)
- **About** — personal bio/profile section
- **Projects** — showcase grid with project cards
- **Tech stack** — skills and tools display
- **Testimonials** — carousel of endorsements (Embla Carousel)
- **Contact** — form-based contact section (react-hook-form + zod validation)
- **Dark theme** — via `next-themes`, Radix UI primitives, Tailwind CSS, Geist font
- **Analytics** — `@vercel/analytics` integrated

## Tech stack

| Layer     | Tech                                              |
|-----------|---------------------------------------------------|
| Framework | Next.js 15.2 (App Router), React 19, TypeScript    |
| Styling   | Tailwind CSS, tailwindcss-animate, Geist           |
| UI kit    | Radix UI primitives, shadcn/ui-style `components/ui` |
| Motion    | Framer Motion                                     |
| Carousel  | Embla Carousel                                    |
| Forms     | react-hook-form, zod, @hookform/resolvers          |
| Deploy    | GitHub Pages (static export)                       |

## Quick start

```bash
# install
pnpm install        # or: npm install --legacy-peer-deps

# dev server
pnpm dev            # http://localhost:3000

# production build (static export)
pnpm build          # output goes to out/
```

> **Security note:** `next` was bumped from `15.2.4` → `15.2.8` — earlier 15.2.x releases are affected by CVE-2025-55182 (React2Shell RCE).

## Project structure

```
app/                # App Router — layout.tsx, page.tsx, globals.css
components/         # hero, about, projects, tech-stack, testimonials, contact, footer, navbar
  ui/               # Radix-based primitives
lib/                # utilities
public/             # images
styles/             # global styles
```

## Environment variables

None required. `@vercel/analytics` works out of the box on Vercel; on GitHub Pages it is inert.

## Deployment notes

- This app has **no API routes and no server actions**, so it is statically exported (`output: 'export'` in `next.config.mjs`) and hosted on **GitHub Pages** from the `gh-pages` branch.
- `next.config.mjs` sets `basePath: '/modern-portfolio'` because GitHub Pages serves it from the `/modern-portfolio/` subpath. **If you deploy to a root domain or Vercel instead, remove the `basePath` line.**
- `images.unoptimized: true` is set, so no image-optimization backend is needed.

---

Built by Girish Lade — https://ladestack.in

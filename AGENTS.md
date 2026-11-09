## Project rules

- Temporary inboxes come from the public Guerrilla Mail API, called directly from the browser (`src/lib/tempmail.ts`): it allows any origin and keeps rate limits per visitor instead of on one shared server IP.
- The active inbox session (address + sid token) persists in localStorage so a reload resumes the same address.
- Static SPA for GitHub Pages: hash history in `src/router.tsx`, `base` set in `vite.config.ts`. Do not add server-only code (no SSR, server functions, or Node APIs).
- Never use plain `<a href="/...">` for internal navigation; use TanStack `<Link>`. Reference public assets through the Vite base path.

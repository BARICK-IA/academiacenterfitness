# Center Fitness — Landing Page

## Overview
A single-page marketing/landing site for "Center Fitness", a gym. Built with
React + TypeScript + Vite, styled with Tailwind CSS and Radix UI primitives.
Frontend-only — there is no backend/server in this project.

## Tech stack
- Vite (dev server + build)
- React 19 + TypeScript
- Tailwind CSS v4
- Radix UI component primitives, lucide-react icons, framer-motion, wouter

## Running the app
- The `Start application` workflow runs `PORT=5000 BASE_PATH=/ npm run dev`
  (Vite's config requires `PORT` and `BASE_PATH` env vars to be set).
- `npm run build` — production build to `dist/public`
- `npm run typecheck` — TypeScript check

## Notes on the import
This project was extracted from a larger pnpm workspace/monorepo, so a few
things needed fixing to run standalone here:
- `package.json` used pnpm `catalog:` version placeholders and a
  `workspace:*` dependency (`@workspace/api-client-react`, which was unused
  in the code) — these were replaced with real pinned versions / removed.
- `tsconfig.json` extended a monorepo-root `tsconfig.base.json` and referenced
  a sibling package that don't exist here — made self-contained.
- `vite.config.ts`'s `@assets` alias and the cartographer plugin's `root`
  pointed two directories above the project (correct for the monorepo layout,
  wrong here) — repointed to this project's own `attached_assets` folder/root.

## User preferences
None recorded yet.

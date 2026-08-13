# Next.js Learning Journey

A step-by-step learning project documenting my progression through Next.js fundamentals, built with Next.js 16, React 19, TypeScript, and Tailwind CSS v4.

## 📚 Project Overview

This repository serves as a structured learning log for mastering Next.js App Router. Each commit represents a milestone in understanding core concepts — from project scaffolding to routing, layouts, and component architecture.

## 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | Next.js 16.3.0 (App Router) |
| Language | TypeScript 5 |
| UI Library | React 19.2.8 |
| Styling | Tailwind CSS v4 |
| Linting | ESLint 9 (Next.js config) |
| Package Manager | npm |

## 📁 Project Structure

```text
project/
├── app/                    # App Router pages & layouts
│   ├── layout.tsx          # Root layout (shared UI, fonts, metadata)
│   ├── page.tsx            # Home page (/)
│   ├── about/              # About section
│   │   ├── page.tsx        # /about
│   │   └── mission/        # Nested route
│   │       └── page.tsx    # /about/mission
│   └── products/           # Products section
│       └── page.tsx        # /products
├── public/                 # Static assets
├── .next/                  # Build output (git-ignored)
├── node_modules/           # Dependencies (git-ignored)
├── eslint.config.mjs       # ESLint flat config
├── next.config.ts          # Next.js configuration
├── package.json            # Project metadata & scripts
├── postcss.config.mjs      # PostCSS config (Tailwind v4)
├── tsconfig.json           # TypeScript configuration
└── README.md               # This file
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18.17 or later
- npm 9+

### Installation

```bash
# Navigate to project directory
cd project

# Install dependencies
npm install

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the app.

### Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start dev server with Turbopack |
| `npm run build` | Create production build |
| `npm run start` | Run production server |
| `npm run lint` | Run ESLint checks |

## 🎯 Learning Milestones

### Phase 1: Project Setup & Fundamentals
- [x] Initialize Next.js project with `create-next-app`
- [x] Configure TypeScript with strict mode
- [x] Set up Tailwind CSS v4 via PostCSS
- [x] Configure ESLint with Next.js recommended rules
- [x] Understand App Router directory structure

### Phase 2: Routing & Navigation
- [x] Create root layout (`app/layout.tsx`) with shared metadata & fonts
- [x] Build home page (`app/page.tsx`)
- [x] Implement nested routes:
  - `/about` → `app/about/page.tsx`
  - `/about/mission` → `app/about/mission/page.tsx`
  - `/products` → `app/products/page.tsx`
- [x] Learn file-based routing conventions

### Phase 3: Component Architecture (In Progress)
- [ ] Extract reusable components (Header, Footer, Card, etc.)
- [ ] Implement layout components for consistent structure
- [ ] Explore Server vs Client Components
- [ ] Add dynamic routing with `[slug]` parameters

### Phase 4: Data Fetching & State
- [ ] Server-side data fetching with `async/await` in components
- [ ] Client-side data fetching with SWR/React Query
- [ ] Form handling with Server Actions
- [ ] Caching strategies (fetch, revalidate, no-store)

### Phase 5: Advanced Features
- [ ] Middleware for auth/redirects
- [ ] Internationalization (i18n)
- [ ] Image optimization with `next/image`
- [ ] API routes with Route Handlers
- [ ] Streaming & Suspense boundaries

## 📖 Key Concepts Learned

| Concept | Description | Files |
|---------|-------------|-------|
| **App Router** | File-system based routing with nested layouts | `app/**/*` |
| **Root Layout** | Shared UI shell, metadata, font loading | `app/layout.tsx` |
| **Page Components** | Default export = route segment UI | `app/**/page.tsx` |
| **Nested Routes** | Folder hierarchy = URL hierarchy | `app/about/mission/` |
| **TypeScript** | Type-safe props, components, hooks | `tsconfig.json` |
| **Tailwind v4** | Utility-first CSS with native CSS variables | `globals.css`, `postcss.config.mjs` |

## 🔧 Configuration Highlights

### TypeScript (`tsconfig.json`)
- Strict mode enabled
- Path aliases (`@/*` → `./src/*` or `./app/*`)
- Next.js plugin for type-safe routing

### Next.js (`next.config.ts`)
- TypeScript configuration
- Image optimization defaults
- Experimental features as needed

### Tailwind CSS v4 (`postcss.config.mjs`)
```js
export default {
  plugins: {
    '@tailwindcss/postcss': {},
  },
}
```

## 📝 Development Notes

### File Naming Conventions
- **Pages**: `page.tsx` (required for route segments)
- **Layouts**: `layout.tsx` (optional, wraps children)
- **Components**: PascalCase (`Header.tsx`, `ProductCard.tsx`)
- **Utilities**: camelCase (`formatDate.ts`, `api.ts`)

### Server vs Client Components
- Default: **Server Components** (no `'use client'`)
- Add `'use client'` directive for:
  - Interactivity (event handlers, `useState`, `useEffect`)
  - Browser-only APIs (`window`, `localStorage`)
  - Third-party libraries requiring client context

### Import Aliases
```ts
import Link from 'next/link'
import { Metadata } from 'next'
import styles from './page.module.css' // CSS Modules
```

## 🚢 Deployment

### Vercel (Recommended)
1. Push to GitHub/GitLab/Bitbucket
2. Import project in [Vercel Dashboard](https://vercel.com/new)
3. Zero-config deployment with automatic preview URLs

### Manual Build
```bash
npm run build
npm run start
```

## 📚 Resources

- [Next.js Documentation](https://nextjs.org/docs) — Official guide
- [Next.js Learn Course](https://nextjs.org/learn) — Interactive tutorial
- [App Router Reference](https://nextjs.org/docs/app) — Routing, layouts, data fetching
- [TypeScript Handbook](https://www.typescriptlang.org/docs/) — Type system fundamentals
- [Tailwind CSS v4 Docs](https://tailwindcss.com/docs) — Utility-first styling

## 📄 License

MIT — Free for learning and experimentation.

---

> **Progress Tracking**: This README evolves with each learning milestone. Check git history for detailed commit-by-commit breakdown of concepts explored.
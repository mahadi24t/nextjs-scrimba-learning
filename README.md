# Next.js Learning Journey

A step-by-step learning repository documenting my progression through Next.js fundamentals — from zero to production-ready applications.

## 🎯 Repository Purpose

This monorepo-style structure captures the **entire learning arc**:

| Directory | Purpose | Origin |
|-----------|---------|--------|
| `/` (root) | Main learning workspace — manual App Router setup, custom configs | Built from scratch |
| `/project` | `create-next-app@latest` scaffold — reference for defaults & conventions | Generated via CLI |

The `project/` folder exists intentionally as a **learning artifact** — it shows what `create-next-app` bootstraps out of the box, so I can compare manual vs. scaffolded setups.

## 🛠 Tech Stack (Root Workspace)

| Layer | Technology |
|-------|------------|
| Framework | Next.js 16.3.0 (App Router) |
| Language | JavaScript (ESM) — *learning JS first, TS later* |
| UI Library | React 19.2.8 |
| Styling | Tailwind CSS v4 (via PostCSS) |
| Linting | ESLint 9 (Next.js flat config) |

## 📁 Repository Structure

```text
next-learn/
├── app/                    # Root workspace — manual App Router pages
│   ├── layout.jsx          # Root layout (shared UI, metadata, fonts)
│   ├── page.jsx            # Home page (/)
│   ├── about/              # About section
│   │   └── page.jsx        # /about
│   └── products/           # Products section
│       └── page.jsx        # /products
├── project/                # create-next-app@latest reference project
│   ├── app/                #   (TypeScript, stricter defaults)
│   ├── public/
│   ├── .next/
│   ├── eslint.config.mjs
│   ├── next.config.ts
│   ├── package.json
│   ├── postcss.config.mjs
│   ├── tsconfig.json
│   └── README.md           #   Project-specific docs
├── .next/                  # Build output (git-ignored)
├── node_modules/           # Dependencies (git-ignored)
├── .gitignore
├── package.json            # Root workspace scripts & deps
├── package-lock.json
└── README.md               # This file
```

## 🚀 Getting Started

### Root Workspace (Manual Setup)

```bash
# Install dependencies
npm install

# Start dev server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Reference Project (`/project`)

```bash
cd project
npm install
npm run dev
```

Runs on [http://localhost:3001](http://localhost:3001) (or next available port).

## 📚 Learning Milestones

### Phase 1: Manual App Router Setup (Root)
- [x] Initialize `package.json` with Next.js, React, React-DOM
- [x] Create `app/` directory with `layout.jsx` + `page.jsx`
- [x] Configure ESLint flat config (`eslint.config.mjs`)
- [x] Set up Tailwind CSS v4 via PostCSS
- [x] Add nested routes: `/about`, `/products`
- [x] Understand `layout.jsx` vs `page.jsx` roles

### Phase 2: Scaffolded Project Analysis (`/project`)
- [x] Run `npx create-next-app@latest project`
- [x] Compare folder structure & configs vs. manual setup
- [x] Note TypeScript defaults, strict mode, path aliases
- [x] Observe Turbopack integration
- [x] Document differences in `project/README.md`

### Phase 3: Core Concepts Deep Dive (In Progress)
- [ ] Server vs Client Components (`'use client'`)
- [ ] Data fetching patterns (`async/await` in Server Components)
- [ ] Dynamic routes (`[slug]`, `[...slug]`)
- [ ] Route groups (`(auth)`, `(marketing)`)
- [ ] Parallel & Intercepting Routes

### Phase 4: Advanced Features
- [ ] Middleware (`middleware.ts`)
- [ ] Server Actions & Forms
- [ ] Streaming & Suspense
- [ ] Image Optimization (`next/image`)
- [ ] API Routes (Route Handlers)
- [ ] Authentication patterns

### Phase 5: Production Readiness
- [ ] Environment variables & config
- [ ] CI/CD pipeline
- [ ] Performance optimization
- [ ] Deployment to Vercel
- [ ] Monitoring & Analytics

## 🔑 Key Concepts Learned (Root Workspace)

| Concept | Implementation | Files |
|---------|----------------|-------|
| **App Router Basics** | File-system routing, nested layouts | `app/layout.jsx`, `app/page.jsx` |
| **Root Layout** | Shared HTML shell, metadata, fonts | `app/layout.jsx` |
| **Page Segments** | Default export = route UI | `app/**/page.jsx` |
| **Nested Routes** | Folder = URL segment | `app/about/`, `app/products/` |
| **ESM + JSX** | `.jsx` extension, `import`/`export` | All `.jsx` files |
| **Tailwind v4** | CSS-first, native variables | `app/globals.css` (if added) |

## 🧪 Experiments & Comparisons

| Aspect | Root (Manual) | `/project` (Scaffolded) |
|--------|---------------|-------------------------|
| Language | JavaScript (`.jsx`) | TypeScript (`.tsx`) |
| Config Style | Flat ESLint, manual TS | Opinionated defaults |
| Strictness | Opt-in | Strict mode on by default |
| Path Aliases | Manual | `@/*` → `./src/*` |
| Turbopack | Manual opt-in | Enabled by default |
| Git Ignore | Minimal | Comprehensive |

## 📖 Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Next.js Learn Course](https://nextjs.org/learn)
- [App Router Reference](https://nextjs.org/docs/app)
- [React 19 Docs](https://react.dev)
- [Tailwind CSS v4](https://tailwindcss.com/docs)

## 📄 License

MIT — Learning repository, free to reference and fork.

---

> **Note**: This README tracks the **root workspace** learning path. For the scaffolded project's documentation, see [`project/README.md`](project/README.md).
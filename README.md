# Turborepo + TailwindCSS + Prisma Template

Production-ready monorepo starter template using Turborepo, TailwindCSS, Prisma, Bun, and TypeScript.

Built for scalable full-stack applications with shared packages, reusable UI components, centralized configs, and database tooling.

---

## Features

- ⚡ Turborepo monorepo architecture
- 🎨 Shared TailwindCSS configuration
- 🗄️ Shared Prisma setup & database client
- 📦 Shared packages support
- 🧩 Reusable UI components
- 🧹 Shared ESLint configuration
- 🔥 Bun-first workflow
- 🛠️ TypeScript support
- 🚀 Scalable project structure

---

## Tech Stack

| Tool        | Purpose                   |
| ----------- | ------------------------- |
| Turborepo   | Monorepo build system     |
| Bun         | Package manager & runtime |
| Next.js     | Frontend framework        |
| React       | UI library                |
| TailwindCSS | Styling                   |
| Prisma      | Database ORM              |
| ESLint      | Linting                   |
| TypeScript  | Type safety               |

---

## Project Structure

```txt
.
├── apps
│   ├── web/                    # Main frontend application
│   └── docs/                   # Documentation application
│
├── packages
│   ├── ui/                     # Shared UI components
│   ├── db/                     # Prisma schema & database client
│   ├── eslint-config/          # Shared ESLint configuration
│   └── tailwind-config/        # Shared Tailwind configuration
│
├── turbo.json
├── package.json
├── bun.lock
└── README.md
```

---

## Getting Started

### Use as Template

Click **"Use this template"** on GitHub to create a new repo from this template.

### Clone Repository

```bash
git clone https://github.com/anshul333y/turborepo-tailwind-prisma-template.git
cd turborepo-tailwind-prisma-template
```

### Install Dependencies

```bash
bun install
```

---

## Environment Variables

Create `packages/db/.env`:

```env
DATABASE_URL="postgresql://USER:PASSWORD@localhost:5432/db_name"
```

---

## Prisma Setup

```bash
bun run db:migrate       # Run migrations
bun run db:generate      # Generate Prisma client
bun run db:deploy        # Deploy migrations
bunx --bun prisma migrate reset  # Reset database
```

---

## Development

```bash
bun run dev    # Start all apps
bun run build  # Build everything
bun run lint   # Lint workspace
```

---

## TailwindCSS Setup

Shared Tailwind configuration lives inside `packages/tailwind-config`.

Example usage:

```css
@import "tailwindcss";
@source "../../../packages/ui/src";
```

---

## ESLint Setup

Shared ESLint configuration lives inside `packages/eslint-config`, allowing consistent linting rules across all apps and packages.

---

## Apps

### `apps/web`

Main frontend application.

### `apps/docs`

Documentation application for project docs, guides, and references.

---

## Shared Packages

### `@repo/ui`

Reusable UI components shared across applications.

### `@repo/db`

Shared Prisma client, schema, and database utilities.

### `@repo/tailwind-config`

Centralized TailwindCSS configuration for consistent styling.

### `@repo/eslint-config`

Reusable ESLint configuration shared across the monorepo.

---

## Turborepo Commands

```bash
bunx --bun turbo run dev
bunx --bun turbo run build
bunx --bun turbo run lint
```

---

## Why This Template?

This template is designed for:

- Full-stack applications
- Scalable architecture
- Shared frontend/backend code
- Multi-app projects
- Faster development workflows
- Reusable configurations
- Future project bootstrapping

---

## Recommended Additions

- Authentication
- API server
- Docker support
- CI/CD
- Shared Prettier config
- Testing setup
- Storybook
- Environment validation
- Redis
- Queue system

---

## Create New Apps

```bash
mkdir apps/admin
```

Add your new app and Turborepo will automatically include it in the workspace.

---

## Notes

- Uses Bun as the default package manager.
- Prisma client is shared through `@repo/db`.
- Tailwind configuration is centralized for consistency.
- ESLint configuration is shared across all apps/packages.
- Optimized for future scalability and template reuse.

---

## License

This project is licensed under the [MIT License](./LICENSE).

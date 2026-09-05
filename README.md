# Openlet

Openlet is an open-source flashcard application with FSRS spaced repetition. It supports several study modes, deck creation and import, image occlusion, folders, sharing, and account-backed synchronization.

The app uses React with TanStack Start and Router. Production data and authentication require a Supabase project.

## Run locally

Requirements: Node.js 20 or newer, pnpm, and a Supabase project.

```sh
pnpm install
cp .env.example .env
pnpm dev
```

Set the database and Supabase values documented in [`.env.example`](.env.example) before using account or sync flows.

## Build and test

```sh
pnpm build
pnpm lint
pnpm test
pnpm format:check
```

The FSRS implementation has focused tests in [lib/fsrs.test.ts](lib/fsrs.test.ts). Database changes are recorded in [drizzle/](drizzle/); apply them only to the intended Supabase project.

## Documentation

Start with [SECURITY.md](SECURITY.md) for security reporting and the source tree for current route and data behavior.

## License

Openlet is available under the [MIT license](LICENSE).

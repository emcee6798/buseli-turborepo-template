# Buseli Turborepo

Monorepo scaffolded with [Turborepo](https://turborepo.com/) and Yarn 4 (Berry) that wires up

- `packages/shared` – shared SCSS theme

## Getting started

```bash
yarn install
```

All workspace scripts run through Turbo:

| Script       | Description                                                            |
| ------------ | ---------------------------------------------------------------------- |
| `yarn dev`   | Runs `dev` in every workspace (use `--filter` to target specific apps) |
| `yarn build` | Builds all apps                                                        |
| `yarn lint`  | Type-checks each workspace                                             |

### Shared assets & config

The `@buseli/shared` package exposes:

- `@buseli/shared/styles.scss` – global styles shared by every app

Each app imports those exports either inside their entry files or build configs so changes propagate everywhere from one place.

### Testing builds

```bash
yarn turbo run build
```

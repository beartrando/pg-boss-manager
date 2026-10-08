# @shared/pg-boss-manager

pg-boss job queue manager for Lenvora services.

Depends on [`@shared/logger`](https://github.com/beartrando/logger) and [
`@shared/kafka-manager`](https://github.com/beartrando/kafka-manager).

## Development

```bash
pnpm install
pnpm dev    # tsc -w
pnpm build  # tsc -p tsconfig.json
```

## Release

1. Commit changes.
2. Bump `version` in `package.json` (semver).
3. Tag and push: `git tag v1.0.0 && git push --tags`.
4. Update consumers (`services/*/package.json`) to the new tag:
   `git+https://github.com/beartrando/pg-boss-manager.git#v1.0.0`.

> Packed consumers build the package automatically on `pnpm install` via the `prepare` script.

# White-label recipes strategy

This repository is the service/recipe catalog fork used by the desktop app.

## Why keep a recipes fork?

A recipes fork lets future white-label builds control:

- Available/default services
- Client-specific service bundles
- Service icons and metadata
- Custom internal services
- Emergency fixes without waiting for upstream

## Upstream sync workflow

```bash
git remote add upstream https://github.com/ferdium/ferdium-recipes.git # first time only
git fetch upstream
git checkout main
git merge upstream/main
```

## White-label approach

Prefer additive client-specific recipe bundles over modifying upstream recipes directly. If a client needs private/internal services, keep those additions clearly separated and documented.

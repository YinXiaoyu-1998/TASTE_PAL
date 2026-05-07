# TASTE_PAL Meta Repository

This repository is the parent orchestration repo for Taste Pal. It tracks the frontend and backend as Git submodules and pins a known-good combined version.

## Submodules

- `TASTE_PAL_FRONTEND` → `git@github.com:YinXiaoyu-1998/TASTE_PAL_FRONTEND.git`
- `TASTE_PAL_BACKEND` → `git@github.com:YinXiaoyu-1998/TASTE_PAL_BACKEND.git`

## Clone and Initialize

```bash
git clone git@github.com:YinXiaoyu-1998/TASTE_PAL.git
cd TASTE_PAL
git submodule update --init --recursive
```

## Daily Workflow

1. Work inside submodules as usual:
   - commit/push in `TASTE_PAL_FRONTEND`
   - commit/push in `TASTE_PAL_BACKEND`
2. Return to parent repo root.
3. Stage updated submodule pointers:
   ```bash
   git add TASTE_PAL_FRONTEND TASTE_PAL_BACKEND
   git commit -m "Bump frontend/backend submodule pointers"
   git push
   ```

## Update an Existing Clone

```bash
git pull
git submodule update --init --recursive
```

## Scope of This Parent Repo

- Tracked: `.gitignore`, `.gitmodules`, this `README.md`, and two submodule entries.
- Ignored by default: everything else under this folder unless explicitly allowlisted.

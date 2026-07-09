# AGENTS.md

Kalman filter data science project — notebooks only, no `.py` files.

## Toolchain

- **Python** 3.14.3, venv at `venv/`
- **Formatter:** Black (`black .`)
- **Linter + import sorter:** Ruff (`ruff check .`)

## Commands

```sh
venv\Scripts\activate                  # Windows — always activate first
ruff check .                          # lint
black --check .                       # verify formatting (CI-style)
ruff check --fix .                    # auto-fix + organize imports
black .                               # format
```

## Directory layout

- `index.ipynb` — overview / landing page (minimal code).
- `exemplos/` — example notebooks (the real code lives here).
- `tutoriais/` — tutorial notebooks, organized by topic.
- `arquivos/` — data files (CSV, etc.).
- `consultas/` — quick-reference markdown (e.g., pandas cheat sheet).

## Conventions

- No `.py` files — all code lives in notebook cells.
- Always format (Black) before committing.
- `.gitignore` excludes `venv/`, `Resumo Markdown*`, `.vscode*`, `.opencode*`, `.ruff_cache`.

## Notebook work

- LaTeX math: inline `$E = mc^2$`, display `$$ ... $$`.
- Markdown reference: `Resumo Markdown.txt`.
- Prefer descriptive link text over "clique aqui".

## Gotcha

- `README.md` links to `examples/example1.ipynb` but the actual path is `exemplos/examplo_1.ipynb` (Portuguese directory + typo in filename). Verify paths before creating new notebooks.

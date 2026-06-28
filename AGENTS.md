# AGENTS.md

Single-notebook data science project — Kalman filter applications.

## Toolchain

- **Python** 3.14.3, venv at `venv/`
- **Formatter:** Black (`black .`)
- **Linter + import sorter:** Ruff (`ruff check . && ruff format .`)
- **Notebook:** `index.ipynb` is the only source file

## Commands

```sh
ruff check .           # lint
ruff format .          # format (Black-equivalent; skip if Black used)
black --check .        # verify formatting (CI-style)
ruff check --fix .     # auto-fix + organize imports
```

## Conventions

- Format on save (Black, imports organized). Always format before committing.
- VS Code type-checking: basic mode (`python.analysis.typeCheckingMode: basic`).
- Only `index.ipynb` matters — no `.py` files. All code lives in notebook cells.
- `.gitignore` excludes `venv/`, `Resumo Markdown*`, `.vscode*`.

## Notebook work

- Use **markdown cells** for documentation (see `Resumo Markdown.txt` for MD reference).
- Use **Shift+Enter** to run a cell and advance; **Ctrl+Enter** to run in place.
- LaTeX math inline: `$E = mc^2$`; display: `$$ ... $$`.
- Prefer descriptive link text over "clique aqui".

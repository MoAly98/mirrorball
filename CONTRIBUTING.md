# Contributing to mirrorball

We welcome contributions to mirrorball. This guide explains how to set up a development environment, run tests and checks, and submit changes.

---

## 1. Prerequisites

- **Python 3.11 or later** (we test 3.11–3.13)
- **uv** for dependency management ([installation guide](https://docs.astral.sh/uv/))
- **pre-commit** hooks (install with `uv run pre-commit install --install-hooks`)

---

## 2. Setup

Clone and install dependencies:

```bash
git clone https://github.com/<your-org>/mirrorball.git
cd mirrorball
uv sync --group dev
```

---

## 3. Development workflow

1. Create a branch off `main`
2. Make your changes
3. Run checks (see next section)
4. Commit with a semantic prefix (e.g. `feat:`, `fix:`, `docs:`)
5. Push and open a pull request

---

## 4. Running checks

### Format and lint

```bash
uv run pre-commit run --all-files
```

### Tests

```bash
uv run pytest -ra --cov --cov-report=term
```

Add tests for every feature or bugfix. Keep output clean—no unexpected warnings or logs.

### Documentation

```bash
uv run --group docs sphinx-build -M html docs docs/_build/html -W --keep-going
```

Update docs whenever public APIs or workflows change.

---

## 5. Benchmark examples

TODO:: this is a stub

---

## 6. Pull requests

Use semantic commit messages (`feat:`, `fix:`, `docs:`, `refactor:`).

Pull requests should explain:
- Why the change is needed
- What changed
- How you tested it

---

## 7. Reporting issues

Bug reports should include:
- Error message and stack trace
- Steps to reproduce
- Environment details (`uv pip list`, Python version, OS)

For feature requests, describe the motivating benchmarking use case and desired outcome.

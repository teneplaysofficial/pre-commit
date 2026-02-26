# pre-commit

> A shared, versioned pre-commit configuration

[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/teneplaysofficial/pre-commit/main.svg)](https://results.pre-commit.ci/latest/github/teneplaysofficial/pre-commit/main)

## Includes

- biome
- prettier

## Installation

1. Install pre-commit:

   ```sh
   pip install pre-commit
   ```

2. Add `.pre-commit-config.yaml`:

   ```yml
   repos:
     - repo: https://github.com/teneplaysofficial/pre-commit
       rev: v1.0.0
       hooks:
         - id: prettier
   ```

3. Install hooks:
   ```sh
   pre-commit install
   ```

## CI Usage

```yml
- run: pre-commit run --all-files --show-diff-on-failure
```

## Available Hooks

| Hook ID    | Description                                                        |
| ---------- | ------------------------------------------------------------------ |
| `biome`    | Lints and formats project files using Biome.                       |
| `prettier` | Formats project files using your project's Prettier configuration. |

> [!CAUTION]
> Do not enable both **Prettier** and **Biome** formatting at the same time.
>
> If using both hooks, disable Biome’s formatter:
>
> ```json
> {
>   "formatter": { "enabled": false }
> }
> ```

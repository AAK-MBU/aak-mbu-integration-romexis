# aak-mbu-integration-romexis
Internal Python package for Romexis-related integrations.

## Installation

Install directly from GitHub:

```bash
pip install git+https://github.com/AAK-MBU/aak-mbu-integration-romexis.git
```

For reproducible builds, pin to a specific commit:

```bash
pip install git+https://github.com/AAK-MBU/aak-mbu-integration-romexis.git@<commit-hash>
```

---

## Commit Message Convention

Commit messages control versioning and must follow this format:

```
<type>: <short description>
```

### Supported Types

| Type       | Example                                | Version Impact |
|------------|----------------------------------------|----------------|
| fix        | fix: handle timeout                    | Patch          |
| feat       | feat: add export endpoint              | Minor          |
| feat!      | feat!: change API response format      | Major          |
| refactor   | refactor: simplify request builder     | None           |
| perf       | perf: improve query performance        | Patch          |

### Rules

- Use lowercase type
- Use imperative tone (e.g. "add", not "added")
- Keep the message short and clear
- Breaking changes must use `!` or include `BREAKING CHANGE` in the body

---

## Versioning

Do not manually update the version in `pyproject.toml`.

Versioning is handled automatically using semantic versioning:

- `fix:` increments patch version (1.0.0 → 1.0.1)
- `feat:` increments minor version (1.0.0 → 1.1.0)
- `feat!:` increments major version (1.0.0 → 2.0.0)

---

## Using This Package in Other Projects

```python
import romexis
```


Add as a dependency in `pyproject.toml`:

```toml
dependencies = [
  "aak-mbu-integration-romexis @ git+https://github.com/AAK-MBU/aak-mbu-integration-romexis.git@<commit-hash>"
]
```

Using a commit hash is recommended to ensure reproducibility.
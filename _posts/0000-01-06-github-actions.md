---
layout: slide
title: "GitHub Actions"
---

## GitHub Actions

Automatize builds, testes e deploys direto no GitHub.

---

### Exemplo básico

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Instalar dependências
        run: pip install -r requirements.txt
      - name: Rodar testes
        run: pytest
```

---

### Gatilhos comuns

`push` · `pull_request` · `schedule` · `workflow_dispatch`

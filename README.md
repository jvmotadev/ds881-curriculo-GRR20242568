# ds881-curriculo-GRR20242568

Currículo online desenvolvido com Hugo, publicado via GitHub Pages.  
Projeto individual da disciplina DS881 — UFPR.

🔗 **[Ver currículo em produção](https://jvmotadev.github.io/ds881-curriculo-GRR20242568/)**

---

## Execução local via Docker

### Pré-requisitos
- [Docker](https://www.docker.com/) instalado

### Passos

1. Clone o repositório:
```bash
   git clone https://github.com/jvmotadev/ds881-curriculo-GRR20242568.git
   cd ds881-curriculo-GRR20242568
```

2. Inicie o ambiente de desenvolvimento:
```bash
   docker compose up --build
```

3. Acesse no navegador: [http://localhost:8080](http://localhost:8080)

> Alterações nos arquivos de `site/` são refletidas automaticamente no browser (hot reload).

Para parar o servidor:
```bash
Ctrl+C
```

---

## Pipeline CI/CD

O workflow `.github/workflows/main.yml` executa automaticamente:

1. **Lint** — valida a estrutura do projeto
2. **Build** — compila o site com Hugo
3. **Deploy** — publica no GitHub Pages (apenas na `main`)

---

## Governança de código

- Push direto na `main` é bloqueado
- Toda alteração deve ser feita via branch + Pull Request
- O merge só é permitido com o pipeline CI em verde
- Commits seguem o padrão [Conventional Commits](https://www.conventionalcommits.org/)

---

## Branch Protection

A branch `main` está configurada com as seguintes regras:

- ✅ Require a pull request before merging
- ✅ Require status checks to pass before merging
- ✅ Require branches to be up to date before merging
- ✅ Block force pushes
- ✅ Restrict deletions

![alt text](/docs/image.png)
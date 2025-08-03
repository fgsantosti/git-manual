
````markdown
# Git Manual - Guia de Referência Rápida

## 📋 Índice
- [⚙️ Configuração Inicial](#️-configuração-inicial)
- [🚀 Inicialização de Repositório](#-inicialização-de-repositório)
- [📁 Adicionando Arquivos](#-adicionando-arquivos)
- [💾 Commits](#-commits)
- [📝 Tipos de Commit](#-tipos-de-commit-conventional-commits)
- [🌐 Repositório Remoto](#-repositório-remoto)
- [⬆️ Push](#️-push)
- [⬇️ Pull](#️-pull)
- [📥 Fetch](#-fetch)
- [🌿 Branches](#-branches)
- [🔧 Comandos Úteis Extras](#-comandos-úteis-extras)
- [📚 Fluxo de Trabalho Básico](#-fluxo-de-trabalho-básico)
- [⚠️ Dicas Importantes](#️-dicas-importantes)

---

## ⚙️ Configuração Inicial
```bash
git config --global user.email "seu-email@exemplo.com"
git config --global user.name "Seu Nome"
````

---

## 🚀 Inicialização de Repositório

```bash
git init                              # Inicializa repositório na pasta atual
git init <nome-do-repositorio>        # Cria e inicializa novo repositório
git init --bare                       # Cria repositório bare (servidor)
git init --bare <nome-do-repositorio> # Cria repositório bare com nome específico
```

---

## 📁 Adicionando Arquivos

```bash
git add .                    # Adiciona todos os arquivos
git add <nome-do-arquivo>    # Adiciona arquivo específico
git add -N                   # Adiciona arquivos novos (tracked)
git add -n                   # Dry run - mostra o que seria adicionado
git add -u                   # Adiciona apenas arquivos modificados
git add -A                   # Adiciona todos (novos, modificados, deletados)
git add -i                   # Modo interativo
git add -p                   # Adiciona partes específicas (patch mode)
```

---

## 💾 Commits

```bash
git commit -m "mensagem do commit"           # Commit com mensagem
git commit -a -m "mensagem do commit"        # Commit de todos os arquivos modificados
```

---

## 📝 Tipos de Commit (Conventional Commits)

| Tipo     | Descrição               |
| -------- | ----------------------- |
| feat     | Nova funcionalidade     |
| fix      | Correção de bug         |
| docs     | Documentação            |
| style    | Formatação/estilo       |
| refactor | Refatoração de código   |
| perf     | Melhoria de performance |
| test     | Testes                  |
| build    | Ferramentas de build    |
| ci       | CI/CD                   |
| chore    | Tarefas de manutenção   |

**Exemplo:**

```bash
git commit -m "feat: adiciona função de login"
```

---

## 🌐 Repositório Remoto

### Configuração

```bash
git remote add origin <url-do-repositorio>
git remote set-url origin <url-do-repositorio>
```

### Informações

```bash
git remote -v
git remote show origin
```

### Gerenciamento

```bash
git remote rm origin
git remote rename origin <novo-nome>
```

---

## ⬆️ Push

```bash
git push origin main
git push origin <nome-do-branch>
git push origin <nome-do-branch> --force
git push --force-with-lease origin main
```

---

## ⬇️ Pull

```bash
git pull origin main
git pull origin <nome-do-branch>
git pull origin <nome-do-branch> --rebase
git pull origin <nome-do-branch> --rebase --autostash
```

---

## 📥 Fetch

```bash
git fetch origin
git fetch origin <nome-do-branch>
git fetch origin <nome-do-branch> --prune
```

---

## 🌿 Branches

### Criação e Navegação

```bash
git branch <nome-do-branch>
git checkout <nome-do-branch>
git checkout -b <nome-do-branch>
git checkout -B <nome-do-branch>
```

### Gerenciamento

```bash
git branch -d <nome-do-branch>
git branch -D <nome-do-branch>
git branch -m <novo-nome>
git branch -M <novo-nome>
```

### Visualização

```bash
git branch
git branch -a
git branch -r
git branch -vv
git branch --merged
git branch --no-merged
```

### Desfazer Alterações

```bash
git checkout -- <nome-do-arquivo>
```

---

## 🔧 Comandos Úteis Extras

```bash
git status
git log
git log --oneline
git diff
git stash
git stash pop
```

---

## 📚 Fluxo de Trabalho Básico

1. Clone/Init: `git clone <url>` ou `git init`
2. Configure: `git config --global user.name/email`
3. Trabalhe: Edite seus arquivos
4. Stage: `git add .`
5. Commit: `git commit -m "mensagem"`
6. Push: `git push origin main`

---

## ⚠️ Dicas Importantes

* Use `--force-with-lease` ao invés de `--force` para maior segurança
* Sempre faça `git pull` antes de `git push`
* Use mensagens de commit descritivas
* Crie branches para features: `git checkout -b feature/nova-funcionalidade`

---

> Manual criado para referência rápida dos comandos Git mais utilizados.

```
```

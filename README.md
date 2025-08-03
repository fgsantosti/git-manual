

# Git Manual - Guia de Referência Rápida

## 📋 Índice
- [Configuração Inicial](#configuração-inicial)
- [Inicialização de Repositório](#inicialização-de-repositório)
- [Adicionando Arquivos](#adicionando-arquivos)
- [Commits](#commits)
- [Repositório Remoto](#repositório-remoto)
- [Push](#push)
- [Pull](#pull)
- [Fetch](#fetch)
- [Branches](#branches)
- [Tipos de Commit](#tipos-de-commit)

---

## ⚙️ Configuração Inicial

```bash
# Configura email e nome globalmente
git config --global user.email "seu-email@exemplo.com"
git config --global user.name "Seu Nome"
```

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
git commit -a -m "mensagem do commit"       # Commit de todos os arquivos modificados
```

### 📝 Tipos de Commit (Conventional Commits)

| Tipo | Descrição |
|------|-----------|
| `feat` | Nova funcionalidade |
| `fix` | Correção de bug |
| `docs` | Documentação |
| `style` | Formatação/estilo |
| `refactor` | Refatoração de código |
| `perf` | Melhoria de performance |
| `test` | Testes |
| `build` | Ferramentas de build |
| `ci` | CI/CD |
| `chore` | Tarefas de manutenção |

**Exemplo:** `git commit -m "feat: adiciona função de login"`

---

## 🌐 Repositório Remoto

```bash
# Configuração
git remote add origin <url-do-repositorio>     # Adiciona repositório remoto
git remote set-url origin <url-do-repositorio> # Altera URL do repositório

# Informações
git remote -v                    # Lista repositórios remotos
git remote show origin           # Mostra informações detalhadas

# Gerenciamento
git remote rm origin             # Remove repositório remoto
git remote rename origin <novo-nome> # Renomeia repositório remoto
```

---

## ⬆️ Push

```bash
git push origin main                        # Push para branch main
git push origin <nome-do-branch>            # Push para branch específico
git push origin <nome-do-branch> --force   # Push forçado (cuidado!)
git push --force-with-lease origin main    # Push forçado com segurança
```

---

## ⬇️ Pull

```bash
git pull origin main                           # Pull do branch main
git pull origin <nome-do-branch>              # Pull de branch específico
git pull origin <nome-do-branch> --rebase     # Pull com rebase
git pull origin <nome-do-branch> --rebase --autostash # Pull com rebase e autostash
```

---

## 📥 Fetch

```bash
git fetch origin                        # Busca atualizações do remoto
git fetch origin <nome-do-branch>       # Busca branch específico
git fetch origin <nome-do-branch> --prune # Remove referências de branches deletados
```

---

## 🌿 Branches

### Criação e Navegação
```bash
git branch <nome-do-branch>              # Cria novo branch
git checkout <nome-do-branch>            # Muda para o branch
git checkout -b <nome-do-branch>         # Cria e muda para novo branch
git checkout -B <nome-do-branch>         # Força criação e mudança
```

### Gerenciamento
```bash
git branch -d <nome-do-branch>           # Deleta branch (seguro)
git branch -D <nome-do-branch>           # Deleta branch (forçado)
git branch -m <novo-nome>                # Renomeia branch atual
git branch -M <novo-nome>                # Renomeia branch (forçado)
```

### Visualização
```bash
git branch                               # Lista branches locais
git branch -a                            # Lista todos os branches
git branch -r                            # Lista branches remotos
git branch -vv                           # Lista com informações detalhadas
git branch --merged                      # Branches já mesclados
git branch --no-merged                   # Branches não mesclados
```

### Desfazer Alterações
```bash
git checkout -- <nome-do-arquivo>       # Desfaz alterações no arquivo
```

---

## 🔧 Comandos Úteis Extras

```bash
git status                               # Status do repositório
git log                                  # Histórico de commits
git log --oneline                        # Histórico resumido
git diff                                 # Diferenças não commitadas
git stash                                # Salva alterações temporariamente
git stash pop                            # Recupera alterações do stash
```

---

## 📚 Fluxo de Trabalho Básico

1. **Clone/Init:** `git clone <url>` ou `git init`
2. **Configure:** `git config --global user.name/email`
3. **Trabalhe:** Edite seus arquivos
4. **Stage:** `git add .`
5. **Commit:** `git commit -m "mensagem"`
6. **Push:** `git push origin main`

---

## ⚠️ Dicas Importantes

- Use `--force-with-lease` ao invés de `--force` para maior segurança
- Sempre faça `git pull` antes de `git push`
- Use mensagens de commit descritivas
- Crie branches para features: `git checkout -b feature/nova-funcionalidade`

---


# Git Manual - Guia de Referência Rápida

## 📋 Índice
- [Configuração Inicial](#configuração-inicial)
- [Inicialização de Repositório](#inicialização-de-repositório)
- [Adicionando Arquivos](#adicionando-arquivos)
- [Commits](#commits)
- [Repositório Remoto](#repositório-remoto)
- [Push](#push)
- [Pull](#pull)
- [Fetch](#fetch)
- [Branches](#branches)
- [Tipos de Commit](#tipos-de-commit)

---

## ⚙️ Configuração Inicial

```bash
# Configura email e nome globalmente
git config --global user.email "seu-email@exemplo.com"
git config --global user.name "Seu Nome"
```

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
git commit -a -m "mensagem do commit"       # Commit de todos os arquivos modificados
```

### 📝 Tipos de Commit (Conventional Commits)

| Tipo | Descrição |
|------|-----------|
| `feat` | Nova funcionalidade |
| `fix` | Correção de bug |
| `docs` | Documentação |
| `style` | Formatação/estilo |
| `refactor` | Refatoração de código |
| `perf` | Melhoria de performance |
| `test` | Testes |
| `build` | Ferramentas de build |
| `ci` | CI/CD |
| `chore` | Tarefas de manutenção |

**Exemplo:** `git commit -m "feat: adiciona função de login"`

---

## 🌐 Repositório Remoto

```bash
# Configuração
git remote add origin <url-do-repositorio>     # Adiciona repositório remoto
git remote set-url origin <url-do-repositorio> # Altera URL do repositório

# Informações
git remote -v                    # Lista repositórios remotos
git remote show origin           # Mostra informações detalhadas

# Gerenciamento
git remote rm origin             # Remove repositório remoto
git remote rename origin <novo-nome> # Renomeia repositório remoto
```

---

## ⬆️ Push

```bash
git push origin main                        # Push para branch main
git push origin <nome-do-branch>            # Push para branch específico
git push origin <nome-do-branch> --force   # Push forçado (cuidado!)
git push --force-with-lease origin main    # Push forçado com segurança
```

---

## ⬇️ Pull

```bash
git pull origin main                           # Pull do branch main
git pull origin <nome-do-branch>              # Pull de branch específico
git pull origin <nome-do-branch> --rebase     # Pull com rebase
git pull origin <nome-do-branch> --rebase --autostash # Pull com rebase e autostash
```

---

## 📥 Fetch

```bash
git fetch origin                        # Busca atualizações do remoto
git fetch origin <nome-do-branch>       # Busca branch específico
git fetch origin <nome-do-branch> --prune # Remove referências de branches deletados
```

---

## 🌿 Branches

### Criação e Navegação
```bash
git branch <nome-do-branch>              # Cria novo branch
git checkout <nome-do-branch>            # Muda para o branch
git checkout -b <nome-do-branch>         # Cria e muda para novo branch
git checkout -B <nome-do-branch>         # Força criação e mudança
```

### Gerenciamento
```bash
git branch -d <nome-do-branch>           # Deleta branch (seguro)
git branch -D <nome-do-branch>           # Deleta branch (forçado)
git branch -m <novo-nome>                # Renomeia branch atual
git branch -M <novo-nome>                # Renomeia branch (forçado)
```

### Visualização
```bash
git branch                               # Lista branches locais
git branch -a                            # Lista todos os branches
git branch -r                            # Lista branches remotos
git branch -vv                           # Lista com informações detalhadas
git branch --merged                      # Branches já mesclados
git branch --no-merged                   # Branches não mesclados
```

### Desfazer Alterações
```bash
git checkout -- <nome-do-arquivo>       # Desfaz alterações no arquivo
```

---

## 🔧 Comandos Úteis Extras

```bash
git status                               # Status do repositório
git log                                  # Histórico de commits
git log --oneline                        # Histórico resumido
git diff                                 # Diferenças não commitadas
git stash                                # Salva alterações temporariamente
git stash pop                            # Recupera alterações do stash
```

---

## 📚 Fluxo de Trabalho Básico

1. **Clone/Init:** `git clone <url>` ou `git init`
2. **Configure:** `git config --global user.name/email`
3. **Trabalhe:** Edite seus arquivos
4. **Stage:** `git add .`
5. **Commit:** `git commit -m "mensagem"`
6. **Push:** `git push origin main`

---

## ⚠️ Dicas Importantes

- Use `--force-with-lease` ao invés de `--force` para maior segurança
- Sempre faça `git pull` antes de `git push`
- Use mensagens de commit descritivas
- Crie branches para features: `git checkout -b feature/nova-funcionalidade`

---


# Git Manual - Guia de Referência Rápida

## 📋 Índice
- [Configuração Inicial](#configuração-inicial)
- [Inicialização de Repositório](#inicialização-de-repositório)
- [Adicionando Arquivos](#adicionando-arquivos)
- [Commits](#commits)
- [Repositório Remoto](#repositório-remoto)
- [Push](#push)
- [Pull](#pull)
- [Fetch](#fetch)
- [Branches](#branches)
- [Tipos de Commit](#tipos-de-commit)

---

## ⚙️ Configuração Inicial

```bash
# Configura email e nome globalmente
git config --global user.email "seu-email@exemplo.com"
git config --global user.name "Seu Nome"
```

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
git commit -a -m "mensagem do commit"       # Commit de todos os arquivos modificados
```

### 📝 Tipos de Commit (Conventional Commits)

| Tipo | Descrição |
|------|-----------|
| `feat` | Nova funcionalidade |
| `fix` | Correção de bug |
| `docs` | Documentação |
| `style` | Formatação/estilo |
| `refactor` | Refatoração de código |
| `perf` | Melhoria de performance |
| `test` | Testes |
| `build` | Ferramentas de build |
| `ci` | CI/CD |
| `chore` | Tarefas de manutenção |

**Exemplo:** `git commit -m "feat: adiciona função de login"`

---

## 🌐 Repositório Remoto

```bash
# Configuração
git remote add origin <url-do-repositorio>     # Adiciona repositório remoto
git remote set-url origin <url-do-repositorio> # Altera URL do repositório

# Informações
git remote -v                    # Lista repositórios remotos
git remote show origin           # Mostra informações detalhadas

# Gerenciamento
git remote rm origin             # Remove repositório remoto
git remote rename origin <novo-nome> # Renomeia repositório remoto
```

---

## ⬆️ Push

```bash
git push origin main                        # Push para branch main
git push origin <nome-do-branch>            # Push para branch específico
git push origin <nome-do-branch> --force   # Push forçado (cuidado!)
git push --force-with-lease origin main    # Push forçado com segurança
```

---

## ⬇️ Pull

```bash
git pull origin main                           # Pull do branch main
git pull origin <nome-do-branch>              # Pull de branch específico
git pull origin <nome-do-branch> --rebase     # Pull com rebase
git pull origin <nome-do-branch> --rebase --autostash # Pull com rebase e autostash
```

---

## 📥 Fetch

```bash
git fetch origin                        # Busca atualizações do remoto
git fetch origin <nome-do-branch>       # Busca branch específico
git fetch origin <nome-do-branch> --prune # Remove referências de branches deletados
```

---

## 🌿 Branches

### Criação e Navegação
```bash
git branch <nome-do-branch>              # Cria novo branch
git checkout <nome-do-branch>            # Muda para o branch
git checkout -b <nome-do-branch>         # Cria e muda para novo branch
git checkout -B <nome-do-branch>         # Força criação e mudança
```

### Gerenciamento
```bash
git branch -d <nome-do-branch>           # Deleta branch (seguro)
git branch -D <nome-do-branch>           # Deleta branch (forçado)
git branch -m <novo-nome>                # Renomeia branch atual
git branch -M <novo-nome>                # Renomeia branch (forçado)
```

### Visualização
```bash
git branch                               # Lista branches locais
git branch -a                            # Lista todos os branches
git branch -r                            # Lista branches remotos
git branch -vv                           # Lista com informações detalhadas
git branch --merged                      # Branches já mesclados
git branch --no-merged                   # Branches não mesclados
```

### Desfazer Alterações
```bash
git checkout -- <nome-do-arquivo>       # Desfaz alterações no arquivo
```

---

## 🔧 Comandos Úteis Extras

```bash
git status                               # Status do repositório
git log                                  # Histórico de commits
git log --oneline                        # Histórico resumido
git diff                                 # Diferenças não commitadas
git stash                                # Salva alterações temporariamente
git stash pop                            # Recupera alterações do stash
```

---

## 📚 Fluxo de Trabalho Básico

1. **Clone/Init:** `git clone <url>` ou `git init`
2. **Configure:** `git config --global user.name/email`
3. **Trabalhe:** Edite seus arquivos
4. **Stage:** `git add .`
5. **Commit:** `git commit -m "mensagem"`
6. **Push:** `git push origin main`

---

## ⚠️ Dicas Importantes

- Use `--force-with-lease` ao invés de `--force` para maior segurança
- Sempre faça `git pull` antes de `git push`
- Use mensagens de commit descritivas
- Crie branches para features: `git checkout -b feature/nova-funcionalidade`

---

> Manual criado para referência rápida dos comandos Git mais utilizados.

```
```

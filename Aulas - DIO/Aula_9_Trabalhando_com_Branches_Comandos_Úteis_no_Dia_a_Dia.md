### **Aula 9: Comandos Úteis com Branches (resumo fácil)**

---

#### 1. **git pull = baixar + mesclar**

* `git pull` é a combinação de dois comandos:

```bash
git fetch  # baixa as mudanças do repositório remoto para seu computador (sem misturar)
git merge  # junta essas mudanças com seu trabalho atual
```

* Você pode fazer separado:

```bash
git fetch origin main      # baixa as mudanças da branch main
git diff main origin/main  # vê a diferença entre sua main e a que baixou
git merge origin/main      # junta as mudanças baixadas com a sua main
```

---

#### 2. **Clonar uma branch específica:**

```bash
git clone URL --branch teste --single-branch
```

> Baixa só a branch "teste", não todo o projeto.

---

#### 3. **Guardar mudanças temporariamente com stash:**

* `git stash` guarda as mudanças que você fez mas ainda não quer salvar em commit, para voltar a um estado limpo.

```bash
git stash          # guarda as mudanças atuais
git stash list     # mostra as stashes guardadas
```

---

#### 4. **Trabalhar com stash e branches:**

```bash
git checkout -b teste-2  # cria e muda para a branch teste-2
git checkout teste       # muda para a branch teste
git stash list           # ver as stashes guardadas
git stash pop            # aplica a stash mais recente e remove da lista
git stash apply          # aplica a stash mais recente mas mantém na lista
```
### **Aula 6: Desfazendo Alterações no Repositório Local (resumo fácil)**

Às vezes, você precisa **voltar atrás** ou corrigir algo que fez no Git. Aqui estão os comandos para isso:

---

#### 1. **Apagar todo o controle do Git numa pasta (cuidado!):**

```bash
rm -rf .git
```

> Apaga a pasta oculta `.git`, ou seja, remove todo o histórico e controle do Git daquele projeto.

---

#### 2. **Desfazer mudanças em um arquivo (voltar ao último estado salvo):**

```bash
git restore README.md
```

> Restaura o arquivo, desfazendo alterações que ainda não foram salvas no commit.

---

#### 3. **Mudar a mensagem do último commit:**

```bash
git commit --amend -m "nova mensagem"
```

> Altera a mensagem do último commit feito, sem criar um novo.

---

#### 4. **Voltar para um commit anterior (várias formas):**

* **`git reset --soft HASH`**
  Volta para o commit indicado, mantendo os arquivos preparados para o próximo commit (na “staging area”).

* **`git reset --mixed HASH`**
  Volta para o commit indicado, mas deixa os arquivos como não preparados (untracked ou modificados).

* **`git reset --hard HASH`**
  Apaga tudo após o commit indicado, incluindo mudanças nos arquivos. Cuidado, é como jogar tudo na lixeira.

---

#### 5. **Ver o histórico de todos os movimentos (mesmo os que você desfez):**

```bash
git reflog
```

> Mostra uma lista de todos os comandos de commit e reset que você fez, para recuperar estados antigos.

---

#### 6. **Explicação do exemplo de comandos:**

1.

```bash
touch resumos/aula-01.md resumos/aula-02.md
```

> Criou dois arquivos novos.

2.

```bash
git reset resumos/aula-01.md
```

> Tirou o arquivo `aula-01.md` da área de preparação (staging area), mas ele continua no disco.

3.

```bash
git status
```

> Mostra que `aula-01.md` não está preparado para commit, e `aula-02.md` ainda está preparado.

4.

```bash
git restore --staged resumos/aula-02.md
```

> Também removeu `aula-02.md` da área de preparação, ou seja, nenhum dos dois arquivos está pronto para ser salvo.
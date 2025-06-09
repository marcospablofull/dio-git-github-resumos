### **Aula 5: Salvando Alterações no Repositório Local (resumo fácil)**

Para controlar seu projeto, o Git precisa saber o que você mudou, salvar essas mudanças e organizar tudo.

---

#### 1. **Verificar o status dos arquivos:**

```bash
git status
```

* **Untracked files:** arquivos novos que o Git ainda não está acompanhando.
* **Changes to be committed:** arquivos que você já adicionou para salvar (via `git add`), esperando o commit.
* **Nothing to commit, working tree clean:** tudo está salvo e nada mudou.

---

#### 2. **Criar um arquivo novo:**

```bash
touch README.md
```

> Cria um arquivo chamado README.md (pode ser usado para descrição do projeto).

---

#### 3. **Adicionar arquivo para salvar no Git:**

```bash
git add README.md
```

> Prepara o arquivo para ser salvo no próximo commit.

---

#### 4. **Salvar as mudanças no repositório local:**

```bash
git commit -m "Commit inicial"
```

> Salva oficialmente as mudanças com uma mensagem para explicar o que foi feito.

---

#### 5. **Ver o histórico de commits:**

```bash
git log
```

> Mostra a lista das versões salvas, quem fez e quando.

---

#### 6. **Git não reconhece pastas vazias:**

* Para o Git “ver” uma pasta, ela precisa ter pelo menos um arquivo.
* Por exemplo, crie um arquivo vazio:

```bash
touch aulas/.gitkeep
```

> Esse arquivo é só para o Git reconhecer a pasta.

---

#### 7. **Ignorar arquivos e pastas com `.gitignore`:**

* Arquivos que você não quer salvar no Git (como arquivos temporários, senhas, etc) devem ser listados no `.gitignore`.
* Para criar e ignorar uma pasta chamada `resumos/`:

```bash
echo resumos/ > .gitignore
```

* Para apagar tudo que estava no `.gitignore` antes:

```bash
echo > .gitignore
```

---

#### 8. **Adicionar tudo que mudou:**

```bash
git add .
```

> Prepara todos os arquivos modificados para salvar.

---

#### 9. **Quando você modifica um arquivo já salvo:**

* O Git mostra que ele está modificado.
* Se você desfizer as mudanças e o arquivo voltar ao estado salvo, o Git não mostra modificação.
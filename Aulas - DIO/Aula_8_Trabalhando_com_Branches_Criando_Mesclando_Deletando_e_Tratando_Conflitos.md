### **Aula 8: Trabalhando com Branches (resumo fácil)**

---

#### O que é uma **branch**?

* É um “ramo” do projeto, uma linha paralela de desenvolvimento.
* Cada branch aponta para um ponto (commit) no histórico.
* Quando você cria uma nova branch, ela começa copiando o estado da branch atual.
* Você pode trabalhar nela separado da branch principal (main).

---

#### Comandos importantes:

* **Criar e mudar para uma nova branch chamada "teste":**

```bash
git checkout -b teste
```

* **Ver os últimos commits e em quais branches eles estão:**

```bash
git log
```

* **Voltar para a branch principal (main):**

```bash
git checkout main
```

* **Mostrar as branches existentes e seus últimos commits:**

```bash
git branch -v
```

* **Juntar (mesclar) a branch "teste" na branch atual:**

```bash
git merge teste
```

* \**Ver em qual branch você está (a branch atual aparece com *):**

```bash
git branch
```

* **Deletar a branch "teste" depois que foi mesclada:**

```bash
git branch -d teste
```

---

#### O que é conflito de merge?

* Acontece quando duas branches modificam a mesma parte do arquivo de forma diferente.
* O Git não sabe qual versão usar e pede para você resolver.

---

#### Como resolver um conflito?

1. Edite o arquivo que está com conflito.
2. Escolha qual versão quer manter (ou faça uma mistura).
3. Remova os marcadores que o Git adiciona:

   ```
   <<<<<<< HEAD
   sua versão
   =======
   outra versão
   >>>>>>>
   ```
4. Salve o arquivo.
5. Adicione o arquivo para o commit:

   ```bash
   git add nome-do-arquivo
   ```
6. Faça o commit para finalizar a resolução:

   ```bash
   git commit
   ```
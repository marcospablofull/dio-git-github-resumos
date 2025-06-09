### **Aula 1: Configurando o Git (resumo para iniciantes)**

Antes de usar o Git, é importante configurar quem você é. Assim, ele sabe quem está fazendo as alterações.

#### **Comandos principais:**

1. **Definir seu nome:**

```bash
git config --global user.name "Seu Nome"
```

2. **Definir seu e-mail:**

```bash
git config --global user.email seu@email.com
```

> Isso identifica suas contribuições nos projetos.

3. **Verificar o nome configurado:**

```bash
git config user.name
```

4. **Verificar o e-mail configurado:**

```bash
git config user.email
```

5. **Ver o nome do ramo (branch) padrão:**

```bash
git config init.defaultBranch
```

6. **Definir o nome do ramo padrão como “main”:**

```bash
git config --global init.defaultBranch main
```

> “main” é o nome usado atualmente no lugar de “master”.

7. **Ver todas as configurações feitas:**

```bash
git config --global --list
```

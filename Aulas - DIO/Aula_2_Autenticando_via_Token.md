### **Aula 2: Autenticando via Token (resumo fácil)**

Para usar o Git com o GitHub via internet, você precisa se conectar com segurança. Hoje, o jeito recomendado é usar um **token**, que é tipo uma senha especial.

---

#### 1. **Clonar um projeto com token:**

```bash
git clone URL-HTTPS
```

* Para funcionar, a URL precisa de um **token** (uma senha gerada no GitHub).
* Se você não tiver salvo suas credenciais (nome e senha/token), o Git vai pedir para você digitar.

---

#### 2. **Guardar suas credenciais para não digitar toda hora:**

* Salvar para sempre no computador (armazenar):

```bash
git config --global credential.helper store
```

* Guardar só temporariamente na memória (cache):

```bash
git config --global credential.helper cache
```

* Ver qual método está configurado:

```bash
git config --global credential.helper
```

* Mostrar de onde vem essa configuração:

```bash
git config --global --show-origin credential.helper
```

---

#### 3. **Comandos para ver arquivos de configuração e credenciais:**

* **`cat`** é um comando para mostrar o conteúdo de um arquivo.

* Mostrar o arquivo de configurações do Git:

```bash
cat .gitconfig
```

* Mostrar o arquivo onde as credenciais podem estar salvas (não recomendado salvar assim, pois não é seguro):

```bash
cat .git-credentials
```

---

#### 4. **Remover credenciais salvas no Windows:**

Se você salvou seu token ou senha e quer apagar para proteger sua conta:

* Abra o menu **Iniciar**.
* Procure por **Gerenciador de Credenciais**.
* Vá em **Credenciais do Windows**.
* Encontre as entradas relacionadas ao Git ou GitHub.
* Clique nelas e escolha **Remover** ou **Excluir**.

Assim, o Git vai pedir suas credenciais novamente na próxima vez que você usar.
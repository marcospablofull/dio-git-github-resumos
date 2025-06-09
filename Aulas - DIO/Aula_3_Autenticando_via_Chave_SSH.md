### **Aula 3: Autenticando via Chave SSH (resumo fácil)**

Outra forma segura de conectar o Git ao GitHub é usando **chaves SSH**. É uma “chave digital” que prova quem é você, sem precisar digitar senha toda hora.

---

#### Passos principais:

1. **Verificar se já tem chaves SSH no seu computador:**

```bash
ls -al ~/.ssh
```

> Lista as chaves que você já tem na pasta secreta do SSH.

---

2. **Gerar uma nova chave SSH (se não tiver):**

```bash
ssh-keygen -t ed25519 -C "seu_email@example.com"
```

> Cria uma nova chave segura, associada ao seu e-mail.

---

3. **Iniciar o agente SSH para gerenciar a chave:**

```bash
eval "$(ssh-agent -s)"
```

---

4. **Adicionar sua chave SSH ao agente:**

```bash
ssh-add ~/.ssh/id_ed25519
```

---

5. **Adicionar a chave SSH ao GitHub (na sua conta):**

* Abra o arquivo da chave pública:

```bash
cat ~/.ssh/id_ed25519.pub
```

* Copie todo o conteúdo que aparecer.
* No GitHub, vá em **Configurações > SSH and GPG keys > New SSH key**.
* Cole a chave e salve.

---

6. **Clonar um projeto usando a conexão SSH:**

```bash
git clone git@github.com:usuario/repositorio.git
```

> Use o link SSH, não o HTTPS.

---

Pronto! Agora o Git usa essa chave para se conectar automaticamente ao GitHub, sem pedir senha.

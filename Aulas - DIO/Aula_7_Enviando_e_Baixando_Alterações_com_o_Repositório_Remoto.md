### **Aula 7: Enviando e Baixando Alterações com o Repositório Remoto (resumo fácil)**

Quando você trabalha com Git, pode enviar suas mudanças para um lugar online (GitHub) e também baixar atualizações feitas por outras pessoas.

---

#### Passos para conectar seu projeto local ao GitHub:

1. **Adicionar o repositório remoto (online):**

```bash
git remote add origin URL-do-GitHub
```

> Esse comando conecta sua pasta local ao repositório online, e o nome padrão dessa conexão é **origin**.

---

2. **Enviar suas mudanças para o GitHub (primeiro envio):**

```bash
git push -u origin main
```

> Envia a branch principal (“main”) para o GitHub e cria uma referência para facilitar futuros envios.

---

3. **Baixar mudanças do GitHub para sua máquina:**

```bash
git pull
```

> Atualiza seu projeto local com as mudanças feitas no repositório remoto.

---

Assim, você mantém seu trabalho sincronizado entre sua máquina e o GitHub.
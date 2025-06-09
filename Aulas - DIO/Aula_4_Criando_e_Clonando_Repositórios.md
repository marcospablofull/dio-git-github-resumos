### **Aula 4: Criando e Clonando Repositórios (resumo fácil)**

Você pode ter um projeto Git na sua máquina de duas maneiras:

---

#### 1. **Criar um repositório Git do zero numa pasta que você já tem:**

* Criar uma pasta nova:

```bash
mkdir nome-da-pasta
```

* Entrar na pasta:

```bash
cd nome-da-pasta
```

* Transformar essa pasta em um repositório Git:

```bash
git init
```

> Isso começa a controlar as mudanças nessa pasta.

---

#### O que é o arquivo **.git**?

* Quando você cria um repositório Git, ele cria uma pasta oculta chamada **.git** dentro da pasta do projeto.
* Essa pasta **.git** guarda todas as informações importantes para o Git controlar seu projeto: histórico, versões, configurações.
* Sem ela, o Git não reconhece o projeto.

---

#### 2. **Clonar um repositório que já existe na internet (ou em outro lugar):**

* Copiar todo o projeto para sua máquina:

```bash
git clone URL nome-do-diretório
```

* Se não indicar o nome do diretório, ele cria uma pasta com o nome do repositório.

---

#### O que é o **remote "origin"**?

* Quando você clona um repositório, o Git cria uma conexão com o projeto original, chamada **remote**.
* O nome padrão desse remote é **origin**.
* Ele serve para enviar (push) ou baixar (pull) atualizações do projeto online.

---

#### Comandos úteis para remote:

* Ver os remotes configurados:

```bash
git remote -v
```

* Adicionar um remote chamado "origin" (quando você cria o repositório localmente e quer ligar ao GitHub):

```bash
git remote add origin URL-HTTPS
```

---

#### Clonar uma branch específica:

* Por padrão, o Git clona só a branch principal (geralmente chamada "main").
* Para clonar uma branch específica:

```bash
git clone URL --branch nome-da-branch --single-branch
```

---

#### Criar o arquivo **.gitignore**:

* Arquivo onde você lista arquivos ou pastas que o Git deve **ignorar** (não acompanhar nem enviar para o repositório).

```bash
touch .gitignore
```
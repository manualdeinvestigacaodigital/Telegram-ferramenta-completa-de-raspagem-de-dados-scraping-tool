<p align="center">
  <img src="https://raw.githubusercontent.com/manualdeinvestigacaodigital/telegram-app/main/Telegram_logo.svg.png" width="120">
</p>

<h1 align="center">Telegram - ferramenta completa de raspagem de dados (scraping-tool)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/status-estável-success">
  <img src="https://img.shields.io/badge/version-v1.0-blue">
  <img src="https://img.shields.io/badge/platform-Node.js-lightgrey">
  <img src="https://img.shields.io/badge/focus-OSINT-orange">
  <img src="https://img.shields.io/badge/license-Uso%20educacional-important">
</p>

---

# 🔎 VISÃO GERAL

Ferramenta desenvolvida para **coleta, análise e exploração estruturada de dados da plataforma Telegram**, com foco em:

- 🕵️ investigação digital
- 🧠 inteligência
- 🌐 OSINT

A aplicação permite:

- análise de chats, grupos e canais
- busca interna e global de entidades
- coleta de membros
- extração de mensagens e mídias
- exportação estruturada com integridade verificável

---

# 🧠 FASE 1 — ARQUITETURA DO SISTEMA

## 🔹 Backend (Node.js + Express)

Responsável por:

- autenticação com Telegram
- integração via biblioteca **GramJS**
- streaming de dados (NDJSON)
- gerenciamento de cache local

---

## 🔹 Serviços internos

- `services/telegram.js` → comunicação com Telegram
- `services/telegram_public.js` → consultas públicas
- `services/telegram_global.js` → busca global

---

## 🔹 Frontend

Interface web com:

- grid estruturada de resultados
- filtros avançados
- visualização de mídia
- exportação de dados

---

# ⚙️ FASE 2 — PREPARAÇÃO DO AMBIENTE

Antes de utilizar a ferramenta, é necessário preparar o ambiente com os programas necessários para execução do projeto.

---

## 📥 1. INSTALAR NODE.JS

Acesse o site oficial do Node.js:

    https://nodejs.org

Em seguida:

1. Baixe a versão **LTS**.
2. Execute o instalador.
3. Mantenha as opções padrão.
4. Conclua a instalação normalmente.

---

## 📥 2. INSTALAR PYTHON

Acesse o site oficial do Python:

    https://www.python.org/downloads/

Durante a instalação, marque obrigatoriamente a opção:

- ✔ **Add Python to PATH**

Essa opção permite que o Python seja reconhecido no Prompt de Comando, PowerShell ou Terminal.

---

# 🔍 FASE 3 — VERIFICAÇÃO DO AMBIENTE

Após instalar o Node.js, o npm e o Python, abra o Prompt de Comando (CMD), PowerShell ou Terminal e execute:

    node -v
    npm -v
    python --version

Se os comandos retornarem as respectivas versões, o ambiente estará pronto para execução da ferramenta.

---

# 🔐 FASE 4 — OBTENÇÃO DA API DO TELEGRAM

Para utilizar a ferramenta, é necessário obter credenciais de API no site oficial do Telegram.

Acesse:

    https://my.telegram.org

## 🛠️ Passo a passo

1. Faça login com seu número de telefone.
2. Acesse **API development tools**.
3. Crie uma aplicação.
4. Copie as credenciais geradas.

As informações necessárias são:

- `API_ID`
- `API_HASH`

⚠️ Essas credenciais são obrigatórias para funcionamento da ferramenta.

---

# 📥 FASE 5 — DOWNLOAD DO PROJETO

Existem duas formas distintas para realizar o download do projeto:

1. 📦 Download direto pela página do projeto no GitHub, sem necessidade de instalar o Git.
2. 🖥️ Download via Git, executando comandos no Prompt de Comando, PowerShell ou Terminal.

A seguir, serão descritas detalhadamente ambas as possibilidades.

---

## 📦 OPÇÃO 1 — DOWNLOAD DIRETO PELA PÁGINA DO PROJETO

Também é possível baixar a ferramenta diretamente pelo GitHub, sem utilizar o Git.

### 🌐 Passo a passo

1. Acesse o repositório:

    https://github.com/manualdeinvestigacaodigital/telegram-app

2. Clique no botão verde **`<> Code`**.

3. Selecione a opção **`Download ZIP`**.

4. Aguarde o download do arquivo compactado.

5. Extraia o conteúdo do arquivo ZIP em uma pasta de sua preferência.

---

## 🖥️ OPÇÃO 2 — DOWNLOAD VIA GIT

O Git é uma ferramenta amplamente utilizada para baixar e atualizar projetos hospedados no GitHub.

### 🔎 VERIFICAR SE O GIT ESTÁ INSTALADO

Abra o Prompt de Comando, PowerShell ou Terminal e execute o seguinte comando:

    git --version

### ✅ Resultado esperado

Se o Git estiver instalado corretamente, será exibida uma mensagem semelhante a:

    git version 2.49.0.windows.1

### ❌ Caso o Git não esteja instalado

Se aparecer mensagem informando que o comando `git` não é reconhecido, será necessário instalar o Git.

---

## 🛠️ INSTALAÇÃO DO GIT NO WINDOWS

### 🌐 1. Acesse o site oficial do Git

    https://git-scm.com/download/win

### 📥 2. Baixe o instalador

O download normalmente inicia automaticamente.

### ▶️ 3. Execute o instalador

Clique duas vezes no arquivo baixado.

### ⚙️ 4. Instalação recomendada

Durante a instalação:

- ✔ Mantenha as opções padrão
- ✔ Clique em **Next** em todas as etapas
- ✔ Ao final, clique em **Install**
- ✔ Depois, clique em **Finish**

### 🔄 5. Reinicie o terminal

Feche e abra novamente o Prompt de Comando ou PowerShell.

### 🔎 6. Teste novamente

    git --version

Se a versão for exibida, o Git foi instalado com sucesso.

---

## 🚀 CLONAR O REPOSITÓRIO

Após confirmar que o Git está instalado, execute:

    git clone https://github.com/manualdeinvestigacaodigital/telegram-app.git

Depois, acesse a pasta do projeto:

    cd telegram-app

---

# 📦 FASE 6 — INSTALAÇÃO DAS DEPENDÊNCIAS DO PROJETO

Dentro da pasta do projeto, execute:

    npm install

## 📦 O que o `npm install` faz

O comando:

- instala as dependências do projeto
- instala a biblioteca **GramJS**
- prepara o ambiente backend
- baixa os pacotes necessários para execução local da ferramenta

---

# ▶️ FASE 7 — EXECUÇÃO DO SISTEMA

Para iniciar a ferramenta, execute:

    node server.js

---

# 🔑 FASE 8 — CONFIGURAÇÃO AUTOMÁTICA

Na primeira execução, o sistema irá solicitar:

- `API_ID`
- `API_HASH`

Após o preenchimento:

- ✔ O arquivo `.env` será criado automaticamente
- ✔ Não é necessário criar o arquivo `.env` manualmente

---

# 🔐 FASE 9 — LOGIN NO TELEGRAM

Durante a execução no terminal, você informará:

- 📱 número de telefone
- 🔢 código enviado pelo Telegram
- 🔒 senha, caso tenha autenticação em dois fatores (2FA)

Após o login:

- ✔ A sessão será salva automaticamente em `session.txt`
- ✔ O login ficará persistente nas próximas execuções

---

# 🌐 FASE 10 — ACESSO AO SISTEMA

Abra o navegador e acesse:

    http://localhost:3000

---

# 🚀 FASE 11 — FUNCIONALIDADES

## 📡 1. Consulta interna

Permite analisar dados da conta, incluindo:

- chats
- grupos
- canais
- mensagens
- membros

---

## 🌐 2. Busca global

Permite localizar entidades públicas, incluindo:

- canais
- grupos
- usuários

---

## 🔍 3. Filtros avançados

Permite refinamento por:

- 📅 data inicial/final
- 👤 autor
- 🔤 username
- 📞 telefone
- 🖼️ tipo de mídia
- 👁️ views

---

## 📊 4. Resultado estruturado

Exibe:

- mensagens
- autores
- mídia
- metadados

Ações disponíveis:

- ▶️ usar entidade
- 🔐 ingressar em grupo/canal

---

# 🎥 FASE 12 — EXTRAÇÃO DE MÍDIA

A ferramenta possui suporte completo a:

- imagens
- vídeos
- documentos
- áudios

Recursos disponíveis:

- ✔ download automático
- ✔ cache local
- ✔ miniaturas

---

# 📁 FASE 13 — EXPORTAÇÃO DE DADOS

Formatos disponíveis:

- 📄 HTML
- 📊 XLS
- 🧾 JSON
- 📑 TXT

---

# 🔐 FASE 14 — INTEGRIDADE DOS DADOS

A ferramenta realiza geração automática de:

- SHA-256
- SHA-512

Permite:

- validação pericial
- rastreabilidade
- cadeia de custódia

---

# 🔄 FASE 15 — FLUXO OPERACIONAL

1. Iniciar sistema
2. Fazer login
3. Carregar chats
4. Executar busca
5. Aplicar filtros
6. Analisar resultados
7. Exportar dados
8. Validar integridade

---

# ⚠️ FASE 16 — SEGURANÇA

Nunca compartilhe:

- `.env`
- `session.txt`
- `API_ID`
- `API_HASH`
- código de verificação

---

# ⚠️ FASE 17 — LIMITAÇÕES

[Não verificado] Pode variar conforme:

- mudanças na API do Telegram
- restrições de acesso
- conteúdo privado

---

# 📜 FASE 18 — LICENÇA

Uso permitido para:

- fins educacionais
- pesquisa
- investigação digital

Não autorizado para:

- violação de termos
- coleta indevida de dados
- atividades ilícitas

---

# 📚 FASE 19 — REFERÊNCIA TÉCNICA E AUTORIA

Este projeto integra um conjunto mais amplo de ferramentas voltadas à investigação digital, inteligência e OSINT.

O autor deste projeto é também autor da obra:

📖 **Manual de Investigação Digital — Editora Juspodivm**

    https://www.editorajuspodivm.com.br/authors/page/view/id/206/

A obra reúne fundamentos teóricos e aplicações práticas voltadas à investigação digital contemporânea, incluindo metodologias, técnicas operacionais e utilização de ferramentas tecnológicas para coleta, preservação e análise de dados.

---

# 🧠 FASE 20 — INTEGRAÇÃO COM A OBRA

Este repositório representa uma aplicação prática de técnicas abordadas no livro, permitindo:

- ✔ Aplicação direta de conceitos de OSINT
- ✔ Estruturação de coleta de dados digitais
- ✔ Organização de evidências
- ✔ Apoio a análises investigativas

---

# 👤 AUTOR

**Guilherme Caselli**  
Delegado de Polícia  
Especialista em investigação digital

    https://instagram.com/guilhermecaselli

---

# 🎯 FINALIDADE

- 🕵️ Investigação digital
- 🧠 Inteligência
- 🌐 OSINT
- 📊 Análise de dados
- 📁 Produção de evidência digital

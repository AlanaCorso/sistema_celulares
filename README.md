<div align="center">

![Header animado](https://capsule-render.vercel.app/api?type=waving&color=0:0B1220,45:123A5A,100:168AAD&height=190&section=header&text=Sistemas%20Celulares&fontSize=42&fontColor=FFFFFF&animation=fadeIn&fontAlignY=35&desc=GEST%C3%83O%20INTELIGENTE%20PARA%20ASSIST%C3%8ANCIA%20T%C3%89CNICA&descAlignY=58&descSize=15)

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=19&duration=2600&pause=700&color=38BDF8&center=true&vCenter=true&width=700&height=60&lines=Organize+clientes+e+aparelhos;Gerencie+servi%C3%A7os+e+agendamentos;Deixe+a+assist%C3%AAncia+mais+organizada)](https://git.io/typing-svg)

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-3.0.3-000000?style=for-the-badge&logo=flask&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-Structure-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-Interface-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Interactions-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

**Projeto acadêmico • Desenvolvimento de Sistemas**


</div>

---

## 📘 Visão geral

> Uma assistência técnica organizada começa com informações bem
> conectadas.

O **Sistemas Celulares** é uma aplicação web desenvolvida para apoiar a
rotina de uma assistência técnica de celulares. A proposta é reunir, em
um único sistema, o cadastro de clientes, o controle dos aparelhos
recebidos e a organização dos agendamentos de serviços.

O sistema conta com autenticação de usuários, operações de cadastro,
consulta, edição e exclusão (CRUD), validações e integração com banco de
dados MySQL.

```{=html}
<table>
```
```{=html}
<tr>
```
```{=html}
<td width="65%" valign="top">
```
### A proposta

Cada atendimento envolve um cliente, um aparelho e um serviço. O sistema
relaciona essas informações para facilitar o acompanhamento dos
registros e deixar a rotina da assistência mais clara e organizada.

### Objetivo

Aplicar na prática conceitos de desenvolvimento web, lógica de
programação, autenticação, manipulação de banco de dados e
relacionamento entre tabelas.

```{=html}
</td>
```
```{=html}
<td width="35%" align="center" valign="top">
```
### 🔴 TEMA

Assistência técnica de celulares

`<br>`{=html}

### 🧩 APLICAÇÃO

Sistema web

`<br>`{=html}

### 🗄️ BANCO DE DADOS

MySQL

```{=html}
</td>
```
```{=html}
</tr>
```
```{=html}
</table>
```
## 🔎 O que o sistema faz

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}👤 01 --- Clientes \| Cadastro e
consulta`</strong>`{=html}
```{=html}
</summary>
```
`<br>`{=html}

Permite registrar e administrar as informações dos clientes atendidos.

-   Cadastrar clientes.
-   Consultar e pesquisar registros por nome, telefone ou e-mail.
-   Localizar um cliente pelo CPF completo.
-   Editar informações cadastradas.
-   Excluir clientes, respeitando os vínculos com aparelhos.

**Validações:** nome, formato do e-mail, quantidade de dígitos do CPF e
prevenção de CPF duplicado.

```{=html}
</details>
```
`<br>`{=html}

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}📱 02 --- Aparelhos \| Controle dos
equipamentos`</strong>`{=html}
```{=html}
</summary>
```
`<br>`{=html}

Organiza os celulares recebidos pela assistência e mantém cada aparelho
associado a um cliente.

-   Cadastrar aparelhos com marca, modelo, cor e defeito informado.
-   Consultar e editar os equipamentos.
-   Identificar o cliente proprietário.
-   Excluir aparelhos quando não houver agendamentos vinculados.

**Validações:** IMEI com 15 dígitos, campos obrigatórios, cliente
existente e IMEI não duplicado.

```{=html}
</details>
```
`<br>`{=html}

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}📅 03 --- Agendamentos \| Organização dos
serviços`</strong>`{=html}
```{=html}
</summary>
```
`<br>`{=html}

Permite organizar os atendimentos e relacionar o aparelho ao serviço que
será realizado.

-   Cadastrar agendamentos com data e horário.
-   Consultar os atendimentos registrados.
-   Editar data, horário, status e observações.
-   Excluir agendamentos.

**Status disponíveis:** AGENDADO, EM_ANDAMENTO, CONCLUIDO e CANCELADO.

```{=html}
</details>
```
`<br>`{=html}

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}🔐 04 --- Autenticação \| Acesso
protegido`</strong>`{=html}
```{=html}
</summary>
```
`<br>`{=html}

O acesso às páginas e operações do sistema é protegido por login.

-   Validar usuário e senha.
-   Manter uma sessão autenticada.
-   Bloquear páginas e operações da API para quem não estiver
    autenticado.
-   Encerrar a sessão ao sair.
-   Expirar a sessão após 30 minutos de inatividade/tempo desde o login.

As senhas dos usuários e os CPFs dos clientes são armazenados em formato
de hash bcrypt, em vez de texto puro.

```{=html}
</details>
```
## 🔄 Como as informações se conectam

  -----------------------------------------------------------------------
  Registro                            Relacionamento
  ----------------------------------- -----------------------------------
  **Cliente**                         Pode possuir vários aparelhos
                                      cadastrados.

  **Aparelho**                        Pertence a um cliente e pode
                                      possuir agendamentos.

  **Serviço**                         É associado aos agendamentos
                                      realizados.

  **Agendamento**                     Conecta um aparelho a um serviço,
                                      com data, status e observação.

  **Usuário**                         Realiza o acesso ao sistema por
                                      meio da autenticação.
  -----------------------------------------------------------------------

## 🛠️ Tecnologias

  Tecnologia                   Utilização
  ---------------------------- -----------------------------------------------------
  **Python**                   Linguagem principal e regras da aplicação.
  **Flask 3.0.3**              Servidor web e rotas.
  **MySQL 8+**                 Armazenamento e relacionamento dos dados.
  **mysql-connector-python**   Conexão entre Python e MySQL.
  **bcrypt**                   Hash de senhas e CPFs.
  **HTML**                     Estrutura das páginas.
  **CSS**                      Estilização e identidade visual.
  **JavaScript**               Interações com a interface e comunicação com a API.

## 💻 Como executar

### 1. Pré-requisitos

Antes de começar, instale:

-   [Python 3.10 ou superior](https://www.python.org/downloads/)
-   [MySQL 8 ou superior](https://dev.mysql.com/downloads/installer/)
-   [Visual Studio Code](https://code.visualstudio.com/) (recomendado)

### 2. Abra a pasta do projeto

Extraia o ZIP e abra no VS Code a pasta
`sistema_celulares_flask_desafio`, que contém o arquivo `app.py`.

Abra o terminal integrado do VS Code em **Terminal → Novo Terminal**.

### 3. Crie e ative o ambiente virtual

**Windows --- Prompt de Comando (CMD):**

``` cmd
python -m venv venv
venv\Scripts\activate
```

**Windows --- PowerShell:**

``` powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

**Linux/macOS:**

``` bash
python3 -m venv venv
source venv/bin/activate
```

### 4. Instale as dependências

Com o ambiente virtual ativado, execute:

``` bash
pip install -r requirements.txt
```

### 5. Crie o banco de dados

O arquivo `assistencia_db.sql` contém a estrutura do banco
`assistencia_db` e registros iniciais para teste.

No MySQL Workbench, conecte ao servidor, abra `assistencia_db.sql` e
execute o script.

> **Atenção:** o script começa com
> `DROP DATABASE IF EXISTS assistencia_db`. Isso apaga e recria esse
> banco. Se você já tiver dados importantes nele, faça um backup antes
> de executar.

### 6. Configure a conexão com o MySQL

Por padrão, a aplicação tenta conectar usando:

  Configuração   Valor padrão
  -------------- ------------------
  Host           `localhost`
  Porta          `3306`
  Usuário        `root`
  Senha          vazia
  Banco          `assistencia_db`

Se o seu MySQL usa outra senha, configure as variáveis de ambiente antes
de iniciar a aplicação.

**Windows --- CMD:**

``` cmd
set DB_HOST=localhost
set DB_PORT=3306
set DB_USER=root
set DB_PASSWORD=sua_senha
set DB_NAME=assistencia_db
set SECRET_KEY=coloque_uma_chave_secreta
```

**Windows --- PowerShell:**

``` powershell
$env:DB_HOST="localhost"
$env:DB_PORT="3306"
$env:DB_USER="root"
$env:DB_PASSWORD="sua_senha"
$env:DB_NAME="assistencia_db"
$env:SECRET_KEY="coloque_uma_chave_secreta"
```

Troque `sua_senha` pela senha configurada no seu MySQL. Esses comandos
valem para o terminal atual; se abrir outro terminal, será necessário
configurá-los novamente.

### 7. Inicie o sistema

Com o ambiente virtual ativado e o MySQL em execução, rode:

``` bash
python app.py
```

Quando aparecer a mensagem indicando que o servidor está rodando, abra o
navegador em:

``` text
http://127.0.0.1:5000
```

Para encerrar o servidor, volte ao terminal e pressione `Ctrl + C`.

## 🔑 Usuários para teste

O banco de dados inclui três contas de demonstração:

  Usuário    Senha
  ---------- -------------
  `admin`    `admin123`
  `carlos`   `carlos123`
  `ana`      `ana12345`

> São credenciais disponibilizadas para teste local. Não utilize essas
> senhas em um ambiente real.

## 🗂️ Estrutura do projeto

``` text
sistema_celulares_flask_desafio/
│
├── app.py                  # Inicialização da aplicação Flask
├── rotas.py                # Rotas das páginas e da API
├── db.py                   # Conexão e operações com o MySQL
├── autenticacao.py         # Login, sessão e validação de acesso
├── clientes.py             # Regras do módulo de clientes
├── aparelhos.py            # Regras do módulo de aparelhos
├── agendamento.py          # Regras do módulo de agendamentos
│
├── assistencia_db.sql      # Criação e dados iniciais do banco
├── requirements.txt        # Dependências Python
├── ROTEIRO.md              # Roteiro complementar de execução e testes
├── testar_conexao.py       # Teste de conexão com o banco
│
├── templates/              # Páginas HTML
│   ├── login.html
│   ├── principal.html
│   ├── clientes.html
│   ├── aparelhos.html
│   └── agendamentos.html
│
└── static/                 # Arquivos de estilo e interação
    ├── style.css
    └── app.js
```

## 🧪 Testes e regras importantes

-   O sistema não permite acessar páginas protegidas sem login.
-   O CPF é validado pela quantidade de 11 dígitos e armazenado com hash
    bcrypt.
-   O IMEI deve conter 15 dígitos e não pode estar duplicado.
-   Um aparelho precisa estar associado a um cliente cadastrado.
-   Um cliente com aparelhos vinculados não pode ser excluído.
-   Um aparelho com agendamentos vinculados não pode ser excluído.
-   As consultas ao banco utilizam parâmetros SQL para reduzir o risco
    de SQL Injection.
-   A API retorna mensagens de erro quando uma validação ou regra de
    negócio impede a operação.

Para conferir a conexão com o banco, com o servidor MySQL ativo e as
configurações corretas, execute:

``` bash
python testar_conexao.py
```

## 📚 Conceitos colocados em prática

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Ver os conceitos trabalhados no
projeto`</strong>`{=html}
```{=html}
</summary>
```
`<br>`{=html}

  -----------------------------------------------------------------------
  Conceito                            Aplicação
  ----------------------------------- -----------------------------------
  **CRUD**                            Cadastro, consulta, edição e
                                      exclusão de registros.

  **Relacionamento entre tabelas**    Ligação entre clientes, aparelhos,
                                      serviços e agendamentos.

  **Autenticação**                    Verificação de usuário e senha.

  **Sessões**                         Controle do acesso durante a
                                      navegação.

  **Validação**                       Verificação dos dados enviados
                                      pelos formulários.

  **API**                             Comunicação entre a interface e o
                                      servidor.

  **Segurança**                       Hash bcrypt e consultas
                                      parametrizadas.
  -----------------------------------------------------------------------

```{=html}
</details>
```

------------------------------------------------------------------------

::: {align="center"}
### SISTEMAS CELULARES

*Mais organização para cada cliente, aparelho e atendimento.*

**Projeto acadêmico · Desenvolvimento de Sistemas**


<sub>Python • Flask • MySQL • HTML • CSS • JavaScript</sub>

![Footer animado](https://capsule-render.vercel.app/api?type=waving&color=0:168AAD,55:123A5A,100:0B1220&height=110&section=footer)

</div>


<div align="center">
<sub>Feito com 🩵 por Alana Corso</sub>
</div>



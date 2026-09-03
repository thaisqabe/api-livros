# 📚 API Livros

<p align="center">
  <strong>Uma API REST para gerenciamento de livros de uma biblioteca.</strong>
</p>

<p align="center">
  Desenvolvida com 🐍 Python, ⚡ FastAPI e 🐬 MySQL.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-ff69b4?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-API-ff69b4?style=for-the-badge&logo=fastapi&logoColor=white">
  <img src="https://img.shields.io/badge/MySQL-Database-ff69b4?style=for-the-badge&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/SQLAlchemy-ORM-ff69b4?style=for-the-badge&logo=sqlalchemy&logoColor=white">
</p>

---

## 🌷 Sobre o projeto

A **API Livros** é uma aplicação desenvolvida para realizar o gerenciamento de livros de uma biblioteca.

Por meio da API, é possível **cadastrar, consultar, listar, atualizar e excluir livros**, utilizando uma arquitetura REST e comunicação com um banco de dados MySQL.

Cada livro possui informações como:

- 📖 Título
- ✍️ Autor
- 📅 Ano de publicação
- 📚 Disponibilidade

---

## ✨ Funcionalidades

A API disponibiliza as seguintes operações:

| Método | Rota | Objetivo |
|:------:|:-----|:---------|
| 💗 `POST` | `/livros` | Criar um livro |
| 🌸 `GET` | `/livros` | Listar livros |
| 🔎 `GET` | `/livros/{id}` | Consultar um livro específico |
| ✏️ `PUT` | `/livros/{id}` | Atualizar um livro |
| 🗑️ `DELETE` | `/livros/{id}` | Excluir um livro |

---

## 📖 Estrutura de um livro

Cada livro possui os seguintes dados:

| Campo | Tipo | Descrição |
| --- | --- | --- |
| `id` | `integer` | Identificador único do livro |
| `titulo` | `string` | Título do livro |
| `autor` | `string` | Nome do autor |
| `ano_publicacao` | `integer` | Ano em que o livro foi publicado |
| `disponivel` | `boolean` | Indica se o livro está disponível |

### Exemplo

```json
{
  "id": 1,
  "titulo": "O Pequeno Príncipe",
  "autor": "Antoine de Saint-Exupéry",
  "ano_publicacao": 1943,
  "disponivel": true
}
```

---

## 🛠️ Tecnologias

Este projeto foi desenvolvido utilizando:

- **Python** — linguagem principal da aplicação
- **FastAPI** — framework para criação da API
- **Uvicorn** — servidor para execução da aplicação
- **SQLAlchemy** — ORM para comunicação com o banco de dados
- **PyMySQL** — driver Python para conexão com MySQL
- **Pydantic Settings** — gerenciamento e validação das configurações
- **MySQL** — banco de dados relacional

---

## 📁 Estrutura do projeto

```text
api-livros/
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── models/
│   │   └── livro.py
│   ├── schemas/
│   │   └── livro.py
│   ├── routes/
│   │   └── livros.py
│   └── database/
│       └── database.py
│
├── .env
├── .gitignore
├── requirements.txt
└── README.md
```

> A estrutura pode variar de acordo com a organização utilizada no projeto.

---

## 🚀 Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/thaisqabe/api-livros.git
cd api-livros
```

### 2. Crie um ambiente virtual

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```

**Linux / macOS:**

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Configure o banco de dados

Crie um banco de dados MySQL e configure as informações de conexão no arquivo `.env`.

Exemplo:

```env
DATABASE_URL=mysql+pymysql://usuario:senha@localhost:3306/api_livros
```

> **Importante:** não compartilhe o arquivo `.env` no GitHub. Adicione-o ao `.gitignore`.

### 5. Execute a aplicação

```bash
uvicorn app.main:app --reload
```

A API estará disponível em:

```text
http://localhost:8000
```

---

## 📚 Documentação

A API possui documentação interativa gerada automaticamente pelo FastAPI.

### Swagger UI

Acesse:

```text
http://localhost:8000/docs
```

### ReDoc

Também é possível acessar:

```text
http://localhost:8000/redoc
```

O Swagger permite visualizar os endpoints e realizar requisições diretamente pelo navegador.

---

## 🧪 Exemplos de requisições

### Criar um livro

**POST** `/livros`

```json
{
  "titulo": "Dom Casmurro",
  "autor": "Machado de Assis",
  "ano_publicacao": 1899,
  "disponivel": true
}
```

### Listar livros

**GET** `/livros`

Exemplo de resposta:

```json
[
  {
    "id": 1,
    "titulo": "Dom Casmurro",
    "autor": "Machado de Assis",
    "ano_publicacao": 1899,
    "disponivel": true
  }
]
```

### Consultar um livro

**GET** `/livros/{id}`

Exemplo:

```text
GET /livros/1
```

Retorna os dados do livro correspondente ao ID informado.

### Atualizar um livro

**PUT** `/livros/{id}`

Exemplo:

```text
PUT /livros/1
```

```json
{
  "titulo": "Dom Casmurro",
  "autor": "Machado de Assis",
  "ano_publicacao": 1899,
  "disponivel": false
}
```

### Excluir um livro

**DELETE** `/livros/{id}`

Exemplo:

```text
DELETE /livros/1
```

Remove o livro correspondente ao ID informado.

---

## 🎯 Objetivo

O projeto foi desenvolvido com o objetivo de praticar conceitos de desenvolvimento de **APIs REST**, incluindo:

- Criação e organização de endpoints
- Operações CRUD
- Validação de dados
- Integração com banco de dados
- Utilização de ORM
- Gerenciamento de configurações
- Documentação automática
- Organização e separação de responsabilidades

---


<p align="center">
  Desenvolvido  por <strong>Thaís Abe</strong>
  <br>
  <a href="https://github.com/thaisqabe">@thaisqabe</a>
</p>
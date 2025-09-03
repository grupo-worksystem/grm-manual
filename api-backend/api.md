# GRM API – Documentação Oficial

API desenvolvida em Node.js com objetivo de gerenciar usuários, autenticação e controle de acesso no sistema GRM.

---

## Índice

- [GRM API – Documentação Oficial](#grm-api--documentação-oficial)
  - [Índice](#índice)
  - [Requisitos](#requisitos)
  - [Instalação](#instalação)
  - [Configuração](#configuração)
  - [Execução](#execução)
  - [Para Build e Produção](#para-build-e-produção)
  - [📡 Endpoints](#-endpoints)
    - [Usuário:](#usuário)
    - [Formulários:](#formulários)

---

## Requisitos

- Node.js v22+
- PostgreSQL16
- npm ou yarn

---

## Instalação

Clone o repositório:

```bash
git clone https://github.com/grupo-worksystem/grm-api.git
cd grm-api

```

## Configuração

Crie um arquivo `.env` na raiz do projeto com base no `.env.example`. Preencha as variáveis conforme seu ambiente.

---

## Execução

Para rodar em modo de desenvolvimento:

```bash
npm run dev
```

## Para Build e Produção

```
npm run build
npm start
```

## 📡 Endpoints

### Usuário:

| Método | Rota             | Descrição                 | Protegida |
| ------ | ---------------- | ------------------------- | --------- |
| POST   | `/api/auth`      | Autenticação (login)      | ❌        |
| POST   | `/api/user`      | Cria um novo usuário      | ✅        |
| GET    | `/api/user/all`  | Lista todos usuários      | ✅        |
| GET    | `/api/user/{id}` | Busca usuário por Id      | ✅        |
| PUT    | `/api/user/{id}` | Atualiza dados do usuário | ✅        |
| DELETE | `/api/user/{id}` | Remove o usuário          | ✅        |

### Formulários:

| Método | Rota             | Descrição                 | Protegida  |
| ------ | ---------------- | ------------------------- | ---------  |
| POST   | `/api/form`      | Cria um novo usuário      | ✅        |
| GET    | `/api/form/all`  | Lista todos usuários      | ✅        |
| GET    | `/api/form/{id}` | Busca usuário por Id      | ✅        |
| PUT    | `/api/form/{id}` | Atualiza dados do usuário | ✅        |
| DELETE | `/api/form/{id}` | Remove o usuário          | ✅        |

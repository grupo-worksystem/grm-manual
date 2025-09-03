# GRM Front

Interface web do projeto **GRM (Gestão de Relatórios de Manutenção)**.

Este repositório contém o front-end da aplicação, desenvolvido com foco em produtividade, integração com APIs externas e uma experiência de usuário fluida e responsiva.

## 🔧 Tecnologias Utilizadas

- **Next.js 14**
- **TypeScript**
- **Tailwind CSS**
- Outros pacotes e bibliotecas estão listados no arquivo [`package.json`](./package.json).

## 🌐 Hospedagem

A aplicação está hospedada na **Vercel**, com integração contínua e deploy automático a partir da branch principal.

## ⚙️ Backend e Integrações

O front-end inclui rotas de **API** internas (Next.js API Routes) que fazem a ponte entre a interface do usuário e serviços externos como:

- **TOM Ticket** – para gerenciamento de chamados e tickets.
- **Telegram** – para envio de notificações automatizadas.

Além disso, o GRM conta com uma **API de backend separada**, responsável por:

- Autenticação e controle de acesso dos usuários
- Integração com banco de dados
- Cadastro e gerenciamento de formulários personalizados

Essa API também utiliza variáveis de ambiente, documentadas separadamente no repositório correspondente.
Repositório aqui [GRM-API](https://github.com/grupo-worksystem/grm-api)

## 💾 Otimização com Local Storage

Durante a utilização dos formulários, o GRM salva os dados localmente no navegador por meio do `localStorage`. Essa abordagem evita requisições desnecessárias ao servidor, especialmente considerando que os dados preenchidos **não são armazenados na própria ferramenta**, mas apenas enviados para serviços externos.

## 🚀 Fluxo de Finalização de Relatório

Ao finalizar o preenchimento de um relatório:

1. O GRM envia os dados diretamente para o sistema principal **TOMTicket**.
2. Em seguida, dispara uma notificação automática para o **Telegram**, informando sobre o envio.

## 📁 Variáveis de Ambiente

Para rodar o projeto localmente, é necessário configurar as variáveis de ambiente. Um exemplo está disponível no arquivo:

```
.env.example
```

## Padronização de campos "select"

São as opções disponiveis no checklist dos formularios

| Variante                       | Tipo                                                              |
| ------------------------------ | ----------------------------------------------------------------- |
| Limpeza                        | `Realizada,Não Realizada,Não aplicavel`                           |
| Recursos essenciais / Inspeção | `Ok,Abrir ticket Correção ,Corrigido na preventiva,Não realizado` |
| Teste                          | `Passou,Não passou (agendar correção)`                            |
| Funcionamento                  | `Em plena operação,Em operação parcial,Desligado ou desativado`   |
| Fixação                        | `OK,Corrigido,Abrir ticket Correção `                             |

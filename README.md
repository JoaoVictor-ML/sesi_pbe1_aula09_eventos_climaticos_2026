# Backend - Aula 09 — Registro de Eventos Climáticos

## Sobre o projeto

O **Sistema de Registro de Eventos Climáticos** é um projeto acadêmico desenvolvido no curso técnico de Desenvolvimento de Sistemas do SENAI. A aplicação tem como objetivo registrar e organizar informações sobre eventos climáticos ocorridos em diferentes cidades, permitindo acompanhar temperaturas máximas e níveis de impacto.

O sistema utiliza um banco de dados relacional para armazenar os usuários responsáveis pelos registros e os respectivos eventos climáticos, facilitando a consulta e a organização dessas informações.

## Objetivos

- Criar e popular um banco de dados relacional utilizando SQL.
- Desenvolver um back-end com Node.js e Express.
- Implementar a conexão entre a aplicação e o banco de dados MariaDB.
- Desenvolver operações para cadastrar e listar usuários.
- Desenvolver operações para cadastrar e listar eventos climáticos.
- Relacionar os eventos aos usuários responsáveis por seus registros.
- Testar as requisições HTTP utilizando o Thunder Client.

## Funcionalidades

| Funcionalidade | Método HTTP | Endpoint |
|---|---|---|
| Verificar o funcionamento da API | GET | `/` |
| Cadastrar usuário | POST | `/usuarios` |
| Listar usuários | GET | `/usuarios` |
| Cadastrar evento climático | POST | `/eventos` |
| Listar eventos climáticos | GET | `/eventos` |

## Modelagem do banco de dados

O banco de dados `registros_climaticos` possui duas tabelas principais:

- **usuario:** armazena o identificador, nome, e-mail e senha dos usuários.
- **evento:** armazena a cidade, o tipo de evento, a temperatura máxima, a data, o nível de impacto e o identificador do usuário responsável.

A tabela `evento` possui uma chave estrangeira (`usuarioId`) que estabelece o relacionamento com a tabela `usuario`.

### Níveis de impacto

| Nível | Descrição |
|---|---|
| Baixo | Evento com baixo nível de impacto registrado. |
| Médio | Evento com nível intermediário de impacto. |
| Alto | Evento com alto nível de impacto registrado. |

## Tecnologias e ferramentas

- **JavaScript** — desenvolvimento da aplicação.
- **Node.js** — ambiente de execução.
- **Express** — gerenciamento do servidor e das rotas.
- **MariaDB / MySQL** — banco de dados relacional.
- **SQL** — criação, relacionamento e população das tabelas.
- **Visual Studio Code** — ambiente de desenvolvimento.
- **Thunder Client** — realização de testes das requisições HTTP.

## Estrutura do projeto

```text
eventos_climaticos/
├── db/
│   └── script.sql
├── src/
│   ├── controllers/
│   │   ├── evento.js
│   │   └── usuario.js
│   ├── db.js
│   └── routes.js


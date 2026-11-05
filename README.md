# Cloude_Oracle

Repositório de códigos Oracle (SQL e PL/SQL) desenvolvidos com auxílio do Claude Code.

## Estrutura

| Pasta                | Conteúdo                                                  |
|----------------------|-----------------------------------------------------------|
| `tables/`            | DDL de tabelas, constraints e índices                     |
| `views/`             | Views e materialized views                                |
| `packages/`          | Packages (`.pks` = specification, `.pkb` = body)          |
| `procedures/`        | Procedures standalone (`.prc`)                            |
| `functions/`         | Functions standalone (`.fnc`)                             |
| `triggers/`          | Triggers (`.trg`)                                         |
| `sequences/`         | Sequences (`.sql`)                                        |
| `scripts/migrations/`| Scripts de alteração versionados (`V001__descricao.sql`)  |
| `scripts/utils/`     | Consultas úteis: diagnóstico, tuning, monitoramento       |
| `docs/`              | Documentação e anotações                                  |

## Segurança

- **Nunca** versionar senhas, strings de conexão, `tnsnames.ora`, `sqlnet.ora` ou wallets.
- **Nunca** versionar dados reais de clientes ou dumps (`.dmp`).
- Credenciais devem vir de variáveis de ambiente ou de um arquivo local ignorado pelo Git.

# Instruções para o Claude

Projeto de códigos Oracle (SQL e PL/SQL). Responder em **português**.

## Padrões de código

- Palavras reservadas em MAIÚSCULAS (`SELECT`, `FROM`, `BEGIN`); nomes de objetos em minúsculas.
- Indentação de 2 espaços.
- Prefixos de variáveis PL/SQL:
  - `p_` parâmetros, `l_` variáveis locais, `g_` variáveis globais de package,
  - `c_` constantes, `cur_` cursores, `t_` tipos, `e_` exceções.
- Usar bind variables; nunca concatenar valores em SQL dinâmico (evitar SQL injection).
- Preferir operações em conjunto (SQL puro, `BULK COLLECT`/`FORALL`) a loops linha a linha.
- Tratar exceções de forma explícita; não usar `WHEN OTHERS THEN NULL`.
- Todo script de criação deve ser reexecutável quando possível (`CREATE OR REPLACE`).
- Comentar o propósito de cada package, procedure e function no cabeçalho.

## Organização

- Um objeto por arquivo, nomeado com o nome do objeto (ex.: `packages/pkg_clientes.pks`).
- Alterações de estrutura vão em `scripts/migrations/` com prefixo sequencial (`V001__`, `V002__`...).

## Segurança

- Nunca incluir senhas, hosts, strings de conexão ou dados reais de clientes nos arquivos.

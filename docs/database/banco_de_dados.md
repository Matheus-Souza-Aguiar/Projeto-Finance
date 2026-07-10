# Banco de Dados

## Objetivo

O banco de dados do Projeto Finance será responsável por armazenar as informações dos usuários, receitas, despesas, categorias e movimentações financeiras mensais.

## Entidades iniciais

### Usuário
Representa a pessoa que utiliza o sistema.

Campos iniciais:
- id
- nome
- email
- senha_hash
- data_criacao
- ativo

---

### Categoria
Representa os tipos de receitas e despesas.

Exemplos:
- Salário
- Freelance
- Alimentação
- Transporte
- Moradia
- Lazer
- Dívidas
- Investimentos

Campos iniciais:
- id
- usuario_id
- nome
- tipo
- data_criacao

---

### Transação
Representa uma entrada ou saída financeira.

Campos iniciais:
- id
- usuario_id
- categoria_id
- tipo
- descricao
- valor
- data_transacao
- data_criacao

Tipos:
- receita
- despesa

---

## Relacionamentos

Um usuário pode ter várias categorias.

Um usuário pode ter várias transações.

Uma categoria pode estar vinculada a várias transações.

## Regras iniciais do banco de dados

- Cada usuário visualiza apenas seus próprios dados.
- Toda transação deve ser receita ou despesa.
- Toda transação deve ter valor maior que zero.
- Uma transação pode ou não ter categoria.
- O saldo mensal será calculado com base nas receitas menos despesas.

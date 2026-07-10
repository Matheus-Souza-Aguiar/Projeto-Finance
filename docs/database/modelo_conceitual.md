# Modelo Conceitual — Projeto Finance

## Entidades

* Usuário
* Conta/Carteira
* Receita
* Despesa
* Categoria
* Cartão de Crédito
* Fatura
* Anexo

---

## Usuário

* Um Usuário pode possuir várias Contas/Carteiras `(1:N)`.

* Uma Conta/Carteira pertence a um único Usuário `(N:1)`.

* Um Usuário pode registrar várias Receitas `(1:N)`.

* Uma Receita pertence a um único Usuário `(N:1)`.

* Um Usuário pode registrar várias Despesas `(1:N)`.

* Uma Despesa pertence a um único Usuário `(N:1)`.

---

## Conta/Carteira

* Uma Conta/Carteira pode possuir vários Cartões de Crédito `(1:N)`.

* Um Cartão de Crédito pertence a uma única Conta/Carteira `(N:1)`.

* Uma Conta/Carteira pode receber várias Receitas `(1:N)`.

* Uma Receita pertence a uma única Conta/Carteira `(N:1)`.

* Uma Conta/Carteira pode estar vinculada a várias Despesas `(1:N)`.

* Uma Despesa pode estar vinculada a uma única Conta/Carteira `(N:1)`.

A vinculação da Despesa com uma Conta/Carteira pode ser opcional quando a despesa tiver sido realizada por meio de um Cartão de Crédito.

---

## Receita

* Uma Receita pertence a um único Usuário `(N:1)`.

* Um Usuário pode registrar várias Receitas `(1:N)`.

* Uma Receita pertence a uma única Conta/Carteira `(N:1)`.

* Uma Conta/Carteira pode receber várias Receitas `(1:N)`.

* Uma Receita pertence a uma única Categoria `(N:1)`.

* Uma Categoria pode classificar várias Receitas `(1:N)`.

---

## Categoria

* Uma Categoria pode classificar várias Receitas `(1:N)`.

* Uma Receita pertence a uma única Categoria `(N:1)`.

* Uma Categoria pode classificar várias Despesas `(1:N)`.

* Uma Despesa pertence a uma única Categoria `(N:1)`.

---

## Despesa

* Uma Despesa pertence a um único Usuário `(N:1)`.

* Um Usuário pode registrar várias Despesas `(1:N)`.

* Uma Despesa pertence a uma única Categoria `(N:1)`.

* Uma Categoria pode classificar várias Despesas `(1:N)`.

* Uma Despesa pode estar vinculada a uma única Conta/Carteira `(N:1)`.

* Uma Conta/Carteira pode estar vinculada a várias Despesas `(1:N)`.

* Uma Despesa pode estar vinculada a um único Cartão de Crédito `(N:1)`.

* Um Cartão de Crédito pode estar vinculado a várias Despesas `(1:N)`.

* Uma Despesa realizada por Cartão de Crédito pode pertencer a uma única Fatura `(N:1)`.

* Uma Fatura pode agrupar várias Despesas `(1:N)`.

* Uma Despesa pode possuir vários Anexos `(1:N)`.

* Um Anexo pertence a uma única Despesa `(N:1)`.

Uma Despesa poderá estar vinculada diretamente a uma Conta/Carteira ou a um Cartão de Crédito, conforme a forma de pagamento utilizada.

---

## Cartão de Crédito

* Um Cartão de Crédito pertence a uma única Conta/Carteira `(N:1)`.

* Uma Conta/Carteira pode possuir vários Cartões de Crédito `(1:N)`.

* Um Cartão de Crédito pode estar vinculado a várias Despesas `(1:N)`.

* Uma Despesa pode estar vinculada a um único Cartão de Crédito `(N:1)`.

* Um Cartão de Crédito pode possuir várias Faturas `(1:N)`.

* Uma Fatura pertence a um único Cartão de Crédito `(N:1)`.

---

## Fatura

* Uma Fatura pertence a um único Cartão de Crédito `(N:1)`.

* Um Cartão de Crédito pode possuir várias Faturas `(1:N)`.

* Uma Fatura pode agrupar várias Despesas `(1:N)`.

* Uma Despesa realizada por Cartão de Crédito pode pertencer a uma única Fatura `(N:1)`.

---

## Anexo

* Um Anexo pertence a uma única Despesa `(N:1)`.
* Uma Despesa pode possuir vários Anexos `(1:N)`.

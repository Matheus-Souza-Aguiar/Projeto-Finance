Usuário
- Um Usuário pode possuir várias Contas/Carteiras (1:N)
- Uma Conta/Carteira pertence a um único Usuário (N:1)

- Um Usuário pode possuir várias Receitas (1:N)
- Uma Receita pertence a um único Usuário (N:1)

- Um Usuário pode possuir várias Despesas (1:N)
- Uma Despesa pertence a um único Usuário (N:1)

- Um Usuário pode possuir vários Cartões de Crédito (1:N)
- Um Cartão de Crédito pertence a um único Usuário (N:1)


Conta/Carteira
- Uma Conta/Carteira pode possuir vários Cartões de Crédito (1:N)
- Um Cartão de Crédito pertence a uma única Conta/Carteira (N:1)

- Uma Conta/Carteira pode possuir várias Receitas (1:N)
- Uma Receita pertence a uma única Conta/Carteira (N:1)

- Uma Conta/Carteira pode estar relacionada a várias Despesas (1:N)
- Uma Despesa pode estar relacionada a uma Conta/Carteira (N:1)


Categoria
- Uma Categoria pode classificar várias Receitas (1:N)
- Uma Receita pertence a uma única Categoria (N:1)

- Uma Categoria pode classificar várias Despesas (1:N)
- Uma Despesa pertence a uma única Categoria (N:1)


Cartão de Crédito
- Um Cartão de Crédito pode possuir várias Despesas (1:N)
- Uma Despesa pode estar vinculada a um Cartão de Crédito (N:1)

- Um Cartão de Crédito pode possuir várias Faturas (1:N)
- Uma Fatura pertence a um único Cartão de Crédito (N:1)


Despesa
- Uma Despesa pode possuir vários Anexos (1:N)
- Um Anexo pertence a uma única Despesa (N:1)

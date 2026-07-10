# Regras de Negócio — Projeto Finance (Versão 1.0)

## Usuários

### RN001 — Cadastro de Usuário

O sistema deve permitir o cadastro de usuários.

Cada usuário deve possuir uma conta individual e poderá visualizar apenas os seus próprios dados.

### RN002 — Autenticação

O acesso ao sistema deverá exigir autenticação.

O usuário permanecerá autenticado durante sua sessão, conforme as regras de segurança definidas pela aplicação.

---

## Contas e Carteiras

### RN003 — Cadastro de Contas

O usuário poderá cadastrar contas ou carteiras financeiras.

**Exemplos:**

* Banco Inter
* Nubank
* Caixa Econômica
* Dinheiro em espécie
* Carteira física

Cada conta deverá possuir:

* Nome
* Tipo
* Saldo atual
* Status (Ativa ou Inativa)

---

## Receitas

### RN004 — Cadastro de Receitas

O usuário poderá:

* Cadastrar receitas;
* Editar receitas;
* Excluir receitas.

Cada receita deverá possuir:

* Descrição;
* Valor;
* Data;
* Conta de destino.

**Status possíveis:**

* Recebida
* Pendente

---

## Categorias

### RN005 — Categorias

Toda despesa deverá obrigatoriamente possuir uma categoria.

O usuário poderá criar categorias personalizadas.

**Categorias padrão:**

* Alimentação
* Moradia
* Transporte
* Saúde
* Educação
* Lazer
* Contas Fixas
* Outros

---

## Despesas

### RN006 — Cadastro de Despesas

O usuário poderá:

* Cadastrar despesas;
* Editar despesas;
* Excluir despesas.

Cada despesa deverá possuir:

* Descrição;
* Valor;
* Data;
* Categoria;
* Conta utilizada.

**Status possíveis:**

* Paga
* Pendente

---

## Despesas Recorrentes

### RN007 — Cadastro de Recorrências

O usuário poderá cadastrar despesas recorrentes.

**Exemplos:**

* Internet
* Aluguel
* Academia
* Condomínio

Cada recorrência deverá possuir:

* Descrição;
* Valor;
* Categoria;
* Conta;
* Frequência;
* Data de início;
* Data de término (opcional).

O sistema deverá gerar automaticamente as despesas correspondentes conforme a frequência definida.

---

## Despesas Pendentes

### RN008 — Controle de Pendências

O sistema deverá identificar automaticamente despesas não pagas.

O usuário poderá:

* Quitar a despesa;
* Realocar a despesa para o mês seguinte.

O histórico das movimentações deverá permanecer preservado.

---

## Cartões de Crédito

### RN009 — Cadastro de Cartões

O usuário poderá cadastrar cartões de crédito.

Cada cartão deverá possuir:

* Nome;
* Limite total;
* Limite disponível;
* Dia de fechamento;
* Dia de vencimento.

O limite do cartão **não deverá ser considerado como receita**.

---

## Faturas

### RN010 — Controle de Faturas

Toda compra realizada utilizando cartão de crédito deverá compor uma fatura.

Cada fatura deverá possuir:

* Cartão;
* Competência;
* Data de vencimento;
* Valor total;
* Status.

**Status possíveis:**

* Aberta
* Fechada
* Paga

O pagamento da fatura deverá gerar uma despesa vinculada à conta escolhida pelo usuário.

---

## Anexos

### RN011 — Comprovantes

O usuário poderá anexar comprovantes às despesas pagas.

**Formatos permitidos:**

* PDF
* JPG
* PNG

O sistema deverá permitir:

* Visualização;
* Download.

Cada comprovante deverá estar vinculado a uma única despesa.

---

## Consultas

### RN012 — Filtros

O sistema deverá permitir consultas utilizando filtros como:

* Período;
* Categoria;
* Conta;
* Cartão;
* Status;
* Tipo de movimentação.

---

## Dashboard

### RN013 — Indicadores Financeiros

O sistema deverá apresentar automaticamente:

* Receitas do mês;
* Despesas do mês;
* Saldo mensal;
* Maiores categorias de gasto;
* Percentual de gastos por categoria;
* Evolução financeira mensal.

---

## Auditoria

### RN014 — Histórico de Registros

Todos os registros deverão armazenar:

* Data de criação;
* Data da última atualização.

---

## Segurança

### RN015 — Isolamento dos Dados

Um usuário nunca poderá visualizar, editar ou excluir informações pertencentes a outro usuário.

---

# Regras Gerais

### RN016 — Valores Financeiros

Valores financeiros deverão ser obrigatoriamente maiores que zero.

---

### RN017 — Responsabilidade das Movimentações

Toda movimentação financeira deverá estar vinculada a um usuário responsável.

---

### RN018 — Categoria Obrigatória

Toda despesa deverá possuir obrigatoriamente uma categoria.

---

### RN019 — Vinculação de Contas

Toda receita e toda despesa deverão estar vinculadas a uma conta ou carteira financeira.

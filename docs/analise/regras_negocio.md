Regras de Negócio — Projeto Finance (Versão 1.0)
1. Usuários
RN001 — Cadastro de Usuário
O sistema deve permitir o cadastro de usuários.
Cada usuário possui uma conta individual.
Cada usuário visualiza apenas seus próprios dados.
RN002 — Autenticação
O acesso ao sistema deve exigir autenticação.
O usuário deve permanecer autenticado durante sua sessão.
2. Contas e Carteiras
RN003 — Cadastro de Contas

O usuário poderá cadastrar contas ou carteiras financeiras.

Exemplos:

Banco Inter
Nubank
Caixa
Dinheiro
Carteira Física

Cada conta deve possuir:

Nome
Tipo
Saldo atual
Status (Ativa/Inativa)
3. Receitas
RN004 — Cadastro de Receitas

O usuário poderá:

cadastrar
editar
excluir receitas.

Cada receita deve possuir:

descrição
valor
data
conta de destino

Status:

Recebida
Pendente
4. Categorias
RN005 — Categorias

Cada despesa deve obrigatoriamente possuir uma categoria.

O usuário poderá criar categorias personalizadas.

Categorias padrão:

Alimentação
Moradia
Transporte
Saúde
Educação
Lazer
Contas Fixas
Outros
5. Despesas
RN006 — Cadastro de Despesas

O usuário poderá:

cadastrar
editar
excluir despesas.

Cada despesa deve conter:

descrição
valor
data
categoria
conta utilizada

Status:

Paga
Pendente
6. Despesas Recorrentes
RN007 — Cadastro de Recorrências

O usuário poderá cadastrar despesas recorrentes.

Exemplos:

Internet
Aluguel
Academia
Condomínio

A recorrência deve possuir:

descrição
valor
categoria
conta
frequência
data início
data fim (opcional)

O sistema deverá gerar automaticamente as despesas correspondentes.

7. Despesas Pendentes
RN008 — Pendências

O sistema deverá identificar despesas não pagas.

O usuário poderá:

quitar a despesa;
realocar para o mês seguinte.

O histórico deve permanecer preservado.

8. Cartões de Crédito
RN009 — Cadastro de Cartões

O usuário poderá cadastrar cartões.

Cada cartão deve possuir:

nome
limite total
limite disponível
dia do fechamento
dia do vencimento

O limite do cartão não representa receita.

9. Faturas
RN010 — Controle de Faturas

Toda compra realizada no cartão deverá compor uma fatura.

Uma fatura deve possuir:

cartão
competência
vencimento
valor total
status

Status:

Aberta
Fechada
Paga

O pagamento da fatura gera uma despesa na conta escolhida pelo usuário.

10. Anexos
RN011 — Comprovantes

O usuário poderá anexar comprovantes em despesas pagas.

Formatos permitidos:

PDF
JPG
PNG

O sistema permitirá:

visualizar
baixar

Cada comprovante pertence a uma despesa.

11. Consultas
RN012 — Filtros

O usuário poderá consultar informações por:

período
categoria
conta
cartão
status
tipo de movimentação
12. Indicadores
RN013 — Dashboard

O sistema deverá apresentar automaticamente:

receitas do mês
despesas do mês
saldo do mês
maiores categorias
percentual por categoria
evolução mensal
13. Auditoria
RN014 — Histórico

Todos os registros deverão possuir:

data de criação
data da última atualização
14. Segurança
RN015 — Isolamento dos Dados

Um usuário nunca poderá visualizar informações pertencentes a outro usuário.

15. Regras Gerais
RN016

Valores financeiros não podem ser negativos.

RN017

Toda movimentação financeira deve possuir um usuário responsável.

RN018

Toda despesa deve possuir categoria.

RN019

Toda receita e despesa deve estar vinculada a uma conta.
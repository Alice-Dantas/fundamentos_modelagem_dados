# Entenda o que são as Propriedades ACID no Banco de Dados

Ao usamos sistemas digitais no dia a dia — como aplicativos de banco, lojas online, redes sociais ou sistemas escolares — estamos constantemente interagindo com **bancos de dados**. Esses bancos armazenam e organizam informações importantes, como seu saldo bancário, histórico de pedidos ou notas escolares.

Para manter esses dados sempre corretos, seguros e atualizados, os bancos de dados usam um conceito chamado **transação** (conjunto de ações que devem acontecer **juntas e com sucesso**).

Por exemplo, ao fazer uma transferência bancária, o sistema precisa:
1. Tirar o valor da sua conta,
2. Adicionar esse valor à conta de outra pessoa.

Essas duas etapas devem acontecer **ao mesmo tempo**, ou então **nenhuma delas** deve acontecer. Mesmo porque, não faz sentido tirar dinheiro da sua conta se ele não for enviado a outra.

Mas se o sistema travar no meio do processo, ou duas pessoas tentarem fazer ações no mesmo saldo ao mesmo tempo... como o banco de dados garante que os dados **não se percam**, **não se corrompam** ou fiquem **inconsistentes**?

Para evitar esse tipo de problema, os bancos de dados seguem um conjunto de regras chamadas de **propriedades ACID**.
Elas garantem que as transações funcionem de forma segura e confiável, mesmo em situações de falha, uso simultâneo ou erro do sistema.

A tabela a seguir resume o que cada uma dessas propriedades significa e por que elas são importantes:


| Letra | Nome             | O que garante                                                               | Por que é importante?                                   |
|-------|------------------|-----------------------------------------------------------------------------|---------------------------------------------------------|
| A     | **Atomicidade**  | Tudo ou nada: ou todas as operações da transação ocorrem, ou nenhuma ocorre.| Evita operações incompletas que corrompem os dados.     |
| C     | **Consistência** | O banco de dados sai de um estado válido para outro válido.                 | Mantém os dados dentro das regras definidas (válidos).  |
| I     | **Isolamento**   | Transações simultâneas não se atrapalham.                                   | Garante que ações simultâneas não interfiram entre si.  |
| D     | **Durabilidade** | Dados persistem mesmo após falhas.                                          | Garante que dados confirmados nunca sejam perdidos.     |

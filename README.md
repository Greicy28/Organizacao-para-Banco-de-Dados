# Organizacao-para-Banco-de-Dados
# O que devo fazer?

 Você foi convocado para um time que desenvolverá o novo Airbnb
Descreva como você organizaria um banco de dados que precisa , no inicio, de:

Usuários;
Lugares para se hospedar - cadastrados pelos usuários;
Hospedagens (um período de tempo no qual usuário Y vai ficar no lugar X) - realizadas também por usuários;
 Avaliações feitas pelos usuários nas hospedagens.

 A descrição deve conter: 

 Nomes de tabelas que você faria;
 Colunas que você acha mais importantes nas tabelas;
Relacionamentos delas e como ficaria nas colunas das tabelas;
 Uma explicação mínima de o que te levou por essas decisões.


 ### Organização do Banco de Dados para novo Airbnb

### Tabelas e Colunas

### Usuários

id_usuario (PK)

nome

email

senha

data_criacao

telefone

endereco

### Lugares

id_lugar (PK)

id_usuario (FK)

nome

descricao

endereco

preco_por_noite

data_criacao

### Hospedagens

id_hospedagem (PK)

id_usuario (FK)

id_lugar (FK)

data_inicio

data_fim

preco_total

status

### Avaliações

id_avaliacao (PK)

id_hospedagem (FK)

id_usuario (FK)

nota

comentario

data_avaliacao

### Relacionamentos
**Usuários e Lugares**: Um usuário pode cadastrar vários lugares, mas cada lugar é cadastrado por um único usuário. Relacionamento 1:N.

**Usuários e Hospedagens**: Um usuário pode realizar várias hospedagens, mas cada hospedagem é realizada por um único usuário. Relacionamento 1:N.

**Lugares e Hospedagens**: Um lugar pode ser hospedado várias vezes, mas cada hospedagem refere-se a um único lugar. Relacionamento 1:N.

**Hospedagens e Avaliações**: Uma hospedagem pode ter várias avaliações, mas cada avaliação refere-se a uma única hospedagem. Relacionamento 1:N.

**Usuários e Avaliações**: Um usuário pode fazer várias avaliações, mas cada avaliação é feita por um único usuário. Relacionamento 1:N.

### Explicação
**Usuários**: A tabela de usuários é fundamental para armazenar informações básicas e de contato dos usuários, além de garantir a segurança com a coluna de senha.

**Lugares**: Esta tabela armazena os detalhes dos lugares disponíveis para hospedagem, incluindo o usuário que cadastrou o lugar.

**Hospedagens**: Registra as reservas feitas pelos usuários, incluindo as datas de início e fim, e o status da hospedagem (confirmada, cancelada, etc.).

**Avaliações**: Permite que os usuários avaliem suas hospedagens, fornecendo feedback que pode ser útil para outros usuários e para os proprietários dos lugares.

Essa estrutura garante que todas as informações necessárias sejam armazenadas de forma detalhada e que os relacionamentos entre as tabelas sejam claros e eficientes. 
 

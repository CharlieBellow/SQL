## Mais comandos SQL

# INSET INTO

-- insere informações na tabela

<!-- nesse exemplo da escola, o campo matricula é gerado automaticamente, então a gente nao precisa preencher, é a primary key -->
-- Inserindo um novo aluno

INSERT INTO aluno(nome, cpf, responsavel) VALUES('Maria Luiza', 00044477756, 'manuel soares')

-- é necessário colocar os campos que são em formato de texto entre aspas

# UPDATE

--  atualiza ados da tabela, para achar a pessoa que quer mudar, diz qual é o id dela com o comando WHERE
--  se não colocar o where ele altera todos os nomes.
-- atualize na tabela aluno o nome para esse entre aspas e o responsável para esse entre aspas onde o id for 2. Se eu ignorei o CPF é pq não quero alterar

-- OBS.: o Id/primary key sempre vai estar indcado na página/aba da tabela com uma chavezinha azul do lado

UPDATE aluno SET nome='Mariano Garcia', responsavel='Marcio Soares', cpf=00011122233 WHERE matricula = 2

 # DELETE

--  apaga dados da tabela. mas ele apaga a linha inteira da pessoa, a ficha de cadastro. 
-- e não só apaga o cpf ou só o nome da pessoa. apaga todo o registro dela
--  não pode fazer delete sem WHERE pq se não ele vai deletar tudo

DELETE FROM aluno WHERE matricula = 3 


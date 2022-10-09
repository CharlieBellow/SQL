<!--## Criando um bando de dados-->

## Comandos nas tabelas

# CREATE TABLE

para criar a tabela:
CREATE TABLE nomeDaTabela (
  campos,
  da, 
  tabela,

  EX.:
  matricula INTEGER PRIMARY KEY AUTOINCREMENT
  <!--(número inteiro), aqui tô dizendo que é um número inteiro que vai ter nesse campo--> 
  <!-- PRIMARY KEY: diz que esse vai ser o ID principal da tabela -->
  <!-- autoincrementar para preencher automaticamente a primary key sempre que o registro de um novo aluno for adicionado. nesse caso, quando for adicionar mais um aluno, não precisa passar o campo de matricula-->
  nome TEXT,
  cpf INTEGER UNIQUE, <!-- campo único não pode ter dois cpf igual -->
  responsavel TEXT
)

outra tabela:
CREATE TABLE PROFESSORES (
  ID_PROFESSOR INTEGER PRIMARY KEY AUTOINCREMENT,
  NOME TEXT,
  CPF INTEGER UNIQUE,
  MATERIA TEXT
)

* FOREIGN KEY 
CREATE TABLE AULAS(
  ID_PROFESSOR INTEGER,
  MATRICULA INTEGER,
  FOREIGN KEY(ID_PROFESSOR) REFERENCES PROFESSORES(ID_PROFESSOR),
  FOREIGN KEY(MATRICULA) REFERENCES ALUNOS(MATRICULA)
)

# ALTER TABLE / RENAME TO

* faz alterações nas tabelas
* mudando o nome da tabela
ALTER TABLE aluno RENAME TO alunos
ALTER TABLE professor RENAME TO professores

* trocando o nome do id (O nome do campo)
ALTER TABLE AULAS RENAME COLUMN MATRICULA TO matricula_aluno

# Drop tables 
* apaga a tabela e os registros
* CUIDADO APAGA TODOS OS BANCOS DE DADOS
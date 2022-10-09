# Tabelas

no banco de dados tudo é salvo em tabelas

-----------------------------------------------
| Nome     | Nome de Usuário   | Descrição   |
| Josefina | @jose_demais      | dancinhas.. |
| mariano  | @marianoano       | oh no no no |
 ---------------------------------------------


# Campos

* nome das informações
  - nome
  - nome de usuário
  - descrição

# informações

* são as informações que a gente cadastra no banco de dados e que ficam inseridas na tabela
ex:
  * no campo Nome temos:
      - josefina
      - Mariano

  * no campo Nome de Usuário temos:
      - @jose_demais
      - @Marianoano

# Relações entre tabelas

- podemos relacionar uma tabela com a outra
- geralmente se relaciona com um dado que não se repete pq nunca haverá a mesma pessoa com o mesmo arroba nas redes sociais
- ou podemos relacionar pelo Id:

|------------------------------------------------|
| Nome     | Nome de Usuário  | Descrição   | Id |
| Josefina | @jose_demais     | dancinhas.. | 1  |
| mariano  | @marianoano      | oh no no no | 2  |
|------------------------------------------------|

|------------------------------------------------------------|
| Nome de Usuário | Post            | Video     | Id_usuário |
| @jose_demais    | #bancodedados   | video.mp4 | 1          |
| @marianoano     | olha esse video | video.mp4 | 2          |
| @jose_demais    | esse é um post  | foto.jpg  | 1          |
|------------------------------------------------------------|

# exemplo: Escola

banco de dados: Escola guerreiros do amanhã

Tabela 1: ALUNOS
informações dos alunos:
1 - Número de matrícula (Id - identificador)
2 - Nome
3 - CPF
4 - Responsável

|--------------------------------------------|
| Matrícula | Nome     | CPF   | Responsável |
| 0101      | Charlie  | ***** | Pai         |
| 0202      | Jakeliny | 1234  | Mãe         |
| 0102      | aluno    | 5687  | jota        |
|--------------------------------------------|

Tabela 2: PROFESSORES
informações dos professores:
1 - Identificador (Id)
2 - Nome
3 - CPF
4 - matéria

|------------------------------------------|
| id_prof | Nome     | CPF   | Matéria     |
| 0101    | Charlie  | ***** | Psico       |
| 0202    | mayk     | 1234  | JS          |
| 0102    | prof     | 5687  | HTML        |
|------------------------------------------|

obs.: por mais que os identificadores sejam iguais, os contextos são diferentes. um é identificador de aluno (que tá sendo entendido como matrícula) e outro é identificador de professor (id_professor).

Tabela 3: Aulas (relacionando professores e alunos)
informações:
1 - Identificador do professor (Id)
2 - id_aluno
3 - CPF
4 - matéria

|------------------------|
| id_prof | id_aluno     | 
| 0101    | 0101         | 
| 0101    | 0202         | 
| 0101    | 0102         |
| 0202    | 0202         | 
| 0202    | 0101         | 
| 0102    | 0202         | 
| 0102    | 0101         |  
|------------------------|

obs.: nesse caso dizemos que o professor 0101 tm um relacionamento de professor aluno com o aluno 0101. isso é uma organização sistêmica.

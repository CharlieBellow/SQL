<!-- Usa o beekeper pra abrir o banco de dados e roda os comandos lá -->

# SELECT: BUSCA INFORMAÇÕES

    SELECT * FROM aluno

* os comando aparecem em rosa (e são sempre em maiúsculo) e as informações que queremos aparecem em branco
* tem que escrever o nome da informação do jeito que tá respeitando maiusculas e minuscula

* precisa selecionar o código pra rodar

* pra fazer comentário: ctrl+/
    SELECT * FROM professor


    SELECT * FROM aulas

* para selecionar algumas informações da tabela, é só colocar os nomes dos campos que  quer:

SELECT nome, responsavel FROM aluno

*  os campos vão aparecendo de acordo com a ordem que eu colocar no comando:
SELECT nome, materia, cpf FROM professor
SELECT nome, cpf, materia FROM professor

# SELECT com where

-- SELECT com WHERE: consigo procurar os dados de um único aluno só pelo número de matricula, por exemplo

SELECT * FROM aluno WHERE matricula = 1

* fazendo a busca por nome do aluno:
procura alunos que começam com J

SELECT * FROM aluno WHERE nome like 'j%'

* procurando uma letra no meio da palavra:

SELECT * FROM aluno WHERE nome like '%G%'

* pegar dados específicos de uma pessoa que tem a letra g no nome

SELECT matricula, cpf FROM aluno WHERE nome like '%G%'
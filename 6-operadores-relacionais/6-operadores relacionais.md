## OPERADORES RELACIONAIS

# igual =

se eu quiser buscar o aluno pelo CPF identico/igual a = (serve pra quando eu tiver um dado específico da pessoa e quero procurar por ele)

SELECT * FROM aluno WHERE cpf = 45678945645

* o igual não serve pra comparações do tipo texto


# like

* funciona da mesma forma do igual. só que o like é pra campos de texto co já vimos no outro tópico:

SELECT * FROM aluno WHERE nome like 'Jakeliny Gracielly'
* OBS.: sempre que trabalha com texto tem que colocar entre aspas. (no meu só funciona aspas simples)

* pesquisando por sobrenome
SELECT * FROM aluno WHERE responsavel like '%Gracielly'

# Maior que >

--  pega um dado que seja maior que o número indicado

SELECT * FROM aluno WHERE matricula > 1

# Menor que <
--  pega um dado que seja menor que o número indicado

SELECT * FROM aluno WHERE matricula < 4

--  o 4 é menor que 3 que são todos os alunos, então tra todos

# maior/igual que >=
--  pega um dado que seja maior u igual que o número indicado

SELECT * FROM aluno WHERE matricula >= 2

-- pega o 3 e o 2


# menor/igual que <=

--  pega um dado que seja menor ou igual que o número indicado

SELECT * FROM aluno WHERE matricula <= 2

--  pega o 1 e o 2


 # Não igual a <>

SELECT * FROM aluno WHERE matricula <> 2

-- traz só o 1 e 3 pq são diferentes de dois

-- SELECT * FROM aluno WHERE cpf <> '123%'
-- não funciona com número tipo string (entre aspas

# Diferente de !=

SELECT * FROM aluno WHERE matricula != 3

-- trouxe só 1 e 2 pq são diferentes de 3

## Operadores Lógicos

 # AND

-- junta duas condições

-- procura todos os dados da tabela aluno onde o nome comece com J e a matrícula seja menor que dois

SELECT * FROM aluno WHERE nome like 'J%' AND matricula < 2

-- traz a jakeliny com o numero de matricula 1

SELECT * FROM aluno WHERE nome like 'J%' AND matricula > 2

-- traz o joão com o numero de matricula 3

# OR (ou)

SELECT * FROM aluno WHERE matricula > 2 OR nome like 'G%'

-- o numero de matricula é maior que 2 ou o nome começa com G

<!-- a partir daqui usamos outro banco de dados unindo_tabela.sqlite -->

 # BETWEEN (entre) / NOT BETWEEN (não está entre)

-- pega dados que estão entre um numero e outro de id

SELECT * FROM funcionarios WHERE id_funcionario BETWEEN 4 AND 7

-- pega numeros de id que NÂO estão dentro desse intervalo (ignora o intervalo que eu coloquei)

SELECT * FROM funcionarios WHERE id_funcionario NOT BETWEEN 4 AND 7

 # IN (dentro) / NOT IN (não está dentro)

-- pega dados que estejam dentro desses parâmetros passados dentro do parênteses

SELECT * FROM funcionarios WHERE id_departamento IN (1, 2, 5)

-- O NOT IN faz o contrário do IN. Ignora os parâmetros apresentados

SELECT * FROM funcionarios WHERE id_departamento NOT IN (1, 3, 5)

 # IS NULL (vazio)/ IS NOT NULL (não está vazio)

-- mostra dados que estão vazio

SELECT * FROM funcionarios WHERE id_departamento IS NULL

-- mostra dados que NÃO estão vazios

SELECT * FROM funcionarios WHERE id_departamento IS NOT NULL


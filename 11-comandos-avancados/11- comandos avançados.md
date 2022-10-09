## COmandos avançados

 # ORDER BY (por order de)
-- pra quando eu quiser pegar uma tabela por ordem alfabética e não do ID que é o padrão

SELECT * FROM aluno ORDER BY nome

-- por ordem decrescente

SELECT * FROM professor ORDER BY materia DESC

-- organizando por número:

SELECT * FROM professor ORDER BY cpf

-- por número decrescente

SELECT * FROM professor ORDER BY cpf DESC

 # LIMIT

--  limita a quantidade de resultados
-- tipo, traga os dois primeiros resultados que você encontrar

SELECT * FROM aluno LIMIT 2


# OFFSET


-- diz quantos registros é pra ignorar e o limite diz quantos é pra trazer
-- então da pra criar um intervalo de resultados que vc quer que apareça

SELECT * FROM funcionarios
LIMIT 3 OFFSET 4 -- ignora os 4 primeiros resultados e mostra só os próximos 2

  # COUNT (conte)
-- conta quantos dados (quantas linhas) tem preenchida na tabela considerando o campo colocado nos parênteses
--  só funciona se escrever em letra minúcula

SELECT count(nome) FROM funcionarios

--  nesse caso, se tiver outros campos que esteja nulo, ele vai mostrar também.
-- mas se eu não quiser considerar esse espaço vazio é só pegar por esse campo:

SELECT count(id_departamento) FROM funcionarios

 # GROUP BY
-- agrupa dados semelhantes
-- se eu quiser saber quantos funcionários existem em cada departamento

SELECT id_departamento, count(id_departamento) 
FROM funcionarios
GROUP BY id_departamento

 # JOIN, GROUP BY e COUNT juntos
-- quero saber quantos funcionários exestem por departamento, 
-- mas quero ver o nome do departamento também

SELECT departamentos.descricao, count(funcionarios.id_departamento) 
FROM funcionarios
JOIN departamentos
ON funcionarios.id_departamento = departamentos.id_dept
GROUP BY departamentos.id_dept

-- o group by pode agrupar por um campo que não vai ser mostrado

  # HAVING
-- pegar todos os funcionarios que possuem departamentos 
-- e contar quantos funciionarios tem em cada departamento

SELECT departamentos.descricao, COUNT(funcionarios.id_departamento)
FROM funcionarios
JOIN departamentos
ON funcionarios.id_departamento = departamentos.id_dept
GROUP BY departamentos.id_dept
HAVING count(funcionarios.id_departamento) >= 2
-- trouxe departamentos que tenham 2 ou mais funcionários

-- o where, só serve pra fazer comparações com outros campos, 
-- não serve pra campos agrupados. por isso usamos o HAVING

--  também funciona com operadores logicos

SELECT departamentos.descricao, COUNT(funcionarios.id_departamento)
FROM funcionarios
JOIN departamentos
ON funcionarios.id_departamento = departamentos.id_dept
GROUP BY departamentos.id_dept
HAVING count(funcionarios.id_departamento) IN (2, 4)
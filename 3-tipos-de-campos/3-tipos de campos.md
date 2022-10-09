# Text

todo campo precisa de uma configuração que diz que tipo de infirmação vai ser guardada. ex: texto, números, caracteres especiais

Tabela: perfil

* nome: TEXT (podem tem caracteres especiais, espaços, letras, números)
*nome de usuário: TEXT
*descrição: TEXT

# Number

- só aceita números sem espaços

Telefone: Number

# Datatime

* (data e hora)

* guarda números e traços

tabela: posts
data: DATATIME

# Primary Key

* identificador (Id)
* o banco controla a primary key e não deixa que tenha números iguais, ou seja as informarções da pessoa são únicas
tabela: perfil:

* id user: Number Primary KEY
(pra poder conter só numeros na primary key é necesário criar um id-user quando o identificador da pessoa tem carcteres especiais)

tabela: perfil:

* nome: TEXT (podem tem caracteres especiais, espaços, letras, números)
* nome de usuário: TEXT
* descrição: TEXT
* telefone: number
* id user: Number Primary KEY
(pra poder conter só numeros na primary key é necesário criar um id-user quando o identificador da pessoa tem carcteres especiais)

# foreign key

* chave estrangeira: faz relação de uma tabela com a outra

* faz referência à primary kay de outra tabela.. tipo no exemplo da relação entre alunos e professores...
exemplo:
primary key: id user
foreign key: id_user

* OBS.: toda tabela precisa ter um identificador
<!-- então vamos colocar o identificador da tabela post -->
id_post: primary key

tabela post:
id_post: primary key
post: TEXT
video: TEXT
data: DATATIME
id_user: Number foreing key (perfil) <!-- ou seja, a id_user é uma chave estrangeira da tabela perfil --> essa chave pode se repetir na tabela pq ela está referenciando a primary key de outra tabela, mas a primary key não pode se repetir

# Unique

no caso da rede social, um nome de usuário não pode ser igual ao outro. por isso, além da primary key (que é um number) não poder se repetir, nós também não podemos repetir o nome de usuário (que é um text). pra isso usa o unique

tabela: perfil:

* nome: TEXT (podem tem caracteres especiais, espaços, letras, números)
* nome de usuário: TEXT UNIQUE
* descrição: TEXT
* telefone: number
* id user: Number Primary KEY
(pra poder conter só numeros na primary key é necesário criar um id-user quando o identificador da pessoa tem carcteres especiais)

# Nomes de campos em tabelas

* Regras para escrever nome de tabelas e de campos

1 - Deve começar por uma letra do alfabeto

2 - Os caracteres seguintes não são permitidos:
 () + - / ** " : = & | # > < ^ ' { } % ~ ç ã ê é í

3 - Não pode conter espaços nem traços-para-separar

4 - usa underline ou CamelCase para separar as palavras

5 - não pode ter acentuação

* corrigindo as tabelas:

tabela: perfil:

* nome: TEXT (podem tem caracteres especiais, espaços, letras, números)
* nomeDeUsuario: TEXT UNIQUE
* descricao: TEXT
* telefone: number
* id_user: Number Primary KEY

tabela post:
id_post: primary key
post: TEXT
video: TEXT
data: DATATIME
id_user: Number foreing key

# exemplo da escola

tabela alunos:

matricula: NUMBER PRIMARY KEY
nome: TEXT
cpf: NUMBER Unique
responsavel: TEXT

tabela professores:

id_professor: NUMBER PRIMARY KEY
nome: TEXT
cpf: NUMBER Unique
materia: TEXT

Tabela de aulas:

id_professor: Number foreing key (professor)
id_aluno: Number foreing key (aluno)
<!-- uma tabela pode ter sduas foreing key, mas nao pode ter 2 primary key-->
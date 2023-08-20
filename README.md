# modelagem-banco-de-dados
Exercício de aula UnisãoMiguel 1º período em GTI

Resolução de 5 questões solictadas pela Profª Sônia Oliveira na disciplina Banco de dados.
Atividade BD 3- UniSãoMiguel
Professora Sônia Oliveira
1- Elaborar um diagrama E-R para uma seguradora de automóveis
Entidades: Cliente, Apólice, Carro e Acidentes.
Requisitos:
a) Um cliente pode ter várias apólices (no mínimo uma);
b) Cada apólice somente dá cobertura a um carro;
c) Um carro pode ter zero ou n registros de acidentes a ele.
Atributos:
a) Cliente: Número, Nome e Endereço;
b) Apólice: Número e Valor;
c) Carro: Registro e Marca;
d) Acidente: Data, Hora e Local;

número
cliente
nome
(1,n)

endereço
observações sobre modelagem de dados: PK é representada por sublinhado e cor azul.
FK é representada pela elipse vermelha
2 elipses significam chave composta de atributo
Entidades: Cliente, Apólice, Carro e Acidentes.
atributos: número, nome, valor, registro, marca, data, hora e etc...
possui
(1,1)
número
data
apólice
(1,1)
possui
hora
valor
local
(1,1)
registro
carro
(1,n)
cobre
acidente
(1,1)
marca

2 - Elaborar um diagrama para uma Indústria.
Entidades: Peças, Depósitos, Fornecedor, Projeto, Funcionário e Departamento.
Requisitos:
a) Cada Funcionário pode estar alocado a somente um Departamento;
b) Cada Funcionário pode pertencer a mais de um Projeto;
c) Um projeto pode utilizar-se de vários Fornecedores e de várias Peças;
d) Uma Peça pode ser fornecida por vários Fornecedores e atender a vários Projetos;
e) Um Fornecedor pode atender a vários Projetos e fornecer várias Peças;
f) Um Depósito pode conter várias Peças;
g) Deseja-se ter um controle do material utilizado por cada Projeto, identificando
inclusive o seu Fornecedor. Gravar as informações de data de Início e Horas
Trabalhadas no Projeto.
entidades e atributos:
Peças: Número, Peso e Cor;
Depósitos: Número e Endereço;
Fornecedor: Número e Endereço;
Projeto: Número e Orçamento;
Funcionário: Número, Salário e Telefone;
Departamento: Número e Setor.
hora
data
DÚVIDA!
Como relaciona fornecedor em controle?
Sendo fornecedor uma entidade?
orçamento
controle
número
número
endereço
(n,1)
número
salário
(0,n)
Funcionário
pertence
(1,n)
projeto
depósito
faz
telefone
(1,1)(n,n)
trabalhausa
(1,1)
(n,1)
peças
(1,1)
usa
(1,n)
(1,1)
cor
número
peso
departamento
fornecedor
número
setor
número
orçamento

3 - Um departamento tem como chave
primária um código de departamento,
e também possui um nome, e um setor.
Os cursos também irá possuir um
código, nome do curso, quantidade de
vagas. Os relacionamentos entre eles
se mapeia da seguinte maneira: Um
departamento pode possuir 1 curso ou
vários cursos, enquanto vários cursos só
pode ser inseridos em pelo menos 1
departamento e somente 1.
Entidades: departamento, curso
Atributos: código do departamento, nome do departamento, setor do departamento,
código do curso, quantidade de vagas, nome do curso
código
código
nome
(1,n)
departamento
(1,1)
pertence
curso
nome
setor
qts_de_vagas

4 - Um aluno precisa de um professor
para orientar o seu trabalho, ele tem
como atributos: nome, matricula,
endereço, e telefone.
O Orientador
tem como atributos: nome, CPF,
matricula, endereço, telefone e titulo
acadêmico.
O relacionamento entre
eles se mapeia da seguinte forma: O
aluno pode ser orientado no mínimo
por 1 orientador e no máximo 1
orientador.
Enquanto o orientador pode orientar pelo menos 1 aluno
ou váriosalunos.
Entidades: departamento, curso
Atributos: código do departamento, código do departamento, setor do departamento,
código do curso, quantidade de vagas, nome do curso
matricula
matrícula
nome
(1,1)
precisa
(1,n)
aluno
orientador
nome
endereço
CPF
telefone
endereço
telefone
título_academico

5 - Um instrutor pode realizar no mínimo um curso online ou vários cursos online.
Um curso possui pelo menos um assunto ou vários assuntos. Um curso pode ter
pelo menos uma linha de pesquisa ou no máximo uma linha de pesquisa. Um
curso pode possuir no mínimo um tipo de formatação e no máximo uma. Sabendo
dessa informação, realize os diagramas de modo que, o instrutor tem: nome,
cpf, telefone e e-mail. O curso tem: código_curso, nome do curso, instrutor do
curso, data_criação. A linha de pesquisa tem: código, tema. E os assuntos tem:
cod_assunto, nome, descrição.
Entidades: instrutor, curso, pesquisa, assunto
Atributos: nome instrutor, CPF, telefone, email, código do curso, nomedo curso,
instrutor, data decriação,código da pesquisa, tema da pesquisa,
código do assunto, nome do assunto, descrição do assunto
cód_curso
cód_assunto
nome
nome
instrutor
descrição
data_criação
nome
cpf
instrutor
(1,n)
realiza
(1,n)
curso
(1,n)
possui
(1,n)
assunto
fone
(1,1)
email
(1,1)
tem
formatação
(1,n)
cód_pesquisa
pesquisa
tema
Dúvida: é possível deixar uma entidade sem atributos?

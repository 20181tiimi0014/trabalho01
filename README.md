# TRABALHO 01:  SmartSales
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado.

# Sumário

##### 1 Componentes
##### 2 Introdução e Motivação
##### 3 Mini-Mundo
##### 4 Rascunhos Básicos da Interface
##### 4.1 Relatórios
###### 4.2 Tabela com os Dados do Sistema
##### 5 Modelo Conceitual
###### 5.1 Descrição dos Dados
##### 6 Modelo Lógico
##### 7 Modelo Físico
##### 8 Insert Aplicado nas Tabelas do Banco de Dados
###### 8.1 Detalhamento das Informações
###### 8.2 Inclusão do Script para Exclusão de Tabelas e Inserção de Dados
###### 8.3 Inclusão do Script para a Exclusão de Tabelas Existentes, Criação de Tabelas Novas e Inserção de Dados
##### 9 Tabelas e Principais Consultas
###### 9.1 Consultas das Tabelas com Todos os Dados Inseridos
###### 9.2 Consuktas das Tabelas com o Filtro Where
###### 9.3 Consultas que Usam Operadores Lógicos, Aritméticos e Tabelas ou Campos Renomeados
###### 9.4 Consuktas que Usam Operadores Like e Data
###### 9.5 Atualização e Exclusão de Dados
###### 9.6 Consultas com Junção e Ordenação
###### 9.7 Consultas com Goup By e Funções de Agrupamento
###### 9.8 Condultas com Left e Right Join
###### 9.9 Consultas com Self Join e View
###### 9.10 Subconsultas
###### 9.11 Lista de Códios das Funções e Triggers
###### 9.12 Geração de Dados
###### 9.13 Backup do Banco de Dados
###### 9.14 Aplicação de Índices e Testes de Performance

<br>

### 1. COMPONENTES<br>

Beatriz Auer Mariano: biaauer03@gmail.com<br>
 

### 2.INTRODUÇÃO E MOTIVAÇAO<br>

> A empresa SmartSales visa auxiliar a gestão de compra e venda de produtos, desde miniempresas a grandes negócios. Sabe-se que é demandado muito tempo para listar, estocar e fazer o balanço financeiro de uma empresa, o que pode resultar em falhas e, consequentemente, prejuízos. Sendo assim, a SmartSales tem como objetivo servir de apoio para o empresário, a fim de agilizar certos processos e contribuir no aumento da lucratividade. Após o cadastro de informações, que podem ser feitos manualmente ou por meio de sensores no estoque físico o sistema gerará relatórios que atenderão aos interesses do cliente.
 

### 3.MINI-MUNDO<br>

> O sistema proposto para a SmartSales conterá as informações aqui detalhadas. Para melhores entendimentos, o termo "compra" está relacionado à aquisição de produtos da loja/estabelecimento, e "venda" está relacionado à saída de produtos da loja / estabelecimento.Inicialmente, serão cadastrados em uma determinada data os  fornecedores de produtos, que contém um código, que será um número de documento padrão da escolha do usuário, nome fantasia, razão social, latitude e longitude da loja matriz,ramo e contato da empresa. Espera-se que, com esses dados, os responsáveis pela gestão da loja/estabelecimento saibam onde estão aplicando seu dinheiro, quais os fornecedores mais frequentes e até mesmo o que costuma ter os produtos mais baratos. Em seguida, é cadastrada a aquisição de produtos da loja/estabelecimento indicando a data e hora da compra, o preço de aquisição e quantidade de produto adquirida. Sobre o produto, será preciso cadastrar seu código, código de barras, descrição, preço de venda, categoria, marca e unidade. A partir dessas informações, o sistema já está pronto para computar sua função principal: a saída de produtos da loja ou empresa, a partir da nota fiscal, que será gerada pela tabela compra, que contém número identificador, data da venda e o cliente para o qual o produto foi vendido. Também será necessário informar quais os produtos vendidos e sua quantidade. Os clientes serão cadastrados quando realizarem a primeira compra e terão código, que será um número de documento padrão da escolha do usuário, nome, data de nascimento, data_cadastro, latitude e longitude de sua residêncida, sexo e contato.


### 4. RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto consta o pdf com o rascunho da interface do nosso programa. <br>

![Menu Inicial SmartSales](https://github.com/auerbeatriz/modtrab/blob/master/imagens/menu%20incial%20SS.jpg)
![Arquivo PDF do Protótipo Balsamiq feito para Empresa SmartSales](https://github.com/20181tiimi0014/trabalho01/blob/master/novo%20Mini%20Mundo.pdf)

### 4.1 RELATÓRIOS

> Para que o programa seja iniciado, ele precisa dos seguintes relatórios:
* Informações dos fornecedores com código, nome, ramo e contato.
* Informação do produto com código, nome, fornecedor, data de compra, quantidade comprada, preço de compra, preço de venda. Caso seja a primeira vez que o produto seja comprado, ele será inserido à tabela dos produtos. Caso não, a quantidade será somada a já existente.
* Informação dos clientes, que serão cadastrados ao fazerem sua primeira compra, com código, nome, idade e sexo.

>Para que funcione, precisa dos seguintes relatórios:
* Venda (funciona como uma nota fiscal) contendo o número da nota, o código do produto, a quantidade vendida, o desconto, se houver e o cliente para o qual o produto foi vendido.

> Com esses relatórios, o sistema consegue responder às seguintes questões:
* Quantos e quais produtos foram vendidos;
* Qual o produto menos e mais vendido;
* Quanto foi a despesa e o lucro com os produtos;
* Qual a média de idade dos clientes da empresa/estabelecimento;
* Qual categoria de produtos mais vendida;
* Qual é a marca de produtos mais vendida;
* Quais são os principais ramos dos fornecedores.
 
### 4.2 TABELA DE DADOS DO SISTEMA:

> A tabela aqui anexada contém os atributos do sistema SmartSales. Ela simula um relatório com todos os dados que serão armazenados.

    CLIENTE: tabela que contém as informações de todos os clientes da empresa/estabelecimento.
    REALIZA: tabela de relação entre CLIENTE e COMPRA, onde um cliente realiza uma compra.
    COMPRA: tabela que contém as informações de todas as vendas dos produtos da empresa/estabelecimento.
    COMPRA_POSSUI_PRODUTO: tabela de relação entre COMPRA e PRODUTO, onde cada compra pode ter uma quantidade específica de um ou vários produtos.
    PRODUTO: tabela que contém as informações de todos os produtos comercializados pela empresa/estabelecimento.
    PRODUTO_POSSUI_TIPO_PRODUTO: tabela que contém os tipos aos quais os produtos pertencem.
    FORNECEDOR: tabela que contém as informações de todos os fornecedores da empresa/estabelecimento.
    FORNECE: tabela de relação entre FORNECEDOR e PRODUTO, onde um fornecedor fornece um produto para a empresa/estabelecimento.
    RAMO: tabela que guarda os ramos aos quais os forncededores pertencem.
    CONTATO: tabela que contém os contatos de cada forncedor e um código com o tipo de contato.
    TIPO_CONTATO: tabela que contém os tipos de contato, como telefone, email site, entre outros.
    CLIENTE: tabela que contém as informações de todos os clientes da empresa/estabelecimento.
    
![Exemplo de Tabela de dados da Empresa SmartSales](https://github.com/auerbeatriz/modtrab/blob/master/arquivos/nova%20PlanilhaSmartsSales%20%20em%20ods.ods?raw=true "Tabela - Empresa SmartSales")

### 5.MODELO CONCEITUAL<br>

> O modelo conceitual apresenta as entidades existentes no programa e os relacionamentos que elas possuem entre si.
        
![Modelo Conceitual](https://github.com/auerbeatriz/modtrab/blob/master/imagens/img_modelo_conceitual_22_09.png?raw=true "Modelo Conceitual SmartSales")

### 5.1 DESCRIÇÃO DOS DADOS DESATUALIZADO

    Tabela CLIENTE
	CODIGO: campo que armazena o código do cliente.
	NOME: campo que armazena o nome do cliente.
	SEXO: campo que armazena o sexo do cliente.
	IDADE: campo que armazena a idade do cliente.
	LATITUDE: campo que armazena a latitude da residência do cliente.
	LONGITUDE: campo que armazena a longitude da residência de um cliente.

    Tabela COMPRA
	NUMERO_NOTA: camo que armazena o número identificador da nota fiscal.
	HORA: campo que armazena a hora em que a nota foi emitida.
	DATA: campo que armazena a data em que a nota foi emitida.

    Tabela POSSUI
	QTD: campo que armazena a quantidade de produtos que foram vendidos naquela nota.

    Tabela PRODUTO
	CODIGO: campo que armazena o código do produto.
	NOME: campo que armazena o nome do produto.
	VALOR: campo que armazena o valor do produto.

    Tabela FORNECEDOR
	NOME: campo que armazena o nome fantasia da empresa.
	CODIGO: campo que armazena o código da empresa.

    Tabela RAMO
	CODIGO: campo que armazena o código do ramo.
	DESCRICAO: campo que armazena a descrição do ramo (exemplo: alimentos, sapato).

    Tabela CONTATO
	DESCRICAO: campo que armaena a descrição do contato (exemplo: número de telefone).

    Tabela TIPO_CONTATO
	CODIGO: campo que armazena o código do tipo de contato.
	TIPO: campo que armazena o o tipo de contato (exemplo: telefone, email).

### 6	MODELO LÓGICO<br>

> Aqui consta o modelo lógico do nosso banco de dados.

![Modelo Lógico SmartSales](https://github.com/auerbeatriz/modtrab/blob/master/imagens/img_modelo_logico_22_09.png?raw=true "Modelo Lógico - Empresa SmartSales")

### 7	MODELO FÍSICO ATUALIZADO<br>
    /* Lógico_1: */

	CREATE TABLE COMPRA (
    		numero_nota integer PRIMARY KEY,
    		data date,
    		hora varchar(10)
	);

	CREATE TABLE PRODUTO (
	    	codigo integer PRIMARY KEY,
		descricao varchar(100),
    		valor_venda float,
    		FK_CATEGORIA_codigo integer,
    		FK_MARCA_codigo integer,
    		FK_UNIDADE_codigo integer

	);

	CREATE TABLE CATEGORIA (
    		codigo integer PRIMARY KEY,
    		categoria varchar(200)
	);

	CREATE TABLE MARCA (
    		codigo integer PRIMARY KEY,
    		marca varchar(100)
	);

	CREATE TABLE CLIENTE (
	    	codigo integer PRIMARY KEY,
    		nome varchar(100),
    		data_nasc date,
    		data_cadastro date,
    		latitude varchar(20),
    		longitude varchar(20)
	);

	CREATE TABLE FORNECEDOR (
    		codigo integer PRIMARY KEY,
    		nome varchar(100),
    		data_cadastro date,
    		latitude varchar(20),
    		longitude varchar(20),
    		FK_RAMO_codigo integer
	);

	CREATE TABLE UNIDADE (
    		codigo integer PRIMARY KEY,
    		unidade varchar(30)
	);

	CREATE TABLE RAMO (
    		codigo integer PRIMARY KEY,
    		ramo varchar(60)
	);

	CREATE TABLE CONTATO (
    		codigo integer PRIMARY KEY,
    		descricao varchar(50),
    		FK_FORNECEDOR_codigo integer,
    		FK_CLIENTE_codigo integer,
    		FK_TIPO_CONTATO_codigo integer
	);

	CREATE TABLE TIPO_CONTATO (
    		codigo integer PRIMARY KEY,
    		descricao varchar(50)
	);

	CREATE TABLE Contém (
    		fk_COMPRA_numero_nota integer,
    		fk_PRODUTO_codigo integer,
    		qtd Integer
	);

	CREATE TABLE Realizada_por (
    		fk_CLIENTE_codigo integer,
    		fk_COMPRA_numero_nota integer
	);

	CREATE TABLE É_Fornecido (
    		fk_FORNECEDOR_codigo integer,
    		fk_PRODUTO_codigo integer,
    		data_aquisicao Date,
    		hora_aquisicao varchar(10),
    		preco_aquisicao float,
    		qtd_adquirida Integer
	);
 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_2
    		FOREIGN KEY (FK_CATEGORIA_codigo)
    		REFERENCES CATEGORIA (codigo)
    		ON DELETE RESTRICT;
 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_3
    		FOREIGN KEY (FK_MARCA_codigo)
    		REFERENCES MARCA (codigo)
    		ON DELETE RESTRICT;
 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_4
	    	FOREIGN KEY (FK_UNIDADE_codigo)
    		REFERENCES UNIDADE (codigo)
    		ON DELETE RESTRICT;
 
	ALTER TABLE FORNECEDOR ADD CONSTRAINT FK_FORNECEDOR_2
    		FOREIGN KEY (FK_RAMO_codigo)
    		REFERENCES RAMO (codigo)
    		ON DELETE RESTRICT;
 
	ALTER TABLE CONTATO ADD CONSTRAINT FK_CONTATO_2
    		FOREIGN KEY (FK_FORNECEDOR_codigo)
    		REFERENCES FORNECEDOR (codigo)
    		ON DELETE CASCADE;
 
	ALTER TABLE CONTATO ADD CONSTRAINT FK_CONTATO_3
    		FOREIGN KEY (FK_CLIENTE_codigo)
    		REFERENCES CLIENTE (codigo)
    		ON DELETE CASCADE;
 
	ALTER TABLE CONTATO ADD CONSTRAINT FK_CONTATO_4
    		FOREIGN KEY (FK_TIPO_CONTATO_codigo)
    		REFERENCES TIPO_CONTATO (codigo)
    		ON DELETE CASCADE;
 
	ALTER TABLE Contém ADD CONSTRAINT FK_Contém_1
    		FOREIGN KEY (fk_COMPRA_numero_nota)
    		REFERENCES COMPRA (numero_nota)
    		ON DELETE RESTRICT;
 
	ALTER TABLE Contém ADD CONSTRAINT FK_Contém_2
    		FOREIGN KEY (fk_PRODUTO_codigo)
    		REFERENCES PRODUTO (codigo)
    		ON DELETE RESTRICT;
 
	ALTER TABLE Realizada_por ADD CONSTRAINT FK_Realizada_por_1
    		FOREIGN KEY (fk_CLIENTE_codigo)
    		REFERENCES CLIENTE (codigo)
    		ON DELETE RESTRICT;
 
	ALTER TABLE Realizada_por ADD CONSTRAINT FK_Realizada_por_2
    		FOREIGN KEY (fk_COMPRA_numero_nota)
    		REFERENCES COMPRA (numero_nota)
    		ON DELETE RESTRICT;
 
	ALTER TABLE É_Fornecido ADD CONSTRAINT FK_É_Fornecido_1
    		FOREIGN KEY (fk_FORNECEDOR_codigo)
    		REFERENCES FORNECEDOR (codigo)
    		ON DELETE RESTRICT;
 
	ALTER TABLE É_Fornecido ADD CONSTRAINT FK_É_Fornecido_2
    		FOREIGN KEY (fk_PRODUTO_codigo)
    		REFERENCES PRODUTO (codigo)
    		ON DELETE RESTRICT;
		
## Marco de Entrega 07 em: (27/05/2019)<br>

### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS ATUALIZADO<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        #Inserção de dados em FORNECEDOR
	INSERT INTO
		FORNECEDOR
	VALUES (0001, 'Biancogres', 'alimentos', '(11)1111-1111', 'biancogres@destino.com'),
		(0002, 'Sepé', 'alimentos', '(22)2222-2222', 'sepe@destino.com'),
		(0003, 'Camil', 'alimentos', '(33)3333-3333', 'camil@destino.com'),
		(0004, 'Bonduelle', 'alimentos', '(44)4444-4444', 'bonduelle@destino.com'),
		(0005, 'cofril', 'alimentos', '(55)5555-5555', 'cofril@destino.com'),
		(0006, 'Eliana', 'panos', '(66)6666-6666', 'eliana@destino.com'),
		(0007, 'Tilibra', 'papelaria', '(77)7777-7777', 'tilibra@destino.com'),
		(0008, 'PifPaf', 'alimentos', '(88)8888-8888', 'pifpaf@destino.com'),
		(0009, 'Renata', 'alimentos', '(99)9999-9999', 'renata@destino.com'),
		(0010, 'Bauducco', 'alimentos', '(10)1010-1010', 'bauducco@destino.com'),
		(0011, 'Trakinas', 'alimentos', '(11)0111-0111', 'trakinas@destino.com'),
		(0012, 'Garoto', 'alimentos', '(12)1212-1212', 'garoto@destino.com');
		(0013, 'Hershers', 'alimentos', '(13)1313-1313', 'hershers@destino.com'),
		(0014, 'Veja', 'produtos quimicos', '(14)1414-1414', 'veja@destino.com'),
		(0015, 'Qboa', 'produtos quimicos', '(15)1515-1515', 'qboa@destino.com');



	#Inserção de dados em PRODUTO
	INSERT INTO 
		PRODUTO
	VALUES (11111, 'arroz sepé', 10.98, 'arroz 5kg'), 
		(22222, 'feijão  camil', 3.78, 'feijão'),
		(33333, 'milho bonduelle', 1.15, 'milho verde'),
		(44444, 'linguica cofril', 13.89, 'linguica defumada'),
		(55555, 'pano de prato eliana', 4, 'pano de prato'),
		(66666, 'caderno superpoderosas tilibra', 18.50, 'caderno 1 materia'),
		(77777, 'arroz biancogres', 9.70, 'arroz 5kg'),
		(88888, 'arroz sepé', 7.90, 'arroz 1kg'),
		(99999, 'arroz biancogres', 6.00, 'arroz 1kg'),
		(10101, 'linguica pifpaf', 10.60, 'linguica defumada'),
		(10102, 'biscoito renata', 1.00, 'biscoito recheado'),
		(10103, 'bicoito recheado bauducco', 1.89, 'biscoito recheado'),
		(10104, 'biscoito recheado trakinas', 1.78, 'biscoito recheado'),
		(10105, 'barra ao leite garoto', 5.99, 'barra chocolate'),
		(10106, 'barra meio amargo garoto', 5.99, 'barra chocolate'),
		(10107, 'desengordurante veja', 3.98, 'produtos quimicos'),
		(10108, 'agua sanitaria qboa', 3.99, 'produtos quimicos');


	#Inserção de dados em COMPRA
	INSERT INTO
		COMPRA
	VALUES (1, '2019-08-19', '8:03'),
		(2, '2019-08-19', '8:17'),
		(3, '2019-08-19', '8:25'),
		(4, '2019-08-19', '8:28'),
		(5, '2019-08-19', '8;37'),
		(6, '2019-08-19', '8:40'),
		(7, '2019-08-19', '8:46'),
		(8, '2019-08-19', '8:51'),
		(9, '2019-08-19', '8:58'),
		(10, '2019-08-19', '9:02'),
		(11, '2019-08-19', '9:11'),
		(12, '2019-08-19', '9:15'),
		(13, '2019-08-19', '9:18'),
		(14, '2019-08-19', '9:24'),
		(15, '2019-08-19', '9:35');

	#Inserção de dados em CLIENTE
	INSERT INTO
		CLIENTE
	VALUES (1, 'Joana', 'F', 18, 1111111111, 1111111111),
		(2, 'Jonas', 'M', 22, 2222222222, 2222222222),
		(3, 'Lucas', 'M', 25, 3333333333, 3333333333),
		(4, 'Lúcia', 'F', 19, 444444444, 444444444),
		(5, 'Maria Eduarda', 'F', 19, 555555555, 555555555),
		(6, 'Eloina', 'F', 47, 66666666, 666666666),
		(7, 'Caio', 'M', 26, 777777777, 777777777),
		(8, 'Mateus', 'M', 18, 888888888, 888888888),
		(9, 'Weverton', 'M', 20, 999999999, 999999999),
		(10, 'Marcos', 'M', 49, 10000000, 10000000),
		(11, 'José', 'M', 28, 11000000, 11000000),
		(12, 'Bianca', 'F', 23, 12000000, 12000000),
		(13, 'Brenda', 'F', 22, 13000000, 13000000),
		(14, 'Bruna', 'F', 26, 1400000, 14000000),
		(15, 'Rodolfo', 'M', 25, 15000000, 15000000);


	#Inserção de dados em POSSUI
	INSERT INTO
		POSSUI
	VALUES (1, 11111, 2),
		(1, 22222, 5),
		(1, 44444, 2),
		(2, 10102, 10),
		(2, 10106, 2),
		(3, 10107, 2),
		(3, 10108, 1),
		(3, 99999, 1),
		(4, 10105, 3),
		(4, 10106, 3),
		(5, 88888, 2),
		(5, 22222, 2),
		(5, 10103, 5),
		(5, 10107, 1),
		(6, 77777, 1),
		(6, 33333, 3),
		(6, 10101, 1.5),
		(6, 55555, 2),
		(7, 66666, 1),
		(7, 10107, 1),
		(7, 10101, 0.5),
		(8, 22222, 1),
		(8, 33333, 2),
		(9, 10104, 3),
		(10, 10103, 2),
		(11, 11111, 1),
		(12, 10105, 2),
		(13, 88888, 1),
		(14, 10108, 1),
		(15, 66666, 5);
	

	#Inserção de dados em FORNECE
	INSERT INTO
		FORNECE
	VALUES (0001, 77777, 4, 300, '13:15', '2019-08-19'),
		(0001, 99999, 1.99, 300, '13:17', '2019-08-19'),
		(0002, 11111, 4.70, 300, '14:17', '2019-08-19'),
		(0002, 88888, 2.10, 300, '14:25', '2019-08-19'),
		(0003, 22222, 1.18, 500, '14:30', '2019-08-19'),
		(0004, 33333, 0.35, 600, '14:22', '2019-08-19'),
		(0005, 44444, 6.13, 300, '11:50', '2019-04-19'),
		(0005, 44444, 5.78, 450, '16:55', '2019-03-15'),
		(0005, 44444, 6.13, 100, '10:13', '2019-05-10'),
		(0005, 44444, 6.10, 400, '15:30', '2019-06-30'),
		(0005, 44444, 5.80, 60, '12:10', '2019-07-16'),
		(0005, 44444, 6.40, 260, '9:55', '2019-08-19')',
		(0006, 55555, 0.99, 1000, '10:30', '2019-06-27'),
		(0007, 66666, 5.70, 500, '13:18', '2018-10-17'),
		(0007, 66666, 6.18, 1000, '9:34', '2018-12-02'),
		(0007, 66666, 6.18, 700, '17:45', '2019-01-16'),
		(0007, 66666, 5.50, 300, '12:17', '2019-03-30'),
		(0007, 66666, 5.50, 100, '12:20', '2019-05-10'),
		(0007, 66666, 5.50, 150, '12:00', '2019-06-30'),
		(0007, 66666, 5.50, 150, '11:48', '2019-08-19'),
		(0008, 10101, 7.56, 400, '13:30', '2019-01-03'),
		(0008, 10101, 7.50, 500, '13:03', '2019-02-16'),
		(0008, 10101, 7.90, 400, '13:00', '2019-04-01'),
		(0008, 10101, 7.80, 250, '13:25', '2019-05-28'),
		(0008, 10101, 7.67, 300, '13:05', '2019-06-15'),
		(0008, 10101, 7.67, 300, '13:47', '2019-07-26'),
		(0009, 10102, 0.35, 700, '9:30', '2019-08-19'),
		(0010, 10103, 0.56, 700, '10:17', '2019-08-19'),
		(0011, 10104, 0.51, 700, '16:40', '2019-08-19'),
		(0012, 10105, 1.98, 500, '14:18', '2019-08-19'),
		(0012, 10106, 1.98, 600, '14:22', '2019-08-19');

	#Inserção de dados em REALIZA
	INSERT INTO
		REALIZA
	VALUES (1, 1),
		(2, 2),
		(3, 3),
		(4, 4),
		(5, 5),
		(6, 6),
		(7, 7),
		(8, 8),
		(9, 9),
		(10, 10),
		(11, 11),
		(12, 12),
		(13, 13),
		(14, 14),
		(15, 15);

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
            /* Lógico_2: */

    CREATE TABLE PRODUTO (
       codigo integer PRIMARY KEY,
       nome varchar(30),
       valor float,
       tipo varchar(30)
    );

    CREATE TABLE CLIENTE (
        codigo integer PRIMARY KEY,
        nome varchar(100),
        sexo char,
        idade integer,
        latitude integer,
        longitude integer
    );

    CREATE TABLE COMPRA (
        numero_nota integer PRIMARY KEY,
        data date,
        hora varchar(8),
    );

    CREATE TABLE FORNECEDOR (
        codigo integer PRIMARY KEY,
        nome varchar(30),
        ramo varchar(30),
        telefone varchar(15),
        email varchar(50)
    );

    CREATE TABLE Possui (
        fk_COMPRA_numero_nota integer,
        fk_PRODUTO_codigo integer,
        qtd integer
    );

    CREATE TABLE Fornece (
        fk_FORNECEDOR_codigo integer,
        fk_PRODUTO_codigo integer,
        preco_aquisicao float,
        qtd_adquiria integer,
        hora_aquisicao varchar(8),
        data_aquisicao date
    );

    CREATE TABLE Realiza (
        fk_CLIENTE_codigo integer,
        fk_COMPRA_numero_nota integer
    );
 
    ALTER TABLE Possui ADD CONSTRAINT FK_Possui_1
        FOREIGN KEY (fk_COMPRA_numero_nota)
        REFERENCES COMPRA (numero_nota)
        ON DELETE RESTRICT;
 
    ALTER TABLE Possui ADD CONSTRAINT FK_Possui_2
        FOREIGN KEY (fk_PRODUTO_codigo)
        REFERENCES PRODUTO (codigo)
        ON DELETE RESTRICT;
 
    ALTER TABLE Fornece ADD CONSTRAINT FK_Fornece_1
        FOREIGN KEY (fk_FORNECEDOR_codigo)
        REFERENCES FORNECEDOR (codigo)
        ON DELETE RESTRICT;
 
    ALTER TABLE Fornece ADD CONSTRAINT FK_Fornece_2
        FOREIGN KEY (fk_PRODUTO_codigo)
        REFERENCES PRODUTO (codigo)
        ON DELETE RESTRICT;
 
    ALTER TABLE Realiza ADD CONSTRAINT FK_Realiza_1
        FOREIGN KEY (fk_CLIENTE_codigo)
        REFERENCES CLIENTE (codigo)
        ON DELETE RESTRICT;
 
    ALTER TABLE Realiza ADD CONSTRAINT FK_Realiza_2
        FOREIGN KEY (fk_COMPRA_numero_nota)
        REFERENCES COMPRA (numero_nota)
        ON DELETE RESTRICT;
        
        #Inserção de dados em FORNECEDOR
	INSERT INTO
		FORNECEDOR
	VALUES (0001, 'Biancogres', 'alimentos', '(11)1111-1111', 'biancogres@destino.com'),
		(0002, 'Sepé', 'alimentos', '(22)2222-2222', 'sepe@destino.com'),
		(0003, 'Camil', 'alimentos', '(33)3333-3333', 'camil@destino.com'),
		(0004, 'Bonduelle', 'alimentos', '(44)4444-4444', 'bonduelle@destino.com'),
		(0005, 'cofril', 'alimentos', '(55)5555-5555', 'cofril@destino.com'),
		(0006, 'Eliana', 'panos', '(66)6666-6666', 'eliana@destino.com'),
		(0007, 'Tilibra', 'papelaria', '(77)7777-7777', 'tilibra@destino.com'),
		(0008, 'PifPaf', 'alimentos', '(88)8888-8888', 'pifpaf@destino.com'),
		(0009, 'Renata', 'alimentos', '(99)9999-9999', 'renata@destino.com'),
		(0010, 'Bauducco', 'alimentos', '(10)1010-1010', 'bauducco@destino.com'),
		(0011, 'Trakinas', 'alimentos', '(11)0111-0111', 'trakinas@destino.com'),
		(0012, 'Garoto', 'alimentos', '(12)1212-1212', 'garoto@destino.com');
		(0013, 'Hershers', 'alimentos', '(13)1313-1313', 'hershers@destino.com'),
		(0014, 'Veja', 'produtos quimicos', '(14)1414-1414', 'veja@destino.com'),
		(0015, 'Qboa', 'produtos quimicos', '(15)1515-1515', 'qboa@destino.com');



	#Inserção de dados em PRODUTO
	INSERT INTO 
		PRODUTO
	VALUES (11111, 'arroz sepé', 10.98, 'arroz 5kg'), 
		(22222, 'feijão  camil', 3.78, 'feijão'),
		(33333, 'milho bonduelle', 1.15, 'milho verde'),
		(44444, 'linguica cofril', 13.89, 'linguica defumada'),
		(55555, 'pano de prato eliana', 4, 'pano de prato'),
		(66666, 'caderno superpoderosas tilibra', 18.50, 'caderno 1 materia'),
		(77777, 'arroz biancogres', 9.70, 'arroz 5kg'),
		(88888, 'arroz sepé', 7.90, 'arroz 1kg'),
		(99999, 'arroz biancogres', 6.00, 'arroz 1kg'),
		(10101, 'linguica pifpaf', 10.60, 'linguica defumada'),
		(10102, 'biscoito renata', 1.00, 'biscoito recheado'),
		(10103, 'bicoito recheado bauducco', 1.89, 'biscoito recheado'),
		(10104, 'biscoito recheado trakinas', 1.78, 'biscoito recheado'),
		(10105, 'barra ao leite garoto', 5.99, 'barra chocolate'),
		(10106, 'barra meio amargo garoto', 5.99, 'barra chocolate'),
		(10107, 'desengordurante veja', 3.98, 'produtos quimicos'),
		(10108, 'agua sanitaria qboa', 3.99, 'produtos quimicos');


	#Inserção de dados em COMPRA
	INSERT INTO
		COMPRA
	VALUES (1, '2019-08-19', '8:03'),
		(2, '2019-08-19', '8:17'),
		(3, '2019-08-19', '8:25'),
		(4, '2019-08-19', '8:28'),
		(5, '2019-08-19', '8;37'),
		(6, '2019-08-19', '8:40'),
		(7, '2019-08-19', '8:46'),
		(8, '2019-08-19', '8:51'),
		(9, '2019-08-19', '8:58'),
		(10, '2019-08-19', '9:02'),
		(11, '2019-08-19', '9:11'),
		(12, '2019-08-19', '9:15'),
		(13, '2019-08-19', '9:18'),
		(14, '2019-08-19', '9:24'),
		(15, '2019-08-19', '9:35');

	#Inserção de dados em CLIENTE
	INSERT INTO
		CLIENTE
	VALUES (1, 'Joana', 'F', 18, 1111111111, 1111111111),
		(2, 'Jonas', 'M', 22, 2222222222, 2222222222),
		(3, 'Lucas', 'M', 25, 3333333333, 3333333333),
		(4, 'Lúcia', 'F', 19, 444444444, 444444444),
		(5, 'Maria Eduarda', 'F', 19, 555555555, 555555555),
		(6, 'Eloina', 'F', 47, 66666666, 666666666),
		(7, 'Caio', 'M', 26, 777777777, 777777777),
		(8, 'Mateus', 'M', 18, 888888888, 888888888),
		(9, 'Weverton', 'M', 20, 999999999, 999999999),
		(10, 'Marcos', 'M', 49, 10000000, 10000000),
		(11, 'José', 'M', 28, 11000000, 11000000),
		(12, 'Bianca', 'F', 23, 12000000, 12000000),
		(13, 'Brenda', 'F', 22, 13000000, 13000000),
		(14, 'Bruna', 'F', 26, 1400000, 14000000),
		(15, 'Rodolfo', 'M', 25, 15000000, 15000000);


	#Inserção de dados em POSSUI
	INSERT INTO
		POSSUI
	VALUES (1, 11111, 2),
		(1, 22222, 5),
		(1, 44444, 2),
		(2, 10102, 10),
		(2, 10106, 2),
		(3, 10107, 2),
		(3, 10108, 1),
		(3, 99999, 1),
		(4, 10105, 3),
		(4, 10106, 3),
		(5, 88888, 2),
		(5, 22222, 2),
		(5, 10103, 5),
		(5, 10107, 1),
		(6, 77777, 1),
		(6, 33333, 3),
		(6, 10101, 1.5),
		(6, 55555, 2),
		(7, 66666, 1),
		(7, 10107, 1),
		(7, 10101, 0.5),
		(8, 22222, 1),
		(8, 33333, 2),
		(9, 10104, 3),
		(10, 10103, 2),
		(11, 11111, 1),
		(12, 10105, 2),
		(13, 88888, 1),
		(14, 10108, 1),
		(15, 66666, 5);
	

	#Inserção de dados em FORNECE
	INSERT INTO
		FORNECE
	VALUES (0001, 77777, 4, 300, '13:15', '2019-08-19'),
		(0001, 99999, 1.99, 300, '13:17', '2019-08-19'),
		(0002, 11111, 4.70, 300, '14:17', '2019-08-19'),
		(0002, 88888, 2.10, 300, '14:25', '2019-08-19'),
		(0003, 22222, 1.18, 500, '14:30', '2019-08-19'),
		(0004, 33333, 0.35, 600, '14:22', '2019-08-19'),
		(0005, 44444, 6.13, 300, '11:50', '2019-04-19'),
		(0005, 44444, 5.78, 450, '16:55', '2019-03-15'),
		(0005, 44444, 6.13, 100, '10:13', '2019-05-10'),
		(0005, 44444, 6.10, 400, '15:30', '2019-06-30'),
		(0005, 44444, 5.80, 60, '12:10', '2019-07-16'),
		(0005, 44444, 6.40, 260, '9:55', '2019-08-19')',
		(0006, 55555, 0.99, 1000, '10:30', '2019-06-27'),
		(0007, 66666, 5.70, 500, '13:18', '2018-10-17'),
		(0007, 66666, 6.18, 1000, '9:34', '2018-12-02'),
		(0007, 66666, 6.18, 700, '17:45', '2019-01-16'),
		(0007, 66666, 5.50, 300, '12:17', '2019-03-30'),
		(0007, 66666, 5.50, 100, '12:20', '2019-05-10'),
		(0007, 66666, 5.50, 150, '12:00', '2019-06-30'),
		(0007, 66666, 5.50, 150, '11:48', '2019-08-19'),
		(0008, 10101, 7.56, 400, '13:30', '2019-01-03'),
		(0008, 10101, 7.50, 500, '13:03', '2019-02-16'),
		(0008, 10101, 7.90, 400, '13:00', '2019-04-01'),
		(0008, 10101, 7.80, 250, '13:25', '2019-05-28'),
		(0008, 10101, 7.67, 300, '13:05', '2019-06-15'),
		(0008, 10101, 7.67, 300, '13:47', '2019-07-26'),
		(0009, 10102, 0.35, 700, '9:30', '2019-08-19'),
		(0010, 10103, 0.56, 700, '10:17', '2019-08-19'),
		(0011, 10104, 0.51, 700, '16:40', '2019-08-19'),
		(0012, 10105, 1.98, 500, '14:18', '2019-08-19'),
		(0012, 10106, 1.98, 600, '14:22', '2019-08-19');

	#Inserção de dados em REALIZA
	INSERT INTO
		REALIZA
	VALUES (1, 1),
		(2, 2),
		(3, 3),
		(4, 4),
		(5, 5),
		(6, 6),
		(7, 7),
		(8, 8),
		(9, 9),
		(10, 10),
		(11, 11),
		(12, 12),
		(13, 13),
		(14, 14),
		(15, 15);
  
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (Drop table + Create de tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL

## Marco de Entrega 08 em: (29/05/2019)<br>

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>

#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

> Consulta da tabela "Cliente"

![Print da seleção de dados da tabela "cliente"](https://github.com/auerbeatriz/modtrab/blob/master/imagens/consulta_cliente.png?raw=true "Modelo Lógico - Empresa SmartSales")

> Consulta da tabela "Compra"

![Print da seleção de dados da tabela "compra"](https://github.com/auerbeatriz/modtrab/blob/master/imagens/consulta_compra.png?raw=true "Modelo Lógico - Empresa SmartSales")

> Consulta da tabela "Fornece"

![Print da seleção de dados da tabela "fornece"](https://github.com/auerbeatriz/modtrab/blob/master/imagens/consulta_fornece.png?raw=true "Modelo Lógico - Empresa SmartSales")

> Consulta da tabela "Fornecedor"

![Print da seleção de dados da tabela "fornecedor"](https://github.com/auerbeatriz/modtrab/blob/master/imagens/consulta_fornecedor.png?raw=true "Modelo Lógico - Empresa SmartSales")

> Consulta da tabela "Possui"

![Print da seleção de dados da tabela "possui"](https://github.com/auerbeatriz/modtrab/blob/master/imagens/consulta_possui.png?raw=true "Modelo Lógico - Empresa SmartSales")

> Consulta da tabela "Produto"

![Print da seleção de dados da tabela "produto"](https://github.com/auerbeatriz/modtrab/blob/master/imagens/consulta_produto.png?raw=true "Modelo Lógico - Empresa SmartSales")

> Consulta da tabela "Realiza"

![Print da seleção de dados da tabela "realiza"](https://github.com/auerbeatriz/modtrab/blob/master/imagens/consulta_realiza.png?raw=true "Modelo Lógico - Empresa SmartSales")

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.


    
#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>


#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 3 registros no resultado
        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
        

### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>


#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
#### 9.10	SUBCONSULTAS (Mínimo 3)<br>

#### 9.11	LISTA DE CODIGOS DAS FUNÇÕES E TRIGGERS<br>
        Detalhamento sobre funcionalidade de cada código.
        a) Objetivo
        b) Código do objeto (função/trigger)
        c) exemplo de dados para aplicação
        d) resultados em forma de tabela/imagem
<br>


#### 9.12	GERACAO DE DADOS (MÍNIMO DE 100 MIL REGISTROS PARA PRINCIPAL RELAÇAO)<br>
        a) principal tabela do sistema deve ter no mínimo 100 mil registros
        b) tabelas diretamente relacionadas a tabela principal 10 mil registros
        c) tabelas auxiliares de relacao multivalorada mínimo de 10 registros
        d) registrar o tempo de inserção em cada uma das tabelas do banco de dados
        e) especificar a quantidade de registros inseridos em cada tabela
        Para melhor compreensão verifiquem o exemplo na base de testes:<br>
        https://github.com/discipbd2/base-de-testes-locadora
        

#### 9.13	Backup do Banco de Dados<br>
        Detalhamento do backup.
        a) Tempo
        b) Tamanho
        c) Teste de restauração (backup)
        d) Tempo para restauração
        e) Teste de restauração (script sql)
        f) Tempo para restauração (script sql)
<br>

Data de Entrega: (Data a ser definida)
<br>

#### 9.14	APLICAÇAO DE ÍNDICES E TESTES DE PERFORMANCE<br>
    a) Lista de índices, tipos de índices com explicação de porque foram implementados nas consultas 
    b) Performance esperada VS Resultados obtidos
    c) Tabela de resultados comparando velocidades antes e depois da aplicação dos índices (constando velocidade esperada com planejamento, sem indice e com índice Vs velocidade de execucao real com índice e sem índice).
    d) Escolher as consultas mais complexas para serem analisadas (consultas com menos de 2 joins não serão aceitas)
    e) As imagens do Explain devem ser inclusas no trabalho, bem como explicações sobre os resultados obtidos.
    f) Inclusão de tabela mostrando as 10 execuções, excluindo-se o maior e menor tempos para cada consulta e 
    obtendo-se a media dos outros valores como resultado médio final.
<br>
    Data de Entrega: (Data a ser definida)
<br>   

### 10	ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO FINAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (Data a ser definida)
<br>

### 11 Backup completo do banco de dados postgres 
    a) deve ser realizado no formato "backup" 
        (Em Dump Options #1 Habilitar opções Don't Save Owner e Privilege)
    b) antes de postar o arquivo no git o mesmo deve ser testado/restaurado por outro grupo de alunos/dupla
    c) informar aqui o grupo de alunos/dupla que realizou o teste.

    
### 12	TUTORIAL COMPLETO DE PASSOS PARA RESTAURACAO DO BANCO E EXECUCAO DE PROCEDIMENTOS ENVOLVIDOS NO TRABALHO PARA OBTENÇÃO DOS RESULTADOS<br>
        a) Outros grupos deverão ser capazes de restaurar o banco 
        b) executar todas as consultas presentes no trabalho
        c) executar códigos que tenham sido construídos para o trabalho 
        d) realizar qualquer procedimento executado pelo grupo que desenvolveu o trabalho

### 13	DIFICULDADES ENCONTRADAS PELO GRUPO<br>  

    
Data de Entrega final: (Data a ser definida)
<br>

       
### 14  FORMATACAO NO GIT: https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
   
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/

#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. Caso existam arquivos com conteúdos sigilosos, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário deste GIT, para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


        
        


    






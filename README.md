# TRABALHO 01:  SmartSales
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado.

# Sumário

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
![Arquivo PDF do Protótipo Balsamiq feito para Empresa SmartSales](https://github.com/auerbeatriz/modtrab/blob/master/arquivos/novo%20smartsales%20-%20mini%20mundo.pdf)

### 4.1 RELATÓRIOS

> O sistema proposto consegue responder às seguintes questões:
* Qual o fornecedor de produtos mais frequente;
* Qual o produto mais vendido;
* Quanto foi a despesa e o lucro com os produtos;
* Qual a média de idade dos clientes;
* Qual é a marca de produtos mais vendida;
 
### 4.2 TABELA DE DADOS DO SISTEMA:

> A tabela aqui anexada contém os atributos do sistema SmartSales. Ela simula um relatório com todos os dados que serão armazenados.

![Exemplo de Tabela de dados da Empresa SmartSales](https://github.com/auerbeatriz/modtrab/blob/master/arquivos/nova%20PlanilhaSmartsSales%20%20em%20ods.ods?raw=true "Tabela - Empresa SmartSales")

    FORNECEDOR: tabela que armazena os dados de todos os produtos da empresa/estabelecimento.
    PRODUTO: tabela que armazena os dados de todos os produtos comercializados pela empresa/estabelecimento.
    COMPRA: tabela que armazena a venda de produtos do estabelecimento para um cliente.
    CLIENTE: tabela que armazena os dados dos clientes cadastrados no estabelecimento/empresa.
    CONTATO_FORNECEDOR: tabela que armazena os contatos dos fornecedores de produtos.
    CONTATO_CLIENTE: tabela que armazena os contatos dos clientes da empresa/estabelecimento.
    TIPO_CONTATO: tabela que armazena a categoria dos contatos, como telefone, e-mail, site, entre outros.
    RAMO: tabela que armazena os ramos dos fornecedores, como alimentos, vestuário, entre outros.
    CATEGORIA: tabela que armazena as categorias dos produtos, como alimentos, limpeza, entre outros.
    MARCA: tabela que armazena as marcas dos produtos.
    UNIDADE: tabela que armazena as unidades em que os produtos são vendidos, como quilograma, unidade, entre outros.
    AQUISICAO_PRODUTO: tabela que armazena os dados da aquisição de um produto pela empresa/estabelecimento de um fornecedor.
    COMPRA_PRODUTO: tabela que armazena a quantidade em que cada produto foi vendido em uma compra.
    
### 5.MODELO CONCEITUAL<br>

> O modelo conceitual apresenta as entidades existentes no programa e os relacionamentos que elas possuem entre si. Este é o meu modelo conceitual:
        
![Modelo Conceitual](https://github.com/auerbeatriz/modtrab/blob/master/imagens/modelo_conceitual_smart_sales.png?raw=true "Modelo Conceitual SmartSales")

### 5.1 DESCRIÇÃO DOS DADOS

    Tabela RAMO
    	CODIGO: campo que possui o código identificador do ramo.
    	RAMO: campo que possui a descrição do ramo do fornecedor.
	
    Tabela CATEGORIA
    	CODIGO: campo que possui o código identificador da categoria.
    	CATEGORIA: campo que possui a descrição da categoria do produto.
	
    Tabela MARCA
    	CODIGO: campo que possui o código identificador da marca.
    	CATEGORIA: campo que possui a descrição da marca do produto.
    
    Tabela UNIDADE
    	CODIGO: campo que possui o código identificador da unidade.
    	CATEGORIA: campo que possui a descrição da unidade do produto.
    
    Tabela CLIENTE
    	CODIGO: campo que armazena o código do cliente, sendo ele o número de um documento padrão.
    	NOME: campo que armazena o nome do cliente.
    	SEXO: campo que armazena o sexo do cliente.
    	DATA_NASC: campo que armazena a data de nascimento do cliente.
    	DATA_CADASTRO: campo que armazena a data em que o cliente foi cadastrado.
    	LATITUDE: campo que armazena a latitude da residência do cliente.
    	LONGITUDE: campo que armazena a longitude da residência de um cliente.

    Tabela COMPRA
    	NUMERO_NOTA: camo que armazena o número identificador da nota fiscal.
    	HORA: campo que armazena a hora em que a nota foi emitida.
    	DATA: campo que armazena a data em que a nota foi emitida.
    
    Tabela COMPRA_PRODUTO:
   	QTD: campo que armazena a quantidade de produtos que foram vendidos naquela nota.

    Tabela PRODUTO
	CODIGO: campo que armazena o código do produto.
    	CODIGO_BARRAS: campo que armazena o código de barras do produto.
    	DESCRIÇÃO: campo que armazena a descrição do produto (usada para identificação informal).
    	PRECO_VENDA: campo que armazena o preço de venda do produto.

    Tabela FORNECEDOR
    	CODIGO: campo que armazena o código, sendo o número de um documento padrão, da empresa.
    	NOME_FANTASIA: campo que armazena o nome fantasia da empresa.
    	RAZAO_SOCIAL: campo que armazena o nome jurídico da empresa, sua razão social.
    	DATA_CADASTRO: campo que armazena a data da primeira compra com o fornecedor.
    	LATITUDE: campo que armazena a latitude da loja física do fornecedor
    	LONGITUDE: campo que armazena a longitude da loja física do fornecedor.

    Tabela CONTATO_FORNECEDOR
    	CODIGO: campo que armazena o código do contato.
    	CONTATO: campo que armazena o contato do fornecedor.

    Tabela CONTATO_CLIENTE
    	CODIGO: campo que armazena o código do contato.
    	CONTATO: campo que armaena o contato do cliente.
	
    Tabela TIPO_CONTATO
	CODIGO: campo que armazena o código do tipo de contato.
    	DESCRICAO: campo que armazena o o tipo de contato (exemplo: telefone, email).

### 6	MODELO LÓGICO<br>

> Aqui consta o modelo lógico do meu banco de dados.

![Modelo Lógico SmartSales](https://github.com/auerbeatriz/modtrab/blob/master/imagens/modelo_logico_smart_sales.png?raw=true "Modelo Lógico - Empresa SmartSales")

### 7	MODELO FÍSICO ATUALIZADO<br>
    /* MODELO_LOGICO_SMART_SALES: */

	CREATE TABLE RAMO (
    	codigo integer PRIMARY KEY,
   	ramo varchar
	);

	CREATE TABLE CATEGORIA (
	    codigo integer PRIMARY KEY,
	    categoria varchar
	);
	
	CREATE TABLE MARCA (
	    codigo integer PRIMARY KEY,
	    marca varchar
	);
	
	CREATE TABLE UNIDADE (
	    codigo integer PRIMARY KEY,
	    unidade varchar
	);
		
	CREATE TABLE FORNECEDOR (
	    codigo varchar PRIMARY KEY,
	    nome_fantasia varchar,
	    razao_social varchar,
	    data_cadastro date,
	    latitude varchar,
	    longitude varchar,
	    ramo integer
	);

	CREATE TABLE PRODUTO (
	    codigo integer PRIMARY KEY,
	    codigo_barras varchar,
	    descricao varchar,
	    preco_venda float,
	    categoria integer,
	    unidade integer,
	    marca integer
	);

	CREATE TABLE VENDA (
	    numero_nota integer PRIMARY KEY,
	    data date,
	    hora varchar,
	    cliente varchar
	);

	CREATE TABLE CLIENTE (
	    codigo varchar PRIMARY KEY,
	    nome varchar,
	    data_nasc date,
	    data_cadastro date,
	    latitude varchar,
	    longitude varchar,
	    sexo char
	);

	CREATE TABLE CONTATO_FORNECEDOR (
	    codigo integer PRIMARY KEY,
	    contato varchar,
	    fornecedor varchar,
	    tipo_contato integer
	);

	CREATE TABLE TIPO_CONTATO (
	    codigo integer PRIMARY KEY,
	    descricao varchar
	);

	CREATE TABLE CONTATO_CLIENTE (
	    codigo integer PRIMARY KEY,
	    contato varchar,
	    cliente varchar,
	    tipo_contato integer
	);

	CREATE TABLE AQUISICAO_PRODUTO (
	    fornecedor varchar,
	    produto integer,
	    data_aquisicao date,
	    hora_aquisicao varchar,
	    qtd_aquisicao integer,
	    preco_aquisicao float
	);

	CREATE TABLE VENDA_PRODUTO (
	    numero_nota integer,
	    produto integer,
	    qtd float
	);
 
	ALTER TABLE FORNECEDOR ADD CONSTRAINT FK_FORNECEDOR_2
	    FOREIGN KEY (ramo)
	    REFERENCES RAMO (codigo)
	    ON DELETE RESTRICT;
 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_2
	    FOREIGN KEY (categoria)
	    REFERENCES CATEGORIA (codigo)
	    ON DELETE RESTRICT;
 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_3
	    FOREIGN KEY (unidade)
	    REFERENCES UNIDADE (codigo)
	    ON DELETE RESTRICT;
	 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_4
	    FOREIGN KEY (marca)
	    REFERENCES MARCA (codigo)
	    ON DELETE RESTRICT;
 
	ALTER TABLE VENDA ADD CONSTRAINT FK_VENDA_2
	    FOREIGN KEY (cliente)
	    REFERENCES CLIENTE (codigo)
	    ON DELETE RESTRICT;
 
	ALTER TABLE CONTATO_FORNECEDOR ADD CONSTRAINT FK_CONTATO_FORNECEDOR_2
	    FOREIGN KEY (fornecedor)
	    REFERENCES FORNECEDOR (codigo)
	    ON DELETE CASCADE;
 
	ALTER TABLE CONTATO_FORNECEDOR ADD CONSTRAINT FK_CONTATO_FORNECEDOR_3
	    FOREIGN KEY (tipo_contato)
	    REFERENCES TIPO_CONTATO (codigo)
	    ON DELETE RESTRICT;
 	
	ALTER TABLE CONTATO_CLIENTE ADD CONSTRAINT FK_CONTATO_CLIENTE_2
	    FOREIGN KEY (cliente)
	    REFERENCES CLIENTE (codigo)
	    ON DELETE CASCADE;
 
	ALTER TABLE CONTATO_CLIENTE ADD CONSTRAINT FK_CONTATO_CLIENTE_3
	    FOREIGN KEY (tipo_contato)
	    REFERENCES TIPO_CONTATO (codigo)
	    ON DELETE RESTRICT;
	 
	ALTER TABLE AQUISICAO_PRODUTO ADD CONSTRAINT FK_AQUISICAO_PRODUTO_1
	    FOREIGN KEY (fornecedor)
	    REFERENCES FORNECEDOR (codigo)
	    ON DELETE RESTRICT;
 
	ALTER TABLE AQUISICAO_PRODUTO ADD CONSTRAINT FK_AQUISICAO_PRODUTO_2
	    FOREIGN KEY (produto)
	    REFERENCES PRODUTO (codigo)
	    ON DELETE RESTRICT;
 
	ALTER TABLE VENDA_PRODUTO ADD CONSTRAINT FK_VENDA_PRODUTO_1
	    FOREIGN KEY (numero_nota)
	    REFERENCES VENDA (numero_nota)
	    ON DELETE RESTRICT;
	 
	ALTER TABLE VENDA_PRODUTO ADD CONSTRAINT FK_VENDA_PRODUTO_2
	    FOREIGN KEY (produto)
	    REFERENCES PRODUTO (codigo)
	    ON DELETE RESTRICT;

### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS ATUALIZADO<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
       	INSERT INTO RAMO VALUES 
	(1, 'alimentos organicos');

	INSERT INTO CATEGORIA VALUES 
	(1, 'fruta'),
	(2, 'verdura'),
	(3, 'hortalica'),
	(4, 'linguica'),
	(5, 'queijo');

	INSERT INTO UNIDADE VALUES
	(1, 'kg');

	INSERT INTO MARCA VALUES
	(1, 'hortifruti'),
	(2, 'seasa');

	INSERT INTO TIPO_CONTATO VALUES
	(1, 'Telefone'),
	(2, 'E-Mail'),
	(3, 'Facebook'),
	(4, 'Twitter'),
	(5, 'Instagram'),
	(6, 'Site');

	INSERT INTO CLIENTE VALUES
	('365.728.948-86', 'Camila Pinto Alves', '1992-2-23', '2017-7-20', '-3.2125445', '-6.832034', 'F'),
	('192.154.940-81', 'Gabriela Castro da Costa', '2004-5-4', '2018-3-2', '37.0049765', '-167.999536', 'F'),
	('051.049.739-05', 'Juliana Azevedo Castro', '2002-2-9', '2018-5-8', '-13.2917825', '44.258601', 'F'),
	('562.175.036-54', 'Isabella Campos Pires', '1982-12-7', '2018-12-12', '19.2732755', '-48.844405', 'F'),
	('196.083.621-80', 'Mariane Caldeira Nogueira', '2000-11-5', '2018-3-10', '21.152234', '20.190571', 'F'),
	('293.690.116-25', 'Alana da Conceição Viana', '1947-8-1', '2016-11-20', '63.8673555', '-31.990231', 'F'),
	('909.320.903-54', 'Ana Lívia Almeida da Costa', '1962-6-16', '2017-4-15', '-2.1824555', '18.227164', 'F'),
	('442.847.425-31', 'Ana Laura da Mata Moura', '1963-11-3', '2017-12-27', '57.2975025', '-131.715842', 'F'),
	('661.660.624-43', 'Manuela Correia Ribeiro', '1956-10-10', '2018-9-28', '26.914186', '-56.445934', 'F'),
	('218.003.800-38', 'Caroline Castro da Luz', '1929-2-11', '2018-12-5', '-42.696304', '117.056578', 'F'),
	('161.591.311-41', 'Olivia da Rocha Farias', '1989-5-10', '2018-3-17', '-2.0723475', '-134.025987', 'F'),
	('592.189.369-21', 'Gabrielly Barbosa Correia', '1978-2-1', '2017-4-15', '-79.302171', '-18.346412', 'F'),
	('807.147.057-05', 'Catarina Fogaça Moreira', '1931-12-1', '2017-5-19', '-23.1273225', '148.340027', 'F'),
	('101.923.093-23', 'Isis Peixoto Araújo', '1963-12-26', '2018-6-1', '73.7187695', '66.205137', 'F'),
	('986.418.387-75', 'Maria Cecília Castro Silva', '1968-4-22', '2016-11-7', '66.8340885', '-156.163327', 'F'),
	('954.897.650-11', 'Olivia da Cunha Mendes', '1949-7-22', '2019-7-27', '-61.9986875', '-44.206946', 'F'),
	('533.897.771-05', 'Cecília Barros da Conceição', '1999-7-5', '2019-9-13', '59.532996', '147.128030', 'F'),
	('242.027.503-90', 'Nina Castro Dias', '1940-8-2', '2017-1-6', '22.5758335', '59.389895', 'F'),
	('761.312.625-00', 'Marina Rezende Almeida', '1966-10-9', '2019-8-9', '-87.845712', '54.952627', 'F'),
	('318.624.060-30', 'Mariane da Cunha Duarte', '1968-5-9', '2017-1-14', '-66.4832815', '-52.328383', 'F'),
	('430.206.866-36', 'Enzo Correia Carvalho', '1976-2-12', '2018-5-23', '-46.2587105', '49.054216', 'M'),
	('428.464.848-99', 'Enzo Lima Lima', '1939-6-18', '2018-1-17', '57.1306305', '166.209945', 'M'),
	('959.031.846-00', 'Cauê Melo Moreira', '2006-6-9', '2017-5-18', '-54.781919', '26.387546', 'M'),
	('289.081.666-45', 'João Gabriel Silveira Peixoto', '1992-7-23', '2017-9-27', '-83.9795035', '154.865067', 'M'),
	('630.703.207-32', 'Vicente Castro Azevedo', '1977-7-23', '2017-11-19', '23.573548', '-79.343364', 'M'),
	('710.164.760-00', 'Vitor Gabriel Freitas Moraes', '1992-6-8', '2018-9-27', '-39.8420775', '69.385340', 'M'),
	('552.934.949-88', 'Davi Luiz Santos Silveira', '1968-2-17', '2019-6-8', '1.982571', '176.879138', 'M'),
	('944.344.086-58', 'João Pedro Cavalcanti Silva', '1964-3-3', '2018-4-27', '50.7625935', '146.450740', 'M'),
	('020.879.003-96', 'Pedro Henrique Freitas Costela', '1980-5-21', '2018-8-18', '-79.0520905', '-172.036972', 'M'),
	('970.122.418-37', 'Daniel Freitas Araújo', '1957-7-29', '2018-11-2', '-35.3585215', '-177.939287', 'M'),
	('636.541.312-20', 'Anthony da Luz Vieira', '1955-1-23', '2017-12-2', '-85.283735', '-27.917500', 'M'),
	('602.150.938-28', 'Enzo da Cunha Cardoso', '1980-1-17', '2019-8-18', '-7.890234', '-69.768677', 'M'),
	('226.968.600-41', 'Renan Sales Lima', '1979-7-28', '2018-2-22', '-2.6822365', '149.443722', 'M'),
	('517.146.035-39', 'Nathan Viana Aragão', '1955-5-28', '2018-3-15', '86.3842065', '14.052799', 'M'),
	('897.094.953-48', 'Rodrigo Alves Gonçalves', '1981-12-27', '2018-9-4', '87.700105', '22.281184', 'M'),
	('193.648.568-05', 'Luiz Gustavo Nogueira Souza', '1929-3-23', '2019-1-3', '30.4297755', '-101.631940', 'M'),
	('208.664.918-56', 'Maria Cecília Aragão Castro', '2006-8-7', '2018-2-24', '-47.264432', '116.194005', 'F'),
	('630.507.657-04', 'Júlia Carvalho Costela', '1993-6-12', '2017-3-9', '28.686795', '4.175100', 'F'),
	('521.588.578-89', 'Isabelly Ribeiro Ferreira', '1976-4-2', '2019-9-9', '44.0687225', '-63.479234', 'F'),
	('454.849.805-26', 'Emanuelly Costa da Mota', '1997-10-2', '2017-6-8', '77.418242', '-74.991038', 'F'),
	('126.465.446-42', 'Lavínia Pinto Lopes', '1959-1-31', '2018-8-4', '-43.6772375', '3.346787', 'F'),
	('788.378.234-79', 'Valentina Nunes Nunes', '1933-7-1', '2017-3-20', '-16.126069', '-40.616331', 'F'),
	('020.478.274-00', 'Maria Vitória Lima Silva', '1995-2-25', '2018-2-9', '17.417615', '169.132909', 'F'),
	('938.320.985-26', 'Sofia Cunha Souza', '1986-12-20', '2019-3-5', '11.461169', '69.614268', 'F'),
	('266.600.930-01', 'Esther Silveira Freitas', '1950-10-5', '2018-3-20', '-70.3651705', '94.798713', 'F'),
	('761.322.769-39', 'Alana Oliveira Souza', '1961-11-3', '2018-3-1', '71.8508345', '45.850076', 'F'),
	('374.914.799-01', 'Clarice Mendes Duarte', '1955-8-13', '2017-11-11', '-58.510483', '-47.336912', 'F'),
	('176.489.865-66', 'Larissa Ramos Silva', '1982-8-31', '2017-10-17', '-70.401062', '158.061593', 'F'),
	('477.023.447-33', 'Sophia Souza Sales', '1994-10-11', '2018-1-6', '-83.3999315', '-84.402458', 'F'),
	('261.156.571-64', 'Bernardo Silva Rezende', '2003-10-20', '2017-3-31', '-10.7721285', '-4.716711', 'M'),
	('174.767.513-02', 'João Vitor Cunha da Cunha', '1958-10-25', '2019-5-28', '70.3046905', '-115.237992', 'M'),
	('127.754.185-03', 'Daniel Oliveira Moura', '1980-1-9', '2017-2-23', '-40.335424', '-142.178283', 'M'),
	('095.725.968-96', 'Isabelly Ferreira Ramos', '1955-2-1', '2019-6-14', '45.946030', '78.717733', 'F'),
	('227.345.725-16', 'Maria Cecília Fernandes Martins', '1945-12-29', '2019-9-30', '9.721010', '-158.614337', 'F'),
	('287.649.002-15', 'Manuela Pinto Vieira', '1995-9-13', '2018-12-29', '-26.357600', '60.414009', 'F'),
	('742.933.399-06', 'Ana Luiza Cunha Moraes', '1936-6-17', '2017-12-15', '27.6457345', '58.777843', 'F'),
	('586.822.245-85', 'Catarina Dias da Costa', '1952-8-19', '2017-1-28', '6.443707', '18.642783', 'F'),
	('809.181.088-10', 'Nina Souza Barros', '2001-2-27', '2018-6-20', '3.394399', '-131.593893', 'F'),
	('485.407.175-30', 'Larissa Teixeira Campos', '1995-4-9', '2018-3-18', '44.9720015', '94.873868', 'F'),
	('035.703.579-88', 'Sophia da Mata Oliveira', '1985-10-16', '2017-4-23', '-44.1153335', '28.486222', 'F'),
	('032.505.905-50', 'Emanuel Mendes Cardoso', '1951-11-23', '2018-8-2', '-33.4520555', '151.237981', 'M'),
	('128.318.589-09', 'André Barros Lopes', '1956-5-11', '2019-9-8', '-20.1194715', '-171.854721', 'M'),
	('219.549.192-20', 'Bruno das Neves Porto', '1982-8-20', '2017-5-2', '-35.795486', '33.268421', 'M'),
	('476.119.804-40', 'Camila Moura Almeida', '1999-11-16', '2018-2-7', '-60.401269', '113.404030', 'F'),
	('480.796.652-90', 'Olivia Martins das Neves', '1995-8-18', '2018-5-18', '-60.464169', '122.351432', 'F'),
	('192.283.160-39', 'Yasmin da Mata Vieira', '1956-4-30', '2018-3-20', '-52.774795', '-104.803532', 'F'),
	('402.246.463-11', 'Bruna Araújo Aragão', '1972-3-22', '2019-6-21', '-79.2028665', '8.408097', 'F'),
	('901.363.990-96', 'Nicole Nascimento Rezende', '1945-12-26', '2019-6-5', '54.4719435', '-160.119142', 'F'),
	('298.322.674-39', 'Ana Júlia da Cunha Cardoso', '1947-1-6', '2019-2-15', '43.2412495', '127.856870', 'F'),
	('147.988.057-42', 'Lara Santos Dias', '1964-8-18', '2018-6-30', '-87.666231', '-22.935573', 'F'),
	('191.144.047-02', 'Sofia Melo Carvalho', '1943-2-13', '2018-8-14', '-21.6183075', '-57.774954', 'F'),
	('338.640.851-60', 'Alana da Mota Castro', '1983-5-10', '2018-1-7', '33.3067665', '23.335813', 'F'),
	('774.236.197-36', 'Maria Julia da Costa Barros', '2005-6-17', '2018-1-7', '15.422150', '-130.713410', 'F'),
	('581.002.072-08', 'Carolina Lopes Pereira', '1995-10-3', '2018-1-25', '63.759358', '-176.727886', 'F'),
	('493.684.111-07', 'Catarina Araújo Pires', '1935-12-25', '2017-7-12', '71.4494835', '-79.609639', 'F'),
	('455.254.563-97', 'Renan Melo Duarte', '1957-2-19', '2019-2-10', '-48.442406', '-102.137918', 'M'),
	('274.442.369-68', 'João Gabriel Cardoso da Costa', '1933-9-24', '2017-12-19', '85.1178925', '-60.745044', 'M'),
	('559.453.538-17', 'Paulo Porto Sales', '1958-5-25', '2018-4-25', '34.3164595', '133.816711', 'M'),
	('707.929.509-25', 'Cauê da Mota Lima', '1975-8-14', '2018-5-9', '-13.9454365', '63.031472', 'M'),
	('682.112.737-99', 'João Felipe Vieira Gomes', '1955-1-22', '2018-12-6', '62.0004735', '6.033362', 'M'),
	('493.595.641-09', 'Kaique Souza Souza', '1949-12-13', '2019-8-6', '23.882562', '44.736021', 'M'),
	('487.832.626-36', 'Pietro Costela Nogueira', '1931-11-8', '2017-12-30', '-46.732508', '76.756211', 'M'),
	('043.307.895-23', 'Felipe Rocha da Luz', '1999-5-17', '2018-2-4', '36.428485', '42.461127', 'M'),
	('680.184.160-28', 'Pedro Pinto Vieira', '1963-5-12', '2018-9-29', '89.5599865', '146.213438', 'M'),
	('136.818.661-04', 'Nicole Pires Oliveira', '1960-5-25', '2016-11-11', '-24.498195', '155.039130', 'F'),
	('543.031.325-43', 'Clarice da Paz Pinto', '1999-12-16', '2018-10-9', '70.9449105', '160.649931', 'F'),
	('905.180.103-33', 'Sabrina Martins Silveira', '1963-12-22', '2017-10-8', '-24.4614885', '169.668815', 'F'),
	('445.247.565-58', 'Joana Santos Duarte', '1991-12-10', '2019-2-21', '-51.812271', '136.167408', 'F'),
	('887.450.522-12', 'Maitê Rocha Ferreira', '1936-1-17', '2017-3-28', '0.8280035', '151.699945', 'F'),
	('874.524.521-51', 'Leonardo Costela Souza', '1940-9-4', '2017-12-26', '-9.063991', '-89.100074', 'M'),
	('108.844.854-20', 'Enrico da Rocha Novaes', '1959-6-2', '2017-9-28', '-12.2130465', '-7.601735', 'M'),
	('995.106.177-09', 'Nicolas Rodrigues Rezende', '1975-12-15', '2018-7-27', '-77.1019865', '29.636113', 'M'),
	('675.071.897-32', 'Noah Monteiro Gonçalves', '1930-7-13', '2018-1-28', '46.320081', '161.622634', 'M'),
	('954.840.995-01', 'Thomas Gomes Dias', '1957-1-23', '2018-1-18', '58.5910055', '128.106974', 'M'),
	('032.609.977-84', 'Danilo Alves Dias', '1965-12-18', '2018-7-19', '-26.698048', '-155.975999', 'M'),
	('503.977.886-49', 'Maria Clara Melo Farias', '1961-1-23', '2017-8-9', '64.688391', '-171.278066', 'F'),
	('576.766.726-86', 'Maysa Lopes Freitas', '1986-5-10', '2016-11-2', '-73.954531', '-97.982631', 'F'),
	('117.291.560-10', 'Kamilly Nunes Porto', '1969-6-21', '2018-7-25', '-27.2996365', '-103.477064', 'F'),
	('364.045.102-35', 'Maria Cecília Melo da Rosa', '1955-3-7', '2018-3-26', '-40.4871725', '-40.055865', 'F'),
	('883.382.447-08', 'Sofia Carvalho Porto', '1970-3-1', '2018-12-10', '-59.979340', '-39.002192', 'F'),
	('027.480.123-05', 'Vitor Hugo Fernandes Pereira', '1953-3-30', '2018-6-2', '-47.783428', '-53.142469', 'M'),
	('569.154.071-89', 'Rafael Costa Ferreira', '1983-9-30', '2017-8-3', '-1.7893265', '-62.992009', 'M'),
	('682.453.539-73', 'Pedro Aragão Peixoto', '1969-9-7', '2019-2-12', '-81.503690', '-150.173959', 'M'),
	('608.706.384-67', 'Emanuel Santos Campos', '1991-1-31', '2017-10-11', '3.1137125', '118.812325', 'M'),
	('728.299.197-93', 'João Freitas Santos', '1994-10-20', '2019-5-17', '54.5469135', '-44.063632', 'M'),
	('360.902.402-06', 'Yuri Monteiro Silva', '1944-3-22', '2018-5-1', '-59.8666455', '156.396111', 'M');

	INSERT INTO FORNECEDOR VALUES
	('100.973.580-29', 'Joaquim Teixeira Viana', 'Joaquim Teixeira Viana', '2018-5-30', '-28.405890', '-76.481920', 1),
	('781.245.184-40', 'João Pedro Novaes Santos', 'João Pedro Novaes Santos', '2016-10-26', '-24.8214445', '-142.741479', 1),
	('277.315.375-87', 'Miguel da Rosa Caldeira', 'Miguel da Rosa Caldeira', '2017-2-18', '24.748410', '165.968518', 1),
	('73.146.873/6990-52', 'Souza', 'Souza', '2017-11-9', '20.824489', '171.780080', 1),
	('11.795.090/5557-17', 'Costela', 'Costela', '2016-12-19', '-34.836326', '-146.940230', 1),
	('23.937.977/1806-05', 'Ribeiro', 'Ribeiro', '2018-9-10', '-73.3419155', '-2.287984', 1),
	('88.485.809/6229-50', 'da Cruz', 'da Cruz', '2017-5-26', '24.5207145', '20.757367', 1),
	('85.543.393/1625-40', 'Nunes', 'Nunes', '2018-1-25', '27.5908205', '-51.476896', 1),
	('84.581.712/9436-05', 'Novaes - EI', 'Novaes - EI', '2018-2-21', '29.681180', '-16.758698', 1),
	('70.402.893/4672-71', 'Moura Porto S/A', 'Moura Porto S/A', '2018-7-12', '-7.353292', '71.567299', 1),
	('64.915.583/9842-36', 'da Rosa Vieira S/A', 'da Rosa Vieira S/A', '2017-9-22', '-48.316154', '127.025400', 1),
	('70.549.729/7374-26', 'Teixeira', 'Teixeira', '2018-9-2', '4.062261', '119.496281', 1),
	('07.007.581/6319-81', 'Viana - EI', 'Viana - EI', '2017-7-6', '76.121837', '83.884092', 1),
	('98.358.394/2040-72', 'Gonçalves da Costa e Filhos', 'Gonçalves da Costa e Filhos', '2018-9-8', '-11.1165055', '69.935721', 1),
	('22.323.793/8688-99', 'Costa Souza Ltda.', 'Costa Souza Ltda.', '2017-10-25', '84.617385', '28.595988', 1),
	('47.747.905/4651-53', 'Viana', 'Viana', '2018-7-8', '30.439752', '-29.390847', 1),
	('11.034.406/6331-47', 'Ramos', 'Ramos', '2017-5-21', '23.4043555', '33.167127', 1),
	('97.273.164/1628-84', 'Barros', 'Barros', '2017-2-15', '-53.006299', '24.310945', 1),
	('44.835.073/5577-69', 'Duarte', 'Duarte', '2017-5-26', '-4.8435855', '-107.718215', 1),
	('16.947.184/9819-65', 'Rezende e Filhos', 'Rezende e Filhos', '2017-11-1', '-50.186964', '-47.532575', 1),
	('98.713.604/0853-12', 'Pinto Ltda.', 'Pinto Ltda.', '2016-10-7', '-40.937135', '-56.069672', 1),
	('06.045.166/6050-10', 'Mendes', 'Mendes', '2017-12-3', '-32.957085', '25.019930', 1),
	('56.208.130/2496-06', 'Rocha', 'Rocha', '2018-6-30', '52.0351165', '45.952317', 1),
	('33.919.413/5511-97', 'Vieira', 'Vieira', '2018-7-27', '14.8096365', '-103.528867', 1),
	('11.454.766/8092-39', 'Jesus', 'Jesus', '2017-1-2', '33.5498685', '82.192621', 1),
	('73.291.809/3985-37', 'Melo Pinto S.A.', 'Melo Pinto S.A.', '2018-5-16', '39.275925', '37.795510', 1),
	('72.765.004/8577-22', 'Oliveira e Filhos', 'Oliveira e Filhos', '2017-8-23', '41.471050', '-73.908391', 1),
	('06.217.954/2750-71', 'Barbosa - EI', 'Barbosa - EI', '2016-11-6', '-40.9568685', '-148.958364', 1),
	('68.926.971/7135-98', 'da Mata Fogaça - EI', 'da Mata Fogaça - EI', '2018-4-4', '-40.1665345', '67.105077', 1),
	('07.819.576/1312-29', 'Gomes', 'Gomes', '2018-6-15', '37.6527085', '47.417166', 1),
	('53.293.511/6491-44', 'Monteiro - EI', 'Monteiro - EI', '2018-1-10', '-21.6651885', '135.704316', 1),
	('84.339.811/3490-07', 'Rodrigues - ME', 'Rodrigues - ME', '2018-8-26', '80.0460305', '-154.339867', 1),
	('97.711.726/6953-00', 'Silva', 'Silva', '2017-4-17', '-16.943651', '131.557895', 1),
	('48.328.049/2183-10', 'Pires', 'Pires', '2017-12-3', '-1.629994', '11.165089', 1),
	('64.976.849/9365-23', 'da Paz', 'da Paz', '2017-11-23', '-25.9726295', '69.408759', 1),
	('22.352.107/7239-15', 'Silveira', 'Silveira', '2017-6-10', '-84.554480', '127.833390', 1),
	('02.357.393/3970-88', 'Dias S.A.', 'Dias S.A.', '2018-8-7', '-26.498161', '-5.091408', 1),
	('05.095.078/0906-30', 'Silveira', 'Silveira', '2017-5-9', '-75.946631', '73.547627', 1),
	('38.124.301/1142-94', 'Azevedo', 'Azevedo', '2017-7-17', '-43.8474545', '116.692238', 1),
	('18.831.608/3434-03', 'da Luz', 'da Luz', '2017-10-25', '1.389946', '55.701595', 1),
	('29.068.782/3837-66', 'da Paz', 'da Paz', '2017-8-31', '-70.5488965', '-84.466929', 1),
	('22.433.349/6540-01', 'da Costa Araújo Ltda.', 'da Costa Araújo Ltda.', '2018-9-1', '79.7429655', '2.587280', 1),
	('84.540.585/3190-21', 'Rodrigues S.A.', 'Rodrigues S.A.', '2017-3-23', '-1.1823925', '13.692588', 1),
	('74.056.082/4785-02', 'Vieira', 'Vieira', '2018-5-4', '62.080437', '-60.205704', 1),
	('04.370.899/9570-23', 'da Costa', 'da Costa', '2017-9-17', '-62.5315065', '-106.088852', 1),
	('56.380.407/3394-02', 'Costa', 'Costa', '2017-2-18', '-71.636306', '39.510145', 1),
	('28.422.429/2139-39', 'Santos Ltda.', 'Santos Ltda.', '2017-8-4', '-9.8467925', '-8.178918', 1),
	('20.802.069/5550-16', 'Carvalho', 'Carvalho', '2017-6-17', '74.524222', '-176.037246', 1),
	('41.900.454/1097-00', 'Vieira Gomes - EI', 'Vieira Gomes - EI', '2017-10-26', '-87.717482', '-95.211148', 1),
	('82.256.860/7907-09', 'da Costa S/A', 'da Costa S/A', '2017-6-4', '55.967587', '11.168347', 1),
	('54.549.266/2345-33', 'Moura', 'Moura', '2017-1-27', '75.871090', '22.073282', 1),
	('97.322.164/7356-14', 'Costela Costela S/A', 'Costela Costela S/A', '2017-9-11', '23.4936105', '96.338894', 1),
	('10.507.365/8503-85', 'Barbosa - EI', 'Barbosa - EI', '2016-12-26', '6.9623735', '-120.303351', 1),
	('23.856.760/7963-53', 'das Neves S/A', 'das Neves S/A', '2018-9-20', '70.318515', '-101.649537', 1),
	('89.936.340/3573-91', 'Alves Cardoso Ltda.', 'Alves Cardoso Ltda.', '2018-4-11', '89.096701', '70.579381', 1),
	('46.825.729/5937-51', 'Oliveira', 'Oliveira', '2017-12-1', '-72.592665', '100.839343', 1),
	('79.460.664/7483-76', 'Nascimento', 'Nascimento', '2017-8-9', '-83.0463395', '-18.729988', 1),
	('79.315.423/8747-11', 'Moura da Cunha S.A.', 'Moura da Cunha S.A.', '2017-10-11', '-35.3891795', '43.638708', 1),
	('01.059.020/2794-56', 'Viana e Filhos', 'Viana e Filhos', '2018-3-21', '-77.463571', '-37.193289', 1),
	('84.428.432/7582-52', 'Souza', 'Souza', '2017-9-21', '3.3176195', '165.708562', 1),
	('07.293.879/9225-41', 'das Neves', 'das Neves', '2018-2-2', '-71.0860225', '-157.781707', 1),
	('38.973.389/4931-39', 'Novaes', 'Novaes', '2017-11-17', '-19.059097', '-31.469397', 1),
	('71.150.726/0688-96', 'da Mata da Rocha e Filhos', 'da Mata da Rocha e Filhos', '2016-12-7', '80.747045', '-59.874794', 1),
	('67.717.709/5760-50', 'Araújo', 'Araújo', '2018-9-14', '36.5540285', '92.003018', 1),
	('68.328.795/7689-07', 'Teixeira - ME', 'Teixeira - ME', '2016-10-9', '32.716640', '77.415424', 1),
	('60.646.070/3907-74', 'Almeida', 'Almeida', '2017-6-1', '80.4597665', '121.781338', 1),
	('56.223.378/2229-42', 'Porto', 'Porto', '2016-11-24', '46.711218', '-1.217147', 1),
	('59.381.457/8845-06', 'Cardoso', 'Cardoso', '2018-2-6', '-50.3070745', '6.409025', 1),
	('40.075.585/7684-12', 'Fernandes', 'Fernandes', '2018-8-22', '-28.031771', '76.542681', 1),
	('03.600.515/0484-07', 'Cardoso Ltda.', 'Cardoso Ltda.', '2018-4-16', '-15.3366615', '-116.636329', 1),
	('44.920.432/4409-19', 'Melo Fernandes e Filhos', 'Melo Fernandes e Filhos', '2017-6-3', '66.243007', '72.526255', 1),
	('45.831.290/7823-56', 'da Luz S/A', 'da Luz S/A', '2018-9-8', '71.8266625', '48.499687', 1),
	('16.073.821/4462-85', 'Peixoto', 'Peixoto', '2018-5-29', '52.8254645', '13.522729', 1),
	('15.932.569/3394-10', 'Campos', 'Campos', '2017-7-27', '-57.502358', '61.408235', 1),
	('37.804.067/0956-37', 'Alves', 'Alves', '2017-9-11', '-31.2242065', '167.746340', 1),
	('26.941.738/9900-23', 'da Cunha S/A', 'da Cunha S/A', '2017-1-6', '16.8227425', '43.028561', 1),
	('01.560.639/7251-64', 'Pires - ME', 'Pires - ME', '2017-2-21', '-18.429804', '151.940314', 1),
	('95.776.695/3314-88', 'Barros Barbosa S/A', 'Barros Barbosa S/A', '2017-4-27', '0.5498175', '-112.670959', 1),
	('26.593.635/6363-56', 'Nascimento da Luz e Filhos', 'Nascimento da Luz e Filhos', '2017-4-1', '-75.515594', '-36.139931', 1),
	('89.070.202/7783-94', 'das Neves', 'das Neves', '2017-7-7', '87.8088255', '32.706234', 1),
	('71.328.725/7280-66', 'Lima da Paz e Filhos', 'Lima da Paz e Filhos', '2018-9-13', '39.113196', '123.402485', 1),
	('05.727.536/9986-83', 'Freitas', 'Freitas', '2017-3-8', '12.0695915', '139.501385', 1),
	('80.074.691/8229-72', 'Azevedo', 'Azevedo', '2017-4-30', '67.791984', '57.251618', 1),
	('90.465.421/0713-63', 'da Paz e Filhos', 'da Paz e Filhos', '2018-4-9', '-81.630576', '77.092699', 1),
	('02.059.648/4763-25', 'Sales', 'Sales', '2016-12-28', '2.967914', '13.007912', 1),
	('46.185.233/4935-45', 'da Rosa - EI', 'da Rosa - EI', '2017-1-29', '60.068406', '68.803947', 1),
	('78.440.900/1662-07', 'Moura S/A', 'Moura S/A', '2017-4-12', '30.515030', '44.471200', 1),
	('13.818.067/1028-53', 'Santos', 'Santos', '2017-10-23', '-65.961989', '-32.097609', 1),
	('45.023.221/1140-46', 'Novaes e Filhos', 'Novaes e Filhos', '2018-1-19', '-25.393456', '-72.751802', 1),
	('76.680.896/6201-16', 'Farias S/A', 'Farias S/A', '2017-5-12', '74.581487', '-13.447003', 1),
	('06.025.833/0170-88', 'Barros Teixeira e Filhos', 'Barros Teixeira e Filhos', '2018-5-28', '1.2055495', '95.037991', 1),
	('87.896.565/7373-25', 'Cavalcanti', 'Cavalcanti', '2017-7-3', '79.5230915', '138.272764', 1),
	('38.604.625/4002-30', 'Pereira', 'Pereira', '2016-11-14', '31.9083715', '-172.291343', 1),
	('75.946.122/5806-69', 'Peixoto e Filhos', 'Peixoto e Filhos', '2017-6-1', '57.175818', '-158.153253', 1),
	('16.006.416/0092-94', 'Rocha Barbosa S.A.', 'Rocha Barbosa S.A.', '2016-12-30', '20.2758515', '11.698364', 1),
	('38.275.756/6301-36', 'Cardoso', 'Cardoso', '2017-6-19', '-41.1814925', '137.199047', 1),
	('22.923.768/6897-55', 'Lopes Caldeira - EI', 'Lopes Caldeira - EI', '2017-5-24', '-52.638824', '129.761738', 1),
	('04.963.065/1999-25', 'Moreira S/A', 'Moreira S/A', '2017-1-25', '28.8314395', '-47.631003', 1),
	('46.230.735/3474-80', 'Caldeira', 'Caldeira', '2017-2-9', '-89.7148195', '122.348545', 1),
	('02.984.527/1287-82', 'Jesus Rodrigues e Filhos', 'Jesus Rodrigues e Filhos', '2017-1-12', '31.8920235', '-82.468496', 1);

	INSERT INTO PRODUTO VALUES
	(1, '18694291', 'abacate', 4.8, 1, 1, 2),
	(2, '08451750', 'abacate avocado', 3.0, 1, 1, 2),
	(3, '60551610', 'abacaxi havaiano', 3.7, 1, 1, 2),
	(4, '92310193', 'abacaxi perol', 3.4, 1, 1, 2),
	(5, '74168705', 'ameixa branca', 10.7, 1, 1, 2),
	(6, '11469193', 'ameixa importada', 5.5, 1, 1, 2),
	(7, '63229875', 'ameixa rosa', 2.3, 1, 1, 2),
	(8, '53399250', 'antenova', 5.0, 1, 1, 2),
	(9, '05374403', 'banana catur organica', 1.1, 1, 1, 2),
	(10, '23128637', 'banana da terra', 5.3, 1, 1, 2),
	(11, '09092495', 'banana maca', 3.4, 1, 1, 2),
	(12, '00566308', 'banana prata', 4.1, 1, 1, 2),
	(13, '29578252', 'mexerica montenegra', 1.9, 1, 1, 2),
	(14, '81706020', 'mexerica morgot', 0.8, 1, 1, 2),
	(15, '02750927', 'mexerica poca', 5.6, 1, 1, 2),
	(16, '87655483', 'mexerica importada', 10.1, 1, 1, 2),
	(17, '59640936', 'caqui chocolate', 10.2, 1, 1, 2),
	(18, '20128371', 'caqui coracao', 1.2, 1, 1, 2),
	(19, '84011428', 'caqui forte', 5.8, 1, 1, 2),
	(20, '63645231', 'caqui fuyu', 7.2, 1, 1, 2),
	(21, '91237057', 'caqui importado', 7.1, 1, 1, 2),
	(22, '73203667', 'carambola', 5.3, 1, 1, 2),
	(23, '63887594', 'coco seco', 0.3, 1, 1, 2),
	(24, '93435925', 'coco', 6.1, 1, 1, 2),
	(25, '49808575', 'coco verde', 8.5, 1, 1, 2),
	(26, '69479892', 'damasco', 10.5, 1, 1, 2),
	(27, '23157095', 'fruta do conde', 1.6, 1, 1, 2),
	(28, '11637615', 'goiaba', 9.9, 1, 1, 2),
	(29, '41760161', 'granadilla silvestre', 2.6, 1, 1, 2),
	(30, '45505522', 'graviola', 6.5, 1, 1, 2),
	(31, '95282237', 'jaca', 4.9, 1, 1, 2),
	(32, '97853480', 'kiwi', 7.6, 1, 1, 2),
	(33, '96110676', 'kiwi zelandia', 6.8, 1, 1, 2),
	(34, '95456669', 'kiwi maca', 4.3, 1, 1, 2),
	(35, '69658433', 'laranja do ceu', 10.1, 1, 1, 2),
	(36, '04705802', 'laranja pera', 7.8, 1, 1, 2),
	(37, '21097737', 'laranja bahia', 10.7, 1, 1, 2),
	(38, '31907903', 'lichia', 8.8, 1, 1, 2),
	(39, '42676911', 'limao tati', 3.0, 1, 1, 2),
	(40, '44516529', 'limao persa', 4.1, 1, 1, 2),
	(41, '67039517', 'limao siciliano', 8.2, 1, 1, 2),
	(42, '99711900', 'laranja de umbigo exp', 9.6, 1, 1, 2),
	(43, '55934329', 'maca rosa', 4.9, 1, 1, 2),
	(44, '41440810', 'maca fugi', 2.6, 1, 1, 2),
	(45, '97790693', 'maca gala', 1.7, 1, 1, 2),
	(46, '37151713', 'maca argentina', 8.9, 1, 1, 2),
	(47, '91651594', 'maca verde', 6.2, 1, 1, 2),
	(48, '18180886', 'mamao formosa', 4.1, 1, 1, 2),
	(49, '83713248', 'mamao papaya golden', 5.1, 1, 1, 2),
	(50, '96539019', 'mamao papaya esp', 9.3, 1, 1, 2),
	(51, '48273374', 'manga haden', 2.6, 1, 1, 2),
	(52, '89120392', 'manga palmer', 4.4, 1, 1, 2),
	(53, '47791299', 'manga rosa', 8.4, 1, 1, 2),
	(54, '81405275', 'maracuja azedo', 8.5, 1, 1, 2),
	(55, '66694656', 'maracuja doce', 4.8, 1, 1, 2),
	(56, '05484164', 'melancia', 5.4, 1, 1, 2),
	(57, '51595968', 'melancia sem semente', 1.3, 1, 1, 2),
	(58, '82358990', 'melao cantalume', 2.4, 1, 1, 2),
	(59, '69740060', 'melao cepi', 4.5, 1, 1, 2),
	(60, '04613794', 'melao charatane', 10.5, 1, 1, 2),
	(61, '71750545', 'melao espanhol', 5.8, 1, 1, 2),
	(62, '09612266', 'melao gala', 8.1, 1, 1, 2),
	(63, '62533720', 'melao gaucho', 8.3, 1, 1, 2),
	(64, '77402691', 'melao orange', 6.6, 1, 1, 2),
	(65, '71779966', 'melao pele sapo', 1.1, 1, 1, 2),
	(66, '82139469', 'manga tommy', 7.8, 1, 1, 2),
	(67, '87438857', 'nectarina', 0.3, 1, 1, 2),
	(68, '97756620', 'nectarina importada', 7.3, 1, 1, 2),
	(69, '30970458', 'pera asiatica', 4.0, 1, 1, 2),
	(70, '94810158', 'pera damjou', 9.3, 1, 1, 2),
	(71, '70481884', 'pera importada', 3.9, 1, 1, 2),
	(72, '16631069', 'pera nacional', 7.2, 1, 1, 2),
	(73, '64064994', 'pera verde', 2.3, 1, 1, 2),
	(74, '35706182', 'pera portuguesa', 8.1, 1, 1, 2),
	(75, '96453995', 'pera williams', 9.5, 1, 1, 2),
	(76, '02425481', 'pessego amarelo', 4.3, 1, 1, 2),
	(77, '31385350', 'pessego branco', 3.0, 1, 1, 2),
	(78, '54121058', 'pessego importado especial', 3.0, 1, 1, 2),
	(79, '39628770', 'roma', 1.1, 1, 1, 2),
	(80, '55048620', 'uva bentica', 0.1, 1, 1, 2),
	(81, '28658757', 'uva brasil', 3.9, 1, 1, 2),
	(82, '02930688', 'uva importada', 7.5, 1, 1, 2),
	(83, '54537576', 'uva italiana', 4.6, 1, 1, 2),
	(84, '34719565', 'uva niagara branca', 4.1, 1, 1, 2),
	(85, '93432368', 'uva niagara rosa', 0.4, 1, 1, 2),
	(86, '05389797', 'uva red glob', 7.8, 1, 1, 2),
	(87, '19183572', 'uva rubi rosa', 4.7, 1, 1, 2),
	(88, '63924329', 'uva rubi verde', 1.0, 1, 1, 2),
	(89, '81752478', 'uva venus', 7.2, 1, 1, 2),
	(90, '50417292', 'pinhao', 1.1, 1, 1, 2),
	(91, '55271738', 'cebola branca', 7.1, 2, 1, 2),
	(92, '48268257', 'cebola roxa', 0.3, 2, 1, 2),
	(93, '62369602', 'cenoura', 8.7, 2, 1, 2),
	(94, '83867392', 'gengibre', 6.0, 2, 1, 2),
	(95, '40105918', 'tomate italiano', 9.2, 2, 1, 2),
	(96, '80382508', 'cebola branca', 8.3, 3, 1, 1),
	(97, '41218075', 'cebola roxa', 8.5, 3, 1, 1),
	(98, '39357441', 'cenoura', 9.6, 3, 1, 1),
	(99, '50155552', 'gengibre', 9.3, 3, 1, 1),
	(100, '01593921', 'tomate italiano', 7.4, 3, 1, 1);

	INSERT INTO AQUISICAO_PRODUTO VALUES
	('46.825.729/5937-51', 23, '2017-6-3', '21:18:05', 35, 5.5),
	('53.293.511/6491-44', 42, '2016-10-10', '08:07:06', 26, 1.4),
	('23.856.760/7963-53', 67, '2018-4-19', '01:48:25', 7, 1.0),
	('23.937.977/1806-05', 56, '2017-12-7', '22:51:18', 41, 6.4),
	('28.422.429/2139-39', 83, '2018-7-15', '22:44:38', 42, 2.8),
	('07.007.581/6319-81', 47, '2018-7-4', '18:40:22', 26, 4.9),
	('79.315.423/8747-11', 29, '2018-9-29', '06:24:47', 12, 6.3),
	('16.947.184/9819-65', 64, '2018-8-16', '10:38:47', 23, 5.3),
	('46.825.729/5937-51', 39, '2017-2-6', '11:59:12', 32, 5.1),
	('68.328.795/7689-07', 7, '2017-6-17', '20:01:33', 12, 4.5),
	('70.402.893/4672-71', 90, '2017-10-7', '11:15:50', 45, 0.8),
	('18.831.608/3434-03', 28, '2017-11-22', '19:10:05', 9, 3.4),
	('56.380.407/3394-02', 68, '2017-2-14', '21:44:25', 5, 2.2),
	('73.146.873/6990-52', 61, '2016-10-23', '15:09:26', 40, 0.1),
	('89.936.340/3573-91', 17, '2017-6-8', '10:09:33', 49, 3.5),
	('84.428.432/7582-52', 61, '2017-11-17', '12:01:18', 46, 7.0),
	('15.932.569/3394-10', 91, '2017-8-4', '14:24:59', 17, 4.8),
	('06.217.954/2750-71', 18, '2018-3-10', '23:33:31', 6, 6.0),
	('02.357.393/3970-88', 74, '2017-10-31', '09:40:30', 31, 0.9),
	('37.804.067/0956-37', 21, '2016-12-22', '00:36:22', 48, 3.8),
	('56.380.407/3394-02', 35, '2018-8-21', '23:13:42', 7, 5.3),
	('85.543.393/1625-40', 34, '2018-5-3', '01:23:27', 23, 4.9),
	('16.073.821/4462-85', 23, '2018-6-6', '08:19:00', 25, 5.7),
	('22.923.768/6897-55', 66, '2017-12-8', '04:59:09', 29, 1.0),
	('277.315.375-87', 20, '2017-2-27', '23:25:40', 25, 6.4),
	('46.185.233/4935-45', 52, '2017-4-10', '00:04:07', 38, 0.9),
	('70.549.729/7374-26', 12, '2017-4-5', '03:34:15', 2, 2.6),
	('56.208.130/2496-06', 38, '2017-1-11', '14:17:36', 5, 6.0),
	('781.245.184-40', 80, '2017-10-15', '03:30:00', 16, 4.5),
	('40.075.585/7684-12', 64, '2018-1-24', '02:11:33', 13, 3.4),
	('82.256.860/7907-09', 19, '2017-3-23', '17:15:57', 41, 5.2),
	('53.293.511/6491-44', 34, '2016-10-31', '00:35:41', 31, 0.5),
	('64.976.849/9365-23', 91, '2017-3-17', '02:44:01', 41, 1.5),
	('84.540.585/3190-21', 63, '2017-5-1', '22:31:32', 38, 5.1),
	('46.185.233/4935-45', 22, '2017-9-8', '11:56:06', 31, 3.7),
	('98.358.394/2040-72', 93, '2017-12-17', '12:02:02', 29, 6.5),
	('03.600.515/0484-07', 90, '2017-10-19', '15:13:20', 46, 6.7),
	('75.946.122/5806-69', 12, '2018-2-13', '08:34:45', 44, 5.4),
	('79.315.423/8747-11', 88, '2018-6-19', '15:43:51', 43, 6.7),
	('90.465.421/0713-63', 20, '2018-3-6', '19:12:29', 25, 6.3),
	('56.208.130/2496-06', 14, '2018-1-16', '16:03:28', 9, 1.2),
	('75.946.122/5806-69', 49, '2017-3-9', '09:10:39', 36, 2.4),
	('06.045.166/6050-10', 74, '2017-4-15', '13:12:01', 48, 1.1),
	('01.560.639/7251-64', 40, '2017-11-10', '15:45:00', 29, 1.4),
	('75.946.122/5806-69', 12, '2017-11-11', '22:48:26', 3, 4.1),
	('82.256.860/7907-09', 81, '2017-12-13', '03:12:32', 38, 6.0),
	('68.328.795/7689-07', 44, '2018-2-4', '20:43:06', 20, 7.0),
	('64.976.849/9365-23', 85, '2018-1-3', '01:38:58', 1, 7.0),
	('47.747.905/4651-53', 49, '2017-9-2', '19:49:00', 42, 6.2),
	('44.920.432/4409-19', 7, '2018-1-29', '11:06:50', 39, 2.3),
	('78.440.900/1662-07', 31, '2018-1-22', '05:18:40', 3, 2.7),
	('44.835.073/5577-69', 6, '2017-8-15', '02:44:44', 11, 0.9),
	('781.245.184-40', 60, '2018-8-23', '18:57:12', 23, 2.5),
	('07.293.879/9225-41', 84, '2018-5-14', '00:04:20', 16, 5.0),
	('277.315.375-87', 63, '2016-11-9', '11:39:27', 30, 5.7),
	('15.932.569/3394-10', 5, '2017-6-17', '16:01:02', 7, 5.2),
	('02.357.393/3970-88', 96, '2017-12-10', '02:08:08', 41, 6.3),
	('37.804.067/0956-37', 96, '2017-3-25', '07:18:08', 42, 3.6),
	('03.600.515/0484-07', 19, '2018-8-12', '18:03:36', 12, 2.3),
	('11.795.090/5557-17', 72, '2018-3-18', '11:26:05', 48, 1.5),
	('20.802.069/5550-16', 75, '2018-2-23', '07:08:34', 44, 4.9),
	('56.380.407/3394-02', 82, '2018-10-2', '15:32:10', 12, 1.2),
	('76.680.896/6201-16', 98, '2017-8-6', '09:32:02', 40, 0.7),
	('46.230.735/3474-80', 78, '2017-8-14', '03:02:15', 16, 6.3),
	('56.223.378/2229-42', 100, '2017-7-20', '15:52:53', 25, 1.0),
	('22.923.768/6897-55', 7, '2018-8-15', '05:29:07', 32, 3.7),
	('53.293.511/6491-44', 84, '2017-12-6', '02:08:25', 19, 5.6),
	('82.256.860/7907-09', 76, '2017-12-16', '10:50:15', 9, 4.9),
	('23.856.760/7963-53', 62, '2018-7-10', '05:23:06', 4, 3.8),
	('11.454.766/8092-39', 11, '2018-4-23', '21:16:46', 28, 4.2),
	('84.540.585/3190-21', 7, '2018-7-28', '03:33:16', 38, 5.4),
	('68.926.971/7135-98', 12, '2018-3-23', '07:58:01', 29, 3.7),
	('06.025.833/0170-88', 1, '2017-6-13', '14:17:32', 30, 0.6),
	('06.045.166/6050-10', 6, '2017-4-17', '00:48:24', 30, 4.8),
	('38.275.756/6301-36', 98, '2017-11-16', '15:10:07', 25, 3.8),
	('26.941.738/9900-23', 83, '2017-7-10', '06:18:26', 30, 5.9),
	('79.315.423/8747-11', 18, '2018-6-6', '22:16:42', 18, 1.7),
	('37.804.067/0956-37', 33, '2017-7-4', '15:24:40', 34, 0.7),
	('71.150.726/0688-96', 100, '2018-5-3', '00:59:01', 26, 3.8),
	('05.095.078/0906-30', 42, '2017-6-24', '11:56:56', 5, 4.6),
	('70.549.729/7374-26', 53, '2017-11-25', '10:17:56', 38, 4.1),
	('01.560.639/7251-64', 64, '2018-1-30', '11:43:19', 40, 0.8),
	('26.593.635/6363-56', 82, '2017-11-24', '22:23:57', 39, 2.7),
	('44.920.432/4409-19', 69, '2017-12-19', '06:05:28', 40, 6.0),
	('06.025.833/0170-88', 50, '2017-9-16', '05:29:21', 35, 4.9),
	('02.059.648/4763-25', 33, '2017-3-2', '09:58:55', 1, 4.2),
	('90.465.421/0713-63', 57, '2018-5-10', '19:54:00', 20, 1.5),
	('48.328.049/2183-10', 53, '2018-9-3', '12:09:52', 25, 5.2),
	('67.717.709/5760-50', 32, '2017-2-21', '22:51:33', 13, 0.8),
	('71.328.725/7280-66', 75, '2017-1-23', '14:50:07', 29, 6.7),
	('15.932.569/3394-10', 23, '2017-1-16', '20:22:49', 13, 4.6),
	('22.323.793/8688-99', 15, '2017-7-2', '10:14:38', 41, 6.7),
	('11.034.406/6331-47', 11, '2018-6-4', '00:16:54', 37, 3.8),
	('781.245.184-40', 88, '2018-1-12', '01:39:12', 49, 1.8),
	('02.984.527/1287-82', 9, '2016-10-30', '13:44:47', 28, 2.2),
	('97.711.726/6953-00', 66, '2017-11-14', '07:49:21', 2, 5.0),
	('33.919.413/5511-97', 76, '2018-6-9', '21:50:53', 14, 5.5),
	('78.440.900/1662-07', 14, '2017-8-12', '23:26:21', 3, 6.4),
	('64.976.849/9365-23', 72, '2018-2-3', '19:10:28', 23, 2.6),
	('04.370.899/9570-23', 33, '2018-4-27', '07:23:48', 27, 4.6);

	INSERT INTO VENDA VALUES
	(1, '2018-8-17', '00:04:23', '503.977.886-49'),
	(2, '2017-10-30', '18:16:37', '543.031.325-43'),
	(3, '2018-5-16', '17:27:55', '192.283.160-39'),
	(4, '2017-5-4', '01:28:05', '938.320.985-26'),
	(5, '2018-8-17', '02:04:29', '360.902.402-06'),
	(6, '2016-11-22', '15:42:35', '995.106.177-09'),
	(7, '2017-3-23', '00:59:44', '480.796.652-90'),
	(8, '2016-11-4', '16:17:01', '487.832.626-36'),
	(9, '2017-11-9', '14:11:18', '586.822.245-85'),
	(10, '2017-7-14', '12:10:06', '493.684.111-07'),
	(11, '2017-8-7', '21:47:08', '970.122.418-37'),
	(12, '2016-12-22', '07:07:50', '959.031.846-00'),
	(13, '2017-9-26', '07:10:46', '543.031.325-43'),
	(14, '2017-11-7', '19:19:28', '493.684.111-07'),
	(15, '2017-5-13', '01:39:24', '675.071.897-32'),
	(16, '2017-3-27', '09:08:51', '581.002.072-08'),
	(17, '2017-6-25', '21:03:29', '959.031.846-00'),
	(18, '2018-4-28', '15:25:02', '402.246.463-11'),
	(19, '2017-12-13', '21:47:04', '774.236.197-36'),
	(20, '2018-1-10', '11:49:52', '218.003.800-38'),
	(21, '2018-5-17', '06:46:25', '289.081.666-45'),
	(22, '2017-9-5', '03:51:30', '874.524.521-51'),
	(23, '2018-7-20', '00:58:16', '298.322.674-39'),
	(24, '2017-1-28', '02:14:38', '051.049.739-05'),
	(25, '2017-8-10', '08:53:50', '592.189.369-21'),
	(26, '2018-4-3', '13:18:01', '128.318.589-09'),
	(27, '2018-2-25', '08:57:56', '293.690.116-25'),
	(28, '2017-10-7', '02:00:03', '360.902.402-06'),
	(29, '2018-1-30', '23:39:55', '117.291.560-10'),
	(30, '2017-10-25', '05:40:43', '477.023.447-33'),
	(31, '2018-2-3', '05:07:37', '476.119.804-40'),
	(32, '2017-3-5', '01:56:18', '543.031.325-43'),
	(33, '2018-1-14', '13:27:13', '117.291.560-10'),
	(34, '2017-12-3', '21:12:39', '995.106.177-09'),
	(35, '2017-1-27', '00:03:19', '581.002.072-08'),
	(36, '2018-7-4', '07:43:50', '986.418.387-75'),
	(37, '2018-2-8', '15:03:10', '289.081.666-45'),
	(38, '2017-5-2', '19:04:16', '883.382.447-08'),
	(39, '2017-12-19', '18:50:51', '208.664.918-56'),
	(40, '2016-11-7', '23:49:10', '874.524.521-51'),
	(41, '2017-8-24', '06:13:22', '477.023.447-33'),
	(42, '2017-2-26', '16:21:54', '887.450.522-12'),
	(43, '2018-7-4', '09:53:20', '569.154.071-89'),
	(44, '2016-10-20', '17:25:45', '883.382.447-08'),
	(45, '2017-3-12', '10:07:14', '208.664.918-56'),
	(46, '2017-8-21', '06:22:19', '809.181.088-10'),
	(47, '2017-4-24', '07:04:19', '742.933.399-06'),
	(48, '2017-9-9', '12:35:57', '901.363.990-96'),
	(49, '2018-2-27', '18:39:31', '521.588.578-89'),
	(50, '2018-3-20', '12:34:47', '293.690.116-25'),
	(51, '2018-1-3', '08:09:23', '108.844.854-20'),
	(52, '2017-8-8', '21:21:38', '562.175.036-54'),
	(53, '2017-1-3', '18:02:48', '442.847.425-31'),
	(54, '2017-3-23', '03:24:19', '227.345.725-16'),
	(55, '2018-7-1', '09:40:20', '261.156.571-64'),
	(56, '2018-4-6', '20:42:44', '680.184.160-28'),
	(57, '2017-7-9', '22:22:33', '742.933.399-06'),
	(58, '2017-11-28', '18:45:20', '480.796.652-90'),
	(59, '2017-5-2', '16:43:25', '675.071.897-32'),
	(60, '2018-2-24', '21:41:50', '298.322.674-39'),
	(61, '2017-4-24', '00:30:42', '493.684.111-07'),
	(62, '2016-12-10', '05:34:09', '728.299.197-93'),
	(63, '2018-2-25', '18:48:54', '636.541.312-20'),
	(64, '2018-1-8', '05:07:52', '043.307.895-23'),
	(65, '2018-8-29', '22:39:23', '428.464.848-99'),
	(66, '2018-4-19', '04:58:54', '176.489.865-66'),
	(67, '2018-4-14', '05:13:11', '680.184.160-28'),
	(68, '2017-5-28', '08:33:23', '476.119.804-40'),
	(69, '2017-8-22', '03:37:04', '897.094.953-48'),
	(70, '2017-9-26', '14:00:08', '191.144.047-02'),
	(71, '2017-3-30', '18:32:13', '364.045.102-35'),
	(72, '2016-11-10', '20:42:18', '487.832.626-36'),
	(73, '2017-9-1', '00:53:59', '051.049.739-05'),
	(74, '2017-1-18', '00:42:36', '901.363.990-96'),
	(75, '2016-10-21', '15:44:16', '360.902.402-06'),
	(76, '2017-7-16', '02:47:46', '938.320.985-26'),
	(77, '2018-6-18', '21:15:42', '442.847.425-31'),
	(78, '2017-5-31', '22:18:45', '027.480.123-05'),
	(79, '2018-4-3', '08:27:23', '455.254.563-97'),
	(80, '2018-9-19', '20:48:11', '455.254.563-97'),
	(81, '2018-10-3', '00:12:47', '909.320.903-54'),
	(82, '2017-1-27', '13:31:55', '095.725.968-96'),
	(83, '2017-7-31', '05:55:40', '218.003.800-38'),
	(84, '2017-10-30', '04:46:42', '559.453.538-17'),
	(85, '2017-2-15', '04:09:34', '402.246.463-11'),
	(86, '2017-11-22', '16:48:52', '682.453.539-73'),
	(87, '2018-10-2', '04:05:57', '602.150.938-28'),
	(88, '2017-11-14', '02:28:48', '682.453.539-73'),
	(89, '2018-9-11', '08:29:08', '126.465.446-42'),
	(90, '2017-3-8', '04:21:00', '970.122.418-37'),
	(91, '2018-8-5', '15:02:22', '675.071.897-32'),
	(92, '2018-9-21', '12:42:35', '682.112.737-99'),
	(93, '2018-6-16', '21:37:09', '193.648.568-05'),
	(94, '2016-11-23', '05:30:50', '901.363.990-96'),
	(95, '2018-3-30', '17:06:36', '176.489.865-66'),
	(96, '2016-11-12', '23:49:12', '477.023.447-33'),
	(97, '2017-1-10', '12:32:46', '020.879.003-96'),
	(98, '2018-5-29', '08:12:54', '897.094.953-48'),
	(99, '2018-8-6', '12:49:00', '274.442.369-68'),
	(100, '2017-5-30', '00:30:10', '218.003.800-38');

	INSERT INTO VENDA_PRODUTO VALUES
	(62, 4, 2.4),
	(64, 24, 1.2),
	(14, 42, 1.1),
	(5, 96, 0.5),
	(41, 53, 0.9),
	(22, 58, 1.5),
	(68, 98, 1.4),
	(71, 70, 2.0),
	(67, 76, 0.7),
	(11, 83, 2.4),
	(35, 38, 0.1),
	(5, 74, 2.2),
	(64, 19, 1.3),
	(33, 66, 1.0),
	(71, 97, 1.2),
	(91, 41, 1.2),
	(92, 25, 1.4),
	(48, 92, 1.7),
	(38, 10, 0.1),
	(88, 16, 0.3),
	(80, 14, 1.2),
	(29, 83, 0.2),
	(30, 89, 2.9),
	(61, 64, 1.8),
	(45, 60, 2.2),
	(54, 25, 0.6),
	(77, 12, 0.8),
	(77, 77, 2.8),
	(56, 55, 1.8),
	(87, 72, 2.0),
	(61, 94, 3.0),
	(6, 35, 1.7),
	(11, 32, 0.9),
	(53, 45, 1.9),
	(35, 60, 3.0),
	(76, 69, 0.7),
	(99, 50, 0.1),
	(93, 91, 0.6),
	(90, 26, 2.6),
	(87, 39, 0.6),
	(78, 38, 2.4),
	(92, 28, 1.3),
	(45, 66, 2.8),
	(54, 76, 2.2),
	(63, 38, 1.3),
	(77, 77, 1.9),
	(37, 93, 0.2),
	(59, 35, 2.8),
	(50, 95, 1.4),
	(90, 96, 1.4);

	INSERT INTO CONTATO_FORNECEDOR VALUES
	(1, '+55 (021) 4491 2934', '100.973.580-29', 1),
	(2, '+55 (021) 4371-0909', '781.245.184-40', 1),
	(3, '41 5722 7881', '277.315.375-87', 1),
	(4, '+55 11 4649-3727', '73.146.873/6990-52', 1),
	(5, '61 2791-5451', '11.795.090/5557-17', 1),
	(6, '+55 (071) 8173 0422', '23.937.977/1806-05', 1),
	(7, '(051) 5092-1815', '88.485.809/6229-50', 1),
	(8, '31 4417 1366', '85.543.393/1625-40', 1),
	(9, '+55 (031) 5010 5669', '84.581.712/9436-05', 1),
	(10, '+55 21 5381-3676', '70.402.893/4672-71', 1),
	(11, '51 129 1034', '64.915.583/9842-36', 1),
	(12, '21 7926-3434', '70.549.729/7374-26', 1),
	(13, '+55 51 662 2380', '07.007.581/6319-81', 1),
	(14, '21 4921-6618', '98.358.394/2040-72', 1),
	(15, '(071) 4873-3627', '22.323.793/8688-99', 1),
	(16, '+55 (031) 8386-1635', '47.747.905/4651-53', 1),
	(17, '(051) 7137-2265', '11.034.406/6331-47', 1),
	(18, '+55 (011) 3703 0376', '97.273.164/1628-84', 1),
	(19, '(051) 8891-1304', '44.835.073/5577-69', 1),
	(20, '+55 (041) 1940-9309', '16.947.184/9819-65', 1),
	(21, '(041) 3791 7864', '98.713.604/0853-12', 1),
	(22, '61 2330 3197', '06.045.166/6050-10', 1),
	(23, '+55 (061) 2435 9874', '56.208.130/2496-06', 1),
	(24, '31 3181 4508', '33.919.413/5511-97', 1),
	(25, '+55 51 715 5831', '11.454.766/8092-39', 1),
	(26, '+55 31 5928-7429', '73.291.809/3985-37', 1),
	(27, '31 9907-7022', '72.765.004/8577-22', 1),
	(28, '81 2590 0466', '06.217.954/2750-71', 1),
	(29, '+55 (081) 3146 0810', '68.926.971/7135-98', 1),
	(30, '(011) 6855 0724', '07.819.576/1312-29', 1),
	(31, '71 5920-4276', '53.293.511/6491-44', 1),
	(32, '81 9929-9929', '84.339.811/3490-07', 1),
	(33, '11 0012-7426', '97.711.726/6953-00', 1),
	(34, '51 095 8954', '48.328.049/2183-10', 1),
	(35, '+55 (031) 9560 8306', '64.976.849/9365-23', 1),
	(36, '41 1826-6911', '22.352.107/7239-15', 1),
	(37, '81 0411-4899', '02.357.393/3970-88', 1),
	(38, '+55 11 9620 0593', '05.095.078/0906-30', 1),
	(39, '31 8675 6694', '38.124.301/1142-94', 1),
	(40, '+55 81 6445-7193', '18.831.608/3434-03', 1),
	(41, '+55 61 0560 6202', '29.068.782/3837-66', 1),
	(42, '+55 71 1304-3484', '22.433.349/6540-01', 1),
	(43, '81 5483 7319', '84.540.585/3190-21', 1),
	(44, '81 4965-8670', '74.056.082/4785-02', 1),
	(45, '+55 (081) 5090-1436', '04.370.899/9570-23', 1),
	(46, '(031) 5931-2778', '56.380.407/3394-02', 1),
	(47, '+55 (011) 7318 6968', '28.422.429/2139-39', 1),
	(48, '+55 71 5251 5003', '20.802.069/5550-16', 1),
	(49, '+55 (021) 3221-5697', '41.900.454/1097-00', 1),
	(50, '61 8643 6509', '82.256.860/7907-09', 1),
	(51, '(081) 2717-0933', '54.549.266/2345-33', 1),
	(52, '(081) 3510 6428', '97.322.164/7356-14', 1),
	(53, '+55 (061) 5682 3454', '10.507.365/8503-85', 1),
	(54, '71 4871 5834', '23.856.760/7963-53', 1),
	(55, '+55 (051) 7219 5931', '89.936.340/3573-91', 1),
	(56, '+55 (031) 8040-9163', '46.825.729/5937-51', 1),
	(57, '(071) 5930 1480', '79.460.664/7483-76', 1),
	(58, '+55 41 4904-3679', '79.315.423/8747-11', 1),
	(59, '(071) 1097-8554', '01.059.020/2794-56', 1),
	(60, '+55 (031) 7739-5168', '84.428.432/7582-52', 1),
	(61, '+55 21 3240-8865', '07.293.879/9225-41', 1),
	(62, '+55 21 1804 5451', '38.973.389/4931-39', 1),
	(63, '11 6812-6966', '71.150.726/0688-96', 1),
	(64, '+55 61 4879-8462', '67.717.709/5760-50', 1),
	(65, '+55 (051) 1732-3333', '68.328.795/7689-07', 1),
	(66, '(031) 0017-4962', '60.646.070/3907-74', 1),
	(67, '(021) 2607 3380', '56.223.378/2229-42', 1),
	(68, '71 6618 9895', '59.381.457/8845-06', 1),
	(69, '+55 (071) 5006 1305', '40.075.585/7684-12', 1),
	(70, '+55 71 3999-7052', '03.600.515/0484-07', 1),
	(71, '+55 (061) 7769-7804', '44.920.432/4409-19', 1),
	(72, '81 4787-8282', '45.831.290/7823-56', 1),
	(73, '(011) 2555-3976', '16.073.821/4462-85', 1),
	(74, '+55 (061) 0433-4930', '15.932.569/3394-10', 1),
	(75, '11 3158 6677', '37.804.067/0956-37', 1),
	(76, '+55 21 6861-7846', '26.941.738/9900-23', 1),
	(77, '61 1134 5917', '01.560.639/7251-64', 1),
	(78, '+55 11 8850-4646', '95.776.695/3314-88', 1),
	(79, '(061) 1637-3384', '26.593.635/6363-56', 1),
	(80, '+55 41 8953 2741', '89.070.202/7783-94', 1),
	(81, '(081) 8340 4869', '71.328.725/7280-66', 1),
	(82, '+55 (051) 3100 7374', '05.727.536/9986-83', 1),
	(83, '+55 (071) 3257 9045', '80.074.691/8229-72', 1),
	(84, '+55 (051) 2868 2733', '90.465.421/0713-63', 1),
	(85, '+55 81 5668-5387', '02.059.648/4763-25', 1),
	(86, '+55 51 455 6349', '46.185.233/4935-45', 1),
	(87, '+55 (021) 2092 8060', '78.440.900/1662-07', 1),
	(88, '+55 (051) 4522-1052', '13.818.067/1028-53', 1),
	(89, '11 5006-2278', '45.023.221/1140-46', 1),
	(90, '+55 61 0291 0423', '76.680.896/6201-16', 1),
	(91, '+55 81 1794 8223', '06.025.833/0170-88', 1),
	(92, '+55 (061) 7889 4825', '87.896.565/7373-25', 1),
	(93, '+55 (041) 8464 8631', '38.604.625/4002-30', 1),
	(94, '+55 (011) 7091-7031', '75.946.122/5806-69', 1),
	(95, '(061) 4635-7925', '16.006.416/0092-94', 1),
	(96, '31 7361 3424', '38.275.756/6301-36', 1),
	(97, '+55 71 8942-2360', '22.923.768/6897-55', 1),
	(98, '+55 51 627 1147', '04.963.065/1999-25', 1),
	(99, '(011) 6807 1337', '46.230.735/3474-80', 1),
	(100, '61 5321 9464', '02.984.527/1287-82', 1);

	INSERT INTO CONTATO_CLIENTE VALUES
	(1, '+55 71 5177 9477', '365.728.948-86', 1),
	(2, '41 3406 9232', '192.154.940-81', 1),
	(3, '+55 41 1529 1166', '051.049.739-05', 1),
	(4, '+55 71 5282-3157', '562.175.036-54', 1),
	(5, '+55 11 9719-9745', '196.083.621-80', 1),
	(6, '(071) 4858 4764', '293.690.116-25', 1),
	(7, '+55 (021) 9097-4517', '909.320.903-54', 1),
	(8, '+55 41 5996-3170', '442.847.425-31', 1),
	(9, '21 1399-1803', '661.660.624-43', 1),
	(10, '2150 4829', '218.003.800-38', 1),
	(11, '+55 21 5192-1429', '161.591.311-41', 1),
	(12, '+55 (051) 4538-4476', '592.189.369-21', 1),
	(13, '(011) 2885 8018', '807.147.057-05', 1),
	(14, '+55 61 8847-7129', '101.923.093-23', 1),
	(15, '+55 41 8525-1430', '986.418.387-75', 1),
	(16, '21 1945-9484', '954.897.650-11', 1),
	(17, '9643 6244', '533.897.771-05', 1),
	(18, '3817-7300', '242.027.503-90', 1),
	(19, '(081) 3058 3186', '761.312.625-00', 1),
	(20, '81 2215 0542', '318.624.060-30', 1),
	(21, '(061) 0084-6338', '430.206.866-36', 1),
	(22, '+55 31 9874 0098', '428.464.848-99', 1),
	(23, '+55 (041) 6812 1528', '959.031.846-00', 1),
	(24, '+55 (071) 8224 0272', '289.081.666-45', 1),
	(25, '+55 21 7149-3242', '630.703.207-32', 1),
	(26, '51 016 8674', '710.164.760-00', 1),
	(27, '+55 (021) 4925 7099', '552.934.949-88', 1),
	(28, '+55 41 9193-9628', '944.344.086-58', 1),
	(29, '81 9527-8455', '020.879.003-96', 1),
	(30, '51 645 9351', '970.122.418-37', 1),
	(31, '+55 41 3802 2837', '636.541.312-20', 1),
	(32, '31 3285-3051', '602.150.938-28', 1),
	(33, '(061) 5251 4385', '226.968.600-41', 1),
	(34, '41 2209-1638', '517.146.035-39', 1),
	(35, '(061) 7615 7492', '897.094.953-48', 1),
	(36, '(021) 7998 5089', '193.648.568-05', 1),
	(37, '(021) 8195-1305', '208.664.918-56', 1),
	(38, '31 6991-3707', '630.507.657-04', 1),
	(39, '+55 (041) 1147-2202', '521.588.578-89', 1),
	(40, '21 1426 8783', '454.849.805-26', 1),
	(41, '(081) 5037-9756', '126.465.446-42', 1),
	(42, '41 2385-4083', '788.378.234-79', 1),
	(43, '(041) 6698-2541', '020.478.274-00', 1),
	(44, '11 9416-3493', '938.320.985-26', 1),
	(45, '(071) 9945-3408', '266.600.930-01', 1),
	(46, '21 0867-9048', '761.322.769-39', 1),
	(47, '(081) 0682 7107', '374.914.799-01', 1),
	(48, '+55 21 4646 9595', '176.489.865-66', 1),
	(49, '+55 (051) 5112 1115', '477.023.447-33', 1),
	(50, '+55 (041) 6132 9422', '261.156.571-64', 1),
	(51, '+55 51 175 9331', '174.767.513-02', 1),
	(52, '+55 61 6604 2277', '127.754.185-03', 1),
	(53, '21 9650-4662', '095.725.968-96', 1),
	(54, '(051) 7470 0119', '227.345.725-16', 1),
	(55, '+55 (051) 3139 9499', '287.649.002-15', 1),
	(56, '+55 81 2307-6504', '742.933.399-06', 1),
	(57, '(021) 2987-0632', '586.822.245-85', 1),
	(58, '1533-7468', '809.181.088-10', 1),
	(59, '+55 81 9738 0215', '485.407.175-30', 1),
	(60, '(021) 7576-6019', '035.703.579-88', 1),
	(61, '+55 (071) 8927 5608', '032.505.905-50', 1),
	(62, '11 6581 2973', '128.318.589-09', 1),
	(63, '11 9838 6534', '219.549.192-20', 1),
	(64, '+55 (041) 4429-7485', '476.119.804-40', 1),
	(65, '+55 61 2052-4560', '480.796.652-90', 1),
	(66, '+55 (021) 3239-9961', '192.283.160-39', 1),
	(67, '+55 41 8709-9872', '402.246.463-11', 1),
	(68, '+55 61 8436-8308', '901.363.990-96', 1),
	(69, '(041) 8536 5498', '298.322.674-39', 1),
	(70, '+55 81 7652-5808', '147.988.057-42', 1),
	(71, '+55 (011) 1507 8955', '191.144.047-02', 1),
	(72, '+55 51 338 9054', '338.640.851-60', 1),
	(73, '(081) 1400-9483', '774.236.197-36', 1),
	(74, '+55 (031) 2177 9748', '581.002.072-08', 1),
	(75, '71 5363-4035', '493.684.111-07', 1),
	(76, '(061) 1609-4430', '455.254.563-97', 1),
	(77, '+55 (081) 3292 6731', '274.442.369-68', 1),
	(78, '(051) 3985-5976', '559.453.538-17', 1),
	(79, '+55 (061) 7470-5752', '707.929.509-25', 1),
	(80, '+55 81 2636 3308', '682.112.737-99', 1),
	(81, '(081) 6634-4845', '493.595.641-09', 1),
	(82, '81 7428-5708', '487.832.626-36', 1),
	(83, '51 144 6585', '043.307.895-23', 1),
	(84, '(061) 3060-9424', '680.184.160-28', 1),
	(85, '+55 21 1194 7290', '136.818.661-04', 1),
	(86, '(061) 7022 0868', '543.031.325-43', 1),
	(87, '+55 51 896 2341', '905.180.103-33', 1),
	(88, '+55 (081) 2318-9899', '445.247.565-58', 1),
	(89, '(061) 7107 0752', '887.450.522-12', 1),
	(90, '(071) 8379-3132', '874.524.521-51', 1),
	(91, '(051) 1408 3454', '108.844.854-20', 1),
	(92, '+55 11 4787 2647', '995.106.177-09', 1),
	(93, '+55 21 8034-6419', '675.071.897-32', 1),
	(94, '+55 (051) 9982 8724', '954.840.995-01', 1),
	(95, '+55 (081) 5768 2700', '032.609.977-84', 1),
	(96, '21 0278 3084', '503.977.886-49', 1),
	(97, '+55 (011) 2565-3344', '576.766.726-86', 1),
	(98, '41 2609-9642', '117.291.560-10', 1),
	(99, '+55 21 3721 7159', '364.045.102-35', 1),
	(100, '41 1040-3361', '883.382.447-08', 1),
	(101, '51 809 9892', '027.480.123-05', 1),
	(102, '21 5376 9982', '569.154.071-89', 1),
	(103, '(021) 7267 1666', '682.453.539-73', 1),
	(104, '(061) 6400-6487', '608.706.384-67', 1),
	(105, '+55 (021) 4574 9878', '728.299.197-93', 1),
	(106, '(081) 6282-1851', '360.902.402-06', 1);

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
    	/* MODELO_LOGICO_SMART_SALES: */

	CREATE TABLE RAMO (
		codigo integer PRIMARY KEY,
		ramo varchar
	);

	CREATE TABLE CATEGORIA (
		codigo integer PRIMARY KEY,
		categoria varchar
	);

	CREATE TABLE MARCA (
		codigo integer PRIMARY KEY,
		marca varchar
	);

	CREATE TABLE UNIDADE (
		codigo integer PRIMARY KEY,
		unidade varchar
	);

	CREATE TABLE FORNECEDOR (
		codigo varchar PRIMARY KEY,
		nome_fantasia varchar,
		razao_social varchar,
		data_cadastro date,
		latitude varchar,
		longitude varchar,
		ramo integer
	);

	CREATE TABLE PRODUTO (
		codigo integer PRIMARY KEY,
		codigo_barras varchar,
		descricao varchar,
		preco_venda float,
		categoria integer,
		unidade integer,
		marca integer
	);

	CREATE TABLE VENDA (
		numero_nota integer PRIMARY KEY,
		data date,
		hora varchar,
		cliente varchar
	);

	CREATE TABLE CLIENTE (
		codigo varchar PRIMARY KEY,
		nome varchar,
		data_nasc date,
		data_cadastro date,
		latitude varchar,
		longitude varchar,
		sexo char
	);

	CREATE TABLE CONTATO_FORNECEDOR (
		codigo integer PRIMARY KEY,
		contato varchar,
		fornecedor varchar,
		tipo_contato integer
	);

	CREATE TABLE TIPO_CONTATO (
		codigo integer PRIMARY KEY,
		descricao varchar
	);

	CREATE TABLE CONTATO_CLIENTE (
		codigo integer PRIMARY KEY,
		contato varchar,
		cliente varchar,
		tipo_contato integer
	);

	CREATE TABLE AQUISICAO_PRODUTO (
		fornecedor varchar,
		produto integer,
		data_aquisicao date,
		hora_aquisicao varchar,
		qtd_aquisicao integer,
		preco_aquisicao float
	);

	CREATE TABLE VENDA_PRODUTO (
		numero_nota integer,
		produto integer,
		qtd float
	);
	 
	ALTER TABLE FORNECEDOR ADD CONSTRAINT FK_FORNECEDOR_2
		FOREIGN KEY (ramo)
		REFERENCES RAMO (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_2
		FOREIGN KEY (categoria)
		REFERENCES CATEGORIA (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_3
		FOREIGN KEY (unidade)
		REFERENCES UNIDADE (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_4
		FOREIGN KEY (marca)
		REFERENCES MARCA (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE VENDA ADD CONSTRAINT FK_COMPRA_2
		FOREIGN KEY (cliente)
		REFERENCES CLIENTE (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE CONTATO_FORNECEDOR ADD CONSTRAINT FK_CONTATO_FORNECEDOR_2
		FOREIGN KEY (fornecedor)
		REFERENCES FORNECEDOR (codigo)
		ON DELETE CASCADE;
	 
	ALTER TABLE CONTATO_FORNECEDOR ADD CONSTRAINT FK_CONTATO_FORNECEDOR_3
		FOREIGN KEY (tipo_contato)
		REFERENCES TIPO_CONTATO (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE CONTATO_CLIENTE ADD CONSTRAINT FK_CONTATO_CLIENTE_2
		FOREIGN KEY (cliente)
		REFERENCES CLIENTE (codigo)
		ON DELETE CASCADE;
	 
	ALTER TABLE CONTATO_CLIENTE ADD CONSTRAINT FK_CONTATO_CLIENTE_3
		FOREIGN KEY (tipo_contato)
		REFERENCES TIPO_CONTATO (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE AQUISICAO_PRODUTO ADD CONSTRAINT FK_AQUISICAO_PRODUTO_1
		FOREIGN KEY (fornecedor)
		REFERENCES FORNECEDOR (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE AQUISICAO_PRODUTO ADD CONSTRAINT FK_AQUISICAO_PRODUTO_2
		FOREIGN KEY (produto)
		REFERENCES PRODUTO (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE VENDA_PRODUTO ADD CONSTRAINT FK_COMPRA_PRODUTO_1
		FOREIGN KEY (numero_nota)
		REFERENCES VENDA (numero_nota)
		ON DELETE RESTRICT;
	 
	ALTER TABLE COMPRA_PRODUTO ADD CONSTRAINT FK_COMPRA_PRODUTO_2
		FOREIGN KEY (produto)
		REFERENCES PRODUTO (codigo)
		ON DELETE RESTRICT;

	INSERT INTO RAMO VALUES 
	(1, 'alimentos organicos');

	INSERT INTO CATEGORIA VALUES 
	(1, 'fruta'),
	(2, 'verdura'),
	(3, 'hortalica'),
	(4, 'linguica'),
	(5, 'queijo');

	INSERT INTO UNIDADE VALUES
	(1, 'kg');

	INSERT INTO MARCA VALUES
	(1, 'hortifruti'),
	(2, 'seasa');

	INSERT INTO TIPO_CONTATO VALUES
	(1, 'Telefone'),
	(2, 'E-Mail'),
	(3, 'Facebook'),
	(4, 'Twitter'),
	(5, 'Instagram'),
	(6, 'Site');

	INSERT INTO CLIENTE VALUES
	('365.728.948-86', 'Camila Pinto Alves', '1992-2-23', '2017-7-20', '-3.2125445', '-6.832034', 'F'),
	('192.154.940-81', 'Gabriela Castro da Costa', '2004-5-4', '2018-3-2', '37.0049765', '-167.999536', 'F'),
	('051.049.739-05', 'Juliana Azevedo Castro', '2002-2-9', '2018-5-8', '-13.2917825', '44.258601', 'F'),
	('562.175.036-54', 'Isabella Campos Pires', '1982-12-7', '2018-12-12', '19.2732755', '-48.844405', 'F'),
	('196.083.621-80', 'Mariane Caldeira Nogueira', '2000-11-5', '2018-3-10', '21.152234', '20.190571', 'F'),
	('293.690.116-25', 'Alana da Conceição Viana', '1947-8-1', '2016-11-20', '63.8673555', '-31.990231', 'F'),
	('909.320.903-54', 'Ana Lívia Almeida da Costa', '1962-6-16', '2017-4-15', '-2.1824555', '18.227164', 'F'),
	('442.847.425-31', 'Ana Laura da Mata Moura', '1963-11-3', '2017-12-27', '57.2975025', '-131.715842', 'F'),
	('661.660.624-43', 'Manuela Correia Ribeiro', '1956-10-10', '2018-9-28', '26.914186', '-56.445934', 'F'),
	('218.003.800-38', 'Caroline Castro da Luz', '1929-2-11', '2018-12-5', '-42.696304', '117.056578', 'F'),
	('161.591.311-41', 'Olivia da Rocha Farias', '1989-5-10', '2018-3-17', '-2.0723475', '-134.025987', 'F'),
	('592.189.369-21', 'Gabrielly Barbosa Correia', '1978-2-1', '2017-4-15', '-79.302171', '-18.346412', 'F'),
	('807.147.057-05', 'Catarina Fogaça Moreira', '1931-12-1', '2017-5-19', '-23.1273225', '148.340027', 'F'),
	('101.923.093-23', 'Isis Peixoto Araújo', '1963-12-26', '2018-6-1', '73.7187695', '66.205137', 'F'),
	('986.418.387-75', 'Maria Cecília Castro Silva', '1968-4-22', '2016-11-7', '66.8340885', '-156.163327', 'F'),
	('954.897.650-11', 'Olivia da Cunha Mendes', '1949-7-22', '2019-7-27', '-61.9986875', '-44.206946', 'F'),
	('533.897.771-05', 'Cecília Barros da Conceição', '1999-7-5', '2019-9-13', '59.532996', '147.128030', 'F'),
	('242.027.503-90', 'Nina Castro Dias', '1940-8-2', '2017-1-6', '22.5758335', '59.389895', 'F'),
	('761.312.625-00', 'Marina Rezende Almeida', '1966-10-9', '2019-8-9', '-87.845712', '54.952627', 'F'),
	('318.624.060-30', 'Mariane da Cunha Duarte', '1968-5-9', '2017-1-14', '-66.4832815', '-52.328383', 'F'),
	('430.206.866-36', 'Enzo Correia Carvalho', '1976-2-12', '2018-5-23', '-46.2587105', '49.054216', 'M'),
	('428.464.848-99', 'Enzo Lima Lima', '1939-6-18', '2018-1-17', '57.1306305', '166.209945', 'M'),
	('959.031.846-00', 'Cauê Melo Moreira', '2006-6-9', '2017-5-18', '-54.781919', '26.387546', 'M'),
	('289.081.666-45', 'João Gabriel Silveira Peixoto', '1992-7-23', '2017-9-27', '-83.9795035', '154.865067', 'M'),
	('630.703.207-32', 'Vicente Castro Azevedo', '1977-7-23', '2017-11-19', '23.573548', '-79.343364', 'M'),
	('710.164.760-00', 'Vitor Gabriel Freitas Moraes', '1992-6-8', '2018-9-27', '-39.8420775', '69.385340', 'M'),
	('552.934.949-88', 'Davi Luiz Santos Silveira', '1968-2-17', '2019-6-8', '1.982571', '176.879138', 'M'),
	('944.344.086-58', 'João Pedro Cavalcanti Silva', '1964-3-3', '2018-4-27', '50.7625935', '146.450740', 'M'),
	('020.879.003-96', 'Pedro Henrique Freitas Costela', '1980-5-21', '2018-8-18', '-79.0520905', '-172.036972', 'M'),
	('970.122.418-37', 'Daniel Freitas Araújo', '1957-7-29', '2018-11-2', '-35.3585215', '-177.939287', 'M'),
	('636.541.312-20', 'Anthony da Luz Vieira', '1955-1-23', '2017-12-2', '-85.283735', '-27.917500', 'M'),
	('602.150.938-28', 'Enzo da Cunha Cardoso', '1980-1-17', '2019-8-18', '-7.890234', '-69.768677', 'M'),
	('226.968.600-41', 'Renan Sales Lima', '1979-7-28', '2018-2-22', '-2.6822365', '149.443722', 'M'),
	('517.146.035-39', 'Nathan Viana Aragão', '1955-5-28', '2018-3-15', '86.3842065', '14.052799', 'M'),
	('897.094.953-48', 'Rodrigo Alves Gonçalves', '1981-12-27', '2018-9-4', '87.700105', '22.281184', 'M'),
	('193.648.568-05', 'Luiz Gustavo Nogueira Souza', '1929-3-23', '2019-1-3', '30.4297755', '-101.631940', 'M'),
	('208.664.918-56', 'Maria Cecília Aragão Castro', '2006-8-7', '2018-2-24', '-47.264432', '116.194005', 'F'),
	('630.507.657-04', 'Júlia Carvalho Costela', '1993-6-12', '2017-3-9', '28.686795', '4.175100', 'F'),
	('521.588.578-89', 'Isabelly Ribeiro Ferreira', '1976-4-2', '2019-9-9', '44.0687225', '-63.479234', 'F'),
	('454.849.805-26', 'Emanuelly Costa da Mota', '1997-10-2', '2017-6-8', '77.418242', '-74.991038', 'F'),
	('126.465.446-42', 'Lavínia Pinto Lopes', '1959-1-31', '2018-8-4', '-43.6772375', '3.346787', 'F'),
	('788.378.234-79', 'Valentina Nunes Nunes', '1933-7-1', '2017-3-20', '-16.126069', '-40.616331', 'F'),
	('020.478.274-00', 'Maria Vitória Lima Silva', '1995-2-25', '2018-2-9', '17.417615', '169.132909', 'F'),
	('938.320.985-26', 'Sofia Cunha Souza', '1986-12-20', '2019-3-5', '11.461169', '69.614268', 'F'),
	('266.600.930-01', 'Esther Silveira Freitas', '1950-10-5', '2018-3-20', '-70.3651705', '94.798713', 'F'),
	('761.322.769-39', 'Alana Oliveira Souza', '1961-11-3', '2018-3-1', '71.8508345', '45.850076', 'F'),
	('374.914.799-01', 'Clarice Mendes Duarte', '1955-8-13', '2017-11-11', '-58.510483', '-47.336912', 'F'),
	('176.489.865-66', 'Larissa Ramos Silva', '1982-8-31', '2017-10-17', '-70.401062', '158.061593', 'F'),
	('477.023.447-33', 'Sophia Souza Sales', '1994-10-11', '2018-1-6', '-83.3999315', '-84.402458', 'F'),
	('261.156.571-64', 'Bernardo Silva Rezende', '2003-10-20', '2017-3-31', '-10.7721285', '-4.716711', 'M'),
	('174.767.513-02', 'João Vitor Cunha da Cunha', '1958-10-25', '2019-5-28', '70.3046905', '-115.237992', 'M'),
	('127.754.185-03', 'Daniel Oliveira Moura', '1980-1-9', '2017-2-23', '-40.335424', '-142.178283', 'M'),
	('095.725.968-96', 'Isabelly Ferreira Ramos', '1955-2-1', '2019-6-14', '45.946030', '78.717733', 'F'),
	('227.345.725-16', 'Maria Cecília Fernandes Martins', '1945-12-29', '2019-9-30', '9.721010', '-158.614337', 'F'),
	('287.649.002-15', 'Manuela Pinto Vieira', '1995-9-13', '2018-12-29', '-26.357600', '60.414009', 'F'),
	('742.933.399-06', 'Ana Luiza Cunha Moraes', '1936-6-17', '2017-12-15', '27.6457345', '58.777843', 'F'),
	('586.822.245-85', 'Catarina Dias da Costa', '1952-8-19', '2017-1-28', '6.443707', '18.642783', 'F'),
	('809.181.088-10', 'Nina Souza Barros', '2001-2-27', '2018-6-20', '3.394399', '-131.593893', 'F'),
	('485.407.175-30', 'Larissa Teixeira Campos', '1995-4-9', '2018-3-18', '44.9720015', '94.873868', 'F'),
	('035.703.579-88', 'Sophia da Mata Oliveira', '1985-10-16', '2017-4-23', '-44.1153335', '28.486222', 'F'),
	('032.505.905-50', 'Emanuel Mendes Cardoso', '1951-11-23', '2018-8-2', '-33.4520555', '151.237981', 'M'),
	('128.318.589-09', 'André Barros Lopes', '1956-5-11', '2019-9-8', '-20.1194715', '-171.854721', 'M'),
	('219.549.192-20', 'Bruno das Neves Porto', '1982-8-20', '2017-5-2', '-35.795486', '33.268421', 'M'),
	('476.119.804-40', 'Camila Moura Almeida', '1999-11-16', '2018-2-7', '-60.401269', '113.404030', 'F'),
	('480.796.652-90', 'Olivia Martins das Neves', '1995-8-18', '2018-5-18', '-60.464169', '122.351432', 'F'),
	('192.283.160-39', 'Yasmin da Mata Vieira', '1956-4-30', '2018-3-20', '-52.774795', '-104.803532', 'F'),
	('402.246.463-11', 'Bruna Araújo Aragão', '1972-3-22', '2019-6-21', '-79.2028665', '8.408097', 'F'),
	('901.363.990-96', 'Nicole Nascimento Rezende', '1945-12-26', '2019-6-5', '54.4719435', '-160.119142', 'F'),
	('298.322.674-39', 'Ana Júlia da Cunha Cardoso', '1947-1-6', '2019-2-15', '43.2412495', '127.856870', 'F'),
	('147.988.057-42', 'Lara Santos Dias', '1964-8-18', '2018-6-30', '-87.666231', '-22.935573', 'F'),
	('191.144.047-02', 'Sofia Melo Carvalho', '1943-2-13', '2018-8-14', '-21.6183075', '-57.774954', 'F'),
	('338.640.851-60', 'Alana da Mota Castro', '1983-5-10', '2018-1-7', '33.3067665', '23.335813', 'F'),
	('774.236.197-36', 'Maria Julia da Costa Barros', '2005-6-17', '2018-1-7', '15.422150', '-130.713410', 'F'),
	('581.002.072-08', 'Carolina Lopes Pereira', '1995-10-3', '2018-1-25', '63.759358', '-176.727886', 'F'),
	('493.684.111-07', 'Catarina Araújo Pires', '1935-12-25', '2017-7-12', '71.4494835', '-79.609639', 'F'),
	('455.254.563-97', 'Renan Melo Duarte', '1957-2-19', '2019-2-10', '-48.442406', '-102.137918', 'M'),
	('274.442.369-68', 'João Gabriel Cardoso da Costa', '1933-9-24', '2017-12-19', '85.1178925', '-60.745044', 'M'),
	('559.453.538-17', 'Paulo Porto Sales', '1958-5-25', '2018-4-25', '34.3164595', '133.816711', 'M'),
	('707.929.509-25', 'Cauê da Mota Lima', '1975-8-14', '2018-5-9', '-13.9454365', '63.031472', 'M'),
	('682.112.737-99', 'João Felipe Vieira Gomes', '1955-1-22', '2018-12-6', '62.0004735', '6.033362', 'M'),
	('493.595.641-09', 'Kaique Souza Souza', '1949-12-13', '2019-8-6', '23.882562', '44.736021', 'M'),
	('487.832.626-36', 'Pietro Costela Nogueira', '1931-11-8', '2017-12-30', '-46.732508', '76.756211', 'M'),
	('043.307.895-23', 'Felipe Rocha da Luz', '1999-5-17', '2018-2-4', '36.428485', '42.461127', 'M'),
	('680.184.160-28', 'Pedro Pinto Vieira', '1963-5-12', '2018-9-29', '89.5599865', '146.213438', 'M'),
	('136.818.661-04', 'Nicole Pires Oliveira', '1960-5-25', '2016-11-11', '-24.498195', '155.039130', 'F'),
	('543.031.325-43', 'Clarice da Paz Pinto', '1999-12-16', '2018-10-9', '70.9449105', '160.649931', 'F'),
	('905.180.103-33', 'Sabrina Martins Silveira', '1963-12-22', '2017-10-8', '-24.4614885', '169.668815', 'F'),
	('445.247.565-58', 'Joana Santos Duarte', '1991-12-10', '2019-2-21', '-51.812271', '136.167408', 'F'),
	('887.450.522-12', 'Maitê Rocha Ferreira', '1936-1-17', '2017-3-28', '0.8280035', '151.699945', 'F'),
	('874.524.521-51', 'Leonardo Costela Souza', '1940-9-4', '2017-12-26', '-9.063991', '-89.100074', 'M'),
	('108.844.854-20', 'Enrico da Rocha Novaes', '1959-6-2', '2017-9-28', '-12.2130465', '-7.601735', 'M'),
	('995.106.177-09', 'Nicolas Rodrigues Rezende', '1975-12-15', '2018-7-27', '-77.1019865', '29.636113', 'M'),
	('675.071.897-32', 'Noah Monteiro Gonçalves', '1930-7-13', '2018-1-28', '46.320081', '161.622634', 'M'),
	('954.840.995-01', 'Thomas Gomes Dias', '1957-1-23', '2018-1-18', '58.5910055', '128.106974', 'M'),
	('032.609.977-84', 'Danilo Alves Dias', '1965-12-18', '2018-7-19', '-26.698048', '-155.975999', 'M'),
	('503.977.886-49', 'Maria Clara Melo Farias', '1961-1-23', '2017-8-9', '64.688391', '-171.278066', 'F'),
	('576.766.726-86', 'Maysa Lopes Freitas', '1986-5-10', '2016-11-2', '-73.954531', '-97.982631', 'F'),
	('117.291.560-10', 'Kamilly Nunes Porto', '1969-6-21', '2018-7-25', '-27.2996365', '-103.477064', 'F'),
	('364.045.102-35', 'Maria Cecília Melo da Rosa', '1955-3-7', '2018-3-26', '-40.4871725', '-40.055865', 'F'),
	('883.382.447-08', 'Sofia Carvalho Porto', '1970-3-1', '2018-12-10', '-59.979340', '-39.002192', 'F'),
	('027.480.123-05', 'Vitor Hugo Fernandes Pereira', '1953-3-30', '2018-6-2', '-47.783428', '-53.142469', 'M'),
	('569.154.071-89', 'Rafael Costa Ferreira', '1983-9-30', '2017-8-3', '-1.7893265', '-62.992009', 'M'),
	('682.453.539-73', 'Pedro Aragão Peixoto', '1969-9-7', '2019-2-12', '-81.503690', '-150.173959', 'M'),
	('608.706.384-67', 'Emanuel Santos Campos', '1991-1-31', '2017-10-11', '3.1137125', '118.812325', 'M'),
	('728.299.197-93', 'João Freitas Santos', '1994-10-20', '2019-5-17', '54.5469135', '-44.063632', 'M'),
	('360.902.402-06', 'Yuri Monteiro Silva', '1944-3-22', '2018-5-1', '-59.8666455', '156.396111', 'M');

	INSERT INTO FORNECEDOR VALUES
	('100.973.580-29', 'Joaquim Teixeira Viana', 'Joaquim Teixeira Viana', '2018-5-30', '-28.405890', '-76.481920', 1),
	('781.245.184-40', 'João Pedro Novaes Santos', 'João Pedro Novaes Santos', '2016-10-26', '-24.8214445', '-142.741479', 1),
	('277.315.375-87', 'Miguel da Rosa Caldeira', 'Miguel da Rosa Caldeira', '2017-2-18', '24.748410', '165.968518', 1),
	('73.146.873/6990-52', 'Souza', 'Souza', '2017-11-9', '20.824489', '171.780080', 1),
	('11.795.090/5557-17', 'Costela', 'Costela', '2016-12-19', '-34.836326', '-146.940230', 1),
	('23.937.977/1806-05', 'Ribeiro', 'Ribeiro', '2018-9-10', '-73.3419155', '-2.287984', 1),
	('88.485.809/6229-50', 'da Cruz', 'da Cruz', '2017-5-26', '24.5207145', '20.757367', 1),
	('85.543.393/1625-40', 'Nunes', 'Nunes', '2018-1-25', '27.5908205', '-51.476896', 1),
	('84.581.712/9436-05', 'Novaes - EI', 'Novaes - EI', '2018-2-21', '29.681180', '-16.758698', 1),
	('70.402.893/4672-71', 'Moura Porto S/A', 'Moura Porto S/A', '2018-7-12', '-7.353292', '71.567299', 1),
	('64.915.583/9842-36', 'da Rosa Vieira S/A', 'da Rosa Vieira S/A', '2017-9-22', '-48.316154', '127.025400', 1),
	('70.549.729/7374-26', 'Teixeira', 'Teixeira', '2018-9-2', '4.062261', '119.496281', 1),
	('07.007.581/6319-81', 'Viana - EI', 'Viana - EI', '2017-7-6', '76.121837', '83.884092', 1),
	('98.358.394/2040-72', 'Gonçalves da Costa e Filhos', 'Gonçalves da Costa e Filhos', '2018-9-8', '-11.1165055', '69.935721', 1),
	('22.323.793/8688-99', 'Costa Souza Ltda.', 'Costa Souza Ltda.', '2017-10-25', '84.617385', '28.595988', 1),
	('47.747.905/4651-53', 'Viana', 'Viana', '2018-7-8', '30.439752', '-29.390847', 1),
	('11.034.406/6331-47', 'Ramos', 'Ramos', '2017-5-21', '23.4043555', '33.167127', 1),
	('97.273.164/1628-84', 'Barros', 'Barros', '2017-2-15', '-53.006299', '24.310945', 1),
	('44.835.073/5577-69', 'Duarte', 'Duarte', '2017-5-26', '-4.8435855', '-107.718215', 1),
	('16.947.184/9819-65', 'Rezende e Filhos', 'Rezende e Filhos', '2017-11-1', '-50.186964', '-47.532575', 1),
	('98.713.604/0853-12', 'Pinto Ltda.', 'Pinto Ltda.', '2016-10-7', '-40.937135', '-56.069672', 1),
	('06.045.166/6050-10', 'Mendes', 'Mendes', '2017-12-3', '-32.957085', '25.019930', 1),
	('56.208.130/2496-06', 'Rocha', 'Rocha', '2018-6-30', '52.0351165', '45.952317', 1),
	('33.919.413/5511-97', 'Vieira', 'Vieira', '2018-7-27', '14.8096365', '-103.528867', 1),
	('11.454.766/8092-39', 'Jesus', 'Jesus', '2017-1-2', '33.5498685', '82.192621', 1),
	('73.291.809/3985-37', 'Melo Pinto S.A.', 'Melo Pinto S.A.', '2018-5-16', '39.275925', '37.795510', 1),
	('72.765.004/8577-22', 'Oliveira e Filhos', 'Oliveira e Filhos', '2017-8-23', '41.471050', '-73.908391', 1),
	('06.217.954/2750-71', 'Barbosa - EI', 'Barbosa - EI', '2016-11-6', '-40.9568685', '-148.958364', 1),
	('68.926.971/7135-98', 'da Mata Fogaça - EI', 'da Mata Fogaça - EI', '2018-4-4', '-40.1665345', '67.105077', 1),
	('07.819.576/1312-29', 'Gomes', 'Gomes', '2018-6-15', '37.6527085', '47.417166', 1),
	('53.293.511/6491-44', 'Monteiro - EI', 'Monteiro - EI', '2018-1-10', '-21.6651885', '135.704316', 1),
	('84.339.811/3490-07', 'Rodrigues - ME', 'Rodrigues - ME', '2018-8-26', '80.0460305', '-154.339867', 1),
	('97.711.726/6953-00', 'Silva', 'Silva', '2017-4-17', '-16.943651', '131.557895', 1),
	('48.328.049/2183-10', 'Pires', 'Pires', '2017-12-3', '-1.629994', '11.165089', 1),
	('64.976.849/9365-23', 'da Paz', 'da Paz', '2017-11-23', '-25.9726295', '69.408759', 1),
	('22.352.107/7239-15', 'Silveira', 'Silveira', '2017-6-10', '-84.554480', '127.833390', 1),
	('02.357.393/3970-88', 'Dias S.A.', 'Dias S.A.', '2018-8-7', '-26.498161', '-5.091408', 1),
	('05.095.078/0906-30', 'Silveira', 'Silveira', '2017-5-9', '-75.946631', '73.547627', 1),
	('38.124.301/1142-94', 'Azevedo', 'Azevedo', '2017-7-17', '-43.8474545', '116.692238', 1),
	('18.831.608/3434-03', 'da Luz', 'da Luz', '2017-10-25', '1.389946', '55.701595', 1),
	('29.068.782/3837-66', 'da Paz', 'da Paz', '2017-8-31', '-70.5488965', '-84.466929', 1),
	('22.433.349/6540-01', 'da Costa Araújo Ltda.', 'da Costa Araújo Ltda.', '2018-9-1', '79.7429655', '2.587280', 1),
	('84.540.585/3190-21', 'Rodrigues S.A.', 'Rodrigues S.A.', '2017-3-23', '-1.1823925', '13.692588', 1),
	('74.056.082/4785-02', 'Vieira', 'Vieira', '2018-5-4', '62.080437', '-60.205704', 1),
	('04.370.899/9570-23', 'da Costa', 'da Costa', '2017-9-17', '-62.5315065', '-106.088852', 1),
	('56.380.407/3394-02', 'Costa', 'Costa', '2017-2-18', '-71.636306', '39.510145', 1),
	('28.422.429/2139-39', 'Santos Ltda.', 'Santos Ltda.', '2017-8-4', '-9.8467925', '-8.178918', 1),
	('20.802.069/5550-16', 'Carvalho', 'Carvalho', '2017-6-17', '74.524222', '-176.037246', 1),
	('41.900.454/1097-00', 'Vieira Gomes - EI', 'Vieira Gomes - EI', '2017-10-26', '-87.717482', '-95.211148', 1),
	('82.256.860/7907-09', 'da Costa S/A', 'da Costa S/A', '2017-6-4', '55.967587', '11.168347', 1),
	('54.549.266/2345-33', 'Moura', 'Moura', '2017-1-27', '75.871090', '22.073282', 1),
	('97.322.164/7356-14', 'Costela Costela S/A', 'Costela Costela S/A', '2017-9-11', '23.4936105', '96.338894', 1),
	('10.507.365/8503-85', 'Barbosa - EI', 'Barbosa - EI', '2016-12-26', '6.9623735', '-120.303351', 1),
	('23.856.760/7963-53', 'das Neves S/A', 'das Neves S/A', '2018-9-20', '70.318515', '-101.649537', 1),
	('89.936.340/3573-91', 'Alves Cardoso Ltda.', 'Alves Cardoso Ltda.', '2018-4-11', '89.096701', '70.579381', 1),
	('46.825.729/5937-51', 'Oliveira', 'Oliveira', '2017-12-1', '-72.592665', '100.839343', 1),
	('79.460.664/7483-76', 'Nascimento', 'Nascimento', '2017-8-9', '-83.0463395', '-18.729988', 1),
	('79.315.423/8747-11', 'Moura da Cunha S.A.', 'Moura da Cunha S.A.', '2017-10-11', '-35.3891795', '43.638708', 1),
	('01.059.020/2794-56', 'Viana e Filhos', 'Viana e Filhos', '2018-3-21', '-77.463571', '-37.193289', 1),
	('84.428.432/7582-52', 'Souza', 'Souza', '2017-9-21', '3.3176195', '165.708562', 1),
	('07.293.879/9225-41', 'das Neves', 'das Neves', '2018-2-2', '-71.0860225', '-157.781707', 1),
	('38.973.389/4931-39', 'Novaes', 'Novaes', '2017-11-17', '-19.059097', '-31.469397', 1),
	('71.150.726/0688-96', 'da Mata da Rocha e Filhos', 'da Mata da Rocha e Filhos', '2016-12-7', '80.747045', '-59.874794', 1),
	('67.717.709/5760-50', 'Araújo', 'Araújo', '2018-9-14', '36.5540285', '92.003018', 1),
	('68.328.795/7689-07', 'Teixeira - ME', 'Teixeira - ME', '2016-10-9', '32.716640', '77.415424', 1),
	('60.646.070/3907-74', 'Almeida', 'Almeida', '2017-6-1', '80.4597665', '121.781338', 1),
	('56.223.378/2229-42', 'Porto', 'Porto', '2016-11-24', '46.711218', '-1.217147', 1),
	('59.381.457/8845-06', 'Cardoso', 'Cardoso', '2018-2-6', '-50.3070745', '6.409025', 1),
	('40.075.585/7684-12', 'Fernandes', 'Fernandes', '2018-8-22', '-28.031771', '76.542681', 1),
	('03.600.515/0484-07', 'Cardoso Ltda.', 'Cardoso Ltda.', '2018-4-16', '-15.3366615', '-116.636329', 1),
	('44.920.432/4409-19', 'Melo Fernandes e Filhos', 'Melo Fernandes e Filhos', '2017-6-3', '66.243007', '72.526255', 1),
	('45.831.290/7823-56', 'da Luz S/A', 'da Luz S/A', '2018-9-8', '71.8266625', '48.499687', 1),
	('16.073.821/4462-85', 'Peixoto', 'Peixoto', '2018-5-29', '52.8254645', '13.522729', 1),
	('15.932.569/3394-10', 'Campos', 'Campos', '2017-7-27', '-57.502358', '61.408235', 1),
	('37.804.067/0956-37', 'Alves', 'Alves', '2017-9-11', '-31.2242065', '167.746340', 1),
	('26.941.738/9900-23', 'da Cunha S/A', 'da Cunha S/A', '2017-1-6', '16.8227425', '43.028561', 1),
	('01.560.639/7251-64', 'Pires - ME', 'Pires - ME', '2017-2-21', '-18.429804', '151.940314', 1),
	('95.776.695/3314-88', 'Barros Barbosa S/A', 'Barros Barbosa S/A', '2017-4-27', '0.5498175', '-112.670959', 1),
	('26.593.635/6363-56', 'Nascimento da Luz e Filhos', 'Nascimento da Luz e Filhos', '2017-4-1', '-75.515594', '-36.139931', 1),
	('89.070.202/7783-94', 'das Neves', 'das Neves', '2017-7-7', '87.8088255', '32.706234', 1),
	('71.328.725/7280-66', 'Lima da Paz e Filhos', 'Lima da Paz e Filhos', '2018-9-13', '39.113196', '123.402485', 1),
	('05.727.536/9986-83', 'Freitas', 'Freitas', '2017-3-8', '12.0695915', '139.501385', 1),
	('80.074.691/8229-72', 'Azevedo', 'Azevedo', '2017-4-30', '67.791984', '57.251618', 1),
	('90.465.421/0713-63', 'da Paz e Filhos', 'da Paz e Filhos', '2018-4-9', '-81.630576', '77.092699', 1),
	('02.059.648/4763-25', 'Sales', 'Sales', '2016-12-28', '2.967914', '13.007912', 1),
	('46.185.233/4935-45', 'da Rosa - EI', 'da Rosa - EI', '2017-1-29', '60.068406', '68.803947', 1),
	('78.440.900/1662-07', 'Moura S/A', 'Moura S/A', '2017-4-12', '30.515030', '44.471200', 1),
	('13.818.067/1028-53', 'Santos', 'Santos', '2017-10-23', '-65.961989', '-32.097609', 1),
	('45.023.221/1140-46', 'Novaes e Filhos', 'Novaes e Filhos', '2018-1-19', '-25.393456', '-72.751802', 1),
	('76.680.896/6201-16', 'Farias S/A', 'Farias S/A', '2017-5-12', '74.581487', '-13.447003', 1),
	('06.025.833/0170-88', 'Barros Teixeira e Filhos', 'Barros Teixeira e Filhos', '2018-5-28', '1.2055495', '95.037991', 1),
	('87.896.565/7373-25', 'Cavalcanti', 'Cavalcanti', '2017-7-3', '79.5230915', '138.272764', 1),
	('38.604.625/4002-30', 'Pereira', 'Pereira', '2016-11-14', '31.9083715', '-172.291343', 1),
	('75.946.122/5806-69', 'Peixoto e Filhos', 'Peixoto e Filhos', '2017-6-1', '57.175818', '-158.153253', 1),
	('16.006.416/0092-94', 'Rocha Barbosa S.A.', 'Rocha Barbosa S.A.', '2016-12-30', '20.2758515', '11.698364', 1),
	('38.275.756/6301-36', 'Cardoso', 'Cardoso', '2017-6-19', '-41.1814925', '137.199047', 1),
	('22.923.768/6897-55', 'Lopes Caldeira - EI', 'Lopes Caldeira - EI', '2017-5-24', '-52.638824', '129.761738', 1),
	('04.963.065/1999-25', 'Moreira S/A', 'Moreira S/A', '2017-1-25', '28.8314395', '-47.631003', 1),
	('46.230.735/3474-80', 'Caldeira', 'Caldeira', '2017-2-9', '-89.7148195', '122.348545', 1),
	('02.984.527/1287-82', 'Jesus Rodrigues e Filhos', 'Jesus Rodrigues e Filhos', '2017-1-12', '31.8920235', '-82.468496', 1);

	INSERT INTO PRODUTO VALUES
	(1, '18694291', 'abacate', 4.8, 1, 1, 2),
	(2, '08451750', 'abacate avocado', 3.0, 1, 1, 2),
	(3, '60551610', 'abacaxi havaiano', 3.7, 1, 1, 2),
	(4, '92310193', 'abacaxi perol', 3.4, 1, 1, 2),
	(5, '74168705', 'ameixa branca', 10.7, 1, 1, 2),
	(6, '11469193', 'ameixa importada', 5.5, 1, 1, 2),
	(7, '63229875', 'ameixa rosa', 2.3, 1, 1, 2),
	(8, '53399250', 'antenova', 5.0, 1, 1, 2),
	(9, '05374403', 'banana catur organica', 1.1, 1, 1, 2),
	(10, '23128637', 'banana da terra', 5.3, 1, 1, 2),
	(11, '09092495', 'banana maca', 3.4, 1, 1, 2),
	(12, '00566308', 'banana prata', 4.1, 1, 1, 2),
	(13, '29578252', 'mexerica montenegra', 1.9, 1, 1, 2),
	(14, '81706020', 'mexerica morgot', 0.8, 1, 1, 2),
	(15, '02750927', 'mexerica poca', 5.6, 1, 1, 2),
	(16, '87655483', 'mexerica importada', 10.1, 1, 1, 2),
	(17, '59640936', 'caqui chocolate', 10.2, 1, 1, 2),
	(18, '20128371', 'caqui coracao', 1.2, 1, 1, 2),
	(19, '84011428', 'caqui forte', 5.8, 1, 1, 2),
	(20, '63645231', 'caqui fuyu', 7.2, 1, 1, 2),
	(21, '91237057', 'caqui importado', 7.1, 1, 1, 2),
	(22, '73203667', 'carambola', 5.3, 1, 1, 2),
	(23, '63887594', 'coco seco', 0.3, 1, 1, 2),
	(24, '93435925', 'coco', 6.1, 1, 1, 2),
	(25, '49808575', 'coco verde', 8.5, 1, 1, 2),
	(26, '69479892', 'damasco', 10.5, 1, 1, 2),
	(27, '23157095', 'fruta do conde', 1.6, 1, 1, 2),
	(28, '11637615', 'goiaba', 9.9, 1, 1, 2),
	(29, '41760161', 'granadilla silvestre', 2.6, 1, 1, 2),
	(30, '45505522', 'graviola', 6.5, 1, 1, 2),
	(31, '95282237', 'jaca', 4.9, 1, 1, 2),
	(32, '97853480', 'kiwi', 7.6, 1, 1, 2),
	(33, '96110676', 'kiwi zelandia', 6.8, 1, 1, 2),
	(34, '95456669', 'kiwi maca', 4.3, 1, 1, 2),
	(35, '69658433', 'laranja do ceu', 10.1, 1, 1, 2),
	(36, '04705802', 'laranja pera', 7.8, 1, 1, 2),
	(37, '21097737', 'laranja bahia', 10.7, 1, 1, 2),
	(38, '31907903', 'lichia', 8.8, 1, 1, 2),
	(39, '42676911', 'limao tati', 3.0, 1, 1, 2),
	(40, '44516529', 'limao persa', 4.1, 1, 1, 2),
	(41, '67039517', 'limao siciliano', 8.2, 1, 1, 2),
	(42, '99711900', 'laranja de umbigo exp', 9.6, 1, 1, 2),
	(43, '55934329', 'maca rosa', 4.9, 1, 1, 2),
	(44, '41440810', 'maca fugi', 2.6, 1, 1, 2),
	(45, '97790693', 'maca gala', 1.7, 1, 1, 2),
	(46, '37151713', 'maca argentina', 8.9, 1, 1, 2),
	(47, '91651594', 'maca verde', 6.2, 1, 1, 2),
	(48, '18180886', 'mamao formosa', 4.1, 1, 1, 2),
	(49, '83713248', 'mamao papaya golden', 5.1, 1, 1, 2),
	(50, '96539019', 'mamao papaya esp', 9.3, 1, 1, 2),
	(51, '48273374', 'manga haden', 2.6, 1, 1, 2),
	(52, '89120392', 'manga palmer', 4.4, 1, 1, 2),
	(53, '47791299', 'manga rosa', 8.4, 1, 1, 2),
	(54, '81405275', 'maracuja azedo', 8.5, 1, 1, 2),
	(55, '66694656', 'maracuja doce', 4.8, 1, 1, 2),
	(56, '05484164', 'melancia', 5.4, 1, 1, 2),
	(57, '51595968', 'melancia sem semente', 1.3, 1, 1, 2),
	(58, '82358990', 'melao cantalume', 2.4, 1, 1, 2),
	(59, '69740060', 'melao cepi', 4.5, 1, 1, 2),
	(60, '04613794', 'melao charatane', 10.5, 1, 1, 2),
	(61, '71750545', 'melao espanhol', 5.8, 1, 1, 2),
	(62, '09612266', 'melao gala', 8.1, 1, 1, 2),
	(63, '62533720', 'melao gaucho', 8.3, 1, 1, 2),
	(64, '77402691', 'melao orange', 6.6, 1, 1, 2),
	(65, '71779966', 'melao pele sapo', 1.1, 1, 1, 2),
	(66, '82139469', 'manga tommy', 7.8, 1, 1, 2),
	(67, '87438857', 'nectarina', 0.3, 1, 1, 2),
	(68, '97756620', 'nectarina importada', 7.3, 1, 1, 2),
	(69, '30970458', 'pera asiatica', 4.0, 1, 1, 2),
	(70, '94810158', 'pera damjou', 9.3, 1, 1, 2),
	(71, '70481884', 'pera importada', 3.9, 1, 1, 2),
	(72, '16631069', 'pera nacional', 7.2, 1, 1, 2),
	(73, '64064994', 'pera verde', 2.3, 1, 1, 2),
	(74, '35706182', 'pera portuguesa', 8.1, 1, 1, 2),
	(75, '96453995', 'pera williams', 9.5, 1, 1, 2),
	(76, '02425481', 'pessego amarelo', 4.3, 1, 1, 2),
	(77, '31385350', 'pessego branco', 3.0, 1, 1, 2),
	(78, '54121058', 'pessego importado especial', 3.0, 1, 1, 2),
	(79, '39628770', 'roma', 1.1, 1, 1, 2),
	(80, '55048620', 'uva bentica', 0.1, 1, 1, 2),
	(81, '28658757', 'uva brasil', 3.9, 1, 1, 2),
	(82, '02930688', 'uva importada', 7.5, 1, 1, 2),
	(83, '54537576', 'uva italiana', 4.6, 1, 1, 2),
	(84, '34719565', 'uva niagara branca', 4.1, 1, 1, 2),
	(85, '93432368', 'uva niagara rosa', 0.4, 1, 1, 2),
	(86, '05389797', 'uva red glob', 7.8, 1, 1, 2),
	(87, '19183572', 'uva rubi rosa', 4.7, 1, 1, 2),
	(88, '63924329', 'uva rubi verde', 1.0, 1, 1, 2),
	(89, '81752478', 'uva venus', 7.2, 1, 1, 2),
	(90, '50417292', 'pinhao', 1.1, 1, 1, 2),
	(91, '55271738', 'cebola branca', 7.1, 2, 1, 2),
	(92, '48268257', 'cebola roxa', 0.3, 2, 1, 2),
	(93, '62369602', 'cenoura', 8.7, 2, 1, 2),
	(94, '83867392', 'gengibre', 6.0, 2, 1, 2),
	(95, '40105918', 'tomate italiano', 9.2, 2, 1, 2),
	(96, '80382508', 'cebola branca', 8.3, 3, 1, 1),
	(97, '41218075', 'cebola roxa', 8.5, 3, 1, 1),
	(98, '39357441', 'cenoura', 9.6, 3, 1, 1),
	(99, '50155552', 'gengibre', 9.3, 3, 1, 1),
	(100, '01593921', 'tomate italiano', 7.4, 3, 1, 1);

	INSERT INTO AQUISICAO_PRODUTO VALUES
	('46.825.729/5937-51', 23, '2017-6-3', '21:18:05', 35, 5.5),
	('53.293.511/6491-44', 42, '2016-10-10', '08:07:06', 26, 1.4),
	('23.856.760/7963-53', 67, '2018-4-19', '01:48:25', 7, 1.0),
	('23.937.977/1806-05', 56, '2017-12-7', '22:51:18', 41, 6.4),
	('28.422.429/2139-39', 83, '2018-7-15', '22:44:38', 42, 2.8),
	('07.007.581/6319-81', 47, '2018-7-4', '18:40:22', 26, 4.9),
	('79.315.423/8747-11', 29, '2018-9-29', '06:24:47', 12, 6.3),
	('16.947.184/9819-65', 64, '2018-8-16', '10:38:47', 23, 5.3),
	('46.825.729/5937-51', 39, '2017-2-6', '11:59:12', 32, 5.1),
	('68.328.795/7689-07', 7, '2017-6-17', '20:01:33', 12, 4.5),
	('70.402.893/4672-71', 90, '2017-10-7', '11:15:50', 45, 0.8),
	('18.831.608/3434-03', 28, '2017-11-22', '19:10:05', 9, 3.4),
	('56.380.407/3394-02', 68, '2017-2-14', '21:44:25', 5, 2.2),
	('73.146.873/6990-52', 61, '2016-10-23', '15:09:26', 40, 0.1),
	('89.936.340/3573-91', 17, '2017-6-8', '10:09:33', 49, 3.5),
	('84.428.432/7582-52', 61, '2017-11-17', '12:01:18', 46, 7.0),
	('15.932.569/3394-10', 91, '2017-8-4', '14:24:59', 17, 4.8),
	('06.217.954/2750-71', 18, '2018-3-10', '23:33:31', 6, 6.0),
	('02.357.393/3970-88', 74, '2017-10-31', '09:40:30', 31, 0.9),
	('37.804.067/0956-37', 21, '2016-12-22', '00:36:22', 48, 3.8),
	('56.380.407/3394-02', 35, '2018-8-21', '23:13:42', 7, 5.3),
	('85.543.393/1625-40', 34, '2018-5-3', '01:23:27', 23, 4.9),
	('16.073.821/4462-85', 23, '2018-6-6', '08:19:00', 25, 5.7),
	('22.923.768/6897-55', 66, '2017-12-8', '04:59:09', 29, 1.0),
	('277.315.375-87', 20, '2017-2-27', '23:25:40', 25, 6.4),
	('46.185.233/4935-45', 52, '2017-4-10', '00:04:07', 38, 0.9),
	('70.549.729/7374-26', 12, '2017-4-5', '03:34:15', 2, 2.6),
	('56.208.130/2496-06', 38, '2017-1-11', '14:17:36', 5, 6.0),
	('781.245.184-40', 80, '2017-10-15', '03:30:00', 16, 4.5),
	('40.075.585/7684-12', 64, '2018-1-24', '02:11:33', 13, 3.4),
	('82.256.860/7907-09', 19, '2017-3-23', '17:15:57', 41, 5.2),
	('53.293.511/6491-44', 34, '2016-10-31', '00:35:41', 31, 0.5),
	('64.976.849/9365-23', 91, '2017-3-17', '02:44:01', 41, 1.5),
	('84.540.585/3190-21', 63, '2017-5-1', '22:31:32', 38, 5.1),
	('46.185.233/4935-45', 22, '2017-9-8', '11:56:06', 31, 3.7),
	('98.358.394/2040-72', 93, '2017-12-17', '12:02:02', 29, 6.5),
	('03.600.515/0484-07', 90, '2017-10-19', '15:13:20', 46, 6.7),
	('75.946.122/5806-69', 12, '2018-2-13', '08:34:45', 44, 5.4),
	('79.315.423/8747-11', 88, '2018-6-19', '15:43:51', 43, 6.7),
	('90.465.421/0713-63', 20, '2018-3-6', '19:12:29', 25, 6.3),
	('56.208.130/2496-06', 14, '2018-1-16', '16:03:28', 9, 1.2),
	('75.946.122/5806-69', 49, '2017-3-9', '09:10:39', 36, 2.4),
	('06.045.166/6050-10', 74, '2017-4-15', '13:12:01', 48, 1.1),
	('01.560.639/7251-64', 40, '2017-11-10', '15:45:00', 29, 1.4),
	('75.946.122/5806-69', 12, '2017-11-11', '22:48:26', 3, 4.1),
	('82.256.860/7907-09', 81, '2017-12-13', '03:12:32', 38, 6.0),
	('68.328.795/7689-07', 44, '2018-2-4', '20:43:06', 20, 7.0),
	('64.976.849/9365-23', 85, '2018-1-3', '01:38:58', 1, 7.0),
	('47.747.905/4651-53', 49, '2017-9-2', '19:49:00', 42, 6.2),
	('44.920.432/4409-19', 7, '2018-1-29', '11:06:50', 39, 2.3),
	('78.440.900/1662-07', 31, '2018-1-22', '05:18:40', 3, 2.7),
	('44.835.073/5577-69', 6, '2017-8-15', '02:44:44', 11, 0.9),
	('781.245.184-40', 60, '2018-8-23', '18:57:12', 23, 2.5),
	('07.293.879/9225-41', 84, '2018-5-14', '00:04:20', 16, 5.0),
	('277.315.375-87', 63, '2016-11-9', '11:39:27', 30, 5.7),
	('15.932.569/3394-10', 5, '2017-6-17', '16:01:02', 7, 5.2),
	('02.357.393/3970-88', 96, '2017-12-10', '02:08:08', 41, 6.3),
	('37.804.067/0956-37', 96, '2017-3-25', '07:18:08', 42, 3.6),
	('03.600.515/0484-07', 19, '2018-8-12', '18:03:36', 12, 2.3),
	('11.795.090/5557-17', 72, '2018-3-18', '11:26:05', 48, 1.5),
	('20.802.069/5550-16', 75, '2018-2-23', '07:08:34', 44, 4.9),
	('56.380.407/3394-02', 82, '2018-10-2', '15:32:10', 12, 1.2),
	('76.680.896/6201-16', 98, '2017-8-6', '09:32:02', 40, 0.7),
	('46.230.735/3474-80', 78, '2017-8-14', '03:02:15', 16, 6.3),
	('56.223.378/2229-42', 100, '2017-7-20', '15:52:53', 25, 1.0),
	('22.923.768/6897-55', 7, '2018-8-15', '05:29:07', 32, 3.7),
	('53.293.511/6491-44', 84, '2017-12-6', '02:08:25', 19, 5.6),
	('82.256.860/7907-09', 76, '2017-12-16', '10:50:15', 9, 4.9),
	('23.856.760/7963-53', 62, '2018-7-10', '05:23:06', 4, 3.8),
	('11.454.766/8092-39', 11, '2018-4-23', '21:16:46', 28, 4.2),
	('84.540.585/3190-21', 7, '2018-7-28', '03:33:16', 38, 5.4),
	('68.926.971/7135-98', 12, '2018-3-23', '07:58:01', 29, 3.7),
	('06.025.833/0170-88', 1, '2017-6-13', '14:17:32', 30, 0.6),
	('06.045.166/6050-10', 6, '2017-4-17', '00:48:24', 30, 4.8),
	('38.275.756/6301-36', 98, '2017-11-16', '15:10:07', 25, 3.8),
	('26.941.738/9900-23', 83, '2017-7-10', '06:18:26', 30, 5.9),
	('79.315.423/8747-11', 18, '2018-6-6', '22:16:42', 18, 1.7),
	('37.804.067/0956-37', 33, '2017-7-4', '15:24:40', 34, 0.7),
	('71.150.726/0688-96', 100, '2018-5-3', '00:59:01', 26, 3.8),
	('05.095.078/0906-30', 42, '2017-6-24', '11:56:56', 5, 4.6),
	('70.549.729/7374-26', 53, '2017-11-25', '10:17:56', 38, 4.1),
	('01.560.639/7251-64', 64, '2018-1-30', '11:43:19', 40, 0.8),
	('26.593.635/6363-56', 82, '2017-11-24', '22:23:57', 39, 2.7),
	('44.920.432/4409-19', 69, '2017-12-19', '06:05:28', 40, 6.0),
	('06.025.833/0170-88', 50, '2017-9-16', '05:29:21', 35, 4.9),
	('02.059.648/4763-25', 33, '2017-3-2', '09:58:55', 1, 4.2),
	('90.465.421/0713-63', 57, '2018-5-10', '19:54:00', 20, 1.5),
	('48.328.049/2183-10', 53, '2018-9-3', '12:09:52', 25, 5.2),
	('67.717.709/5760-50', 32, '2017-2-21', '22:51:33', 13, 0.8),
	('71.328.725/7280-66', 75, '2017-1-23', '14:50:07', 29, 6.7),
	('15.932.569/3394-10', 23, '2017-1-16', '20:22:49', 13, 4.6),
	('22.323.793/8688-99', 15, '2017-7-2', '10:14:38', 41, 6.7),
	('11.034.406/6331-47', 11, '2018-6-4', '00:16:54', 37, 3.8),
	('781.245.184-40', 88, '2018-1-12', '01:39:12', 49, 1.8),
	('02.984.527/1287-82', 9, '2016-10-30', '13:44:47', 28, 2.2),
	('97.711.726/6953-00', 66, '2017-11-14', '07:49:21', 2, 5.0),
	('33.919.413/5511-97', 76, '2018-6-9', '21:50:53', 14, 5.5),
	('78.440.900/1662-07', 14, '2017-8-12', '23:26:21', 3, 6.4),
	('64.976.849/9365-23', 72, '2018-2-3', '19:10:28', 23, 2.6),
	('04.370.899/9570-23', 33, '2018-4-27', '07:23:48', 27, 4.6);

	INSERT INTO VENDA VALUES
	(1, '2018-8-17', '00:04:23', '503.977.886-49'),
	(2, '2017-10-30', '18:16:37', '543.031.325-43'),
	(3, '2018-5-16', '17:27:55', '192.283.160-39'),
	(4, '2017-5-4', '01:28:05', '938.320.985-26'),
	(5, '2018-8-17', '02:04:29', '360.902.402-06'),
	(6, '2016-11-22', '15:42:35', '995.106.177-09'),
	(7, '2017-3-23', '00:59:44', '480.796.652-90'),
	(8, '2016-11-4', '16:17:01', '487.832.626-36'),
	(9, '2017-11-9', '14:11:18', '586.822.245-85'),
	(10, '2017-7-14', '12:10:06', '493.684.111-07'),
	(11, '2017-8-7', '21:47:08', '970.122.418-37'),
	(12, '2016-12-22', '07:07:50', '959.031.846-00'),
	(13, '2017-9-26', '07:10:46', '543.031.325-43'),
	(14, '2017-11-7', '19:19:28', '493.684.111-07'),
	(15, '2017-5-13', '01:39:24', '675.071.897-32'),
	(16, '2017-3-27', '09:08:51', '581.002.072-08'),
	(17, '2017-6-25', '21:03:29', '959.031.846-00'),
	(18, '2018-4-28', '15:25:02', '402.246.463-11'),
	(19, '2017-12-13', '21:47:04', '774.236.197-36'),
	(20, '2018-1-10', '11:49:52', '218.003.800-38'),
	(21, '2018-5-17', '06:46:25', '289.081.666-45'),
	(22, '2017-9-5', '03:51:30', '874.524.521-51'),
	(23, '2018-7-20', '00:58:16', '298.322.674-39'),
	(24, '2017-1-28', '02:14:38', '051.049.739-05'),
	(25, '2017-8-10', '08:53:50', '592.189.369-21'),
	(26, '2018-4-3', '13:18:01', '128.318.589-09'),
	(27, '2018-2-25', '08:57:56', '293.690.116-25'),
	(28, '2017-10-7', '02:00:03', '360.902.402-06'),
	(29, '2018-1-30', '23:39:55', '117.291.560-10'),
	(30, '2017-10-25', '05:40:43', '477.023.447-33'),
	(31, '2018-2-3', '05:07:37', '476.119.804-40'),
	(32, '2017-3-5', '01:56:18', '543.031.325-43'),
	(33, '2018-1-14', '13:27:13', '117.291.560-10'),
	(34, '2017-12-3', '21:12:39', '995.106.177-09'),
	(35, '2017-1-27', '00:03:19', '581.002.072-08'),
	(36, '2018-7-4', '07:43:50', '986.418.387-75'),
	(37, '2018-2-8', '15:03:10', '289.081.666-45'),
	(38, '2017-5-2', '19:04:16', '883.382.447-08'),
	(39, '2017-12-19', '18:50:51', '208.664.918-56'),
	(40, '2016-11-7', '23:49:10', '874.524.521-51'),
	(41, '2017-8-24', '06:13:22', '477.023.447-33'),
	(42, '2017-2-26', '16:21:54', '887.450.522-12'),
	(43, '2018-7-4', '09:53:20', '569.154.071-89'),
	(44, '2016-10-20', '17:25:45', '883.382.447-08'),
	(45, '2017-3-12', '10:07:14', '208.664.918-56'),
	(46, '2017-8-21', '06:22:19', '809.181.088-10'),
	(47, '2017-4-24', '07:04:19', '742.933.399-06'),
	(48, '2017-9-9', '12:35:57', '901.363.990-96'),
	(49, '2018-2-27', '18:39:31', '521.588.578-89'),
	(50, '2018-3-20', '12:34:47', '293.690.116-25'),
	(51, '2018-1-3', '08:09:23', '108.844.854-20'),
	(52, '2017-8-8', '21:21:38', '562.175.036-54'),
	(53, '2017-1-3', '18:02:48', '442.847.425-31'),
	(54, '2017-3-23', '03:24:19', '227.345.725-16'),
	(55, '2018-7-1', '09:40:20', '261.156.571-64'),
	(56, '2018-4-6', '20:42:44', '680.184.160-28'),
	(57, '2017-7-9', '22:22:33', '742.933.399-06'),
	(58, '2017-11-28', '18:45:20', '480.796.652-90'),
	(59, '2017-5-2', '16:43:25', '675.071.897-32'),
	(60, '2018-2-24', '21:41:50', '298.322.674-39'),
	(61, '2017-4-24', '00:30:42', '493.684.111-07'),
	(62, '2016-12-10', '05:34:09', '728.299.197-93'),
	(63, '2018-2-25', '18:48:54', '636.541.312-20'),
	(64, '2018-1-8', '05:07:52', '043.307.895-23'),
	(65, '2018-8-29', '22:39:23', '428.464.848-99'),
	(66, '2018-4-19', '04:58:54', '176.489.865-66'),
	(67, '2018-4-14', '05:13:11', '680.184.160-28'),
	(68, '2017-5-28', '08:33:23', '476.119.804-40'),
	(69, '2017-8-22', '03:37:04', '897.094.953-48'),
	(70, '2017-9-26', '14:00:08', '191.144.047-02'),
	(71, '2017-3-30', '18:32:13', '364.045.102-35'),
	(72, '2016-11-10', '20:42:18', '487.832.626-36'),
	(73, '2017-9-1', '00:53:59', '051.049.739-05'),
	(74, '2017-1-18', '00:42:36', '901.363.990-96'),
	(75, '2016-10-21', '15:44:16', '360.902.402-06'),
	(76, '2017-7-16', '02:47:46', '938.320.985-26'),
	(77, '2018-6-18', '21:15:42', '442.847.425-31'),
	(78, '2017-5-31', '22:18:45', '027.480.123-05'),
	(79, '2018-4-3', '08:27:23', '455.254.563-97'),
	(80, '2018-9-19', '20:48:11', '455.254.563-97'),
	(81, '2018-10-3', '00:12:47', '909.320.903-54'),
	(82, '2017-1-27', '13:31:55', '095.725.968-96'),
	(83, '2017-7-31', '05:55:40', '218.003.800-38'),
	(84, '2017-10-30', '04:46:42', '559.453.538-17'),
	(85, '2017-2-15', '04:09:34', '402.246.463-11'),
	(86, '2017-11-22', '16:48:52', '682.453.539-73'),
	(87, '2018-10-2', '04:05:57', '602.150.938-28'),
	(88, '2017-11-14', '02:28:48', '682.453.539-73'),
	(89, '2018-9-11', '08:29:08', '126.465.446-42'),
	(90, '2017-3-8', '04:21:00', '970.122.418-37'),
	(91, '2018-8-5', '15:02:22', '675.071.897-32'),
	(92, '2018-9-21', '12:42:35', '682.112.737-99'),
	(93, '2018-6-16', '21:37:09', '193.648.568-05'),
	(94, '2016-11-23', '05:30:50', '901.363.990-96'),
	(95, '2018-3-30', '17:06:36', '176.489.865-66'),
	(96, '2016-11-12', '23:49:12', '477.023.447-33'),
	(97, '2017-1-10', '12:32:46', '020.879.003-96'),
	(98, '2018-5-29', '08:12:54', '897.094.953-48'),
	(99, '2018-8-6', '12:49:00', '274.442.369-68'),
	(100, '2017-5-30', '00:30:10', '218.003.800-38');

	INSERT INTO VENDA_PRODUTO VALUES
	(62, 4, 2.4),
	(64, 24, 1.2),
	(14, 42, 1.1),
	(5, 96, 0.5),
	(41, 53, 0.9),
	(22, 58, 1.5),
	(68, 98, 1.4),
	(71, 70, 2.0),
	(67, 76, 0.7),
	(11, 83, 2.4),
	(35, 38, 0.1),
	(5, 74, 2.2),
	(64, 19, 1.3),
	(33, 66, 1.0),
	(71, 97, 1.2),
	(91, 41, 1.2),
	(92, 25, 1.4),
	(48, 92, 1.7),
	(38, 10, 0.1),
	(88, 16, 0.3),
	(80, 14, 1.2),
	(29, 83, 0.2),
	(30, 89, 2.9),
	(61, 64, 1.8),
	(45, 60, 2.2),
	(54, 25, 0.6),
	(77, 12, 0.8),
	(77, 77, 2.8),
	(56, 55, 1.8),
	(87, 72, 2.0),
	(61, 94, 3.0),
	(6, 35, 1.7),
	(11, 32, 0.9),
	(53, 45, 1.9),
	(35, 60, 3.0),
	(76, 69, 0.7),
	(99, 50, 0.1),
	(93, 91, 0.6),
	(90, 26, 2.6),
	(87, 39, 0.6),
	(78, 38, 2.4),
	(92, 28, 1.3),
	(45, 66, 2.8),
	(54, 76, 2.2),
	(63, 38, 1.3),
	(77, 77, 1.9),
	(37, 93, 0.2),
	(59, 35, 2.8),
	(50, 95, 1.4),
	(90, 96, 1.4);

	INSERT INTO CONTATO_FORNECEDOR VALUES
	(1, '+55 (021) 4491 2934', '100.973.580-29', 1),
	(2, '+55 (021) 4371-0909', '781.245.184-40', 1),
	(3, '41 5722 7881', '277.315.375-87', 1),
	(4, '+55 11 4649-3727', '73.146.873/6990-52', 1),
	(5, '61 2791-5451', '11.795.090/5557-17', 1),
	(6, '+55 (071) 8173 0422', '23.937.977/1806-05', 1),
	(7, '(051) 5092-1815', '88.485.809/6229-50', 1),
	(8, '31 4417 1366', '85.543.393/1625-40', 1),
	(9, '+55 (031) 5010 5669', '84.581.712/9436-05', 1),
	(10, '+55 21 5381-3676', '70.402.893/4672-71', 1),
	(11, '51 129 1034', '64.915.583/9842-36', 1),
	(12, '21 7926-3434', '70.549.729/7374-26', 1),
	(13, '+55 51 662 2380', '07.007.581/6319-81', 1),
	(14, '21 4921-6618', '98.358.394/2040-72', 1),
	(15, '(071) 4873-3627', '22.323.793/8688-99', 1),
	(16, '+55 (031) 8386-1635', '47.747.905/4651-53', 1),
	(17, '(051) 7137-2265', '11.034.406/6331-47', 1),
	(18, '+55 (011) 3703 0376', '97.273.164/1628-84', 1),
	(19, '(051) 8891-1304', '44.835.073/5577-69', 1),
	(20, '+55 (041) 1940-9309', '16.947.184/9819-65', 1),
	(21, '(041) 3791 7864', '98.713.604/0853-12', 1),
	(22, '61 2330 3197', '06.045.166/6050-10', 1),
	(23, '+55 (061) 2435 9874', '56.208.130/2496-06', 1),
	(24, '31 3181 4508', '33.919.413/5511-97', 1),
	(25, '+55 51 715 5831', '11.454.766/8092-39', 1),
	(26, '+55 31 5928-7429', '73.291.809/3985-37', 1),
	(27, '31 9907-7022', '72.765.004/8577-22', 1),
	(28, '81 2590 0466', '06.217.954/2750-71', 1),
	(29, '+55 (081) 3146 0810', '68.926.971/7135-98', 1),
	(30, '(011) 6855 0724', '07.819.576/1312-29', 1),
	(31, '71 5920-4276', '53.293.511/6491-44', 1),
	(32, '81 9929-9929', '84.339.811/3490-07', 1),
	(33, '11 0012-7426', '97.711.726/6953-00', 1),
	(34, '51 095 8954', '48.328.049/2183-10', 1),
	(35, '+55 (031) 9560 8306', '64.976.849/9365-23', 1),
	(36, '41 1826-6911', '22.352.107/7239-15', 1),
	(37, '81 0411-4899', '02.357.393/3970-88', 1),
	(38, '+55 11 9620 0593', '05.095.078/0906-30', 1),
	(39, '31 8675 6694', '38.124.301/1142-94', 1),
	(40, '+55 81 6445-7193', '18.831.608/3434-03', 1),
	(41, '+55 61 0560 6202', '29.068.782/3837-66', 1),
	(42, '+55 71 1304-3484', '22.433.349/6540-01', 1),
	(43, '81 5483 7319', '84.540.585/3190-21', 1),
	(44, '81 4965-8670', '74.056.082/4785-02', 1),
	(45, '+55 (081) 5090-1436', '04.370.899/9570-23', 1),
	(46, '(031) 5931-2778', '56.380.407/3394-02', 1),
	(47, '+55 (011) 7318 6968', '28.422.429/2139-39', 1),
	(48, '+55 71 5251 5003', '20.802.069/5550-16', 1),
	(49, '+55 (021) 3221-5697', '41.900.454/1097-00', 1),
	(50, '61 8643 6509', '82.256.860/7907-09', 1),
	(51, '(081) 2717-0933', '54.549.266/2345-33', 1),
	(52, '(081) 3510 6428', '97.322.164/7356-14', 1),
	(53, '+55 (061) 5682 3454', '10.507.365/8503-85', 1),
	(54, '71 4871 5834', '23.856.760/7963-53', 1),
	(55, '+55 (051) 7219 5931', '89.936.340/3573-91', 1),
	(56, '+55 (031) 8040-9163', '46.825.729/5937-51', 1),
	(57, '(071) 5930 1480', '79.460.664/7483-76', 1),
	(58, '+55 41 4904-3679', '79.315.423/8747-11', 1),
	(59, '(071) 1097-8554', '01.059.020/2794-56', 1),
	(60, '+55 (031) 7739-5168', '84.428.432/7582-52', 1),
	(61, '+55 21 3240-8865', '07.293.879/9225-41', 1),
	(62, '+55 21 1804 5451', '38.973.389/4931-39', 1),
	(63, '11 6812-6966', '71.150.726/0688-96', 1),
	(64, '+55 61 4879-8462', '67.717.709/5760-50', 1),
	(65, '+55 (051) 1732-3333', '68.328.795/7689-07', 1),
	(66, '(031) 0017-4962', '60.646.070/3907-74', 1),
	(67, '(021) 2607 3380', '56.223.378/2229-42', 1),
	(68, '71 6618 9895', '59.381.457/8845-06', 1),
	(69, '+55 (071) 5006 1305', '40.075.585/7684-12', 1),
	(70, '+55 71 3999-7052', '03.600.515/0484-07', 1),
	(71, '+55 (061) 7769-7804', '44.920.432/4409-19', 1),
	(72, '81 4787-8282', '45.831.290/7823-56', 1),
	(73, '(011) 2555-3976', '16.073.821/4462-85', 1),
	(74, '+55 (061) 0433-4930', '15.932.569/3394-10', 1),
	(75, '11 3158 6677', '37.804.067/0956-37', 1),
	(76, '+55 21 6861-7846', '26.941.738/9900-23', 1),
	(77, '61 1134 5917', '01.560.639/7251-64', 1),
	(78, '+55 11 8850-4646', '95.776.695/3314-88', 1),
	(79, '(061) 1637-3384', '26.593.635/6363-56', 1),
	(80, '+55 41 8953 2741', '89.070.202/7783-94', 1),
	(81, '(081) 8340 4869', '71.328.725/7280-66', 1),
	(82, '+55 (051) 3100 7374', '05.727.536/9986-83', 1),
	(83, '+55 (071) 3257 9045', '80.074.691/8229-72', 1),
	(84, '+55 (051) 2868 2733', '90.465.421/0713-63', 1),
	(85, '+55 81 5668-5387', '02.059.648/4763-25', 1),
	(86, '+55 51 455 6349', '46.185.233/4935-45', 1),
	(87, '+55 (021) 2092 8060', '78.440.900/1662-07', 1),
	(88, '+55 (051) 4522-1052', '13.818.067/1028-53', 1),
	(89, '11 5006-2278', '45.023.221/1140-46', 1),
	(90, '+55 61 0291 0423', '76.680.896/6201-16', 1),
	(91, '+55 81 1794 8223', '06.025.833/0170-88', 1),
	(92, '+55 (061) 7889 4825', '87.896.565/7373-25', 1),
	(93, '+55 (041) 8464 8631', '38.604.625/4002-30', 1),
	(94, '+55 (011) 7091-7031', '75.946.122/5806-69', 1),
	(95, '(061) 4635-7925', '16.006.416/0092-94', 1),
	(96, '31 7361 3424', '38.275.756/6301-36', 1),
	(97, '+55 71 8942-2360', '22.923.768/6897-55', 1),
	(98, '+55 51 627 1147', '04.963.065/1999-25', 1),
	(99, '(011) 6807 1337', '46.230.735/3474-80', 1),
	(100, '61 5321 9464', '02.984.527/1287-82', 1);

	INSERT INTO CONTATO_CLIENTE VALUES
	(1, '+55 71 5177 9477', '365.728.948-86', 1),
	(2, '41 3406 9232', '192.154.940-81', 1),
	(3, '+55 41 1529 1166', '051.049.739-05', 1),
	(4, '+55 71 5282-3157', '562.175.036-54', 1),
	(5, '+55 11 9719-9745', '196.083.621-80', 1),
	(6, '(071) 4858 4764', '293.690.116-25', 1),
	(7, '+55 (021) 9097-4517', '909.320.903-54', 1),
	(8, '+55 41 5996-3170', '442.847.425-31', 1),
	(9, '21 1399-1803', '661.660.624-43', 1),
	(10, '2150 4829', '218.003.800-38', 1),
	(11, '+55 21 5192-1429', '161.591.311-41', 1),
	(12, '+55 (051) 4538-4476', '592.189.369-21', 1),
	(13, '(011) 2885 8018', '807.147.057-05', 1),
	(14, '+55 61 8847-7129', '101.923.093-23', 1),
	(15, '+55 41 8525-1430', '986.418.387-75', 1),
	(16, '21 1945-9484', '954.897.650-11', 1),
	(17, '9643 6244', '533.897.771-05', 1),
	(18, '3817-7300', '242.027.503-90', 1),
	(19, '(081) 3058 3186', '761.312.625-00', 1),
	(20, '81 2215 0542', '318.624.060-30', 1),
	(21, '(061) 0084-6338', '430.206.866-36', 1),
	(22, '+55 31 9874 0098', '428.464.848-99', 1),
	(23, '+55 (041) 6812 1528', '959.031.846-00', 1),
	(24, '+55 (071) 8224 0272', '289.081.666-45', 1),
	(25, '+55 21 7149-3242', '630.703.207-32', 1),
	(26, '51 016 8674', '710.164.760-00', 1),
	(27, '+55 (021) 4925 7099', '552.934.949-88', 1),
	(28, '+55 41 9193-9628', '944.344.086-58', 1),
	(29, '81 9527-8455', '020.879.003-96', 1),
	(30, '51 645 9351', '970.122.418-37', 1),
	(31, '+55 41 3802 2837', '636.541.312-20', 1),
	(32, '31 3285-3051', '602.150.938-28', 1),
	(33, '(061) 5251 4385', '226.968.600-41', 1),
	(34, '41 2209-1638', '517.146.035-39', 1),
	(35, '(061) 7615 7492', '897.094.953-48', 1),
	(36, '(021) 7998 5089', '193.648.568-05', 1),
	(37, '(021) 8195-1305', '208.664.918-56', 1),
	(38, '31 6991-3707', '630.507.657-04', 1),
	(39, '+55 (041) 1147-2202', '521.588.578-89', 1),
	(40, '21 1426 8783', '454.849.805-26', 1),
	(41, '(081) 5037-9756', '126.465.446-42', 1),
	(42, '41 2385-4083', '788.378.234-79', 1),
	(43, '(041) 6698-2541', '020.478.274-00', 1),
	(44, '11 9416-3493', '938.320.985-26', 1),
	(45, '(071) 9945-3408', '266.600.930-01', 1),
	(46, '21 0867-9048', '761.322.769-39', 1),
	(47, '(081) 0682 7107', '374.914.799-01', 1),
	(48, '+55 21 4646 9595', '176.489.865-66', 1),
	(49, '+55 (051) 5112 1115', '477.023.447-33', 1),
	(50, '+55 (041) 6132 9422', '261.156.571-64', 1),
	(51, '+55 51 175 9331', '174.767.513-02', 1),
	(52, '+55 61 6604 2277', '127.754.185-03', 1),
	(53, '21 9650-4662', '095.725.968-96', 1),
	(54, '(051) 7470 0119', '227.345.725-16', 1),
	(55, '+55 (051) 3139 9499', '287.649.002-15', 1),
	(56, '+55 81 2307-6504', '742.933.399-06', 1),
	(57, '(021) 2987-0632', '586.822.245-85', 1),
	(58, '1533-7468', '809.181.088-10', 1),
	(59, '+55 81 9738 0215', '485.407.175-30', 1),
	(60, '(021) 7576-6019', '035.703.579-88', 1),
	(61, '+55 (071) 8927 5608', '032.505.905-50', 1),
	(62, '11 6581 2973', '128.318.589-09', 1),
	(63, '11 9838 6534', '219.549.192-20', 1),
	(64, '+55 (041) 4429-7485', '476.119.804-40', 1),
	(65, '+55 61 2052-4560', '480.796.652-90', 1),
	(66, '+55 (021) 3239-9961', '192.283.160-39', 1),
	(67, '+55 41 8709-9872', '402.246.463-11', 1),
	(68, '+55 61 8436-8308', '901.363.990-96', 1),
	(69, '(041) 8536 5498', '298.322.674-39', 1),
	(70, '+55 81 7652-5808', '147.988.057-42', 1),
	(71, '+55 (011) 1507 8955', '191.144.047-02', 1),
	(72, '+55 51 338 9054', '338.640.851-60', 1),
	(73, '(081) 1400-9483', '774.236.197-36', 1),
	(74, '+55 (031) 2177 9748', '581.002.072-08', 1),
	(75, '71 5363-4035', '493.684.111-07', 1),
	(76, '(061) 1609-4430', '455.254.563-97', 1),
	(77, '+55 (081) 3292 6731', '274.442.369-68', 1),
	(78, '(051) 3985-5976', '559.453.538-17', 1),
	(79, '+55 (061) 7470-5752', '707.929.509-25', 1),
	(80, '+55 81 2636 3308', '682.112.737-99', 1),
	(81, '(081) 6634-4845', '493.595.641-09', 1),
	(82, '81 7428-5708', '487.832.626-36', 1),
	(83, '51 144 6585', '043.307.895-23', 1),
	(84, '(061) 3060-9424', '680.184.160-28', 1),
	(85, '+55 21 1194 7290', '136.818.661-04', 1),
	(86, '(061) 7022 0868', '543.031.325-43', 1),
	(87, '+55 51 896 2341', '905.180.103-33', 1),
	(88, '+55 (081) 2318-9899', '445.247.565-58', 1),
	(89, '(061) 7107 0752', '887.450.522-12', 1),
	(90, '(071) 8379-3132', '874.524.521-51', 1),
	(91, '(051) 1408 3454', '108.844.854-20', 1),
	(92, '+55 11 4787 2647', '995.106.177-09', 1),
	(93, '+55 21 8034-6419', '675.071.897-32', 1),
	(94, '+55 (051) 9982 8724', '954.840.995-01', 1),
	(95, '+55 (081) 5768 2700', '032.609.977-84', 1),
	(96, '21 0278 3084', '503.977.886-49', 1),
	(97, '+55 (011) 2565-3344', '576.766.726-86', 1),
	(98, '41 2609-9642', '117.291.560-10', 1),
	(99, '+55 21 3721 7159', '364.045.102-35', 1),
	(100, '41 1040-3361', '883.382.447-08', 1),
	(101, '51 809 9892', '027.480.123-05', 1),
	(102, '21 5376 9982', '569.154.071-89', 1),
	(103, '(021) 7267 1666', '682.453.539-73', 1),
	(104, '(061) 6400-6487', '608.706.384-67', 1),
	(105, '+55 (021) 4574 9878', '728.299.197-93', 1),
	(106, '(081) 6282-1851', '360.902.402-06', 1);

#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        DROP TABLE IF EXISTS VENDA_PRODUTO;
	DROP TABLE IF EXISTS AQUISICAO_PRODUTO;
	DROP TABLE IF EXISTS VENDA;
	DROP TABLE IF EXISTS CONTATO_CLIENTE;
	DROP TABLE IF EXISTS CLIENTE;
	DROP TABLE IF EXISTS PRODUTO;
	DROP TABLE IF EXISTS CATEGORIA;
	DROP TABLE IF EXISTS UNIDADE;
	DROP TABLE IF EXISTS MARCA;
	DROP TABLE IF EXISTS CONTATO_FORNECEDOR;
	DROP TABLE IF EXISTS FORNECEDOR;
	DROP TABLE IF EXISTS RAMO;
	DROP TABLE IF EXISTS TIPO_CONTATO;

	/* MODELO_LOGICO_SMART_SALES: */

	CREATE TABLE RAMO (
		codigo integer PRIMARY KEY,
		ramo varchar
	);

	CREATE TABLE CATEGORIA (
		codigo integer PRIMARY KEY,
		categoria varchar
	);

	CREATE TABLE MARCA (
		codigo integer PRIMARY KEY,
		marca varchar
	);

	CREATE TABLE UNIDADE (
		codigo integer PRIMARY KEY,
		unidade varchar
	);

	CREATE TABLE FORNECEDOR (
		codigo varchar PRIMARY KEY,
		nome_fantasia varchar,
		razao_social varchar,
		data_cadastro date,
		latitude varchar,
		longitude varchar,
		ramo integer
	);

	CREATE TABLE PRODUTO (
		codigo integer PRIMARY KEY,
		codigo_barras varchar,
		descricao varchar,
		preco_venda float,
		categoria integer,
		unidade integer,
		marca integer
	);

	CREATE TABLE VENDA (
		numero_nota integer PRIMARY KEY,
		data date,
		hora varchar,
		cliente varchar
	);

	CREATE TABLE CLIENTE (
		codigo varchar PRIMARY KEY,
		nome varchar,
		data_nasc date,
		data_cadastro date,
		latitude varchar,
		longitude varchar,
		sexo char
	);

	CREATE TABLE CONTATO_FORNECEDOR (
		codigo integer PRIMARY KEY,
		contato varchar,
		fornecedor varchar,
		tipo_contato integer
	);

	CREATE TABLE TIPO_CONTATO (
		codigo integer PRIMARY KEY,
		descricao varchar
	);

	CREATE TABLE CONTATO_CLIENTE (
		codigo integer PRIMARY KEY,
		contato varchar,
		cliente varchar,
		tipo_contato integer
	);

	CREATE TABLE AQUISICAO_PRODUTO (
		fornecedor varchar,
		produto integer,
		data_aquisicao date,
		hora_aquisicao varchar,
		qtd_aquisicao integer,
		preco_aquisicao float
	);

	CREATE TABLE VENDA_PRODUTO (
		numero_nota integer,
		produto integer,
		qtd float
	);
	 
	ALTER TABLE FORNECEDOR ADD CONSTRAINT FK_FORNECEDOR_2
		FOREIGN KEY (ramo)
		REFERENCES RAMO (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_2
		FOREIGN KEY (categoria)
		REFERENCES CATEGORIA (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_3
		FOREIGN KEY (unidade)
		REFERENCES UNIDADE (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_4
		FOREIGN KEY (marca)
		REFERENCES MARCA (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE VENDA ADD CONSTRAINT FK_COMPRA_2
		FOREIGN KEY (cliente)
		REFERENCES CLIENTE (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE CONTATO_FORNECEDOR ADD CONSTRAINT FK_CONTATO_FORNECEDOR_2
		FOREIGN KEY (fornecedor)
		REFERENCES FORNECEDOR (codigo)
		ON DELETE CASCADE;
	 
	ALTER TABLE CONTATO_FORNECEDOR ADD CONSTRAINT FK_CONTATO_FORNECEDOR_3
		FOREIGN KEY (tipo_contato)
		REFERENCES TIPO_CONTATO (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE CONTATO_CLIENTE ADD CONSTRAINT FK_CONTATO_CLIENTE_2
		FOREIGN KEY (cliente)
		REFERENCES CLIENTE (codigo)
		ON DELETE CASCADE;
	 
	ALTER TABLE CONTATO_CLIENTE ADD CONSTRAINT FK_CONTATO_CLIENTE_3
		FOREIGN KEY (tipo_contato)
		REFERENCES TIPO_CONTATO (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE AQUISICAO_PRODUTO ADD CONSTRAINT FK_AQUISICAO_PRODUTO_1
		FOREIGN KEY (fornecedor)
		REFERENCES FORNECEDOR (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE AQUISICAO_PRODUTO ADD CONSTRAINT FK_AQUISICAO_PRODUTO_2
		FOREIGN KEY (produto)
		REFERENCES PRODUTO (codigo)
		ON DELETE RESTRICT;
	 
	ALTER TABLE VENDA_PRODUTO ADD CONSTRAINT FK_COMPRA_PRODUTO_1
		FOREIGN KEY (numero_nota)
		REFERENCES VENDA (numero_nota)
		ON DELETE RESTRICT;
	 
	ALTER TABLE VENDA_PRODUTO ADD CONSTRAINT FK_COMPRA_PRODUTO_2
		FOREIGN KEY (produto)
		REFERENCES PRODUTO (codigo)
		ON DELETE RESTRICT;

	INSERT INTO RAMO VALUES 
	(1, 'alimentos organicos');

	INSERT INTO CATEGORIA VALUES 
	(1, 'fruta'),
	(2, 'verdura'),
	(3, 'hortalica'),
	(4, 'linguica'),
	(5, 'queijo');

	INSERT INTO UNIDADE VALUES
	(1, 'kg');

	INSERT INTO MARCA VALUES
	(1, 'hortifruti'),
	(2, 'seasa');

	INSERT INTO TIPO_CONTATO VALUES
	(1, 'Telefone'),
	(2, 'E-Mail'),
	(3, 'Facebook'),
	(4, 'Twitter'),
	(5, 'Instagram'),
	(6, 'Site');

	INSERT INTO CLIENTE VALUES
	('365.728.948-86', 'Camila Pinto Alves', '1992-2-23', '2017-7-20', '-3.2125445', '-6.832034', 'F'),
	('192.154.940-81', 'Gabriela Castro da Costa', '2004-5-4', '2018-3-2', '37.0049765', '-167.999536', 'F'),
	('051.049.739-05', 'Juliana Azevedo Castro', '2002-2-9', '2018-5-8', '-13.2917825', '44.258601', 'F'),
	('562.175.036-54', 'Isabella Campos Pires', '1982-12-7', '2018-12-12', '19.2732755', '-48.844405', 'F'),
	('196.083.621-80', 'Mariane Caldeira Nogueira', '2000-11-5', '2018-3-10', '21.152234', '20.190571', 'F'),
	('293.690.116-25', 'Alana da Conceição Viana', '1947-8-1', '2016-11-20', '63.8673555', '-31.990231', 'F'),
	('909.320.903-54', 'Ana Lívia Almeida da Costa', '1962-6-16', '2017-4-15', '-2.1824555', '18.227164', 'F'),
	('442.847.425-31', 'Ana Laura da Mata Moura', '1963-11-3', '2017-12-27', '57.2975025', '-131.715842', 'F'),
	('661.660.624-43', 'Manuela Correia Ribeiro', '1956-10-10', '2018-9-28', '26.914186', '-56.445934', 'F'),
	('218.003.800-38', 'Caroline Castro da Luz', '1929-2-11', '2018-12-5', '-42.696304', '117.056578', 'F'),
	('161.591.311-41', 'Olivia da Rocha Farias', '1989-5-10', '2018-3-17', '-2.0723475', '-134.025987', 'F'),
	('592.189.369-21', 'Gabrielly Barbosa Correia', '1978-2-1', '2017-4-15', '-79.302171', '-18.346412', 'F'),
	('807.147.057-05', 'Catarina Fogaça Moreira', '1931-12-1', '2017-5-19', '-23.1273225', '148.340027', 'F'),
	('101.923.093-23', 'Isis Peixoto Araújo', '1963-12-26', '2018-6-1', '73.7187695', '66.205137', 'F'),
	('986.418.387-75', 'Maria Cecília Castro Silva', '1968-4-22', '2016-11-7', '66.8340885', '-156.163327', 'F'),
	('954.897.650-11', 'Olivia da Cunha Mendes', '1949-7-22', '2019-7-27', '-61.9986875', '-44.206946', 'F'),
	('533.897.771-05', 'Cecília Barros da Conceição', '1999-7-5', '2019-9-13', '59.532996', '147.128030', 'F'),
	('242.027.503-90', 'Nina Castro Dias', '1940-8-2', '2017-1-6', '22.5758335', '59.389895', 'F'),
	('761.312.625-00', 'Marina Rezende Almeida', '1966-10-9', '2019-8-9', '-87.845712', '54.952627', 'F'),
	('318.624.060-30', 'Mariane da Cunha Duarte', '1968-5-9', '2017-1-14', '-66.4832815', '-52.328383', 'F'),
	('430.206.866-36', 'Enzo Correia Carvalho', '1976-2-12', '2018-5-23', '-46.2587105', '49.054216', 'M'),
	('428.464.848-99', 'Enzo Lima Lima', '1939-6-18', '2018-1-17', '57.1306305', '166.209945', 'M'),
	('959.031.846-00', 'Cauê Melo Moreira', '2006-6-9', '2017-5-18', '-54.781919', '26.387546', 'M'),
	('289.081.666-45', 'João Gabriel Silveira Peixoto', '1992-7-23', '2017-9-27', '-83.9795035', '154.865067', 'M'),
	('630.703.207-32', 'Vicente Castro Azevedo', '1977-7-23', '2017-11-19', '23.573548', '-79.343364', 'M'),
	('710.164.760-00', 'Vitor Gabriel Freitas Moraes', '1992-6-8', '2018-9-27', '-39.8420775', '69.385340', 'M'),
	('552.934.949-88', 'Davi Luiz Santos Silveira', '1968-2-17', '2019-6-8', '1.982571', '176.879138', 'M'),
	('944.344.086-58', 'João Pedro Cavalcanti Silva', '1964-3-3', '2018-4-27', '50.7625935', '146.450740', 'M'),
	('020.879.003-96', 'Pedro Henrique Freitas Costela', '1980-5-21', '2018-8-18', '-79.0520905', '-172.036972', 'M'),
	('970.122.418-37', 'Daniel Freitas Araújo', '1957-7-29', '2018-11-2', '-35.3585215', '-177.939287', 'M'),
	('636.541.312-20', 'Anthony da Luz Vieira', '1955-1-23', '2017-12-2', '-85.283735', '-27.917500', 'M'),
	('602.150.938-28', 'Enzo da Cunha Cardoso', '1980-1-17', '2019-8-18', '-7.890234', '-69.768677', 'M'),
	('226.968.600-41', 'Renan Sales Lima', '1979-7-28', '2018-2-22', '-2.6822365', '149.443722', 'M'),
	('517.146.035-39', 'Nathan Viana Aragão', '1955-5-28', '2018-3-15', '86.3842065', '14.052799', 'M'),
	('897.094.953-48', 'Rodrigo Alves Gonçalves', '1981-12-27', '2018-9-4', '87.700105', '22.281184', 'M'),
	('193.648.568-05', 'Luiz Gustavo Nogueira Souza', '1929-3-23', '2019-1-3', '30.4297755', '-101.631940', 'M'),
	('208.664.918-56', 'Maria Cecília Aragão Castro', '2006-8-7', '2018-2-24', '-47.264432', '116.194005', 'F'),
	('630.507.657-04', 'Júlia Carvalho Costela', '1993-6-12', '2017-3-9', '28.686795', '4.175100', 'F'),
	('521.588.578-89', 'Isabelly Ribeiro Ferreira', '1976-4-2', '2019-9-9', '44.0687225', '-63.479234', 'F'),
	('454.849.805-26', 'Emanuelly Costa da Mota', '1997-10-2', '2017-6-8', '77.418242', '-74.991038', 'F'),
	('126.465.446-42', 'Lavínia Pinto Lopes', '1959-1-31', '2018-8-4', '-43.6772375', '3.346787', 'F'),
	('788.378.234-79', 'Valentina Nunes Nunes', '1933-7-1', '2017-3-20', '-16.126069', '-40.616331', 'F'),
	('020.478.274-00', 'Maria Vitória Lima Silva', '1995-2-25', '2018-2-9', '17.417615', '169.132909', 'F'),
	('938.320.985-26', 'Sofia Cunha Souza', '1986-12-20', '2019-3-5', '11.461169', '69.614268', 'F'),
	('266.600.930-01', 'Esther Silveira Freitas', '1950-10-5', '2018-3-20', '-70.3651705', '94.798713', 'F'),
	('761.322.769-39', 'Alana Oliveira Souza', '1961-11-3', '2018-3-1', '71.8508345', '45.850076', 'F'),
	('374.914.799-01', 'Clarice Mendes Duarte', '1955-8-13', '2017-11-11', '-58.510483', '-47.336912', 'F'),
	('176.489.865-66', 'Larissa Ramos Silva', '1982-8-31', '2017-10-17', '-70.401062', '158.061593', 'F'),
	('477.023.447-33', 'Sophia Souza Sales', '1994-10-11', '2018-1-6', '-83.3999315', '-84.402458', 'F'),
	('261.156.571-64', 'Bernardo Silva Rezende', '2003-10-20', '2017-3-31', '-10.7721285', '-4.716711', 'M'),
	('174.767.513-02', 'João Vitor Cunha da Cunha', '1958-10-25', '2019-5-28', '70.3046905', '-115.237992', 'M'),
	('127.754.185-03', 'Daniel Oliveira Moura', '1980-1-9', '2017-2-23', '-40.335424', '-142.178283', 'M'),
	('095.725.968-96', 'Isabelly Ferreira Ramos', '1955-2-1', '2019-6-14', '45.946030', '78.717733', 'F'),
	('227.345.725-16', 'Maria Cecília Fernandes Martins', '1945-12-29', '2019-9-30', '9.721010', '-158.614337', 'F'),
	('287.649.002-15', 'Manuela Pinto Vieira', '1995-9-13', '2018-12-29', '-26.357600', '60.414009', 'F'),
	('742.933.399-06', 'Ana Luiza Cunha Moraes', '1936-6-17', '2017-12-15', '27.6457345', '58.777843', 'F'),
	('586.822.245-85', 'Catarina Dias da Costa', '1952-8-19', '2017-1-28', '6.443707', '18.642783', 'F'),
	('809.181.088-10', 'Nina Souza Barros', '2001-2-27', '2018-6-20', '3.394399', '-131.593893', 'F'),
	('485.407.175-30', 'Larissa Teixeira Campos', '1995-4-9', '2018-3-18', '44.9720015', '94.873868', 'F'),
	('035.703.579-88', 'Sophia da Mata Oliveira', '1985-10-16', '2017-4-23', '-44.1153335', '28.486222', 'F'),
	('032.505.905-50', 'Emanuel Mendes Cardoso', '1951-11-23', '2018-8-2', '-33.4520555', '151.237981', 'M'),
	('128.318.589-09', 'André Barros Lopes', '1956-5-11', '2019-9-8', '-20.1194715', '-171.854721', 'M'),
	('219.549.192-20', 'Bruno das Neves Porto', '1982-8-20', '2017-5-2', '-35.795486', '33.268421', 'M'),
	('476.119.804-40', 'Camila Moura Almeida', '1999-11-16', '2018-2-7', '-60.401269', '113.404030', 'F'),
	('480.796.652-90', 'Olivia Martins das Neves', '1995-8-18', '2018-5-18', '-60.464169', '122.351432', 'F'),
	('192.283.160-39', 'Yasmin da Mata Vieira', '1956-4-30', '2018-3-20', '-52.774795', '-104.803532', 'F'),
	('402.246.463-11', 'Bruna Araújo Aragão', '1972-3-22', '2019-6-21', '-79.2028665', '8.408097', 'F'),
	('901.363.990-96', 'Nicole Nascimento Rezende', '1945-12-26', '2019-6-5', '54.4719435', '-160.119142', 'F'),
	('298.322.674-39', 'Ana Júlia da Cunha Cardoso', '1947-1-6', '2019-2-15', '43.2412495', '127.856870', 'F'),
	('147.988.057-42', 'Lara Santos Dias', '1964-8-18', '2018-6-30', '-87.666231', '-22.935573', 'F'),
	('191.144.047-02', 'Sofia Melo Carvalho', '1943-2-13', '2018-8-14', '-21.6183075', '-57.774954', 'F'),
	('338.640.851-60', 'Alana da Mota Castro', '1983-5-10', '2018-1-7', '33.3067665', '23.335813', 'F'),
	('774.236.197-36', 'Maria Julia da Costa Barros', '2005-6-17', '2018-1-7', '15.422150', '-130.713410', 'F'),
	('581.002.072-08', 'Carolina Lopes Pereira', '1995-10-3', '2018-1-25', '63.759358', '-176.727886', 'F'),
	('493.684.111-07', 'Catarina Araújo Pires', '1935-12-25', '2017-7-12', '71.4494835', '-79.609639', 'F'),
	('455.254.563-97', 'Renan Melo Duarte', '1957-2-19', '2019-2-10', '-48.442406', '-102.137918', 'M'),
	('274.442.369-68', 'João Gabriel Cardoso da Costa', '1933-9-24', '2017-12-19', '85.1178925', '-60.745044', 'M'),
	('559.453.538-17', 'Paulo Porto Sales', '1958-5-25', '2018-4-25', '34.3164595', '133.816711', 'M'),
	('707.929.509-25', 'Cauê da Mota Lima', '1975-8-14', '2018-5-9', '-13.9454365', '63.031472', 'M'),
	('682.112.737-99', 'João Felipe Vieira Gomes', '1955-1-22', '2018-12-6', '62.0004735', '6.033362', 'M'),
	('493.595.641-09', 'Kaique Souza Souza', '1949-12-13', '2019-8-6', '23.882562', '44.736021', 'M'),
	('487.832.626-36', 'Pietro Costela Nogueira', '1931-11-8', '2017-12-30', '-46.732508', '76.756211', 'M'),
	('043.307.895-23', 'Felipe Rocha da Luz', '1999-5-17', '2018-2-4', '36.428485', '42.461127', 'M'),
	('680.184.160-28', 'Pedro Pinto Vieira', '1963-5-12', '2018-9-29', '89.5599865', '146.213438', 'M'),
	('136.818.661-04', 'Nicole Pires Oliveira', '1960-5-25', '2016-11-11', '-24.498195', '155.039130', 'F'),
	('543.031.325-43', 'Clarice da Paz Pinto', '1999-12-16', '2018-10-9', '70.9449105', '160.649931', 'F'),
	('905.180.103-33', 'Sabrina Martins Silveira', '1963-12-22', '2017-10-8', '-24.4614885', '169.668815', 'F'),
	('445.247.565-58', 'Joana Santos Duarte', '1991-12-10', '2019-2-21', '-51.812271', '136.167408', 'F'),
	('887.450.522-12', 'Maitê Rocha Ferreira', '1936-1-17', '2017-3-28', '0.8280035', '151.699945', 'F'),
	('874.524.521-51', 'Leonardo Costela Souza', '1940-9-4', '2017-12-26', '-9.063991', '-89.100074', 'M'),
	('108.844.854-20', 'Enrico da Rocha Novaes', '1959-6-2', '2017-9-28', '-12.2130465', '-7.601735', 'M'),
	('995.106.177-09', 'Nicolas Rodrigues Rezende', '1975-12-15', '2018-7-27', '-77.1019865', '29.636113', 'M'),
	('675.071.897-32', 'Noah Monteiro Gonçalves', '1930-7-13', '2018-1-28', '46.320081', '161.622634', 'M'),
	('954.840.995-01', 'Thomas Gomes Dias', '1957-1-23', '2018-1-18', '58.5910055', '128.106974', 'M'),
	('032.609.977-84', 'Danilo Alves Dias', '1965-12-18', '2018-7-19', '-26.698048', '-155.975999', 'M'),
	('503.977.886-49', 'Maria Clara Melo Farias', '1961-1-23', '2017-8-9', '64.688391', '-171.278066', 'F'),
	('576.766.726-86', 'Maysa Lopes Freitas', '1986-5-10', '2016-11-2', '-73.954531', '-97.982631', 'F'),
	('117.291.560-10', 'Kamilly Nunes Porto', '1969-6-21', '2018-7-25', '-27.2996365', '-103.477064', 'F'),
	('364.045.102-35', 'Maria Cecília Melo da Rosa', '1955-3-7', '2018-3-26', '-40.4871725', '-40.055865', 'F'),
	('883.382.447-08', 'Sofia Carvalho Porto', '1970-3-1', '2018-12-10', '-59.979340', '-39.002192', 'F'),
	('027.480.123-05', 'Vitor Hugo Fernandes Pereira', '1953-3-30', '2018-6-2', '-47.783428', '-53.142469', 'M'),
	('569.154.071-89', 'Rafael Costa Ferreira', '1983-9-30', '2017-8-3', '-1.7893265', '-62.992009', 'M'),
	('682.453.539-73', 'Pedro Aragão Peixoto', '1969-9-7', '2019-2-12', '-81.503690', '-150.173959', 'M'),
	('608.706.384-67', 'Emanuel Santos Campos', '1991-1-31', '2017-10-11', '3.1137125', '118.812325', 'M'),
	('728.299.197-93', 'João Freitas Santos', '1994-10-20', '2019-5-17', '54.5469135', '-44.063632', 'M'),
	('360.902.402-06', 'Yuri Monteiro Silva', '1944-3-22', '2018-5-1', '-59.8666455', '156.396111', 'M');

	INSERT INTO FORNECEDOR VALUES
	('100.973.580-29', 'Joaquim Teixeira Viana', 'Joaquim Teixeira Viana', '2018-5-30', '-28.405890', '-76.481920', 1),
	('781.245.184-40', 'João Pedro Novaes Santos', 'João Pedro Novaes Santos', '2016-10-26', '-24.8214445', '-142.741479', 1),
	('277.315.375-87', 'Miguel da Rosa Caldeira', 'Miguel da Rosa Caldeira', '2017-2-18', '24.748410', '165.968518', 1),
	('73.146.873/6990-52', 'Souza', 'Souza', '2017-11-9', '20.824489', '171.780080', 1),
	('11.795.090/5557-17', 'Costela', 'Costela', '2016-12-19', '-34.836326', '-146.940230', 1),
	('23.937.977/1806-05', 'Ribeiro', 'Ribeiro', '2018-9-10', '-73.3419155', '-2.287984', 1),
	('88.485.809/6229-50', 'da Cruz', 'da Cruz', '2017-5-26', '24.5207145', '20.757367', 1),
	('85.543.393/1625-40', 'Nunes', 'Nunes', '2018-1-25', '27.5908205', '-51.476896', 1),
	('84.581.712/9436-05', 'Novaes - EI', 'Novaes - EI', '2018-2-21', '29.681180', '-16.758698', 1),
	('70.402.893/4672-71', 'Moura Porto S/A', 'Moura Porto S/A', '2018-7-12', '-7.353292', '71.567299', 1),
	('64.915.583/9842-36', 'da Rosa Vieira S/A', 'da Rosa Vieira S/A', '2017-9-22', '-48.316154', '127.025400', 1),
	('70.549.729/7374-26', 'Teixeira', 'Teixeira', '2018-9-2', '4.062261', '119.496281', 1),
	('07.007.581/6319-81', 'Viana - EI', 'Viana - EI', '2017-7-6', '76.121837', '83.884092', 1),
	('98.358.394/2040-72', 'Gonçalves da Costa e Filhos', 'Gonçalves da Costa e Filhos', '2018-9-8', '-11.1165055', '69.935721', 1),
	('22.323.793/8688-99', 'Costa Souza Ltda.', 'Costa Souza Ltda.', '2017-10-25', '84.617385', '28.595988', 1),
	('47.747.905/4651-53', 'Viana', 'Viana', '2018-7-8', '30.439752', '-29.390847', 1),
	('11.034.406/6331-47', 'Ramos', 'Ramos', '2017-5-21', '23.4043555', '33.167127', 1),
	('97.273.164/1628-84', 'Barros', 'Barros', '2017-2-15', '-53.006299', '24.310945', 1),
	('44.835.073/5577-69', 'Duarte', 'Duarte', '2017-5-26', '-4.8435855', '-107.718215', 1),
	('16.947.184/9819-65', 'Rezende e Filhos', 'Rezende e Filhos', '2017-11-1', '-50.186964', '-47.532575', 1),
	('98.713.604/0853-12', 'Pinto Ltda.', 'Pinto Ltda.', '2016-10-7', '-40.937135', '-56.069672', 1),
	('06.045.166/6050-10', 'Mendes', 'Mendes', '2017-12-3', '-32.957085', '25.019930', 1),
	('56.208.130/2496-06', 'Rocha', 'Rocha', '2018-6-30', '52.0351165', '45.952317', 1),
	('33.919.413/5511-97', 'Vieira', 'Vieira', '2018-7-27', '14.8096365', '-103.528867', 1),
	('11.454.766/8092-39', 'Jesus', 'Jesus', '2017-1-2', '33.5498685', '82.192621', 1),
	('73.291.809/3985-37', 'Melo Pinto S.A.', 'Melo Pinto S.A.', '2018-5-16', '39.275925', '37.795510', 1),
	('72.765.004/8577-22', 'Oliveira e Filhos', 'Oliveira e Filhos', '2017-8-23', '41.471050', '-73.908391', 1),
	('06.217.954/2750-71', 'Barbosa - EI', 'Barbosa - EI', '2016-11-6', '-40.9568685', '-148.958364', 1),
	('68.926.971/7135-98', 'da Mata Fogaça - EI', 'da Mata Fogaça - EI', '2018-4-4', '-40.1665345', '67.105077', 1),
	('07.819.576/1312-29', 'Gomes', 'Gomes', '2018-6-15', '37.6527085', '47.417166', 1),
	('53.293.511/6491-44', 'Monteiro - EI', 'Monteiro - EI', '2018-1-10', '-21.6651885', '135.704316', 1),
	('84.339.811/3490-07', 'Rodrigues - ME', 'Rodrigues - ME', '2018-8-26', '80.0460305', '-154.339867', 1),
	('97.711.726/6953-00', 'Silva', 'Silva', '2017-4-17', '-16.943651', '131.557895', 1),
	('48.328.049/2183-10', 'Pires', 'Pires', '2017-12-3', '-1.629994', '11.165089', 1),
	('64.976.849/9365-23', 'da Paz', 'da Paz', '2017-11-23', '-25.9726295', '69.408759', 1),
	('22.352.107/7239-15', 'Silveira', 'Silveira', '2017-6-10', '-84.554480', '127.833390', 1),
	('02.357.393/3970-88', 'Dias S.A.', 'Dias S.A.', '2018-8-7', '-26.498161', '-5.091408', 1),
	('05.095.078/0906-30', 'Silveira', 'Silveira', '2017-5-9', '-75.946631', '73.547627', 1),
	('38.124.301/1142-94', 'Azevedo', 'Azevedo', '2017-7-17', '-43.8474545', '116.692238', 1),
	('18.831.608/3434-03', 'da Luz', 'da Luz', '2017-10-25', '1.389946', '55.701595', 1),
	('29.068.782/3837-66', 'da Paz', 'da Paz', '2017-8-31', '-70.5488965', '-84.466929', 1),
	('22.433.349/6540-01', 'da Costa Araújo Ltda.', 'da Costa Araújo Ltda.', '2018-9-1', '79.7429655', '2.587280', 1),
	('84.540.585/3190-21', 'Rodrigues S.A.', 'Rodrigues S.A.', '2017-3-23', '-1.1823925', '13.692588', 1),
	('74.056.082/4785-02', 'Vieira', 'Vieira', '2018-5-4', '62.080437', '-60.205704', 1),
	('04.370.899/9570-23', 'da Costa', 'da Costa', '2017-9-17', '-62.5315065', '-106.088852', 1),
	('56.380.407/3394-02', 'Costa', 'Costa', '2017-2-18', '-71.636306', '39.510145', 1),
	('28.422.429/2139-39', 'Santos Ltda.', 'Santos Ltda.', '2017-8-4', '-9.8467925', '-8.178918', 1),
	('20.802.069/5550-16', 'Carvalho', 'Carvalho', '2017-6-17', '74.524222', '-176.037246', 1),
	('41.900.454/1097-00', 'Vieira Gomes - EI', 'Vieira Gomes - EI', '2017-10-26', '-87.717482', '-95.211148', 1),
	('82.256.860/7907-09', 'da Costa S/A', 'da Costa S/A', '2017-6-4', '55.967587', '11.168347', 1),
	('54.549.266/2345-33', 'Moura', 'Moura', '2017-1-27', '75.871090', '22.073282', 1),
	('97.322.164/7356-14', 'Costela Costela S/A', 'Costela Costela S/A', '2017-9-11', '23.4936105', '96.338894', 1),
	('10.507.365/8503-85', 'Barbosa - EI', 'Barbosa - EI', '2016-12-26', '6.9623735', '-120.303351', 1),
	('23.856.760/7963-53', 'das Neves S/A', 'das Neves S/A', '2018-9-20', '70.318515', '-101.649537', 1),
	('89.936.340/3573-91', 'Alves Cardoso Ltda.', 'Alves Cardoso Ltda.', '2018-4-11', '89.096701', '70.579381', 1),
	('46.825.729/5937-51', 'Oliveira', 'Oliveira', '2017-12-1', '-72.592665', '100.839343', 1),
	('79.460.664/7483-76', 'Nascimento', 'Nascimento', '2017-8-9', '-83.0463395', '-18.729988', 1),
	('79.315.423/8747-11', 'Moura da Cunha S.A.', 'Moura da Cunha S.A.', '2017-10-11', '-35.3891795', '43.638708', 1),
	('01.059.020/2794-56', 'Viana e Filhos', 'Viana e Filhos', '2018-3-21', '-77.463571', '-37.193289', 1),
	('84.428.432/7582-52', 'Souza', 'Souza', '2017-9-21', '3.3176195', '165.708562', 1),
	('07.293.879/9225-41', 'das Neves', 'das Neves', '2018-2-2', '-71.0860225', '-157.781707', 1),
	('38.973.389/4931-39', 'Novaes', 'Novaes', '2017-11-17', '-19.059097', '-31.469397', 1),
	('71.150.726/0688-96', 'da Mata da Rocha e Filhos', 'da Mata da Rocha e Filhos', '2016-12-7', '80.747045', '-59.874794', 1),
	('67.717.709/5760-50', 'Araújo', 'Araújo', '2018-9-14', '36.5540285', '92.003018', 1),
	('68.328.795/7689-07', 'Teixeira - ME', 'Teixeira - ME', '2016-10-9', '32.716640', '77.415424', 1),
	('60.646.070/3907-74', 'Almeida', 'Almeida', '2017-6-1', '80.4597665', '121.781338', 1),
	('56.223.378/2229-42', 'Porto', 'Porto', '2016-11-24', '46.711218', '-1.217147', 1),
	('59.381.457/8845-06', 'Cardoso', 'Cardoso', '2018-2-6', '-50.3070745', '6.409025', 1),
	('40.075.585/7684-12', 'Fernandes', 'Fernandes', '2018-8-22', '-28.031771', '76.542681', 1),
	('03.600.515/0484-07', 'Cardoso Ltda.', 'Cardoso Ltda.', '2018-4-16', '-15.3366615', '-116.636329', 1),
	('44.920.432/4409-19', 'Melo Fernandes e Filhos', 'Melo Fernandes e Filhos', '2017-6-3', '66.243007', '72.526255', 1),
	('45.831.290/7823-56', 'da Luz S/A', 'da Luz S/A', '2018-9-8', '71.8266625', '48.499687', 1),
	('16.073.821/4462-85', 'Peixoto', 'Peixoto', '2018-5-29', '52.8254645', '13.522729', 1),
	('15.932.569/3394-10', 'Campos', 'Campos', '2017-7-27', '-57.502358', '61.408235', 1),
	('37.804.067/0956-37', 'Alves', 'Alves', '2017-9-11', '-31.2242065', '167.746340', 1),
	('26.941.738/9900-23', 'da Cunha S/A', 'da Cunha S/A', '2017-1-6', '16.8227425', '43.028561', 1),
	('01.560.639/7251-64', 'Pires - ME', 'Pires - ME', '2017-2-21', '-18.429804', '151.940314', 1),
	('95.776.695/3314-88', 'Barros Barbosa S/A', 'Barros Barbosa S/A', '2017-4-27', '0.5498175', '-112.670959', 1),
	('26.593.635/6363-56', 'Nascimento da Luz e Filhos', 'Nascimento da Luz e Filhos', '2017-4-1', '-75.515594', '-36.139931', 1),
	('89.070.202/7783-94', 'das Neves', 'das Neves', '2017-7-7', '87.8088255', '32.706234', 1),
	('71.328.725/7280-66', 'Lima da Paz e Filhos', 'Lima da Paz e Filhos', '2018-9-13', '39.113196', '123.402485', 1),
	('05.727.536/9986-83', 'Freitas', 'Freitas', '2017-3-8', '12.0695915', '139.501385', 1),
	('80.074.691/8229-72', 'Azevedo', 'Azevedo', '2017-4-30', '67.791984', '57.251618', 1),
	('90.465.421/0713-63', 'da Paz e Filhos', 'da Paz e Filhos', '2018-4-9', '-81.630576', '77.092699', 1),
	('02.059.648/4763-25', 'Sales', 'Sales', '2016-12-28', '2.967914', '13.007912', 1),
	('46.185.233/4935-45', 'da Rosa - EI', 'da Rosa - EI', '2017-1-29', '60.068406', '68.803947', 1),
	('78.440.900/1662-07', 'Moura S/A', 'Moura S/A', '2017-4-12', '30.515030', '44.471200', 1),
	('13.818.067/1028-53', 'Santos', 'Santos', '2017-10-23', '-65.961989', '-32.097609', 1),
	('45.023.221/1140-46', 'Novaes e Filhos', 'Novaes e Filhos', '2018-1-19', '-25.393456', '-72.751802', 1),
	('76.680.896/6201-16', 'Farias S/A', 'Farias S/A', '2017-5-12', '74.581487', '-13.447003', 1),
	('06.025.833/0170-88', 'Barros Teixeira e Filhos', 'Barros Teixeira e Filhos', '2018-5-28', '1.2055495', '95.037991', 1),
	('87.896.565/7373-25', 'Cavalcanti', 'Cavalcanti', '2017-7-3', '79.5230915', '138.272764', 1),
	('38.604.625/4002-30', 'Pereira', 'Pereira', '2016-11-14', '31.9083715', '-172.291343', 1),
	('75.946.122/5806-69', 'Peixoto e Filhos', 'Peixoto e Filhos', '2017-6-1', '57.175818', '-158.153253', 1),
	('16.006.416/0092-94', 'Rocha Barbosa S.A.', 'Rocha Barbosa S.A.', '2016-12-30', '20.2758515', '11.698364', 1),
	('38.275.756/6301-36', 'Cardoso', 'Cardoso', '2017-6-19', '-41.1814925', '137.199047', 1),
	('22.923.768/6897-55', 'Lopes Caldeira - EI', 'Lopes Caldeira - EI', '2017-5-24', '-52.638824', '129.761738', 1),
	('04.963.065/1999-25', 'Moreira S/A', 'Moreira S/A', '2017-1-25', '28.8314395', '-47.631003', 1),
	('46.230.735/3474-80', 'Caldeira', 'Caldeira', '2017-2-9', '-89.7148195', '122.348545', 1),
	('02.984.527/1287-82', 'Jesus Rodrigues e Filhos', 'Jesus Rodrigues e Filhos', '2017-1-12', '31.8920235', '-82.468496', 1);

	INSERT INTO PRODUTO VALUES
	(1, '18694291', 'abacate', 4.8, 1, 1, 2),
	(2, '08451750', 'abacate avocado', 3.0, 1, 1, 2),
	(3, '60551610', 'abacaxi havaiano', 3.7, 1, 1, 2),
	(4, '92310193', 'abacaxi perol', 3.4, 1, 1, 2),
	(5, '74168705', 'ameixa branca', 10.7, 1, 1, 2),
	(6, '11469193', 'ameixa importada', 5.5, 1, 1, 2),
	(7, '63229875', 'ameixa rosa', 2.3, 1, 1, 2),
	(8, '53399250', 'antenova', 5.0, 1, 1, 2),
	(9, '05374403', 'banana catur organica', 1.1, 1, 1, 2),
	(10, '23128637', 'banana da terra', 5.3, 1, 1, 2),
	(11, '09092495', 'banana maca', 3.4, 1, 1, 2),
	(12, '00566308', 'banana prata', 4.1, 1, 1, 2),
	(13, '29578252', 'mexerica montenegra', 1.9, 1, 1, 2),
	(14, '81706020', 'mexerica morgot', 0.8, 1, 1, 2),
	(15, '02750927', 'mexerica poca', 5.6, 1, 1, 2),
	(16, '87655483', 'mexerica importada', 10.1, 1, 1, 2),
	(17, '59640936', 'caqui chocolate', 10.2, 1, 1, 2),
	(18, '20128371', 'caqui coracao', 1.2, 1, 1, 2),
	(19, '84011428', 'caqui forte', 5.8, 1, 1, 2),
	(20, '63645231', 'caqui fuyu', 7.2, 1, 1, 2),
	(21, '91237057', 'caqui importado', 7.1, 1, 1, 2),
	(22, '73203667', 'carambola', 5.3, 1, 1, 2),
	(23, '63887594', 'coco seco', 0.3, 1, 1, 2),
	(24, '93435925', 'coco', 6.1, 1, 1, 2),
	(25, '49808575', 'coco verde', 8.5, 1, 1, 2),
	(26, '69479892', 'damasco', 10.5, 1, 1, 2),
	(27, '23157095', 'fruta do conde', 1.6, 1, 1, 2),
	(28, '11637615', 'goiaba', 9.9, 1, 1, 2),
	(29, '41760161', 'granadilla silvestre', 2.6, 1, 1, 2),
	(30, '45505522', 'graviola', 6.5, 1, 1, 2),
	(31, '95282237', 'jaca', 4.9, 1, 1, 2),
	(32, '97853480', 'kiwi', 7.6, 1, 1, 2),
	(33, '96110676', 'kiwi zelandia', 6.8, 1, 1, 2),
	(34, '95456669', 'kiwi maca', 4.3, 1, 1, 2),
	(35, '69658433', 'laranja do ceu', 10.1, 1, 1, 2),
	(36, '04705802', 'laranja pera', 7.8, 1, 1, 2),
	(37, '21097737', 'laranja bahia', 10.7, 1, 1, 2),
	(38, '31907903', 'lichia', 8.8, 1, 1, 2),
	(39, '42676911', 'limao tati', 3.0, 1, 1, 2),
	(40, '44516529', 'limao persa', 4.1, 1, 1, 2),
	(41, '67039517', 'limao siciliano', 8.2, 1, 1, 2),
	(42, '99711900', 'laranja de umbigo exp', 9.6, 1, 1, 2),
	(43, '55934329', 'maca rosa', 4.9, 1, 1, 2),
	(44, '41440810', 'maca fugi', 2.6, 1, 1, 2),
	(45, '97790693', 'maca gala', 1.7, 1, 1, 2),
	(46, '37151713', 'maca argentina', 8.9, 1, 1, 2),
	(47, '91651594', 'maca verde', 6.2, 1, 1, 2),
	(48, '18180886', 'mamao formosa', 4.1, 1, 1, 2),
	(49, '83713248', 'mamao papaya golden', 5.1, 1, 1, 2),
	(50, '96539019', 'mamao papaya esp', 9.3, 1, 1, 2),
	(51, '48273374', 'manga haden', 2.6, 1, 1, 2),
	(52, '89120392', 'manga palmer', 4.4, 1, 1, 2),
	(53, '47791299', 'manga rosa', 8.4, 1, 1, 2),
	(54, '81405275', 'maracuja azedo', 8.5, 1, 1, 2),
	(55, '66694656', 'maracuja doce', 4.8, 1, 1, 2),
	(56, '05484164', 'melancia', 5.4, 1, 1, 2),
	(57, '51595968', 'melancia sem semente', 1.3, 1, 1, 2),
	(58, '82358990', 'melao cantalume', 2.4, 1, 1, 2),
	(59, '69740060', 'melao cepi', 4.5, 1, 1, 2),
	(60, '04613794', 'melao charatane', 10.5, 1, 1, 2),
	(61, '71750545', 'melao espanhol', 5.8, 1, 1, 2),
	(62, '09612266', 'melao gala', 8.1, 1, 1, 2),
	(63, '62533720', 'melao gaucho', 8.3, 1, 1, 2),
	(64, '77402691', 'melao orange', 6.6, 1, 1, 2),
	(65, '71779966', 'melao pele sapo', 1.1, 1, 1, 2),
	(66, '82139469', 'manga tommy', 7.8, 1, 1, 2),
	(67, '87438857', 'nectarina', 0.3, 1, 1, 2),
	(68, '97756620', 'nectarina importada', 7.3, 1, 1, 2),
	(69, '30970458', 'pera asiatica', 4.0, 1, 1, 2),
	(70, '94810158', 'pera damjou', 9.3, 1, 1, 2),
	(71, '70481884', 'pera importada', 3.9, 1, 1, 2),
	(72, '16631069', 'pera nacional', 7.2, 1, 1, 2),
	(73, '64064994', 'pera verde', 2.3, 1, 1, 2),
	(74, '35706182', 'pera portuguesa', 8.1, 1, 1, 2),
	(75, '96453995', 'pera williams', 9.5, 1, 1, 2),
	(76, '02425481', 'pessego amarelo', 4.3, 1, 1, 2),
	(77, '31385350', 'pessego branco', 3.0, 1, 1, 2),
	(78, '54121058', 'pessego importado especial', 3.0, 1, 1, 2),
	(79, '39628770', 'roma', 1.1, 1, 1, 2),
	(80, '55048620', 'uva bentica', 0.1, 1, 1, 2),
	(81, '28658757', 'uva brasil', 3.9, 1, 1, 2),
	(82, '02930688', 'uva importada', 7.5, 1, 1, 2),
	(83, '54537576', 'uva italiana', 4.6, 1, 1, 2),
	(84, '34719565', 'uva niagara branca', 4.1, 1, 1, 2),
	(85, '93432368', 'uva niagara rosa', 0.4, 1, 1, 2),
	(86, '05389797', 'uva red glob', 7.8, 1, 1, 2),
	(87, '19183572', 'uva rubi rosa', 4.7, 1, 1, 2),
	(88, '63924329', 'uva rubi verde', 1.0, 1, 1, 2),
	(89, '81752478', 'uva venus', 7.2, 1, 1, 2),
	(90, '50417292', 'pinhao', 1.1, 1, 1, 2),
	(91, '55271738', 'cebola branca', 7.1, 2, 1, 2),
	(92, '48268257', 'cebola roxa', 0.3, 2, 1, 2),
	(93, '62369602', 'cenoura', 8.7, 2, 1, 2),
	(94, '83867392', 'gengibre', 6.0, 2, 1, 2),
	(95, '40105918', 'tomate italiano', 9.2, 2, 1, 2),
	(96, '80382508', 'cebola branca', 8.3, 3, 1, 1),
	(97, '41218075', 'cebola roxa', 8.5, 3, 1, 1),
	(98, '39357441', 'cenoura', 9.6, 3, 1, 1),
	(99, '50155552', 'gengibre', 9.3, 3, 1, 1),
	(100, '01593921', 'tomate italiano', 7.4, 3, 1, 1);

	INSERT INTO AQUISICAO_PRODUTO VALUES
	('46.825.729/5937-51', 23, '2017-6-3', '21:18:05', 35, 5.5),
	('53.293.511/6491-44', 42, '2016-10-10', '08:07:06', 26, 1.4),
	('23.856.760/7963-53', 67, '2018-4-19', '01:48:25', 7, 1.0),
	('23.937.977/1806-05', 56, '2017-12-7', '22:51:18', 41, 6.4),
	('28.422.429/2139-39', 83, '2018-7-15', '22:44:38', 42, 2.8),
	('07.007.581/6319-81', 47, '2018-7-4', '18:40:22', 26, 4.9),
	('79.315.423/8747-11', 29, '2018-9-29', '06:24:47', 12, 6.3),
	('16.947.184/9819-65', 64, '2018-8-16', '10:38:47', 23, 5.3),
	('46.825.729/5937-51', 39, '2017-2-6', '11:59:12', 32, 5.1),
	('68.328.795/7689-07', 7, '2017-6-17', '20:01:33', 12, 4.5),
	('70.402.893/4672-71', 90, '2017-10-7', '11:15:50', 45, 0.8),
	('18.831.608/3434-03', 28, '2017-11-22', '19:10:05', 9, 3.4),
	('56.380.407/3394-02', 68, '2017-2-14', '21:44:25', 5, 2.2),
	('73.146.873/6990-52', 61, '2016-10-23', '15:09:26', 40, 0.1),
	('89.936.340/3573-91', 17, '2017-6-8', '10:09:33', 49, 3.5),
	('84.428.432/7582-52', 61, '2017-11-17', '12:01:18', 46, 7.0),
	('15.932.569/3394-10', 91, '2017-8-4', '14:24:59', 17, 4.8),
	('06.217.954/2750-71', 18, '2018-3-10', '23:33:31', 6, 6.0),
	('02.357.393/3970-88', 74, '2017-10-31', '09:40:30', 31, 0.9),
	('37.804.067/0956-37', 21, '2016-12-22', '00:36:22', 48, 3.8),
	('56.380.407/3394-02', 35, '2018-8-21', '23:13:42', 7, 5.3),
	('85.543.393/1625-40', 34, '2018-5-3', '01:23:27', 23, 4.9),
	('16.073.821/4462-85', 23, '2018-6-6', '08:19:00', 25, 5.7),
	('22.923.768/6897-55', 66, '2017-12-8', '04:59:09', 29, 1.0),
	('277.315.375-87', 20, '2017-2-27', '23:25:40', 25, 6.4),
	('46.185.233/4935-45', 52, '2017-4-10', '00:04:07', 38, 0.9),
	('70.549.729/7374-26', 12, '2017-4-5', '03:34:15', 2, 2.6),
	('56.208.130/2496-06', 38, '2017-1-11', '14:17:36', 5, 6.0),
	('781.245.184-40', 80, '2017-10-15', '03:30:00', 16, 4.5),
	('40.075.585/7684-12', 64, '2018-1-24', '02:11:33', 13, 3.4),
	('82.256.860/7907-09', 19, '2017-3-23', '17:15:57', 41, 5.2),
	('53.293.511/6491-44', 34, '2016-10-31', '00:35:41', 31, 0.5),
	('64.976.849/9365-23', 91, '2017-3-17', '02:44:01', 41, 1.5),
	('84.540.585/3190-21', 63, '2017-5-1', '22:31:32', 38, 5.1),
	('46.185.233/4935-45', 22, '2017-9-8', '11:56:06', 31, 3.7),
	('98.358.394/2040-72', 93, '2017-12-17', '12:02:02', 29, 6.5),
	('03.600.515/0484-07', 90, '2017-10-19', '15:13:20', 46, 6.7),
	('75.946.122/5806-69', 12, '2018-2-13', '08:34:45', 44, 5.4),
	('79.315.423/8747-11', 88, '2018-6-19', '15:43:51', 43, 6.7),
	('90.465.421/0713-63', 20, '2018-3-6', '19:12:29', 25, 6.3),
	('56.208.130/2496-06', 14, '2018-1-16', '16:03:28', 9, 1.2),
	('75.946.122/5806-69', 49, '2017-3-9', '09:10:39', 36, 2.4),
	('06.045.166/6050-10', 74, '2017-4-15', '13:12:01', 48, 1.1),
	('01.560.639/7251-64', 40, '2017-11-10', '15:45:00', 29, 1.4),
	('75.946.122/5806-69', 12, '2017-11-11', '22:48:26', 3, 4.1),
	('82.256.860/7907-09', 81, '2017-12-13', '03:12:32', 38, 6.0),
	('68.328.795/7689-07', 44, '2018-2-4', '20:43:06', 20, 7.0),
	('64.976.849/9365-23', 85, '2018-1-3', '01:38:58', 1, 7.0),
	('47.747.905/4651-53', 49, '2017-9-2', '19:49:00', 42, 6.2),
	('44.920.432/4409-19', 7, '2018-1-29', '11:06:50', 39, 2.3),
	('78.440.900/1662-07', 31, '2018-1-22', '05:18:40', 3, 2.7),
	('44.835.073/5577-69', 6, '2017-8-15', '02:44:44', 11, 0.9),
	('781.245.184-40', 60, '2018-8-23', '18:57:12', 23, 2.5),
	('07.293.879/9225-41', 84, '2018-5-14', '00:04:20', 16, 5.0),
	('277.315.375-87', 63, '2016-11-9', '11:39:27', 30, 5.7),
	('15.932.569/3394-10', 5, '2017-6-17', '16:01:02', 7, 5.2),
	('02.357.393/3970-88', 96, '2017-12-10', '02:08:08', 41, 6.3),
	('37.804.067/0956-37', 96, '2017-3-25', '07:18:08', 42, 3.6),
	('03.600.515/0484-07', 19, '2018-8-12', '18:03:36', 12, 2.3),
	('11.795.090/5557-17', 72, '2018-3-18', '11:26:05', 48, 1.5),
	('20.802.069/5550-16', 75, '2018-2-23', '07:08:34', 44, 4.9),
	('56.380.407/3394-02', 82, '2018-10-2', '15:32:10', 12, 1.2),
	('76.680.896/6201-16', 98, '2017-8-6', '09:32:02', 40, 0.7),
	('46.230.735/3474-80', 78, '2017-8-14', '03:02:15', 16, 6.3),
	('56.223.378/2229-42', 100, '2017-7-20', '15:52:53', 25, 1.0),
	('22.923.768/6897-55', 7, '2018-8-15', '05:29:07', 32, 3.7),
	('53.293.511/6491-44', 84, '2017-12-6', '02:08:25', 19, 5.6),
	('82.256.860/7907-09', 76, '2017-12-16', '10:50:15', 9, 4.9),
	('23.856.760/7963-53', 62, '2018-7-10', '05:23:06', 4, 3.8),
	('11.454.766/8092-39', 11, '2018-4-23', '21:16:46', 28, 4.2),
	('84.540.585/3190-21', 7, '2018-7-28', '03:33:16', 38, 5.4),
	('68.926.971/7135-98', 12, '2018-3-23', '07:58:01', 29, 3.7),
	('06.025.833/0170-88', 1, '2017-6-13', '14:17:32', 30, 0.6),
	('06.045.166/6050-10', 6, '2017-4-17', '00:48:24', 30, 4.8),
	('38.275.756/6301-36', 98, '2017-11-16', '15:10:07', 25, 3.8),
	('26.941.738/9900-23', 83, '2017-7-10', '06:18:26', 30, 5.9),
	('79.315.423/8747-11', 18, '2018-6-6', '22:16:42', 18, 1.7),
	('37.804.067/0956-37', 33, '2017-7-4', '15:24:40', 34, 0.7),
	('71.150.726/0688-96', 100, '2018-5-3', '00:59:01', 26, 3.8),
	('05.095.078/0906-30', 42, '2017-6-24', '11:56:56', 5, 4.6),
	('70.549.729/7374-26', 53, '2017-11-25', '10:17:56', 38, 4.1),
	('01.560.639/7251-64', 64, '2018-1-30', '11:43:19', 40, 0.8),
	('26.593.635/6363-56', 82, '2017-11-24', '22:23:57', 39, 2.7),
	('44.920.432/4409-19', 69, '2017-12-19', '06:05:28', 40, 6.0),
	('06.025.833/0170-88', 50, '2017-9-16', '05:29:21', 35, 4.9),
	('02.059.648/4763-25', 33, '2017-3-2', '09:58:55', 1, 4.2),
	('90.465.421/0713-63', 57, '2018-5-10', '19:54:00', 20, 1.5),
	('48.328.049/2183-10', 53, '2018-9-3', '12:09:52', 25, 5.2),
	('67.717.709/5760-50', 32, '2017-2-21', '22:51:33', 13, 0.8),
	('71.328.725/7280-66', 75, '2017-1-23', '14:50:07', 29, 6.7),
	('15.932.569/3394-10', 23, '2017-1-16', '20:22:49', 13, 4.6),
	('22.323.793/8688-99', 15, '2017-7-2', '10:14:38', 41, 6.7),
	('11.034.406/6331-47', 11, '2018-6-4', '00:16:54', 37, 3.8),
	('781.245.184-40', 88, '2018-1-12', '01:39:12', 49, 1.8),
	('02.984.527/1287-82', 9, '2016-10-30', '13:44:47', 28, 2.2),
	('97.711.726/6953-00', 66, '2017-11-14', '07:49:21', 2, 5.0),
	('33.919.413/5511-97', 76, '2018-6-9', '21:50:53', 14, 5.5),
	('78.440.900/1662-07', 14, '2017-8-12', '23:26:21', 3, 6.4),
	('64.976.849/9365-23', 72, '2018-2-3', '19:10:28', 23, 2.6),
	('04.370.899/9570-23', 33, '2018-4-27', '07:23:48', 27, 4.6);

	INSERT INTO VENDA VALUES
	(1, '2018-8-17', '00:04:23', '503.977.886-49'),
	(2, '2017-10-30', '18:16:37', '543.031.325-43'),
	(3, '2018-5-16', '17:27:55', '192.283.160-39'),
	(4, '2017-5-4', '01:28:05', '938.320.985-26'),
	(5, '2018-8-17', '02:04:29', '360.902.402-06'),
	(6, '2016-11-22', '15:42:35', '995.106.177-09'),
	(7, '2017-3-23', '00:59:44', '480.796.652-90'),
	(8, '2016-11-4', '16:17:01', '487.832.626-36'),
	(9, '2017-11-9', '14:11:18', '586.822.245-85'),
	(10, '2017-7-14', '12:10:06', '493.684.111-07'),
	(11, '2017-8-7', '21:47:08', '970.122.418-37'),
	(12, '2016-12-22', '07:07:50', '959.031.846-00'),
	(13, '2017-9-26', '07:10:46', '543.031.325-43'),
	(14, '2017-11-7', '19:19:28', '493.684.111-07'),
	(15, '2017-5-13', '01:39:24', '675.071.897-32'),
	(16, '2017-3-27', '09:08:51', '581.002.072-08'),
	(17, '2017-6-25', '21:03:29', '959.031.846-00'),
	(18, '2018-4-28', '15:25:02', '402.246.463-11'),
	(19, '2017-12-13', '21:47:04', '774.236.197-36'),
	(20, '2018-1-10', '11:49:52', '218.003.800-38'),
	(21, '2018-5-17', '06:46:25', '289.081.666-45'),
	(22, '2017-9-5', '03:51:30', '874.524.521-51'),
	(23, '2018-7-20', '00:58:16', '298.322.674-39'),
	(24, '2017-1-28', '02:14:38', '051.049.739-05'),
	(25, '2017-8-10', '08:53:50', '592.189.369-21'),
	(26, '2018-4-3', '13:18:01', '128.318.589-09'),
	(27, '2018-2-25', '08:57:56', '293.690.116-25'),
	(28, '2017-10-7', '02:00:03', '360.902.402-06'),
	(29, '2018-1-30', '23:39:55', '117.291.560-10'),
	(30, '2017-10-25', '05:40:43', '477.023.447-33'),
	(31, '2018-2-3', '05:07:37', '476.119.804-40'),
	(32, '2017-3-5', '01:56:18', '543.031.325-43'),
	(33, '2018-1-14', '13:27:13', '117.291.560-10'),
	(34, '2017-12-3', '21:12:39', '995.106.177-09'),
	(35, '2017-1-27', '00:03:19', '581.002.072-08'),
	(36, '2018-7-4', '07:43:50', '986.418.387-75'),
	(37, '2018-2-8', '15:03:10', '289.081.666-45'),
	(38, '2017-5-2', '19:04:16', '883.382.447-08'),
	(39, '2017-12-19', '18:50:51', '208.664.918-56'),
	(40, '2016-11-7', '23:49:10', '874.524.521-51'),
	(41, '2017-8-24', '06:13:22', '477.023.447-33'),
	(42, '2017-2-26', '16:21:54', '887.450.522-12'),
	(43, '2018-7-4', '09:53:20', '569.154.071-89'),
	(44, '2016-10-20', '17:25:45', '883.382.447-08'),
	(45, '2017-3-12', '10:07:14', '208.664.918-56'),
	(46, '2017-8-21', '06:22:19', '809.181.088-10'),
	(47, '2017-4-24', '07:04:19', '742.933.399-06'),
	(48, '2017-9-9', '12:35:57', '901.363.990-96'),
	(49, '2018-2-27', '18:39:31', '521.588.578-89'),
	(50, '2018-3-20', '12:34:47', '293.690.116-25'),
	(51, '2018-1-3', '08:09:23', '108.844.854-20'),
	(52, '2017-8-8', '21:21:38', '562.175.036-54'),
	(53, '2017-1-3', '18:02:48', '442.847.425-31'),
	(54, '2017-3-23', '03:24:19', '227.345.725-16'),
	(55, '2018-7-1', '09:40:20', '261.156.571-64'),
	(56, '2018-4-6', '20:42:44', '680.184.160-28'),
	(57, '2017-7-9', '22:22:33', '742.933.399-06'),
	(58, '2017-11-28', '18:45:20', '480.796.652-90'),
	(59, '2017-5-2', '16:43:25', '675.071.897-32'),
	(60, '2018-2-24', '21:41:50', '298.322.674-39'),
	(61, '2017-4-24', '00:30:42', '493.684.111-07'),
	(62, '2016-12-10', '05:34:09', '728.299.197-93'),
	(63, '2018-2-25', '18:48:54', '636.541.312-20'),
	(64, '2018-1-8', '05:07:52', '043.307.895-23'),
	(65, '2018-8-29', '22:39:23', '428.464.848-99'),
	(66, '2018-4-19', '04:58:54', '176.489.865-66'),
	(67, '2018-4-14', '05:13:11', '680.184.160-28'),
	(68, '2017-5-28', '08:33:23', '476.119.804-40'),
	(69, '2017-8-22', '03:37:04', '897.094.953-48'),
	(70, '2017-9-26', '14:00:08', '191.144.047-02'),
	(71, '2017-3-30', '18:32:13', '364.045.102-35'),
	(72, '2016-11-10', '20:42:18', '487.832.626-36'),
	(73, '2017-9-1', '00:53:59', '051.049.739-05'),
	(74, '2017-1-18', '00:42:36', '901.363.990-96'),
	(75, '2016-10-21', '15:44:16', '360.902.402-06'),
	(76, '2017-7-16', '02:47:46', '938.320.985-26'),
	(77, '2018-6-18', '21:15:42', '442.847.425-31'),
	(78, '2017-5-31', '22:18:45', '027.480.123-05'),
	(79, '2018-4-3', '08:27:23', '455.254.563-97'),
	(80, '2018-9-19', '20:48:11', '455.254.563-97'),
	(81, '2018-10-3', '00:12:47', '909.320.903-54'),
	(82, '2017-1-27', '13:31:55', '095.725.968-96'),
	(83, '2017-7-31', '05:55:40', '218.003.800-38'),
	(84, '2017-10-30', '04:46:42', '559.453.538-17'),
	(85, '2017-2-15', '04:09:34', '402.246.463-11'),
	(86, '2017-11-22', '16:48:52', '682.453.539-73'),
	(87, '2018-10-2', '04:05:57', '602.150.938-28'),
	(88, '2017-11-14', '02:28:48', '682.453.539-73'),
	(89, '2018-9-11', '08:29:08', '126.465.446-42'),
	(90, '2017-3-8', '04:21:00', '970.122.418-37'),
	(91, '2018-8-5', '15:02:22', '675.071.897-32'),
	(92, '2018-9-21', '12:42:35', '682.112.737-99'),
	(93, '2018-6-16', '21:37:09', '193.648.568-05'),
	(94, '2016-11-23', '05:30:50', '901.363.990-96'),
	(95, '2018-3-30', '17:06:36', '176.489.865-66'),
	(96, '2016-11-12', '23:49:12', '477.023.447-33'),
	(97, '2017-1-10', '12:32:46', '020.879.003-96'),
	(98, '2018-5-29', '08:12:54', '897.094.953-48'),
	(99, '2018-8-6', '12:49:00', '274.442.369-68'),
	(100, '2017-5-30', '00:30:10', '218.003.800-38');

	INSERT INTO VENDA_PRODUTO VALUES
	(62, 4, 2.4),
	(64, 24, 1.2),
	(14, 42, 1.1),
	(5, 96, 0.5),
	(41, 53, 0.9),
	(22, 58, 1.5),
	(68, 98, 1.4),
	(71, 70, 2.0),
	(67, 76, 0.7),
	(11, 83, 2.4),
	(35, 38, 0.1),
	(5, 74, 2.2),
	(64, 19, 1.3),
	(33, 66, 1.0),
	(71, 97, 1.2),
	(91, 41, 1.2),
	(92, 25, 1.4),
	(48, 92, 1.7),
	(38, 10, 0.1),
	(88, 16, 0.3),
	(80, 14, 1.2),
	(29, 83, 0.2),
	(30, 89, 2.9),
	(61, 64, 1.8),
	(45, 60, 2.2),
	(54, 25, 0.6),
	(77, 12, 0.8),
	(77, 77, 2.8),
	(56, 55, 1.8),
	(87, 72, 2.0),
	(61, 94, 3.0),
	(6, 35, 1.7),
	(11, 32, 0.9),
	(53, 45, 1.9),
	(35, 60, 3.0),
	(76, 69, 0.7),
	(99, 50, 0.1),
	(93, 91, 0.6),
	(90, 26, 2.6),
	(87, 39, 0.6),
	(78, 38, 2.4),
	(92, 28, 1.3),
	(45, 66, 2.8),
	(54, 76, 2.2),
	(63, 38, 1.3),
	(77, 77, 1.9),
	(37, 93, 0.2),
	(59, 35, 2.8),
	(50, 95, 1.4),
	(90, 96, 1.4);

	INSERT INTO CONTATO_FORNECEDOR VALUES
	(1, '+55 (021) 4491 2934', '100.973.580-29', 1),
	(2, '+55 (021) 4371-0909', '781.245.184-40', 1),
	(3, '41 5722 7881', '277.315.375-87', 1),
	(4, '+55 11 4649-3727', '73.146.873/6990-52', 1),
	(5, '61 2791-5451', '11.795.090/5557-17', 1),
	(6, '+55 (071) 8173 0422', '23.937.977/1806-05', 1),
	(7, '(051) 5092-1815', '88.485.809/6229-50', 1),
	(8, '31 4417 1366', '85.543.393/1625-40', 1),
	(9, '+55 (031) 5010 5669', '84.581.712/9436-05', 1),
	(10, '+55 21 5381-3676', '70.402.893/4672-71', 1),
	(11, '51 129 1034', '64.915.583/9842-36', 1),
	(12, '21 7926-3434', '70.549.729/7374-26', 1),
	(13, '+55 51 662 2380', '07.007.581/6319-81', 1),
	(14, '21 4921-6618', '98.358.394/2040-72', 1),
	(15, '(071) 4873-3627', '22.323.793/8688-99', 1),
	(16, '+55 (031) 8386-1635', '47.747.905/4651-53', 1),
	(17, '(051) 7137-2265', '11.034.406/6331-47', 1),
	(18, '+55 (011) 3703 0376', '97.273.164/1628-84', 1),
	(19, '(051) 8891-1304', '44.835.073/5577-69', 1),
	(20, '+55 (041) 1940-9309', '16.947.184/9819-65', 1),
	(21, '(041) 3791 7864', '98.713.604/0853-12', 1),
	(22, '61 2330 3197', '06.045.166/6050-10', 1),
	(23, '+55 (061) 2435 9874', '56.208.130/2496-06', 1),
	(24, '31 3181 4508', '33.919.413/5511-97', 1),
	(25, '+55 51 715 5831', '11.454.766/8092-39', 1),
	(26, '+55 31 5928-7429', '73.291.809/3985-37', 1),
	(27, '31 9907-7022', '72.765.004/8577-22', 1),
	(28, '81 2590 0466', '06.217.954/2750-71', 1),
	(29, '+55 (081) 3146 0810', '68.926.971/7135-98', 1),
	(30, '(011) 6855 0724', '07.819.576/1312-29', 1),
	(31, '71 5920-4276', '53.293.511/6491-44', 1),
	(32, '81 9929-9929', '84.339.811/3490-07', 1),
	(33, '11 0012-7426', '97.711.726/6953-00', 1),
	(34, '51 095 8954', '48.328.049/2183-10', 1),
	(35, '+55 (031) 9560 8306', '64.976.849/9365-23', 1),
	(36, '41 1826-6911', '22.352.107/7239-15', 1),
	(37, '81 0411-4899', '02.357.393/3970-88', 1),
	(38, '+55 11 9620 0593', '05.095.078/0906-30', 1),
	(39, '31 8675 6694', '38.124.301/1142-94', 1),
	(40, '+55 81 6445-7193', '18.831.608/3434-03', 1),
	(41, '+55 61 0560 6202', '29.068.782/3837-66', 1),
	(42, '+55 71 1304-3484', '22.433.349/6540-01', 1),
	(43, '81 5483 7319', '84.540.585/3190-21', 1),
	(44, '81 4965-8670', '74.056.082/4785-02', 1),
	(45, '+55 (081) 5090-1436', '04.370.899/9570-23', 1),
	(46, '(031) 5931-2778', '56.380.407/3394-02', 1),
	(47, '+55 (011) 7318 6968', '28.422.429/2139-39', 1),
	(48, '+55 71 5251 5003', '20.802.069/5550-16', 1),
	(49, '+55 (021) 3221-5697', '41.900.454/1097-00', 1),
	(50, '61 8643 6509', '82.256.860/7907-09', 1),
	(51, '(081) 2717-0933', '54.549.266/2345-33', 1),
	(52, '(081) 3510 6428', '97.322.164/7356-14', 1),
	(53, '+55 (061) 5682 3454', '10.507.365/8503-85', 1),
	(54, '71 4871 5834', '23.856.760/7963-53', 1),
	(55, '+55 (051) 7219 5931', '89.936.340/3573-91', 1),
	(56, '+55 (031) 8040-9163', '46.825.729/5937-51', 1),
	(57, '(071) 5930 1480', '79.460.664/7483-76', 1),
	(58, '+55 41 4904-3679', '79.315.423/8747-11', 1),
	(59, '(071) 1097-8554', '01.059.020/2794-56', 1),
	(60, '+55 (031) 7739-5168', '84.428.432/7582-52', 1),
	(61, '+55 21 3240-8865', '07.293.879/9225-41', 1),
	(62, '+55 21 1804 5451', '38.973.389/4931-39', 1),
	(63, '11 6812-6966', '71.150.726/0688-96', 1),
	(64, '+55 61 4879-8462', '67.717.709/5760-50', 1),
	(65, '+55 (051) 1732-3333', '68.328.795/7689-07', 1),
	(66, '(031) 0017-4962', '60.646.070/3907-74', 1),
	(67, '(021) 2607 3380', '56.223.378/2229-42', 1),
	(68, '71 6618 9895', '59.381.457/8845-06', 1),
	(69, '+55 (071) 5006 1305', '40.075.585/7684-12', 1),
	(70, '+55 71 3999-7052', '03.600.515/0484-07', 1),
	(71, '+55 (061) 7769-7804', '44.920.432/4409-19', 1),
	(72, '81 4787-8282', '45.831.290/7823-56', 1),
	(73, '(011) 2555-3976', '16.073.821/4462-85', 1),
	(74, '+55 (061) 0433-4930', '15.932.569/3394-10', 1),
	(75, '11 3158 6677', '37.804.067/0956-37', 1),
	(76, '+55 21 6861-7846', '26.941.738/9900-23', 1),
	(77, '61 1134 5917', '01.560.639/7251-64', 1),
	(78, '+55 11 8850-4646', '95.776.695/3314-88', 1),
	(79, '(061) 1637-3384', '26.593.635/6363-56', 1),
	(80, '+55 41 8953 2741', '89.070.202/7783-94', 1),
	(81, '(081) 8340 4869', '71.328.725/7280-66', 1),
	(82, '+55 (051) 3100 7374', '05.727.536/9986-83', 1),
	(83, '+55 (071) 3257 9045', '80.074.691/8229-72', 1),
	(84, '+55 (051) 2868 2733', '90.465.421/0713-63', 1),
	(85, '+55 81 5668-5387', '02.059.648/4763-25', 1),
	(86, '+55 51 455 6349', '46.185.233/4935-45', 1),
	(87, '+55 (021) 2092 8060', '78.440.900/1662-07', 1),
	(88, '+55 (051) 4522-1052', '13.818.067/1028-53', 1),
	(89, '11 5006-2278', '45.023.221/1140-46', 1),
	(90, '+55 61 0291 0423', '76.680.896/6201-16', 1),
	(91, '+55 81 1794 8223', '06.025.833/0170-88', 1),
	(92, '+55 (061) 7889 4825', '87.896.565/7373-25', 1),
	(93, '+55 (041) 8464 8631', '38.604.625/4002-30', 1),
	(94, '+55 (011) 7091-7031', '75.946.122/5806-69', 1),
	(95, '(061) 4635-7925', '16.006.416/0092-94', 1),
	(96, '31 7361 3424', '38.275.756/6301-36', 1),
	(97, '+55 71 8942-2360', '22.923.768/6897-55', 1),
	(98, '+55 51 627 1147', '04.963.065/1999-25', 1),
	(99, '(011) 6807 1337', '46.230.735/3474-80', 1),
	(100, '61 5321 9464', '02.984.527/1287-82', 1);

	INSERT INTO CONTATO_CLIENTE VALUES
	(1, '+55 71 5177 9477', '365.728.948-86', 1),
	(2, '41 3406 9232', '192.154.940-81', 1),
	(3, '+55 41 1529 1166', '051.049.739-05', 1),
	(4, '+55 71 5282-3157', '562.175.036-54', 1),
	(5, '+55 11 9719-9745', '196.083.621-80', 1),
	(6, '(071) 4858 4764', '293.690.116-25', 1),
	(7, '+55 (021) 9097-4517', '909.320.903-54', 1),
	(8, '+55 41 5996-3170', '442.847.425-31', 1),
	(9, '21 1399-1803', '661.660.624-43', 1),
	(10, '2150 4829', '218.003.800-38', 1),
	(11, '+55 21 5192-1429', '161.591.311-41', 1),
	(12, '+55 (051) 4538-4476', '592.189.369-21', 1),
	(13, '(011) 2885 8018', '807.147.057-05', 1),
	(14, '+55 61 8847-7129', '101.923.093-23', 1),
	(15, '+55 41 8525-1430', '986.418.387-75', 1),
	(16, '21 1945-9484', '954.897.650-11', 1),
	(17, '9643 6244', '533.897.771-05', 1),
	(18, '3817-7300', '242.027.503-90', 1),
	(19, '(081) 3058 3186', '761.312.625-00', 1),
	(20, '81 2215 0542', '318.624.060-30', 1),
	(21, '(061) 0084-6338', '430.206.866-36', 1),
	(22, '+55 31 9874 0098', '428.464.848-99', 1),
	(23, '+55 (041) 6812 1528', '959.031.846-00', 1),
	(24, '+55 (071) 8224 0272', '289.081.666-45', 1),
	(25, '+55 21 7149-3242', '630.703.207-32', 1),
	(26, '51 016 8674', '710.164.760-00', 1),
	(27, '+55 (021) 4925 7099', '552.934.949-88', 1),
	(28, '+55 41 9193-9628', '944.344.086-58', 1),
	(29, '81 9527-8455', '020.879.003-96', 1),
	(30, '51 645 9351', '970.122.418-37', 1),
	(31, '+55 41 3802 2837', '636.541.312-20', 1),
	(32, '31 3285-3051', '602.150.938-28', 1),
	(33, '(061) 5251 4385', '226.968.600-41', 1),
	(34, '41 2209-1638', '517.146.035-39', 1),
	(35, '(061) 7615 7492', '897.094.953-48', 1),
	(36, '(021) 7998 5089', '193.648.568-05', 1),
	(37, '(021) 8195-1305', '208.664.918-56', 1),
	(38, '31 6991-3707', '630.507.657-04', 1),
	(39, '+55 (041) 1147-2202', '521.588.578-89', 1),
	(40, '21 1426 8783', '454.849.805-26', 1),
	(41, '(081) 5037-9756', '126.465.446-42', 1),
	(42, '41 2385-4083', '788.378.234-79', 1),
	(43, '(041) 6698-2541', '020.478.274-00', 1),
	(44, '11 9416-3493', '938.320.985-26', 1),
	(45, '(071) 9945-3408', '266.600.930-01', 1),
	(46, '21 0867-9048', '761.322.769-39', 1),
	(47, '(081) 0682 7107', '374.914.799-01', 1),
	(48, '+55 21 4646 9595', '176.489.865-66', 1),
	(49, '+55 (051) 5112 1115', '477.023.447-33', 1),
	(50, '+55 (041) 6132 9422', '261.156.571-64', 1),
	(51, '+55 51 175 9331', '174.767.513-02', 1),
	(52, '+55 61 6604 2277', '127.754.185-03', 1),
	(53, '21 9650-4662', '095.725.968-96', 1),
	(54, '(051) 7470 0119', '227.345.725-16', 1),
	(55, '+55 (051) 3139 9499', '287.649.002-15', 1),
	(56, '+55 81 2307-6504', '742.933.399-06', 1),
	(57, '(021) 2987-0632', '586.822.245-85', 1),
	(58, '1533-7468', '809.181.088-10', 1),
	(59, '+55 81 9738 0215', '485.407.175-30', 1),
	(60, '(021) 7576-6019', '035.703.579-88', 1),
	(61, '+55 (071) 8927 5608', '032.505.905-50', 1),
	(62, '11 6581 2973', '128.318.589-09', 1),
	(63, '11 9838 6534', '219.549.192-20', 1),
	(64, '+55 (041) 4429-7485', '476.119.804-40', 1),
	(65, '+55 61 2052-4560', '480.796.652-90', 1),
	(66, '+55 (021) 3239-9961', '192.283.160-39', 1),
	(67, '+55 41 8709-9872', '402.246.463-11', 1),
	(68, '+55 61 8436-8308', '901.363.990-96', 1),
	(69, '(041) 8536 5498', '298.322.674-39', 1),
	(70, '+55 81 7652-5808', '147.988.057-42', 1),
	(71, '+55 (011) 1507 8955', '191.144.047-02', 1),
	(72, '+55 51 338 9054', '338.640.851-60', 1),
	(73, '(081) 1400-9483', '774.236.197-36', 1),
	(74, '+55 (031) 2177 9748', '581.002.072-08', 1),
	(75, '71 5363-4035', '493.684.111-07', 1),
	(76, '(061) 1609-4430', '455.254.563-97', 1),
	(77, '+55 (081) 3292 6731', '274.442.369-68', 1),
	(78, '(051) 3985-5976', '559.453.538-17', 1),
	(79, '+55 (061) 7470-5752', '707.929.509-25', 1),
	(80, '+55 81 2636 3308', '682.112.737-99', 1),
	(81, '(081) 6634-4845', '493.595.641-09', 1),
	(82, '81 7428-5708', '487.832.626-36', 1),
	(83, '51 144 6585', '043.307.895-23', 1),
	(84, '(061) 3060-9424', '680.184.160-28', 1),
	(85, '+55 21 1194 7290', '136.818.661-04', 1),
	(86, '(061) 7022 0868', '543.031.325-43', 1),
	(87, '+55 51 896 2341', '905.180.103-33', 1),
	(88, '+55 (081) 2318-9899', '445.247.565-58', 1),
	(89, '(061) 7107 0752', '887.450.522-12', 1),
	(90, '(071) 8379-3132', '874.524.521-51', 1),
	(91, '(051) 1408 3454', '108.844.854-20', 1),
	(92, '+55 11 4787 2647', '995.106.177-09', 1),
	(93, '+55 21 8034-6419', '675.071.897-32', 1),
	(94, '+55 (051) 9982 8724', '954.840.995-01', 1),
	(95, '+55 (081) 5768 2700', '032.609.977-84', 1),
	(96, '21 0278 3084', '503.977.886-49', 1),
	(97, '+55 (011) 2565-3344', '576.766.726-86', 1),
	(98, '41 2609-9642', '117.291.560-10', 1),
	(99, '+55 21 3721 7159', '364.045.102-35', 1),
	(100, '41 1040-3361', '883.382.447-08', 1),
	(101, '51 809 9892', '027.480.123-05', 1),
	(102, '21 5376 9982', '569.154.071-89', 1),
	(103, '(021) 7267 1666', '682.453.539-73', 1),
	(104, '(061) 6400-6487', '608.706.384-67', 1),
	(105, '+55 (021) 4574 9878', '728.299.197-93', 1),
	(106, '(081) 6282-1851', '360.902.402-06', 1);

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


        
        


    






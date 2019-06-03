# TRABALHO 01:  SmartSales
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado.

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Beatriz Auer Mariano: biaauer03@gmail.com<br>
Júlia Suzano Fraga: juliasufraga18@gmail.com<br>


### 2.INTRODUÇÃO E MOTIVAÇAO<br>

> A empresa SmartSales visa auxiliar a gestão de estoques, desde miniempresas a grandes negócios. Sabe-se que é demandado muito tempo para listar, estocar e fazer o balanço financeiro de uma empresa, o que pode resultar em falhas e, consequentemente, prejuízos. Sendo assim, nós da SmartSales temos como objetivo servir de apoio para o empresário, a fim de agilizar certos processos e contribuir no aumento da lucratividade. Após o cadastro de informações, que podem ser feitos manualmente ou por meio de sensores no estoque físico o sistema gerará relatórios que atenderão aos interesses do cliente.
 

### 3.MINI-MUNDO Novo<br>

> O sistema proposto para a SmartSales conterá as informações aqui detalhadas. Inicialmente, serão cadastrados o código dos produtos da empresa, o nome de cada produto, a quantidade comprada e em estoque de cada um, o preço de compra e de venda e o fornecedor do produto.
Durante um período de tempo, serão contabilizados quais produtos e em que quantidade foram vendidos, possibilitando uma contagem e controle de estoque. Como um dos objetivos do sistema proposto é identificar o lucro final obtido pela venda dos produtos, também serão contabilizados o valor da venda, incluso o desconto, se tiver. Essas informações poderão ser acessadas pelos funcionários a fim de maximizar o atendimento ao cliente, por exemplo, ao invés de ir até o estoque físico para verificar se um produto está em falta ou não, bastará apenas acessar o sistema. Por fim, o programa gerará um balanço financeiro do intervalo de tempo que pode ser escolhido entre o dia, a semana ou o mês. Esse balanço informará qual o gasto total da empresa com a compra de produtos, qual o lucro e/ou o prejuízo que obteve e qual o percentual de venda de cada produto. A partir desse percentual, o programa apresentará os produtos que mais foram vendidos e aqueles que tiveram menos procura. Caso o usuário informe um lucro esperado para determinado produto, o balanço financeiro também informará se essa margem foi alcançada ou não. Essas informações constarão em uma tabela e serão referentes a todos os produtos cadastrados. Essa parte será acessível apenas para o gestor de vendas, gerente e/ou dono da empresa.


### 4. RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto consta o pdf com o rascunho da interface do nosso programa. <br>

![Alt text](https://github.com/20181tiimi0014/trabalho01/blob/master/mockup.png?raw=true "Interface SS")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Devcom](https://github.com/20181tiimi0014/trabalho01/blob/master/SmartSales.pdf?raw=true "SmartSales")

### 4.1 RELATÓRIOS

> Para que o programa seja iniciado, ele precisa dos seguintes relatórios:
* Informação do produto com código, nome, preço de compra, preço de venda, quantidade comprada e fornecedor. Caso seja a primeira vez que o produto seja comprado, ele será inserido à tabela dos produtos. Caso não, a quantidade será somada a já existente.
* Informações dos fornecedores, com código, nome, ramo, produto e contato.
>Para que funcione, precisa dos seguintes relatórios:
* Nota fiscal, contendo o código do produto, a quantidade vendida, o preço e o desconto, se houver.
> Ao final, serão gerados os seguintes relatórios:
* Relatório do estoque contendo os produtos, a quantidade em estoque, a quantidade vendida e percentual de produtos vendidos.
* Relatório financeiro, contendo o rendimento de cada produto: percentual de quanto foi vendido em comparação com o que foi comprado, lucro ou prejuízo obtido, percentual de lucro.
> Com esses relatórios, o sistema consegue responder às seguintes perguntas:
* Quantos e quais produtos estão em estoque e foram vendidos;
* Quanto foi a despesa e o lucro com os produtos;
* Quais os produtos mais e menos vendidos.
 
### 4.2 TABELA DE DADOS DO SISTEMA:

> A tabela aqui anexada contém os atributos do sistema SmartSales. Ela simula um relatório com todos os dados que serão armazenados.

    PRODUTOS: tabela que contém as informações de todos os produtos comercializados pela empresa.
    FORNECEDORES: tabela que contém as informações de todos os fornecedores da loja.
    VENDAS: tabela que contém as informações de todas as vendas em um certo período. É importante para calcular o lucro e o número de produtos vendidos.
    ESTOQUE: tabela que contém as informações dos produtos que estão em estoque e dos que estão esgotados.
    FINCANÇAS: tabela que contém um relatório dos resultados das vendas realizadas pela empresa.
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>
    
![Exemplo de Tabela de dados da Empresa SmartSales](https://github.com/20181tiimi0014/trabalho01/blob/master/PlanilhaSmartsSales.ods?raw=true "Tabela - Empresa SmartSales")

### 5.MODELO CONCEITUAL<br>

> O modelo conceitual apresenta as entidades existentes no programa e os relacionamentos que elas possuem entre si.
        
![Modelo Conceitual](https://github.com/20181tiimi0014/trabalho01/blob/master/modeloConceitual.png?raw=true "Modelo Conceitual SmartSales")

### 5.1 DESCRIÇÃO DOS DADOS

    CODIGO: Campo que armazena os códigos de cada produto.
    PRODUTO: Campo que armazena os nomes de cada produto .
    FORNECEDOR: Campo que armazena os nomes dos fornecedores de cada produto.
    DATA_COMPRA: Campo que armazena as datas de compra dos produtos.
    PRECO_COMPRA: Campo que armazena os preços de compra de cada produto.
    PRECO_VENDA: Campo que armazena os preços de venda de cada produto.
   
    NUMERO_NOTA: Campo que armazena o código de identificação da nota fiscal emitida ao final da venda de produtos.
    QUANTIDADE_VENDA: Campo que armazena a quantidade de vendida de cada produto.
    DESCONTO: Campo que armazena os descontos que cada produto tem.
    VALOR_TOTAL: Campo que armazena os preços finais de venda (levando em consideração qualquer acréscimo ou decréscimo em cima do preço de venda).

    QUANTIDADE_COMPRADA: Campo que armazena a quantidade comprada pela empresa do fornecedor.
    QUANTIDADE_ESTOQUE: Campo que armazena a quantidade restante de cada produto no estoque.
    PERCENTUAL_VENDIDO: Campo que armazena o percentual de quantidade de produtos vendidos em relação a quantidade comprada.
    QUANTIDADE_VENDA: Campo que armazena a quantidade de vendida de cada produto.
    
    GASTO: Campo que armazena o valor total pago pela empresa na compra de cada tipo de produto pelo fornecedor.
    LUCRO: Campo que armazena o percentual de lucro obtido pela empresa sobre a venda de cada produto.
    CNPJ: Campo que armazena o Cadastro Nacional da Pessoa Jurídica de cada fornecedor.
    NOME: Campo que armazena o nome de cada empresa fornecedora.
    RAMO: Campo que armazena o tipo de mercadoria que a empresa produz.
    ENDERECO: Campo que armazena o endereço do fornecedor.
    CONTATO: Campo que armazena o contato do fornecedor.

### 6	MODELO LÓGICO<br>

> Aqui consta o modelo lógico do nosso banco de dados.

![Modelo Lógico SmartSales](https://github.com/20181tiimi0014/trabalho01/blob/master/modeloLogico.png?raw=true "Modelo Lógico - Empresa SmartSales")

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas DDL 
        (criação de tabelas, alterações, etc..)          

## Marco de Entrega 07 em: (27/05/2019)<br>

### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físic
        b) formato .SQL

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (create para tabelas e estruturas de dados + dados a serem inseridos)
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
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
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


        
        


    






<h1>Diagrama Entidade Relacionamento (DER) no MySQL Workbench</h1>

Um **Diagrama Entidade Relacionamento** (DER) é um Fluxograma que ilustra como as “**Entidades**” (Usuários, Produtos, Postagens), se relacionam entre si dentro de um sistema de Banco de dados Relacional.

Os Diagramas DER são usados principalmente para modelar e criar bancos de dados relacionais, em termos de regras lógicas e regras de negócio dentro de um modelo lógico de dados.

<h2>1.1. Componentes</h2>

**Entidade:**  Algo que pode ser definido e que pode ter dados armazenados sobre ele — como uma pessoa, um objeto, conceito ou evento. Pense em entidades como substantivos. **Exemplos:** um cliente, estudante, carro ou produto. Normalmente representado por um retângulo.

<div align="center"><img src="https://i.imgur.com/z3Yebz0.png" title="source: imgur.com" /></div>

**Relacionamento:** Como entidades atuam umas sobre as outras ou  estão associadas uma com a outra. Pense em relacionamentos como verbos. **Exemplo:** o estudante pode se inscrever em um curso. As duas  entidades seriam o aluno e o curso, e o relacionamento descrito é o ato de matricular-se, assim conectando as duas entidades. Relacionamentos  são tipicamente representados por linhas de ligação.

**Cardinalidade**: Define os atributos numéricos da relação entre duas entidades ou conjuntos de entidades. Os três  principais relacionamentos cardinais são **um-para-um (1:1)**, **um-para-muitos (1:N)** e  **muitos-para-muitos (N:M)**. Um **exemplo de um-para-um** seria um estudante associado a um endereço de correspondência. Um **exemplo de um-para-muitos (ou muitos-para-um, dependendo do sentido da relação):** um estudante se inscreve para vários cursos, mas todos esses cursos têm uma única linha que leva de volta ao aluno. **Exemplo de muitos-para-muitos:** estudantes como um grupo são associados a vários membros do corpo docente, e  membros do corpo docente, por sua vez, são associados a vários alunos. Abaixo temos os símbolos que representam a cardinalidade:

<div align="center"><img src="https://i.imgur.com/ZVkyJnm.png" title="source: imgur.com" /></div>

Na figura abaixo, temos um exemplo de Diagrama DER com Relacionamento:

<div align="center"><img src="https://i.imgur.com/1SE0uXI.png" title="source: imgur.com" /></div>

<h1>2. Criando o DER no MySQL Workbench</h1>

Vamos Criar o Diagrama Entidade Relacionamento de uma Loja de Games, seguindo o modelo abaixo, no MySQL Workbench:

<div align="center"><img src="https://i.imgur.com/drAm4Ga.png" title="source: imgur.com" /></div>

<h2>👣 Passo 01 - Iniciando o Modelo</h2>

1. Abra o **MySQL Workbench**

<div align="center"><img src="https://i.imgur.com/TRNizKc.png" title="source: imgur.com" /></div>

2. No menu lateral, do lado esquerdo superior do Workbench, clique no 2º ícone (**Models**)

<div align="center"><img src="https://i.imgur.com/cXW5UT8.png?1" title="source: imgur.com" /></div>

3. Será aberta a aberta a janela **Models**. Clique no botão <img src="https://i.imgur.com/YyUantg.png" title="source: imgur.com" /> para adicionar um novo **Modelo**.

<div align="center"><img src="https://i.imgur.com/XFzSp5B.png" title="source: imgur.com" /></div>

4. Na Guia **Physical of Schemas**, dê um duplo clique sobre **mydb** para **alterar o nome do Banco de dados**.

<div align="center"><img src="https://i.imgur.com/K5mRtoL.png?1" title="source: imgur.com" /></div>

5. Vamos alterar o nome do Banco de dados para **db_loja_games**.

<div align="center"><img src="https://i.imgur.com/9yP0fm9.png?1" title="source: imgur.com" /></div>

6. Vamos adicionar um novo Diagrama no Modelo. Clique no ícone **Add Diagram**.

<div align="center"><img src="https://i.imgur.com/PSjKjSr.png?1" title="source: imgur.com" /></div>

Antes de começar a criar o DER, vamos configurar alguns itens do Workbench.

1. No menu **File**, clique na opção **Page Setup...** para configurar a página

<div align="center"><img src="https://i.imgur.com/zPRT2aS.png" title="source: imgur.com" /></div>

2. Configure igual a figura abaixo e clique em **OK** para concluir:

<div align="center"><img src="https://i.imgur.com/nkKCaBz.png" title="source: imgur.com" /></div>

3. No menu **Edit**, clique na opção **Preferences** para configurar o Modelo de dados

<div align="center"><img src="https://i.imgur.com/D6PKC9W.png" title="source: imgur.com" /></div>

4. Na guia **Modeling 🡪 Defaults**, configure igual a figura abaixo e clique em **OK** para concluir.

<div align="center"><img src="https://i.imgur.com/muNl0he.png" title="source: imgur.com" /></div>

5. No menu **Model**, clique na opção **Diagram Properties and Size...** para configurar Diagrama

<div align="center"><img src="https://i.imgur.com/Qz7Mh7f.png" title="source: imgur.com" /></div>

6. No item **Name**, informe o nome do Diagrama (**loja_games**) e as propriedades **Width e Height**, vamos configurar ambas com o valor **1** (numero de páginas). Clique em **OK** para concluir.

<div align="center"><img src="https://i.imgur.com/r35dljw.png" title="source: imgur.com" /></div>

<h2>👣 Passo 02 - Criar as Tabelas</h2>

1. Na janela **Diagram**, clique no botão <img src="https://i.imgur.com/bsBXqQG.png" title="source: imgur.com" /> **Place a New Table**, para adicionar uma nova tabela (Entidade) no Diagrama.

<div align="center"><img src="https://i.imgur.com/Mh8geus.png" title="source: imgur.com" /></div>

2. Dê um clique sobre a tela do Diagrama para adicionar a tabela. Para **Editar a tabela**, dê um duplo clique sobre ela.

<div align="center"><img src="https://i.imgur.com/6Oatt5x.png" title="source: imgur.com" /></div>

3. No item **Table Name**, informe o nome da tabela (**tb_categorias**)

<div align="center"><img src="https://i.imgur.com/XQXw8Tg.png?1" title="source: imgur.com" /></div>

4. Para inserir o primeiro atributo da tabela, clique abaixo da coluna Column Name. Observe que o Workbench irá sugerir  o atributo **id** (Chave primária) no formato **BIGINT**. Marque as opções **PK, NN e AI**.

<div align="center"><img src="https://i.imgur.com/HDzYOrI.png" title="source: imgur.com" /></div>

**Opções do atributo:**

| Opção                    | Descrição                                                    |
| ------------------------ | ------------------------------------------------------------ |
| **PK**                   | **Primary Key** 🡪 Chave Primária                             |
| **NN**                   | **Not Null** 🡪 Não pode ser Nulo                             |
| **UQ**                   | **Unique** 🡪 Index Impõe a exclusividade de valores em uma ou mais colunas, além da Chave Primária |
| **B**                    | **Binary** 🡪 Armazena atributos binários ( 0 1)              |
| **UN**                   | **Unsigned Data Type** 🡪 Permite apenas numeros positivos inteiros |
| **ZF**                   | **Zero Fill** 🡪 Preencher numeros inteiros com zeros. **Exemplo:** int(5) = 00001 |
| **AI**                   | **Auto Increment** 🡪 Configurar a Chave Primária como Auto Incremento |
| **G**                    | **Generated Column** 🡪 Gerar colunas com cálculos ou outros valores específicos. |
| Expression <br />Default | Valor Padrão ou a Exprerssão da opção Generated Column.      |


5. Clique na linha de baixo para inserir o segundo atributo. Observe que será sugerido o atributo **col** no formato **varchar(255)**, como mostra a figura abaixo:

<div align="center"><img src="https://i.imgur.com/rF41eMF.png" title="source: imgur.com" /></div>

6. Vamos alterar o nome do atributo para **tipo** e mater o formato. Marque apenas a opção **NN**.

<div align="center"><img src="https://i.imgur.com/ONQWUH3.png" title="source: imgur.com" /></div>

7. Primeira Tabela finalizada, vamos fechar a guia da tabela tb_categorias. Veja o nosso DER com a primeira tabela na figura abaixo:

<div align="center"><img src="https://i.imgur.com/BUFEbQY.png" title="source: imgur.com" /></div>

8. Vamos criar a segunda tabela (**tb_usuarios**), igual a figura abaixo. Siga os passos de 1 a 7 para construir a tabela.

<div align="center"><img src="https://i.imgur.com/XQAdJNC.png" title="source: imgur.com" /></div>

9. Segunda Tabela finalizada, vamos fechar a guia da tabela tb_usuarios. Veja o nosso DER com as duas tabelas na figura abaixo:

<div align="center"><img src="https://i.imgur.com/KUI69cL.png" title="source: imgur.com" /></div>

10. Vamos criar a terceira tabela (**tb_produtos**), igual a figura abaixo. Siga os passos de 1 a 7 para construir a tabela.

<div align="center"><img src="https://i.imgur.com/1SwOgtQ.png" title="source: imgur.com" /></div>

11. Observe que não criamos os atributos **categoria_id e usuario_id**, que são as **chaves estrangeiras** da tabela tb_produtos. Faremos isso no próximo passo. Veja o nosso DER com as 3 tabelas na figura abaixo: 

<div align="center"><img src="https://i.imgur.com/uIIxkBN.png" title="source: imgur.com" /></div>

<h2>👣 Passo 03 - Criar os Relacionamentos</h2>

1. Vamos Criar o primeiro relacionamento (**categoria_id 🡪 id**). Este relacionamento será do tipo um para muitos (1:N). Clique no botão <img src="https://i.imgur.com/Or0HEas.png" title="source: imgur.com" /> (**Place new 1:N Relationship Indentify**). Clique sobre a tabela **tb_produtos** e depois clique sobre a tabela **tb_categorias**.

<div align="center"><img src="https://i.imgur.com/EgAbsgD.png" title="source: imgur.com" /></div>

2. A Chave Estrangeira e o Relacionamento foram criados automaticamente. Observe apenas que o nome do atributo Chave estrangeira está um pouco diferente. Dê um duplo clique sobre a Tabela tb_produtos e altere o nome do atributo **Chave Estrangeira** para **categoria_id** e desmarque a opção **PK e NN**, como mostra a figura abaixo:

<div align="center"><img src="https://i.imgur.com/65ckWjw.png" title="source: imgur.com" /></div>

3. Vamos Criar o segundo relacionamento (**usuario_id 🡪 id**). Este relacionamento será do tipo um para muitos (1:N). Clique no botão <img src="https://i.imgur.com/Or0HEas.png" title="source: imgur.com" /> (**Place new 1:N Relationship Indentify**). Clique sobre a tabela **tb_produtos** e depois clique sobre a tabela **tb_usuarios**.

<div align="center"><img src="https://i.imgur.com/IhidWRc.png" title="source: imgur.com" /></div>

4. A Chave Estrangeira e o Relacionamento foram criados automaticamente. Observe apenas que o nome do atributo Chave estrangeira está um pouco diferente. Dê um duplo clique sobre a Tabela tb_produtos e altere o nome do atributo **Chave Estrangeira** para **usuario_id** e desmarque a opção **PK e NN**, como mostra a figura abaixo:

<div align="center"><img src="https://i.imgur.com/P4lB3iJ.png" title="source: imgur.com" /></div>

5. Na figura abaixo você confere o resultado final. Observe que as linhas do Relacionamento estão pontilhadas, o que indica que o atributo chave estrangeira pode ser nulo. 

<div align="center"><img src="https://i.imgur.com/apjYdON.png" title="source: imgur.com" /></div>

6. Para finalizar, Salve o Modelo. No menu **File**, clique na opção **Save Model** 

<div align="center"><img src="https://i.imgur.com/iXrF7mB.png" title="source: imgur.com" /></div>

7. Na próxima janela, informe onde você deseja Salvar e clique no botão **Salvar**.

<h2>👣 Passo 04 - Exportar como Script SQL</h2>

1. No menu **File**, clique na opção **Export 🡪 Forward Engineer SQL CREATE Script...** 

<div align="center"><img src="https://i.imgur.com/ifd98gU.png" title="source: imgur.com" width="85%"/></div>

2. No item **Output SQL Script File**, Clique no botão com 3 pontos (...) e informe o **nome do arquivo SQL** e onde deseja Salvar.

<div align="center"><img src="https://i.imgur.com/HRFEWNn.png" title="source: imgur.com" width="85%"/></div>

3. Clique em **Next** para continuar

<div align="center"><img src="https://i.imgur.com/HGuDDtx.png" title="source: imgur.com" width="85%"/></div>

4. Clique em **Next** para continuar

<div align="center"><img src="https://i.imgur.com/52To7xs.png" title="source: imgur.com" width="85%"/></div>

5. Clique em **Finish** para concluir

<div align="center"><img src="https://i.imgur.com/jaSU7mn.png" title="source: imgur.com" width="85%"/></div>

6. O Script gerado será semelhante à imagem abaixo:

<div align="center"><img src="https://i.imgur.com/DkWiUuZ.png" title="source: imgur.com" /></div>

<h2>👣 Passo 05 - Exportar como Imagem PNG</h2>

1. No menu **File**, clique na opção **Export 🡪 Export as PNG...** 

<div align="center"><img src="https://i.imgur.com/JwAVbRQ.png" title="source: imgur.com" width="85%"/></div>

2. Informe o **nome do arquivo PNG** e onde deseja Salvar. Clique no botão **Salvar**.

<div align="center"><img src="https://i.imgur.com/50XbCAh.png" title="source: imgur.com" width="85%"/></div>

<h2>👣 Passo 06 - Exportar como PDF</h2>

1. No menu **File**, clique na opção **Export 🡪 Export as Single Page PDF...** 

<div align="center"><img src="https://i.imgur.com/gpkyfq8.png" title="source: imgur.com" width="85%"/></div>

2. Informe o **nome do arquivo PDF** e onde deseja Salvar. Clique no botão **Salvar**.

<div align="center"><img src="https://i.imgur.com/EyTQerr.png" title="source: imgur.com" width="85%"/></div>

<h2>👣 Passo 07 - Exportar para o MySQL</h2>

1. No menu **Database**, clique na opção **Forward Engineer...** 

<div align="center"><img src="https://i.imgur.com/LT2YTyk.png" title="source: imgur.com" width="85%"/></div>

2. Como estamos trabalhando localmente (Localhost), clique em **Next** para continuar. Se estivéssemos  trabalhando com um Banco de dados na Nuvem seria necessário configurar a conexão nesta etapa.

<div align="center"><img src="https://i.imgur.com/IohsHZA.png" title="source: imgur.com" width="85%"/></div>

3. Clique em **Next** para continuar

<div align="center"><img src="https://i.imgur.com/uWoRBKa.png" title="source: imgur.com" width="85%"/></div>

4. Mantenha a primeira opção selecionada (**Criar todas as tabelas do modelo**) e clique em **Next** para continuar

<div align="center"><img src="https://i.imgur.com/l6JrI6g.png" title="source: imgur.com" width="85%"/></div>

5. Clique em **Next** para continuar

<div align="center"><img src="https://i.imgur.com/xjw0jeZ.png" title="source: imgur.com" width="85%"/></div>

6. Clique em **Close** para concluir

<div align="center"><img src="https://i.imgur.com/gunGqUn.png" title="source: imgur.com" width="85%"/></div>

7. Abra a conexão com o MySQL e verifique se o Banco de dados **db_loja_games** com as 3 Tabelas foi criado.

<div align="center"><img src="https://i.imgur.com/SGqnQRD.png" title="source: imgur.com" /></div>

<br />

<div align="left"><img src="https://i.imgur.com/bQGvf3h.png" title="source: imgur.com" width="25px"/> <a href="https://github.com/rafaelq80/cookiebooks_spring/tree/main/02_mysql/der" target="_blank"><b>DER - Loja de Games</b></a>

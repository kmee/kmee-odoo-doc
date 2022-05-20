Treinamento Fiscal
==================

**Treinamento Fiscal Odoo**

**Roadmap Fiscal**

**Semana 01** (1x /sem)

-  Etapa 01 (01/04/2022): Configurações Gerais de Impostos

   -  PIS / COFINS
   -  IPI
   -  ISSQN
   -  CSLL
   -  IRPJ
   -  INSS

OBS: No nível mais geral, configuramos os impostos da empresa, esses
serão carregados automaticamente pelo sistema, sendo sobrescritos pelos
impostos dos casos particulares, quando algum se encaixar

**Semana 02** (1x /sem)

-  Etapa 02 (07/04/2022): Cadastro de NCM’s

   -  IPI
   -  II

OBS: O primeiro nível é o NCM. Esse registro é responsável pela
definição dos impostos referentes ao IPI e ao II.

**Semana 03** (2x /sem)

-  Etapa 03 (13/04/2022): Regulamento do ICMS parte 1

   -  ICMS

-  Etapa 04 (14/04/2022): Regulamento do ICMS parte 2

   -  ICMS ST
   -  ICMS FCP

**Semana 04** (2x /sem)

-  Etapa 05 (20/04/2022)\: Linhas de Operação
-  Etapa 06 (27/04/2022): CFOP

**Semana 05** (1x /sem)

-  Etapa 07 (29/04/2022): Perfil fiscal do parceiro

**Introdução**

As configurações fiscais funcionam em ordem decrescente de
generalidade,ou seja, configura-se do caso mais geral para o caso mais
particular.

Para tomar a decisão sobre quais impostos incidem sobre os itens
fiscais, o sistema se utiliza de um registro chamado Definição de
Imposto.

No nível mais geral, configuramos os impostos da empresa. Esses serão os
impostos carregados automaticamente pelo sistema, sendo sobrescritos
pelos impostos dos casos particulares, quando algum se encaixar.

No caso da empresa ser do Simples Nacional, as configurações dos
impostos de saída na empresa serão suficientes. Uma vez definidos em
qual faixa e anexo a empresa se enquadra, os mesmos impostos serão
aplicados em todas as operações de saída

Caso contrário, se a empresa for do regime normal, a decisão de quais
impostos aplicar passa por outros níveis de configuração até chegar na
decisão final. Em cada nível de decisão, aplicam-se os impostos
especificados nas definições de impostos, se elas forem válidas no caso
atual.

O primeiro nível é o NCM. Esse registro é responsável pela definição dos
impostos referentes ao IPI e ao II, esse último apenas no caso de uma
exportação. Esse nível de decisão é o único que não utiliza registros de
definição de imposto para operar. A definição dos impostos IPI e II é
feita diretamente no cadastro do registro de NCM.

O segundo nível é o regulamento do ICMS. Esse registro é responsável
pela definição dos impostos de ICMS, ICMS ST e ICMS FCP.

O terceiro nível é a linha da operação. Esse registro pode sobrescrever
todo e qualquer imposto dos níveis superiores, inclusive os relativos ao
ICMS. Também é responsável por especificar a CFOP do item.

O quarto nível é a própria CFOP. Assim como as linhas da operação, as
definições de imposto da CFOP podem sobrescrever quaisquer decisões de
impostos tomadas em etapas anteriores. Seu uso é menos comum, pois na
maioria dos casos as definições da linha da operação são suficientes.
Porém, podem haver casos específicos em que impostos diferentes devam
ser aplicados para CFOPs diferentes dentro de uma mesma linha de
operação.

O último nível é o perfil fiscal do parceiro. Ele também tem o poder de
sobrescrever as decisões de impostos dos níveis anteriores. Mas com esse
registro é necessário cautela redobrada, pois uma definição de imposto
aqui valerá para todos os parceiros com o mesmo perfil fiscal.

**Hierarquia de parametrização**

.. image:: .gitbook/assets/1

--------------

**Moedas:**

-  Dólar
-  Real

**Serviços e Produtos**

-  Produção própria
-  Revenda
-  Industrialização a terceiros

**Emissão de notas:**

-  Emissão de notas conforme legislação Brasileira
-  Considerar que trabalham com serviços e venda de produtos
-  Fazem importações

**Código do Regime Tributário (CRT)**

-  3 - Regime Normal

**Cálculo de Lucro**

-  Presumido

**É industria?**

-  Sim

**Tipo de Indústria:** Validar

-  02 - Industrial - Montagem

**CNAE Principal:**

-  

   -  2610-8/00 - Fabricação de Componentes Eletrônicos

**CNAE Secundário:**

-  

   -  7490-1/99 - Outras atividades profissionais, científicas e
      técnicas não especificadas anteriormente

**PIS/COFINS:** Regime de Incidência Cumulativa PIS 0,65% e Cofins 3,00%

**ISSQN:** 5%

**IRPJ - Vendas:** Valor Total x 8% e o resultado x 15% = 1,2%

**CSLL - Vendas:** Valor Total x 12% e o resultado x 9% = 1,08%

**IRPJ - Serviços:** Valor Total x 32% e o resultado x 15% = 4,8%

**CSLL - Serviços:** Valor Total x 32% e o resultado x 9% = 2,88%

**Nível 0: Configurações Fiscais da Empresa**

Nota: Levando em consideração que a Empresa possui operação de venda de
produto e serviço, os impostos como IRPJ, CSLL serão parametrizados no
nível 3: Linha de Operação. No nível zero devemos nos atentar apenas ao
PIS/COFINS

.. image:: .gitbook/assets/2

.. image:: .gitbook/assets/3

**Aba regime tributário**

.. image:: .gitbook/assets/4

Regime Tributário: Se a empresa é do Simples Nacional ou do Regime
Normal.

**Regime Normal** 
^^^^^^^^^^^^^^^^^

Caso a empresa for do regime normal, alguns campos adicionais devem ser
configurados.

.. image:: .gitbook/assets/5

Cálculo de Lucros: Se a empresa é do Lucro Real, Presumido ou
Arbitrário.

É indústria: Se a empresa é uma indústria.

Tipo de Indústria: Se for indústria, especificar o tipo da instalação
industrial.

**CNAE** 
^^^^^^^^

Configurar a atividade principal e secundárias da empresa.

.. image:: .gitbook/assets/6

**Aba Impostos**

.. image:: .gitbook/assets/7

Nessa aba são configurados os impostos padrão, assim como os regimes e
regulamentos fiscais aos quais a empresa é submetida.

**PIS/COFINS** 
^^^^^^^^^^^^^^

.. image:: .gitbook/assets/8

PIS/COFINS: O regime de incidência dos impostos PIS e COFINS.

PIS RET Padrão: O imposto de retenção padrão do PIS.

COFINS RET Padrão: O imposto de retenção padrão do COFINS.

**IPI** 
^^^^^^^

.. image:: .gitbook/assets/9

IPI Padrão: O imposto IPI padrão a ser aplicado.

.. image:: .gitbook/assets/10

RIPI: Se marcado, o imposto IPI a ser aplicado será decidido a partir da
NCM do produto e da operação fiscal.

**ICMS** 
^^^^^^^^

.. image:: .gitbook/assets/11

Regulamento do ICMS: O regulamento de ICMS a ser usado, se a empresa for
do regime normal.

**ISSQN** 
^^^^^^^^^

.. image:: .gitbook/assets/12

ISSQN Padrão: O imposto ISSQN padrão a ser aplicado.

ISSQN RET Padrão: O imposto de retenção de ISSQN padrão a ser aplcado.

**CSLL, IRPJ e INSS** 
^^^^^^^^^^^^^^^^^^^^^

.. image:: .gitbook/assets/13

As mesmas definições feitas no ISSQN podem ser feitas nos demais
impostos.

**Impostos avançados** 
^^^^^^^^^^^^^^^^^^^^^^

.. image:: .gitbook/assets/14

Como resultado das configurações de impostos por meio dos campos
específicos de cada tipo de imposto, ao salvar o cadastro da empresa,
serão criadas definições de impostos. Podem ser criadas outras
definições manualmente nesse campo.

**Aba Estoque**

.. image:: .gitbook/assets/15

Nessa aba são configuradas as operações fiscais padrão a serem usadas
nas operações de estoque.

.. image:: .gitbook/assets/16

**Aba Vendas** 
~~~~~~~~~~~~~~

.. image:: .gitbook/assets/17

Assim como na aba estoque, podem ser definidas operações padrão para
vendas comuns e vendas para consumo final.

.. image:: .gitbook/assets/18

Além disso, pode-se escolher se as observações da venda serão
automaticamente copiadas para as faturas.

**Aba Certificados** 
~~~~~~~~~~~~~~~~~~~~

.. image:: .gitbook/assets/19

**Certificado** 
^^^^^^^^^^^^^^^

.. image:: .gitbook/assets/20

Para que seja possível emitir documentos fiscais é necessário configurar
os certificados digitais da empresa. O sistema atualmente suporta o
certificado A1. Para preencher, basta clicar na seta do campo NFe e
clicar em “Criar e Editar…”:

Após fazer o upload do arquivo no formato PFX e inserir a senha, ao
salvar o registro, o sistema valida o certificado. Em caso de falha, uma
mensagem aparecerá na tela.

**Aba Documentos Eletrônicos** 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Nessa aba ficam as configurações relacionadas aos documentos que podem
ser transmitidos eletronicamente.

Processador documentos eletrônicos: “erpbrasil.edoc” deve ser escolhido
para a emissão de documentos pelo sistema. Se for escolhida a opção
“Nenhum”, os documentos irão para a situação “Autorizado” ao clicar em
enviar, mas o sistema assumirá que a nota foi emitida por terceiros.

Documento Fiscal Padrão: O tipo de documento padrão que a empresa emite.

**Aba NF-e** 
~~~~~~~~~~~~

Nessa aba ficam as informações relativas à emissão da nota fiscal.

Versão da NF-e: A versão oficial do documento.

Ambiente da NF-e: O ambiente em que as notas serão emitidas (“Produção”
ou “Homologação”).

Série Padrão da NF-e: A série que as notas devem ser emitidas.

 
~

.. _section-1:

 
~

.. _section-2:

 
~

**Nível 01: NCM** 
~~~~~~~~~~~~~~~~~

**Especificações gerais** 
~~~~~~~~~~~~~~~~~~~~~~~~~

Código: Código do NCM, no formato “9999.99.99”.

Nome: Nome por extenso do NCM.

Exceção: Caso se trate de uma exceção dentro de um NCM, além de
especificar isso no nome é necessário preencher o número da exceção
nesse campo.

IPI: Imposto IPI a ser aplicado à itens com produtos pertencentes ao
NCM.

II: Imposto II a ser aplicado à itens com produtos pertencentes ao NCM.

UoM de Exportação: Unidade de medida a ser usada na exportação.

**Validação dos impostos e produtos vinculados por NCM**

**Passo 01:** Acessar o Módulo Fiscal

**Passo 02:** Acessar NCMs

**Passo 03:** Pesquise pela NCM no qual deseja validar se está
cadastrada no sistema, assim como seus impostos de IPI e II.

Digite no seguinte formato: “84313110”

**Passo 04:** Valide os impostos, nome e código, bem como os produtos
vinculados. Caso tenha divergência no valor do IPI ou II, basta clicar
em cima da tributação.

Nota: Caso exista algum produto que não esteja na lista do NCM, a
alteração deverá ser feita no Módulo Inventário > Dados Principais >
Produtos e selecionar o produto que necessita de alteração.

**Passo 05:** Editando um imposto

**Passo 06:** Caso o registro de imposto não exista, poderá ser criado
um novo registro de IPI / II clicando em “Criar e editar”

Feito isso, clique em salvar e a nova tributação estará criada.

**Cadastro de NCMs não existentes na tabela original da localização
Brasileira**

Exemplo de NCM faltante: 85411032

**Passo 01**: Dar acesso ao responsável pelo cadastramento.

Configurações > User & Companies > Usuários > Selecionar responsável
pelo cadastramento

**Passo 02:** Marcar a opção de “Maintenance de Dados Fiscais”

**Passo 03:** Entrar no Módulo Fiscal, Configuração, NCM

**Passo 04:** Buscar a NCM mais próxima da que se deseja criar

**Passo 05:** Exportar para Excel

**Passo 06:** Abrir o arquivo excel, alterar os itens marcados em
vermelho, para a descrição desejada, número e tributação efetiva do NCM

**Atenção** especial, para os campos:

Deve-se alterar para o código que representa o percentual da tributação
do NCM.

- tax_ipi_id -> % do IPI - “l10n_br_fiscal.tax_ipi_2” (2%)

- tax_ii_id -> % do II “ l10n_br_fiscal.tax_ii_0” (0%)

**Passo 07:** Arquivo excel “Alterado” com novos dados

**Passo 08:** Clique em “Importar”

**Passo 09:** Carregar o Arquivo modificado

**Passo 10:** Visualizar os dados de importação do NCM e testar a
importação

**Passo 11:** Uma vez validado, pode-se clicar em “Importar”

E isso é tudo para esse processo.

Lembrando que o arquivo excel tem o ID Externo (rota) que permite
importar mais campos, tantos quantos o usuário definiu no momento da
exportação.

**Nível 2: Cadastro de uma tributação de ICMS específica por NCM**

Nota 01: A configuração de uma tributação de saída exemplificada abaixo,
pode ser utilizada como modelo para efetuar a parametrização de outra
tributação específica por um NCM específico, como por exemplo uma
redução de alíquota.

**Passo 01:** Validar cadastro do produto com a NCM correta

**Passo 02:** No módulo Fiscal, ir em Configuração > Regulamento do ICMS

**Passo 03:** Editar o estado que se deseja configurar o ICMS, São Paulo
neste caso

**OBS:** Notar que o Odoo já possui algumas configurações padrão, basta
alterá-las para adaptação à operação da empresa.

**Passo 04:** Clicar em “Adicionar uma Linha”

**Passo 05:** Acessar o menu de criação de Nova Tributação

**Passo 06:** Criar ou adicionar Tributação Nova e CST’s

**Passo 07:** Detalhes da criação da nova tributação

**Passo 08:** Informar o Estado onde se aplica a nova legislação criada

**Passo 09:** Informar o NCM que se deseja tributar

Nota: Caso queira inserir mais de um NCM, basta separá-los por vírgula (
“,” )

**Passo 10:** Confirmar Aprovação da nova regra criada

**Passo 11:** Revisar e Salvar

**Passo 12:** Aprovar e salvar para mudar o status para “Aprovado” e o
motor de impostos do odoo passar a usar a regra

Menu final após a conclusão da criação da nova regra

**Cadastro de uma regra ICMS com redução de alíquota**

**Passo 01:** Acesse o regulamento ICMS e adicione uma nova linha

**Passo 02:** Caso não exista o cadastro do imposto com redução, basta
criar

**Passo 03:** Preencha o nome do imposto conforme o padrão “ICMS 18% Com
Red. 61,11%” e também os demais campos conforme abaixo:

**Passo 04:** Insira o estado destino 

**Passo 05:** Insira o NCM no qual se aplica a redução de alíquota,
utilizaremos como exemplo o “85437099”

**Passo 06:** Sempre lembrar de Revisar e Aprovar o imposto criado

**Cadastro de uma regra ICMS com Substituição Tributária**

Nota: Diferentemente do cadastro de uma regra de ICMS comum, uma regra
de ICMS com Substituição Tributária deverá ser parametrizada a nível de
linha de operação e não pelo regulamento de ICMS como mostra a abaixo

Portanto, para configuração de uma regra ICMS ST, seguiremos os
seguintes passos:

**Passo 01:** Acesse o módulo Fiscal

**Passo 02:** Acesse a configuração das operações

Nota: Cada operação pode ter linhas de operação, como exemplo a operação
“Venda”, pode ter a linha de operação “Venda com Substituição
Tributária”. Portanto, antes de configurar a linha de operação com ST,
selecione a operação Pai.

Neste exemplo, faremos a parametrização de Venda de produto com ST

**Passo 01:** Lembre sempre de voltar a operação para provisório para
poder editar

**Passo 02:** Na aba “Linha de Operação”, clique em adicionar mais uma
linha

**Passo 03:** Configure conforme descrito abaixo

**Passo 04:** Na aba “Definições Fiscais”, defina as tributações

Nota: Para o compreendimento do sistema, precisaremos criar duas regras
de tributação para cada alíquota, sendo elas:

-  ICMS: No qual será responsável por definir o CST = 10
-  ICMS ST: No qual será responsável por definir o IVA/MVA

Iremos utilizar o exemplo de ICMS ST 13.3%

**Passo 05:** Criando a regra ICMS

**Passo 06:** Pesquise pelo ICMS no qual deseja, no caso “ICMS ST 13.3%”

**Passo 07:** Caso não existe, opte pela opção “Criar e editar”

**Passo 08**: Insira o NCM respectivo e salve a regra ICMS

**Passo 09:** Agora criaremos a Regra ICMS ST responsável por carregar o
valor do IVA/MVA

**Passo 10:** Preencha os campos e cria uma nova regra de MVA/IVA caso
necessário

**Passo 11:** Criando uma regra com MVA/IVA

**Passo 12:** Inclua o NCM no qual se deseja aplicar tal regra

Feito isso, a linha de operação com ST estará criada, basta salvar,
revisar e aprovar.

Feito isso, está concluído o registro de uma regra ICMS com ST. Para o
cadastro de novas regras ICMS com ST, elas deverão ser feitas dentro da
mesma linha de operação, no caso “Venda ST”

**Diferença de alíquota do ICMS (DIFAL)**

O DIFAL não necessita de parametrização no Odoo, o sistema já faz o
tratamento a partir de 3 fatores:

-  Tabela ICMS
-  Consumidor final não contribuinte
-  Venda para fora do estado

Segue exemplo de venda abaixo:

Na aba “Impostos”>”ICMS”, podemos verificar o cálculo do DIFAL

**Nível 03: Operação / Linha de Operação** 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

O nível 3 é dividido em Operação e o subnível Linha de Operação.

O objetivo da configuração da Operação é definir 3 variáveis:

-  Definir se é uma operação de entrada ou saída
-  Definir se é uma operação para consumo final
-  Unidade de Preço, sendo ele preço de Venda e preço de Custo

A linha de operação se comporta como filtros no qual irá avaliar 2
variáveis:

-  Se é um produto acabado ou produto de revenda
-  Se o parceiro é contribuinte ou não do ICMS

Nota: Quanto mais campos preenchidos na configuração da Operação e Linha
de Operação, mais preciso será os filtros. Pois quando não existir um
imposto configurado em linha de operação, ele será buscado no
regulamento do ICMS.

**Nível 04: CFOP** 
~~~~~~~~~~~~~~~~~~

É possível configurar impostos em um nível mais baixo que a linha de
operação. Este nível é o nível de CFOP.

Neste nível é possível que existam configurações fiscais diferentes para
os CFOPs interno, externo e de exportação da operação. Logo, é possível,
por exemplo, que para operações de venda, uma venda para dentro do
Estado (CFOP 5101) tenha uma configuração fiscal diferente de uma venda
para fora do Estado (CFOP 6101).

Apesar deste nível possibilitar este tipo de flexibilidade é necessário
cuidado, pois uma vez feita a configuração de impostos a nível de CFOP,
todas as linhas de operação que possuírem aquele CFOP utilizaram a nova
configuração.

Por exemplo, para o CFOP 5101, as linhas de Venda e Venda não
Contribuinte das operações de Venda e Venda de Consumo Final, utilizam o
mesmo CFOP. Caso fosse realizada uma configuração fiscal no CFOP 5101,
todas estas linhas de operação seriam afetadas.

Além disso, mesmo que toda a configuração fiscal seja feita a nível de
CFOP, os filtros da linhas de operação ainda devem ser configurados de
forma correta, pois é através deles que o Odoo toma a decisão de qual
CFOP escolher.

**Casos de Uso** 
~~~~~~~~~~~~~~~~

Nota: É essencial que o cadastro de todos os produtos e de todos os
cliente esteja configurado de maneira correta, pois qualquer erro nesses
cadastros resultará em um erro no cálculo dos impostos

**1- Configurações de produtos:**

Todos os produtos terão o mesmo NCM, de modo a mostrar de forma clara o
processo de seleção de impostos do Odoo.

Além disso, estão sendo preenchidos apenas os campos obrigatórios e os
campos utilizados pelo motor fiscal. O cadastro real dos produtos e dos
parceiros deve ser muito mais completo.

**Produto fabricado pela empresa, sem ocorrência de ST**

Nota: Produtos fabricados pela empresa devem ter o Tipo Fiscal ‘produto
acabado’.

Essa configuração será utilizada para fazer a seleção de linha de
operação entre venda, revenda ou serviço.

O campo Tax Regulation de produtos que não têm ST deve ser deixado em
branco.

**Produto de revenda, sem ocorrência de ST**

Nota: Produtos de revenda devem ter o ‘Tipo Fiscal’ mercadoria de
revenda. E esta é a única diferença entre produtos fabricados e
mercadorias de revenda.

**Produto fabricado pela empresa, com ST**

Nota: A configuração é quase a mesma do produto fabricado sem ST, a
única diferença estará no campo ‘Tax Regulation’ que aqui será
preenchido com o valor Regulamento ICMS ST

**Produto de revenda, com ST**

Nota: O mesmo vale para o produto de revenda com ST. A configuração é a
mesma do produto de revenda sem ST, à parte do campo Tax Regulation.

**2- Configuração de parceiros**

**Parceiro de SP e contribuinte do ICMS**

Para os testes realizados, os perfis Contribuinte e Contribuinte Simples
Nacional são equivalentes, pois as linhas de operação ‘Venda’ e ‘Venda
não Contribuinte’ não fazem diferenciação através do regime do parceiro.
Porém, caso exista alguma linha de operação que seja diferenciada pelo
regime do parceiro, estes perfis resultarão em cálculos de impostos
diferentes.

Nota: Clientes contribuintes do ICMS devem ser marcados como empresa, e
clientes não contribuintes devem ser marcados como Indivíduos.

**Parceiro de SP e não contribuinte do ICMS**

**Parceiro de fora de SP e contribuinte do ICMS**

**Parceiro de fora de SP e não contribuinte do ICMS**

**Caso de Uso 1: Venda de produto acabado sem ST para parceiro
contribuinte de SP**

No módulo Vendas cria-se uma nova cotação, e seleciona-se o parceiro
contribuinte de SP e a operação de Venda.

Ao selecionar-se um produto, serão preenchidos automaticamente os campos
‘Linha de Operação’ e ‘CFOP’. Neste caso, como o parceiro não é
contribuinte e o produto é fabricado e não possui ST, foi selecionada a
Linha de Operação ‘Venda’, e como o parceiro é do mesmo estado da
empresa, foi selecionado o CFOP interno da linha de operação, neste caso
o 5101.

Se verificarmos as definições de impostos da linha de operação ‘Venda’
da operação ‘Venda’, observaremos que o NCM do nosso produto está
cadastrado na lista de NCMs do imposto ICMS 18% com Redução de 51,11% da
base de cálculo. (Obs: Neste ponto eu percebi que tinha colocado o NCM
errado no cadastro dos produtos, então voltei lá e os troquei, assim há
uma pequena inconsistência no manual entre o número do NCM dos produtos
na parte de cadastro de produto e o número do NCM dos produtos desta
seção em diante).

Logo se abrirmos a aba ICMS na janela da venda, veremos que o ICMS 18%
com red de 51,11% foi selecionado automaticamente. Além disso, como a
operação acontece apenas dentro de SP, não há Difal nem FCP.

Além disso, podemos ver que a alíquota de IPI do cadastro do NCM foi
selecionada automaticamente e que o PIS e o COFINS do cadastro geral da
empresa também.

**Caso de Uso 2: Venda de produto acabado com ST para parceiro
contribuinte de fora de SP**

Neste caso, vemos que a linha de operação selecionada foi a ‘Venda ST’,
visto que esta linha de operação filtra produtos que possuem a opção
‘Regulamento ICMS ST’ em seu cadastro. Além disso, como o parceiro é de
fora de SP o CFOP selecionado foi o 6401.

Verificando a aba ICMS vemos que foi selecionado o ICMS 13,3% com ST
para o ICMS padrão e o ICMS 13,3% MVA 41%, assim como consta para o NCM
do nosso produto nas definições de imposto da linha de operação. O ICMS
FCP e Difal continuam em branco, dado que o parceiro é contribuinte do
ICMS.

**Caso de Uso 3: Revenda para parceiro não contribuinte de fora de SP**

Ao selecionar o produto, a linha de operação é preenchida
automaticamente com ‘Revenda não Contribuinte’, pois o produto é um
‘produto acabado’ e o parceiro é não contribuinte, além disso, o CFOP é
preenchido com o valor 6108, uma vez que o parceiro é de fora do Estado.

Na aba ICMS vemos que, como não há definição de imposto ICMS para a
linha de operação Revenda não Contribuinte, foi puxado o valor
registrado no Regulamento de ICMS para uma operação com origem em SP e
destino no PR, ou seja, 12%.

Além disso, esta operação é suscetível à cobrança de ICMS Difal e FCP. O
difal é calculado de maneira automática a partir da tabela de ICMS
interno e externo de cada estado. Já o FCP será incluído caso haja um
cadastro deste imposto na aba outros do estado de origem no regulamento
de ICMS.

Além disso, na linha de operação de ‘Revenda não Contribuinte’, foi
cadastrado o imposto IPI NT, uma vez que o IPI não é cobrado em
revendas. Assim, se abrirmos a aba IPI na venda, veremos que o imposto
IPI NT estará selecionado.

**Caso de Uso 4: Operação de Serviço de Industrialização**

Para decidir qual a linha de operação será utilizada, o Odoo checa as
linhas de operação cadastradas para a operação selecionada na Ordem de
Compra. Esta operação deve ser selecionada manualmente durante a criação
da OC.

Este passo deve ser feito de forma manual pois é possível que exista um
caso no qual uma transação do mesmo produto com o mesmo parceiro ocorra
através de um CFOP diferente (5101, 5124 ou 5125, por exemplo). Neste
caso não há como o Odoo saber qual deles deve ser selecionado, e
consequentemente qual linha de operação selecionar.

Quando uma operação diferente é selecionada na OC, as possíveis linhas
de operação (e consequentemente definições fiscais) são aquelas que
estão dentro do cadastro da operação selecionada.

No caso de ‘Serviço de Industrialização’ há apenas uma linha de operação
cadastrada, então ela será a única linha de operação selecionável na OC.
Mas cuidado, caso os filtros desta linha de operação estejam
configurados de forma que ela não seja selecionada para algum tipo de
produto ou parceiro, uma venda com operação ‘Serviço de
Industrialização’ que contenha este parceiro ou este produto ficará sem
linha de operação, e consequentemente sem configuração fiscal. É muito
importante que os filtros das linhas de operação cubram todos os
possíveis casos daquela operação.

Vemos, então, que com a operação ‘Serviço de Industrialização’
selecionada, a linha de operação escolhida foi a de mesmo nome,
cadastrada no registro da operação.

Logo, os impostos selecionados são aqueles nas definições fiscais desta
linha de operação.

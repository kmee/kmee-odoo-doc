A arquitetura do Odoo
=====================

A arquitetura do Odoo
---------------------

As aplicações construídas em Odoo podem ser divididas em três camadas:

1. **Dados**
2. **Lógica;**
3. **Apresentação;**

.. nextslide::

.. figure:: ./images/three_tier.png

   Source: https://www.odoo.com/documentation/15.0/developer/howtos/rdtraining/01_architecture.html

1. Camada de dados
------------------

- PostgreSQL;
- Storage;

**1.1** PostgreSQL
~~~~~~~~~~~~~~~~~~

A camada de dados é a camada mais baixa e é responsável pelo
armazenamento e persistência dos dados. O Odoo utiliza o PostgreSQL para
isso:

- Código aberto;
- +30 anos: reputação de confiabilidade, robustez de recursos e desempenho.
- https://www.postgresql.org/

.. important::

    **O PostgreSQL é o único SGBD suportado e foi uma escolha técnica para
    facilitar a otimização e performance.** (De vez em quando aparece alguem perguntando se roda em MySQL =D)

1.2 Arquivos Binários: Anexos, documentos e imagens. 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Os arquivos binários do Odoo por padrão são salvos em disco.

.. warning::

    Isso significa que um backup completo do Odoo envolve no mínimo:
        -  Banco de dados;
        -  File store.

2. Camada Lógica: Python
------------------------

A camada lógica é construída em Linguagem Python e é a responsável por
todas as iterações com os dados e é gerenciada pelo Servidor do Odoo. 

- https://www.python.org/
- `Brochura.pdf <https://brochure.getpython.info/media/releases/psf-python-brochure-vol.-i-final-download.pdf/at_download/file>`_

De forma geral o banco de dados só deve ser acessado através desta
camada, assim garantindo a consistência dos dados e às corretas
permissões de acesso.

3. Camada de Apresentação: HTML5, JavaScript e CSS.
---------------------------------------------------

A camada de Apresentação é responsável por apresentar os dados e
interagir com o usuário. Ele é implementado pela parte cliente do
software, que é responsável pela interação do usuário final.

O software cliente usa chamadas de procedimento remoto (RPCs) para o
servidor do Odoo.

.. tip::

    Dependendo do escopo de um módulo ele pode ser construido nas três camadas.


.. nextslide::

**Odoo fornece um cliente web pronto para uso. O cliente da web suporta
todos os recursos necessários para um aplicativo de negócios, como
sessões de login, menus de navegação, listas de dados e formulários.**

A API (JSON-RPC) do servidor Odoo é aberta e todas as funções do servidor estão disponíveis através dela.

É usada pelo cliente web oficial e é a mesma disponível para qualquer
outro aplicativo. Assim, outras implementações de clientes são possíveis
e podem ser construídas em praticamente qualquer plataforma ou linguagem
de programação.

.. nextslide::

.. tip::

    Os aplicativos de desktop e smartphone podem ser criados para fornecer
    interfaces de usuário específicas, aproveitando as camadas de Dados e
    Lógica.

    Existem módulos da comunidade que estendem API, possibilitando outras
    formas de acesso a camada lógica: REST, GraphQL e etc.

    Saiba mais:
        - https://odoo.com/documentation/15.0/developer/misc/api/odoo.html
        - https://github.com/OCA/rest-framework

4. Odoo: Como aprender mais
---------------------------

Uma estrutura de site também está disponível para uso como front-end
público para usuários externos.

Ele também fornece recursos de CMS, permitindo criar páginas da web
estáticas e dinâmicas.

A estrutura do site usa componentes do **controlador** para o código que
implementa a lógica específica da apresentação, mantendo-a separada da
camada lógica (Padrão MVC).

Esta é arquitetura principal do Odoo, módulos como Ponto de Venda, IOT e
outros possuem sua própria arquitetura e serão detalhados em outros
capítulos. 

`Acesse a documentação de desenvolvedor! <https://www.odoo.com/documentation/15.0/developer.html>`_

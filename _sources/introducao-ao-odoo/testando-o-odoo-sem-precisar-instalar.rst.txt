Testando o Odoo sem instalar
============================

Formas simples de testar o Odoo sem precisar instala-lo!

1 - SaaS da Odoo SA
~~~~~~~~~~~~~~~~~~~

Ao acessar o endereço https://www.odoo.com/pt_BR/trial

|

Você consegue um banco de dados válido por alguns dias. Muitas coisas já vem pré configuradas por exemplo o envio de emails.

2 - Ambientes de Testes e Demo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Vale ressaltar todos os ambientes criados com dados de demonstração tem
os seguintes usuários de demo:

+----------+--------+-------------------------------------------------------------------------------------------------------------------------------+
| Usuário  | Senha  | Perfil                                                                                                                        |
+==========+========+===============================================================================================================================+
| admin    | admin  | Todos os acessos, incluindo backend e a maioria dos módulos. Mas pode ser necessário permissões adicionais em alguns casos    |
+----------+--------+-------------------------------------------------------------------------------------------------------------------------------+
| demo     | demo   | Usuário com acesso não gerencial ao backend.                                                                                  |
+----------+--------+-------------------------------------------------------------------------------------------------------------------------------+
| portal   | portal | Acesso somente ao portal.                                                                                                     |
+----------+--------+-------------------------------------------------------------------------------------------------------------------------------+

.. tip::

    A **localização brasileira** adiciona outros usuários:
        - simples, presumido e real.

2.1 Demo da Odoo SA
^^^^^^^^^^^^^^^^^^^

Ao acessar o endereço https://demo.odoo.com você consegue um banco de
dados de demonstração! Que é resetado diariamente.

Ele já vem com vários dados de exemplo e vários apps instalados, o que é
muito bom para fazer validações rápidas.

2.1 Runbot da Odoo SA
^^^^^^^^^^^^^^^^^^^^^

Ao acessar o endereço http://runbot.odoo.com/ você irá ser redirecionado
para a tela abaixo:

.. figure:: ./images/runbot.png
   :alt: Tela principal do runbot

   Tela principal do runbot

.. nextslide::

.. figure:: ./images/runbot-detais.jpeg


2.1 Runbot da OCA
^^^^^^^^^^^^^^^^^

Antigamente a OCA tinha uma infraestrutura de Runbot como a da Odoo SA.
Entretanto devido ao alto custo de manutenção ele foi migrado para uma estrutura mais robusta: *Runboat*!

Ferramenta com o mesmo princípio! Com apenas algumas alterações para o usuário final.

1. Ache o módulo ou projeto que você quer dar experimentar;
2. Clique no link do runbot;
3. Acesse a instancia;

.. nextslide::

.. figure:: ./images/runboat1.png

.. nextslide::

.. figure:: ./images/runboat2.png

.. nextslide::

.. figure:: ./images/runboat3.png


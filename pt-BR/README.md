Documentação de Práticas de Desenvolvimento
===========================================

1. [Versionamento](#versioning)
1. [Framework](#versioning)
1. [Dados](#data)


<a name="versioning"></a>1. Versionamento:
-------------
Sempre utilizar [Versionamento Semântico](http://semver.org)

  1. Ferramenta: [Git](http://git-scm.com/)
  1. Gerenciamento on-line: [Github](https://github.com/) para parojetos públicos, [Bitbucket](https://bitbucket.org/) para projetos privados
  1. GUI sugerida: [SmartGit](http://www.syntevo.com/smartgit/)
  1. Fluxo: [Github Flow](http://scottchacon.com/2011/08/31/github-flow.html), basicamente:
    * Se está em master é deployable
    * Features, bug fixes, etc... são desenvolvidos em branches
    * Branches são commitadas e publicadas com frequência

<a name="framework"></a>2. Framework
------------
[Zend Framework 2](http://framework.zend.com/)

  1. Rotas:
    1. Nomenclatura: em inglês, entidade + '-' + ação: user-authenticate, product-list
    1. Ações comuns: 
      * register (insert)
      * edit (update)
      * list (select all)
      * view (select one)
      * delete

<a name="data"></a>3. Dados
--------

  1. Modelagem: sempre em inglês.
    1. Ferramenta sugerida: [SQL Power Architect](http://www.sqlpower.ca/page/architect)
    1. Regras:
      1. Entidades: Nome, no singular: user, account, profile
      1. Chave Primária: id
      1. Chave Estrangeira: nome_entidade_origem + "_id": user_id, account_id, profile_id
      1. Entidades M:N: nome_entidade_1 + "_" + nome_entidade_2, alfabeticamente: resource_role, category_product

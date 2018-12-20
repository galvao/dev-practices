Development Practices Documentation
===================================

1. [Versioning](#versioning)
1. [Framework](#versioning)
1. [Data](#data)


<a name="versioning"></a>1. Versioning:
-------------
Always use [Semantic Versioning](http://semver.org)

  1. Tool: [Git](http://git-scm.com/)
  1. On-line management: [Github](https://github.com/) for public projects, [Bitbucket](https://bitbucket.org/) for private projects
  1. Suggested GUI: [SmartGit](http://www.syntevo.com/smartgit/)
  1. Flow: [Github Flow](http://scottchacon.com/2011/08/31/github-flow.html), basically:
    * If it's in master it's deployable
    * Features, bug fixes, etc... are devoloped in in branches
    * Branches are commited and published frequently

<a name="framework"></a>2. Framework
------------
[Zend Framework 3](http://framework.zend.com/)

  1. Routes:
  
    1. Naming in english, entity + '-' + action: user-authenticate, product-list
    1. Common actions: 
      * register (insert)
      * edit (update)
      * list (select all)
      * view (select one)
      * delete

<a name="data"></a>3. Data:
--------

  1. Modelling: Always in english.
  
    1. Suggested tool: [SQL Power Architect](http://www.sqlpower.ca/page/architect)
    1. Rules:
      1. Entities: Name, singular: user, account, profile
      1. Primary Key: id
      1. Foreign Key: origin_entity_name + "_id": user_id, account_id, profile_id
      1. M:N Entities: first_entity_name + "_" + second_entity_name, alphabetically: resource_role, category_product
      1. Self-relationships: The FK should be named, literally, "parent_id"

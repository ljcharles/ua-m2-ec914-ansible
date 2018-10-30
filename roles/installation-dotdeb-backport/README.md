Installation dotdeb backport
=========

Ajoute les dépots dotdeb et backports via Ansible pour Ubuntu et/ou Debian.

Role Variables
--------------

Dans defaults/main.yml :
- dotdeb_sources_Debian: sources du repo pour dotdeb Debian
- dotdeb_sources_Ubuntu: sources du repo pour dotdeb Ubuntu
- dotdeb_repo_gpg_key_url: url de la clé du repo dotdeb

Dans vars/Ubuntu.yml :
- backports_url: url backports Ubuntu
- backports_sources: source du repo pour backports Ubuntu

Dans vars/Debian.yml :
- backports_url: url backports Debian
- backports_sources: source du repo pour backports Debian

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: installation-dotdeb-backport }

License
-------
GNU

Author Information
------------------

Loïc JEAN-CHARLES, Etudiant M2 informatique, Université des Antilles.

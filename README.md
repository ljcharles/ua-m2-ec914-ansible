# ua-m2-ec914-ansible

## Installation dotdeb backport et Docker
=========

Ajoute les dépots dotdeb et backports via Ansible pour Ubuntu et/ou Debian. Et installe Docker pour Ubuntu et Debian version 32 et 64bits.

Role Variables
--------------

### Pour  installation-dotdeb-backport :

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


### Pour  installation-docker:

Dans defaults/main.yml :
- paquets_communs: paquets à installer en communs des architectures pour docker
- paquets_repo: paquets nécessaire pour l'ajout de repo en https
- pc_architecture: pour connaitre l'architecture du pc
- docker_sources: source du repo pour Ubuntu et Debian
- docker_repo_gpg_key_url: url de la clé du repo docker

Dans vars/Ubuntu.yml :
- paquets_ubuntu: paquets spécifique pour Ubuntu

Dans vars/Debian.yml :
- paquets_jessie_or_newers: paquets spécifique pour cette version de Debian
- paquets_wheezy_or_olders: paquets spécifique pour cette version de Debian

Example Playbook
----------------

    - hosts: all
      roles:
         - role: installation-dotdeb-backport
         - role: installation-docker

License
-------
GNU

Author Information
------------------

Loïc JEAN-CHARLES, Etudiant M2 informatique, Université des Antilles.

# Introduction

Ansible est un orchestrateur basé sur du push :

- Pas besoin d'agent intaller sur le serveur distant
- Pousse des information sur un serveur distant
- Utilise le ssh pour ce connecter a une machine distante
- Intégration facile dans des outils CI/CD
- Utilisation à base de fichiers .yml
- De nombeux modules et une trés forte communauté
- Système de templating avec jinja 2 (python): variabiliser des fichiers de configugation
- Il est également possible de faire du pull pour exploter des informations sur un serveur

## Différentes notions et definitions

```
- Inventory: inventaire de toute les machines
- Playbook : Fait l'articulation entre l'inventory et les rôle (quoi installer sur quelle machine)
- Rôles: s'intérèsse a une instalation spécifique
```

## Les Outils les plus utiliser

```
  -> Ansible vault
  -> Ansible playbook
  -> Ansible galaxy
  -> Ansible doc
```

## Installation des modules via

```
  -> Les sources
  -> Les paquets
  -> Librairie python (pip)
```

Docs : https://docs.ansible.com

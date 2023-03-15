# Notions et Définitions

## Control node

```
- Noeud disposant de ansible et permettant de déployer
- Accès ssh aux autres machines via ssh ou password (Bastion/Machine de déploiment)
- Sécurité importante
```

## Managed node

```
- Serveurs cibles
- Permet la connexion ssh
- Elévation de privilèges via le user
```

## Inventory

```
- Inventaire des machines (ip, dns)
- Au format ini(plat) ou au format yaml
- Avec des variables (host_vars et group_vars)
- Statique (fichiers) ou dynamique (api via script)
- Utilisation de patterns possible (srv-pg93-0[0-2])
```

## Groupes

```
- Dans un inventaire les machines peuvent être regroupées (serveur web, databases...)
- Possibilité de créer différent niveaux > arbre (parent/enfants)
- Groupe racine : all
```

## Groups Vars

```
- Variables d'un même groupe
- Définie dans le fichier central d'inventory
- Ou dans un répertoire spécifique (reconnu par ansible)
```

## Host Vars:

```
- Variables spécifiques à un serveur en particulier
- Surcharge d'autre variable définies plus haut dans l'arbre -ex - groupe
```

### Exemple de nomenclature d'inventory :

```
inventory.yml
host_vars/
group_vars/
```

## Tasks

```
- Actions variées (user, group, command, module)
- Format yaml
```

## Modules

```
- Ensemble d'action ciblées sur une action commune
- Pour un outil donné : ex. postgres, mysql, vmware...
- Chacune de ses actions est utilisable via une task (qui appelle le module)
- Chaque action prend des options
- Les actions peuvent fournir un retour (id, résultat...)
- Fournis par ansible pour l'essentiel
- Peuvent être chargés spécifiquement
- Contribution possible auprès des mainteneurs
```

## Rôles

```
- Ensemble d'actions coordonnées pour réaliser un enssemble cohérent (installer nginx et le configurer ect)
- Organisé en différents outils (tasks, templates, handlers, variables (default ou non), meta)
- Peuvent être partagés sur le hub ansible galaxy
- Il vaut mieux les versionner
```

## Playbooks

```
- Un fichier (et rien d'autres...)
- Applique des rôles à un inventory
- Partie cruciale inventory > playbook < rôles
- Peut contenir des variables (à éviter)
- Peut contenir des tasks (à éviter)
- Peut contenir des contitions (à éviter)
```

## Plugins

```
- Modifie ou augmente les capacités de ansible
- De différentes manières : output, inventory dynamique, strategy, tests...
```

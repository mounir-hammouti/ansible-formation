# Formation Ansible

## Lien d'hébergement

https://docker.labs.eazytraining.fr/  
id: devops  
mdp: devops

## Création des containers

Container Ansible:

- Cliquer sur la roue dentée puis sélectionner l'Instance Image: eazytraining/ansible
- Fermer la fenêtre de réglages
- Ajouter une instance via le bouton "ADD NEW INSTANCE"

Container client:

- Cliquer sur la roue dentée puis sélectionner l'Instance Image: eazytraining/client
- Fermer la fenêtre de réglages
- Ajouter une instance via le bouton "ADD NEW INSTANCE"

Se connecter à chaque container et lancer les commandes suivantes:

```sh
sudo su admin -
cd
```

## Récupération du code

Pour récupérer le code permettant d'exécuter Ansible, lancer les commandes suivantes:

```sh
git clone https://github.com/mounir-hammouti/ansible-formation.git
cd ansible-formation
git config --global user.email "email"
git config --global user.name "username"
```

## Modification du fichier hosts

Remplacer la valeur de la variable ansible_host dans le fichier hosts.yml par l'adresse ip fournie sur l'interface du container client.

## Lancement des playbooks

Pour exécuter les playbooks, lancer les commandes suivantes:

```sh
ansible-playbook deploy.yml
```

ou

```sh
ansible-playbook deploy_with_role.yml
```

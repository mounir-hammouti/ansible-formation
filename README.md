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

Se connecter au container Ansible.
Pour récupérer le code permettant d'exécuter Ansible, lancer les commandes suivantes:

```sh
git clone https://github.com/mounir-hammouti/ansible-formation.git
cd ansible-formation
git config --global user.email "mounir.hammouti93270@gmail.com"
git config --global user.name "mounir-hammouti"
```

## Modification du fichier hosts

Remplacer la valeur de la variable ansible_host dans le fichier hosts.yml par l'adresse ip fournie sur l'interface du container client.

## Ajouter le mot de passe pour Ansible Vault

Pour décrypter le contenu encrypté par Ansible, écrire son mot de passe dans un fichier avec la commande suivante:

```sh
echo 'my_vault_password' > .vault_pass
```

## Installation des roles Ansible Galaxy

```sh
ansible-galaxy install adnanhodzic.containerized
```

ou 

```sh
ansible-galaxy install -r roles/requirements.yml
```

## Lancement des playbooks

Pour exécuter les playbooks, lancer les commandes suivantes:

```sh
ansible-playbook deploy.yml
```

ou

```sh
ansible-playbook deploy_with_role.yml
```

ou

```sh
ansible-playbook wordpress.yml
```

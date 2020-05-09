# projet_fake_version_2

Ce projet permet de deployer  le jeu battleboat-fake_backend sur un groupe d'hote distant en utilisant ANSIBLE

Roles:
-Backend
-Frondend

1-Le role Backend permet de deployer le container Mysql:5.7 sur l'hote distant
2-Le role Frondend permet de deployer le container battlegame(contenant l'image de fake-backend) sur l'hote distant
3- Le roles de geerlinguy pour installer git et docker

NB: 
----> Rassurez vous d'avoir Ansible installer sur votre machine avant de lancer ce Playbook
----> Configurer le fichier 'hosts' du Repo

Lancer le playbook comme suit:
sudo ansible-playbook fake-backend.yml -i hosts --ask-vault-pass
Le mot de passe est:....
Vous devez indiquer votre fichier secret.yml dans roles/frondend/vars/ tel que indiqué dans le main.yml avec l'appel des variables(docker
hub,dockerlogin...)

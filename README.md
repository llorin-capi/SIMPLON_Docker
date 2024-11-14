## Initiation à Docker

# Phase 1 : Veille et Installation
voir la [veille technique](veille_docker.pdf)

# Phase 2 : Création et Gestion de Conteneurs

* Lancez un conteneur Ubuntu en mode interactif et explorez les commandes Linux dans ce conteneur (ex : créer un fichier, lister les répertoires).
```
docker run -it ubuntu

mkdir mon_dossier               # Créer un dossier
touch mon_dossier/mon_fichier   # Créer un fichier
ls -la                          # Lister les fichiers et répertoires
```

* Utilisez docker exec pour exécuter une commande dans un conteneur en cours d’exécution.
```
docker exec mon_conteneur ls /
```

Utilisez docker logs pour récupérer les logs d’un conteneur et docker rm pour supprimer un conteneur arrêté.
Montez un volume dans un conteneur et créez un fichier dans le volume pour observer la persistance des données après l’arrêt du conteneur.
Créez un réseau Docker et connectez deux conteneurs (par exemple, un serveur et un client simple). Testez la communication entre eux avec une commande simple, comme ping
​

Phase 3 : Création d’Images et Déploiement d’Application

Rédigez un Dockerfile pour créer une image de base Python contenant des bibliothéques spécifiques (ex : pandas)
Construisez l’image avec la commande docker build
Intégrez une application Flask simple dans un conteneur. Cette application doit exposer une API de base qui renvoie un message.
Testez l’application localement en accédant à l’API via le navigateur.
Ajoutez un fichier requirements.txt à votre projet pour gérer les bibliothèques Python, et modifiez le Dockerfile pour installer automatiquement ces dépendances.
​

Phase 4 : Projet de Déploiement en Conditions Réelles

Mettez un modèle en conteneur avec Docker et exposez une API pour effectuer des prédictions. (Brief précédent)
Configurez un volume pour stocker les données de requêtes (par ex., sauvegarder les prédictions et les résultats)

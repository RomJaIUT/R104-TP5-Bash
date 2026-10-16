# R104 TP5 Bash sous Debian 12

## Préparation enseignant
Créer un dépôt GitHub vide et y importer le CONTENU de ce dossier, en conservant `.devcontainer` à sa racine. Dans GitHub, créer le chemin `.devcontainer/devcontainer.json` explicitement si le dossier masqué est ignoré par le téléversement. Ajouter également `.devcontainer/Dockerfile`.
Activer « Template repository » dans Settings si les étudiants doivent utiliser Use this template. Donner le lien du dépôt aux étudiants, ou distribuer les dépôts selon votre organisation habituelle.
Ouvrir un Codespace pilote avant la séance. Vérifier `cat /etc/os-release`, puis `command -v bash grep cut sed lscpu free df tar git`. La construction installe les outils ; les étudiants n'utilisent pas sudo.
Si la configuration est ajoutée à un Codespace existant : palette de commandes, « Codespaces: Rebuild Container ». Vérifier Debian après reconstruction.

## Nature de l'environnement
Le conteneur utilisateur est Debian 12, hébergé sur une VM Linux gérée par GitHub. Ce n'est pas une VM Debian complète avec son propre noyau. Pas de bureau graphique nécessaire. Les commandes de CPU et mémoire ne constituent pas un inventaire du PC local. Le choix df plutôt que lsblk évite de présumer la présence de disques blocs visibles dans le conteneur.

## Avant de distribuer
Tester la création depuis un compte étudiant ou un compte de test, et vérifier les règles de l'organisation ainsi que l'accès à Codespaces. Les quotas et la facturation dépendent du compte : aucune valeur chiffrée n'est présumée ici. Prévoir un terminal Debian local si un compte est bloqué.
L'image et les dépôts de paquets sont distants : la configuration a été préparée et sa syntaxe vérifiée, mais la construction cloud n'a pas été exécutée dans cette session.

## Déroulement et attendus
Durée cible 2 heures, dont 15 minutes pour la première ouverture. Si les comptes ne sont pas prêts, faire cette ouverture avant la séance.
Le sujet annonce cinq scripts au total : bonjour, validations binaire/MAC/IPv4 et fiche système. Les tests attendus sont indiqués dans le sujet. Le compte-rendu Markdown évite une dépendance à Writer dans le navigateur.
Contrôle rapide : syntaxe des cinq scripts ; tests limites ; variables définies dans chaque script ; génération sans doublon ; nom du poste et architecture ajoutés ; Q1 à Q8 et six captures ; archive lisible.
Pas de fonctions, menu ou boucle obligatoire pour cette première séance. Les étudiants pourront aborder ces notions au TP suivant.

## Sources officielles consultées le 15 octobre 2026
- https://docs.github.com/en/codespaces/about-codespaces/what-are-codespaces
- https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers
- https://github.com/devcontainers/images/blob/main/src/base-debian/README.md

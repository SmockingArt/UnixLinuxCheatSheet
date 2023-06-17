# UnixLinuxCheatSheet
---

Source : Unix/Linux 

Projets : Shell

Tags : #Code #Programmation #Formation #FR

✍ fais par : @Smockingart

🧭 Date : 2023-05-22

_**Cheat Sheet for Unix Linux**_ 

---

 📚 **Table of contents** | [Cheat Sheet Image](#Image) 

[HOWTOS](https://www.linuxhowtos.org/sitemap/) | [Linux](https://www.linux.org/) | [gnu](http://www.gnu.org/) | [tldp](http://www.tldp.org/) |

---


# Gestionnaire de paquets

## Mise à jour du système :

|Commande|Description|
|---|---|
|`sudo apt-get update`|Mettre à jour la liste des dépôts.|
|`sudo apt-get upgrade`|Mettre à jour les paquets et leurs dépendances.|
|`sudo apt-get dist-upgrade`|Mettre à jour les paquets et installer de nouveaux paquets si nécessaire.|

## Recherche et installation de paquets :
|Commande|Description|
|---|---|
|`apt-cache search <nom>`|Chercher un paquet par son nom.|
|`sudo apt-get install <paquet>`|Installer un paquet.|
|`sudo apt-get source <paquet>`|Télécharger les sources d'un paquet.|

## Suppression de paquets :

|Commande|Description|
|---|---|
|`sudo apt-get remove <paquet>`|Supprimer un paquet.|
|`sudo apt-get autoremove <paquet>`|Supprimer un paquet et ses dépendances.|
|`sudo apt-get purge <paquet>`|Supprimer un paquet et ses fichiers de configuration.|
|`sudo apt-get autoremove --purge <paquet>`|Supprimer un paquet, ses dépendances et ses fichiers de configuration.|

# Fichiers de configuration

|FICHIER|DESCRIPTION|
|:--|:--|
|/etc/**hostname**|Nom de la machine sur le réseau|
|/etc/**hosts**|Correspondances statiques de noms d'hôtes|
|/etc/apt/**sources.list**|Liste des dépôts (sources) de logiciels|
|/etc/netplan/**\*.yaml**|Configuration des interfaces réseau via [Netplan](https://netplan.io/) (systemd)|
|/etc/network/**interfaces**|Configuration historique des interfaces réseau (sans systemd)|
|/etc/systemd/**network**|Configuration des interfaces réseau via networkd (systemd)|

|Chemin|Contenu|
|---|---|
|**/**|Répertoire racine, base du système de fichiers.|
|**/bin**|Fichiers binaires exécutables.|
|**/boot**|Fichiers nécessaires au démarrage.|
|**/cdrom**|Répertoire de montage par défaut des CD et DVD.|
|**/dev**|Fichiers spéciaux des périphériques.|
|**/etc**|Fichiers de configuration du système et de diverses applications.|
|**/home**|Dossiers personnels des utilisateurs.|
|**/lib**|Bibliothèques du système. On trouve également les dossiers lib32, lib64 et libx32 pour les systèmes supportant plusieurs architectures binaires.|
|**/lib64**|Idem mais en 64 bits.|
|**/lost+found**|Répertoire contenant les fichiers orphelins ou endommagés trouvés lors d’une vérification du système de fichiers. Sa présence indique que le répertoire courant est la racine d’un système de fichiers.|
|**/media**|Répertoire de montage des périphériques temporaires (clé USB, DVD, disque externe, etc.).|
|**/mnt**|Répertoire de montage plutôt utilisé pour les tests de l’administrateur ou des montages manuels.|
|**/opt**|Applications ou bibliothèques supplémentaires devant être placées dans une arborescence spécifique.|
|**/proc**|Système de fichiers virtuel proposant une interface vers les fonctions et paramètres du noyau.|
|**/root**|Dossier de l’administrateur. Il n’est pas dans home.|
|**/sbin**|Fichiers binaires exécutables dédiés à l’administrateur.|
|**/srv**|Données des services offerts par le système.|
|**/sys**|Système de fichiers virtuel, similaire à /proc mais dédié notamment aux périphériques de type blocs.|
|**/tmp**|Fichiers temporaires.|
|**/usr**|Fichiers binaires, bibliothèques, sources, documentations, etc. exploitables par l’utilisateur.|
|**/var**|Fichiers et dossiers à contenus variables comme les journaux système, les spools d’impression, les messages, etc.|


# Fonctions système

|NOM|DESCRIPTION|
|:--:|:--|
|[**exit**](https://man.cx/exit(2)/fr)|Mettre fin au processus appelant|
|[**read**](https://man.cx/read(2)/fr)|Lire depuis un descripteur de fichier|
|[**write**](https://man.cx/write(2)/fr)|Écrire dans un descripteur de fichier|

 Planification de tâches

# Formats de date 

|Format|Description|
|---|---|
|`%A`|Jours (complet ou abrégé)|
|`%a`|Jours (complet ou abrégé)|
|`%B`|Mois (complet ou abrégé)|
|`%b`|Mois (complet ou abrégé)|
|`%d`|Numéro du jour (01 à 31)|
|`%m`|Numéro du mois (01 à 12)|
|`%Y`|Numéro de l'année (ex: 2019)|
|`%y`|Numéro de l'année (ex: 19)|
|`%H`|Heure (00 à 23)|
|`%M`|Minute (00 à 59)|
|`%S`|Seconde (00 à 59)|

## Raccourcis :

|Raccourci|Description|
|---|---|
|`%F`|Équivalent à `%Y-%m-%d`|
|`%T`|Équivalent à `%H:%M:%S`|

## Modification de la date du système :

Le format de modification de la date du système est `mmddHHMMYYYY`.

## Planification de tâches :

|Commande|Description|
|---|---|
|`at`|Programmer une tâche.|
|`atq`|Afficher la liste des tâches planifiées.|
|`atrm`|Supprimer une tâche planifiée.|
|`cron`|Programmation de tâches récurrentes.|
|`crontab -e`|Éditer le fichier crontab.|

## Trouver le chemin d'une commande :

|Commande|Description|
|---|---|
|`whereis <nom de la commande>`|Trouver le chemin d'une commande.|

# Commande Annexe 

|NOM|DESCRIPTION|
|:--:|:--|
|**[addgroup](https://man.cx/addgroup)**|Ajouter un nouveau groupe|
|**[adduser](https://man.cx/adduser)**|Ajouter un nouvel utilisateur (+ création de son répertoire personnel)|
|**[apropos](https://man.cx/apropos)**|Chercher le nom et la description des pages de manuel|
|**[apt](https://man.cx/apt)**|Utilitaire d'APT pour la manipulation de paquets|
|**[apt-get](https://man.cx/apt-get)**|Utilitaire d'APT pour la manipulation de paquets|
|**[aptitude](https://man.cx/aptitude)**|Interface haut-niveau de gestion de paquets|
|**[at](https://man.cx/at)**|Mémoriser des tâches à exécuter ultérieurement|
|**[atq](https://man.cx/atq)**|Examiner des tâches mémorisés|
|**[atrm](https://man.cx/atrm)**|Supprimer des tâches mémorisés|
|**[bash](https://man.cx/bash)**|Lancer un shell **Bash** (Bourne-Again)|
|**[bg](https://man.cx/bg)**|Exécuter des tâches en arrière-plan|
|**[bunzip2](https://man.cx/bunzip2)**|Décompacter des fichiers|
|**[bzip2](https://man.cx/bzip2)**|Compacter ou décompacter des fichiers|
|**[cat](https://man.cx/cat)**|Concaténer des fichiers et les afficher sur la sortie standard|
|**[cd](https://man.cx/cd)**|Changer de répertoire|
|**[chgrp](https://man.cx/chgrp)**|Changer le groupe propriétaire d'un fichier|
|**[chmod](https://man.cx/chmod)**|Modifier les autorisations d'accès à un fichier|
|**[chown](https://man.cx/chown)**|Modifier le propriétaire et le groupe d'un fichier|
|**[clear](https://man.cx/clear)**|Effacer le terminal|
|**[cp](https://man.cx/cp)**|Copier des fichiers et des répertoires|
|**[crontab](https://man.cx/crontab)**|Gérer des tâches CRON|
|**[cut](https://man.cx/cut)**|Supprimer une partie de chaque ligne d'un fichier|
|**[dash](https://man.cx/dash)**|Lancer un shell **Dash** (BSD) ; alias : sh|
|**[date](https://man.cx/date)**|Afficher ou configurer la date et l'heure du système|
|**[declare](https://man.cx/declare)**|Déclare des variables et leur assigne des attributs|
|**[delgroup](https://man.cx/delgroup)**|Supprimer un groupe du système|
|**[deluser](https://man.cx/deluser)**|Supprimer un utilisateur du système|
|**[df](https://man.cx/df)**|Afficher la quantité d'espace occupé par les systèmes de fichiers|
|**[diff](https://man.cx/diff)**|Trouver les différences entre des fichiers|
|**[dpkg](https://man.cx/dpkg)**|Gérer des paquets DEB|
|**[du](https://man.cx/du)**|Afficher les statistiques sur l'utilisation du disque|
|**[echo](https://man.cx/echo)**|Afficher du texte|
|**[exit](https://man.cx/exit)**|Provoquer l'arrêt normal du processus|
|**[fdisk](https://man.cx/fdisk)**|Manipuler des tables de partitions|
|**[fg](https://man.cx/fg)**|Basculer une tâche au premier-plan (devient la tâche en cours)|
|**[file](https://man.cx/file)**|Déterminer le type d'un fichier|
|**[find](https://man.cx/find)**|Rechercher des fichiers dans une hiérarchie de répertoires|
|**[finger](https://man.cx/finger)**|Rechercher des informations sur un utilisateur|
|**[free](https://man.cx/free)**|Afficher la quantité de mémoire libre et utilisée par le système|
|**[grep](https://man.cx/grep)**|Afficher les lignes correspondant à un motif donné|
|**[groups](https://man.cx/groups)**|Afficher les groupes d'un utilisateur|
|**[gunzip](https://man.cx/gunzip)**|Décompacter des fichiers|
|**[gzip](https://man.cx/gzip)**|Compacter ou décompacter des fichiers|
|**[hdparm](https://man.cx/hdparm)**|Obtenir/définir les paramètres de périphérique SATA/IDE|
|**[history](https://man.cx/history(n))**|Lister les commandes précédemment saisies dans le terminal|
|**[host](https://man.cx/host)**|Chercher des noms de machine à l'aide d'un serveur de domaine|
|**[hostname](https://man.cx/hostname)**|Afficher le nom d'hôte du système|
|**[id](https://man.cx/id)**|Afficher les UIDs et GIDs d'un utilisateur|
|**[ip](https://man.cx/ip)**|Afficher/manipuler le routage, les périphériques réseau, les interfaces et les tunnels|
|**[iw](https://man.cx/iw)**|Afficher/manipuler les appareils sans fil et leur configuration|
|**[iptables](https://man.cx/iptables)**|Filtrer les paquets IP et NAT (pare-feu)|
|**[jobs](https://man.cx/jobs)**|Afficher les tâches en cours d'exécution et leur état|
|**[kill](https://man.cx/kill)**|Envoyer un signal à un processus|
|**[killall](https://man.cx/killall)**|Envoyer un signal à des processus indiqués par leurs noms|
|**[less](https://man.cx/less)**|Se déplacer dans un texte, même volumineux (plus flexible que la commande **more**)|
|**[let](https://man.cx/let)**|Effectuer de l'arithmétique sur des variables shell|
|**[locate](https://man.cx/locate)**|Rechercher des fichiers dans une hiérarchie de répertoires|
|**[ln](https://man.cx/ln)**|Créer des liens entre fichiers|
|**[ls](https://man.cx/ls)**|Lister (afficher) le contenu d'un répertoire|
|**[lsblk](https://man.cx/lsblk)**|Lister les périphériques de bloc|
|**[man](https://man.cx/man)**|Afficher le manuel d'une commande/fonction|
|**[mkdir](https://man.cx/mkdir)**|Créer des répertoires|
|**[mkfs](https://man.cx/mkfs)**|Créér un système de fichiers (peut aussi formater un périphérique de stockage)|
|**[more](https://man.cx/more)**|Se déplacer dans un texte, écran par écran|
|**[mount](https://man.cx/mount)**|Monter un système de fichiers|
|**[mv](https://man.cx/mv)**|Déplacer ou renommer un fichier|
|**[nano](https://man.cx/nano)**|Lancer l'éditeur en ligne de commande **Nano**|
|**[nohup](https://man.cx/nohup)**|Exécuter un programme en le rendant insensible aux déconnexions|
|**[passwd](https://man.cx/passwd)**|Modifier le mot de passe d'un utilisateur|
|**[ping](https://man.cx/ping)**|Envoyer des datagrammes à un hôte sur le réseau|
|**[ps](https://man.cx/ps)**|Afficher l'état des processus en cours|
|**[pwd](https://man.cx/pwd)**|Récupérer le nom du répertoire courant|
|**[quota](https://man.cx/quota)**|Afficher l'utilisation du disque et les quotas|
|**[rar](https://man.cx/rar)**|Créer et compresser des archives RAR|
|**[read](https://man.cx/read)**|Lire une ligne de l'entrée standard et la diviser en champs|
|**[readonly](https://man.cx/readonly)**|Marquer une ou plusieurs variables ou fonctions en lecture seule|
|**[rm](https://man.cx/rm)**|Effacer des fichiers (ou répertoires contenant des fichiers)|
|**[rmdir](https://man.cx/rmdir)**|Effacer des répertoires vides|
|**[scp](https://man.cx/scp)**|Copier des fichiers vers une machine distante|
|**[sed](https://man.cx/sed)**|Filtrer et transformer du texte|
|**[set](https://man.cx/set)**|Modifier valeur d'une option de shell, définit paramètres de position, ou afficher noms et valeurs des variables de shell|
|**[sftp](https://man.cx/sftp)**|Transférer des fichiers de manière sécurisée (utilise SSH)|
|**[sh](https://man.cx/sh)**|_voir commande dash_|
|**[shift](https://man.cx/shift)**|Décaler les paramètres de position vers la gauche|
|**[sleep](https://man.cx/sleep)**|Endormir le processus pour une durée déterminée|
|**[sort](https://man.cx/sort)**|Trier les lignes d'un fichier texte|
|**[ss](https://man.cx/ss)**|Analyser les sockets|
|**[ssh](https://man.cx/ssh)**|Se connecter à une machine distante|
|**[su](https://man.cx/su)**|Executer un shell avec un User-ID et un Group-ID différents (ex : root)|
|**[sudo](https://man.cx/sudo)**|Exécuter une commande via un autre utilisateur (généralement root)|
|**[tar](https://man.cx/tar)**|Utilitaire GNU de gestion d'archives TAR|
|**[tee](https://man.cx/tee)**|Copier l'entrée standard sur la sortie standard et dans un fichier|
|**[tload](https://man.cx/tload)**|Afficher graphiquement la charge du système|
|**[top](https://man.cx/top)**|Lister les processus (avec mise à jour toutes les X secondes)|
|**[touch](https://man.cx/touch)**|Modifier l'horodatage d'un fichier (peut aussi en créer)|
|**[traceroute](https://man.cx/traceroute)**|Afficher la trace des paquets routés vers l'hôte réseau|
|**[ufw](https://man.cx/ufw)**|Gérer un pare-feu Netfilter (surchouche d'iptables)|
|**[uniq](https://man.cx/uniq)**|Éliminer les lignes dupliquées dans un fichier trié|
|**[umount](https://man.cx/umount)**|Démonter des systèmes de fichiers|
|**[unrar](https://man.cx/unrar)**|Extraire des fichiers compressés dans une archive RAR|
|**[unset](https://man.cx/unset)**|Annule les valeurs et les attributs des variables et des fonctions|
|**[unzip](https://man.cx/unzip)**|Lister, tester et extraire des fichiers compressés dans une archive ZIP|
|**[uptime](https://man.cx/uptime)**|Afficher le temps depuis lequel la machine est démarrée|
|**[useradd](https://man.cx/useradd)**|Administrer une nouvelle connexion utilisateur sur le système|
|**[usermod](https://man.cx/usermod)**|Modifier les informations d'un utilisateur|
|**[users](https://man.cx/users)**|Afficher les utilisateurs connectés|
|**[vi](https://man.cx/vi)**|Lancer l'éditeur en ligne de commande **Vi**|
|**[w](https://man.cx/w)**|Afficher les utilisateurs connectés et leur activité|
|**[wc](https://man.cx/wc)**|Afficher le nombre d'octets, de mots et de lignes d'un fichier|
|**[wget](https://man.cx/wget)**|Télécharger un fichier depuis le Web|
|**[whereis](https://man.cx/whereis)**|Rechercher les fichiers exécutables, les sources et les pages de manuel d'une commande|
|**[who](https://man.cx/who)**|Afficher les informations d'un utilisateur|
|**[whois](https://man.cx/whois)**|Afficher les informations d'un domaine|
|**[zip](https://man.cx/zip)**|Créer et compresser des archives ZIP|

# Image 

<div align="center">
  <img src="Images/CheatSheetUnixLinux titre.png" alt="Cyberpunk Banner">
</div>

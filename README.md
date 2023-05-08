# Projet_INFRA_SI_GENDRON_BOUTTE

**#Projet Réseau avec pfSense et VMs :**

Ce projet consiste à mettre en place un réseau sécurisé utilisant un pare-feu pfSense et plusieurs machines virtuelles pour héberger différents services. Nous utilisons VMware pour virtualiser les machines.

**#Architecture du réseau :**

-Pare-feu pfSense
-Client Windows
-Serveur Web Debian (Apache)
-Serveur de sauvegarde Web Debian (Rsync)
-Client Linux Debian

**#Plan d'adressage :**

Machine	IP	Masque de sous-réseau	Passerelle	DNS
Pare-feu pfSense	192.168.1.1	255.255.255.0	N/A	N/A
Client Windows	192.168.1.10	255.255.255.0	192.168.1.1	8.8.8.8
Serveur Web	192.168.1.20	255.255.255.0	192.168.1.1	8.8.8.8
Sauvegarde Web	192.168.1.30	255.255.255.0	192.168.1.1	8.8.8.8
Client Linux	192.168.1.40	255.255.255.0	192.168.1.1	8.8.8.8

**#Instructions d'installation et de configuration :**

1.Installer et configurer pfSense dans une VM.
2.Configurer les règles du pare-feu pour permettre la communication entre les machines virtuelles.
3.Installer et configurer les VMs Client Windows, Serveur Web, Sauvegarde Web et Client Linux.
4.Installer Apache sur le serveur Web et configurer un site Web.
5.Installer Rsync sur le serveur de sauvegarde Web et configurer la sauvegarde automatisée du site Web.
6.Configurer le client Linux pour accéder au serveur Web et au serveur de sauvegarde via SSH.
7.Tester la connectivité et la fonctionnalité de tous les services.

**#Utilisation des services :**

-Accéder au site Web via l'adresse IP du serveur Web (192.168.1.20).
-Sauvegarder une nouvelle ressource Web en ajoutant les fichiers au serveur Web et en les synchronisant avec le serveur de sauvegarde Web via Rsync.
-Restaurer le site Web à une date antérieure en récupérant les fichiers de sauvegarde du serveur de sauvegarde Web.

**#Documentation :**

-La documentation d'architecture et d'exploitation est disponible sur le site Web hébergé par le serveur Web (192.168.1.20).
-Des tutoriels détaillés pour la configuration des VMs et des services sont également disponibles sur le site Web.

Pour plus d'informations et des instructions détaillées, consultez la documentation et les tutoriels disponibles sur le site Web du projet.
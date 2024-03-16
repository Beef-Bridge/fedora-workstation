# Installation de l'OS Fedora Workstation

## Télécharement de l'ISO

Je commence par télécharger, sur un autre PC, le fichier `iso` de la version courante de la distribution Fedora Workstation depuis le [site officiel](https://fedoraproject.org/workstation/download).

> [!IMPORTANT]
> Je veille bien à récupérer la version du fichier `iso` correspondant à l'architecture de mon système. Dans mon cas "AMD x86_64" !

## Création d'une clé USB _bootable_
### Depuis MacOS avec BalenaEtcher

Il faut commencer par télécharger et installer l'utilitaire [BalenaEtcher](https://www.balena.io/etcher/).

Une fois fait, on branche une clé USB assez volumineuse pour pouvoir accueillir la distribution Fedora (> 16Go) et on lance l'application BalenaEtcher.

<img src="https://www.macplanete.com/wp-content/uploads/2022/06/creer-une-cle-USB-de-Linux-sur-Mac-balenaEtcher.jpg" alt="utilitaire BalenaEtcher" />

1. Choisir le bouton "Flash from file" et parcourir le Mac à la recherche du fichier ISO de la distribution Linux.
2. Cliquer sur "Select target" et sélectionner la clé USB insérée

<img src="https://www.macplanete.com/wp-content/uploads/2022/06/faire-cle-usb-bootable-ubuntu-sur-mac.jpg" alt="balena etcher - choisir clé USB">
3. De retour à l’interface principale, il ne reste plus qu’à cliquer sur le bouton "Flash!".
4. Une fenêtre s’ouvre en surimpression et nécessite que l'on saisisse le mot de passe administrateur du Mac, et cliquer sur OK lorsque c’est fait.

La phase de copie (_flashing_) de la distribution Linux sur la clé USB est en cours. Cela ne prend que quelques minutes.

Le message final est clair "Flash Complete!". Autrement dit la clé USB bootable de Linux est prête.

### Depuis Fedora avec Fedora Media Writer

Il faut commencer par installer l'utilitaire Fedora Media Writer : 
1. Ouvrir un terminal
2. Lancer la commande pour récupérer d'éventuelles mise à jour des paquets du système :

```sh
$ sudo dnf update
````
3. Installer l'application :
```sh
$ sudo dnf install mediawriter
````

Une fois fait, on branche une clé USB assez volumineuse pour pouvoir accueillir la distribution Fedora (> 16Go) et on lance l'application Fedora Media Writer.

1. Ouvrir l'application Fedora Media Writer
2. Choisir l'option "Select .iso file"
3. Sélectionner la clé USB de destination

<img src="https://ostechnix.com/wp-content/uploads/2023/11/Fedora-Write-Options.png" alt=""/>

4. Cliquer sur le bouton "Writer" pour lancer la création de la clé USB _bootable_.

<img src="https://ostechnix.com/wp-content/uploads/2023/11/Create-Fedora-Bootable-Live-USB-using-Fedora-Media-Writer.png" alt="" />

Patienter quelques minutes jusqu'à ce que la clé USB soit prête.

## Lancer l'installation de Fedora Workstation à partir d'une clé USB _bootable_

Pour lancer l'installation de Fedora à partir d'une clé USB _bootable_, il faut redémarré le PC et _booter_ sur "Fedora Workstation from Live USB.

Durant le processus d'installation, il faudra définir :
1. la langue du clavier (France, Français)
2. la date avec le fuseau horraire (Europe/Paris)
3. le disque dur sur lequel sera installé la distribution.


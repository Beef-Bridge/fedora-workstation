# Installation de Spotify

L'installation de ce logiciel se fait via la commande Flatpak.

1. Activer Flathub pour l'installation de Spotify :
```sh
$ sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
2. Installer Spotify via la commande Flatpak :
```sh
$ flatpak install flathub com.spotify.Client
```
3. Lancement de l'application en CLI :
```sh
$ flatpak run com.spotify.Client
```
4. Lancement de l'application depuis l'interfae utilisateur :
   1. Acivités
   2. Afficher les applications
   3. Rechercher 'Spotify'

5. Have fun!
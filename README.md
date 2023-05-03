# entrainement_reseau

## Debian Server

apt install apache2

systemctl status apache2 → restart if not

su root root

apt install vim

/etc/networks/interfaces

pas le .d

![image](https://user-images.githubusercontent.com/117074595/236054863-3a179158-3e3f-43b9-a378-e77cc52061a5.png)

vim /etc/resolv.conf

![image](https://user-images.githubusercontent.com/117074595/236055344-1d76be7c-8fdc-4b0e-8371-0ae9285f0207.png)

## OPNsense

—> installer

changer le clavier en fr-kbd qqch comme ça

faire entrer partout

une fois dans le cmd, login : installer ; mdp : opnsense

attendre

fermé

maintenant suppr l’iso :

![image](https://user-images.githubusercontent.com/117074595/236056375-6509e8b5-ba12-4b69-82a2-1c682e77b914.png)


ne pas encore réallumer

faire les cartes réseaux nécessaires,

carte réseau 1 sur NAT

carte réseau 2 sur réseau interne, renommé en admin

carte réseau 3 sur réseau interne, renommé en server

asign les interfaces avec 1

on veut pas VLAN

—> em0 c’est configurer sur la carte réseau 1, em1 sur la 2, etc

choisir donc em0 sur le WAN

LAN —> em1

LAN optionnel —> em2

passer à l’étape 2)

configure le LAN en premier (tapez 1 du coup)

—> ne pas mettre le DHCP pour rester en static

—> du coup mettre l’iip fixe : 192.168.1.1

—> mettre 24 pour le masque

—> puis enter pour none car on configure un LAN

—> faire ue des enter après ça

onfigure le LAN 2 après (tapez 2 du coup)

—> pareil mais 2.1

maintenant les config sont finis.

laiiser le opnsense allulmer

et config le debian

allumer le

ping si possible

## windows server

experience de bureau
installation disque personnaliser

une fois sur l'ad
installer adds et le dns
resoudre ainsi les probleme grace au drapeau
c'est a dire creer une foret avec un nom de domaine et un mots de passe ex: ozan.local
faire entré pour le reste

puis aller dans server local, puis ethernet, dans les propriétés,
decoché ipv6, double cliqué sur ipv4, et configurer le :
1.2
auto
1.1

1.2
8888

cocher appliqué, puis --> ok

ensuite aller dans le navigateur mozilla ou autre, taper l'ip de la carte réseau associé à l'opensense, c'est à dire 1.1

root root

atterir sur opn et configurer le bordel

## OPNsense

je sais pas plus pour les règles de parefeu
.

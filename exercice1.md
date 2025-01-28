partition:

sudo fdisk /dev/sdb
n
p
2 0 1-4
p ou entrer
+6G
w pour garder

*1 partition de 6 Go de type ext4 nommée "DATA"
sudo mkfs.ext4 /dev/sdb2
sudo mkfs.ext4 -L DATA /dev/sdb2

*1 partitio avec le reste du disque de type swap nommée "SWAP"
fdisk /dev/sdb
n
t
L 
p
82
w

mkswap /dev/sdb3
swapon/dev/sdb3

*Montage automatique

- Recuperer l'UUID
blkid /dev/sdb2

UUID=b56cb481-a6aa-437d-9bb6-be72412ada3c /mnt/DATA ext4 default 0 2
UUID=fd5ec5e9-b8c7-4333-a498-d944ccb43f98 none swap sw 0 0

*copier sur le:
nano etc/fstab/ dans dernier ligne

UUID=b56cb481-a6aa-437d-9bb6-be72412ada3c /mnt/DATA ext4 default 0 2
UUID=fd5ec5e9-b8c7-4333-a498-d944ccb43f98 none swap sw 0 0
mkdir -p /mnt/DATA
mount /mnt/DATA
VERIFIER:
Lsblk -f

Exercice 2
Script de création d’utilisateurs en Bash
Nom : addUsers.sh
3utilisateur : user1, user2, user3



Utilisateur créé enfin :


EXERCICE – 3
1. cat /etc/passwd
2. chmod 744 myfile
 
3.
Variable d’environnement :ont utilise pour transmettre des confgiurations ou des informations aux  processus enfants (ENV_VAR= « bonjour »)
Variable locale :ont utilise pour les données qui ne doivent pas être accessibles  hors du script ou la fonction (LOCAL_VAR= « Bonjour »)
4 .
Syntaxe de base de la structure if
if [ condition ]; then
    # Code à exécuter si la condition est vraie
elif [ autre_condition ]; then
    # Code à exécuter si l'autre condition est vraie
else
    # Code à exécuter si aucune condition n'est vraie
Fi
____________________________________________________
#!/bin/bash
if [ "$number" -gt 0 ]; then
    echo "Le nombre est positif."
elif [ "$number" -lt 0 ]; then
    echo "Le nombre est négatif."
else
    echo "Le nombre est zéro."
Fi
5. 
echo 'Malgré le prix élevé de 100$, il a dit' echo '"Bonjour !" au vendeur:' echo
'"Bonjour est-ce que ce clavier fonctionne bien ?''' echo '"Evidemment! On peut tout écrire avec, que ce soit des pipe | ou bien des backslash |\ !''' echo '"Même des tildes ~ ?'' echo ""Evidemment!"''
6. 
fg %1
7
. Couche 2 :
Switch : Gère les adresses MAC, relie les appareils sur un même réseau. Pont : Relie des segments de réseau. Couche 3 :
Routeur : Gère les adresses IP, relie différents réseaux. Passerelle : Relie des réseaux de types différents.
8.
 cd: cd
cp: Copy-Item
mkdir : mkdir
ls : Get-ChildItem
9. 
Payload : C'est les données utiles dans une trame Ethernet
10
CIDR : remplace les classes IP :pour mieux gérer les adresses et éviter le gaspillage.

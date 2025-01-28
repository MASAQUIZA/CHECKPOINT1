# EXERCICE 1
## partition:

sudo fdisk /dev/sdb
n
p
2 0 1-4
p ou entrer
+6G
w pour garder

![Capture d'écran 2025-01-28 114034](https://github.com/user-attachments/assets/e5d9296c-7a59-4951-9c44-244e6507903a)

## partition de 6 Go de type ext4 nommée "DATA"
sudo mkfs.ext4 /dev/sdb2
sudo mkfs.ext4 -L DATA /dev/sdb2

## partitio avec le reste du disque de type swap nommée "SWAP"
fdisk /dev/sdb
n
t
L 
p
82
w

mkswap /dev/sdb3
swapon/dev/sdb3

## Montage automatique

- Recuperer l'UUID
blkid /dev/sdb2

UUID=b56cb481-a6aa-437d-9bb6-be72412ada3c /mnt/DATA ext4 default 0 2
UUID=fd5ec5e9-b8c7-4333-a498-d944ccb43f98 none swap sw 0 0
![Capture d'écran 2025-01-28 114044](https://github.com/user-attachments/assets/19ecc6df-7574-4ef8-88d7-abcaf24309a1)

## copier sur le:
nano etc/fstab/ dans dernier ligne

UUID=b56cb481-a6aa-437d-9bb6-be72412ada3c /mnt/DATA ext4 default 0 2
UUID=fd5ec5e9-b8c7-4333-a498-d944ccb43f98 none swap sw 0 0
mkdir -p /mnt/DATA
mount /mnt/DATA
VERIFIER:
Lsblk -f
![Capture d'écran 2025-01-28 114052](https://github.com/user-attachments/assets/fa79dea4-4d88-4cd4-9ab7-331b1555f9b6)

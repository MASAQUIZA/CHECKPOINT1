# EXERCICE 3
## 1.  cat /etc/passwd
<img width="368" alt="image" src="https://github.com/user-attachments/assets/6f68d743-6efe-4755-a07e-c4ac33eb60e5" />

## 2.  chmod 744 myfile
 ![Capture d'écran 2025-01-28 114113](https://github.com/user-attachments/assets/ed44c83d-0619-4ec8-9a63-ef9232a5692c)

## 3.
Variable d’environnement :ont utilise pour transmettre des confgiurations ou des informations aux  processus enfants (ENV_VAR= « bonjour »)
Variable locale :ont utilise pour les données qui ne doivent pas être accessibles  hors du script ou la fonction (LOCAL_VAR= « Bonjour »)
## 4.
Syntaxe de base de la structure if
if [ condition ]; then
    # Code à exécuter si la condition est vraie
elif [ autre_condition ]; then
    # Code à exécuter si l'autre condition est vraie
else
    # Code à exécuter si aucune condition n'est vraie
Fi
________________
#!/bin/bash
if [ "$number" -gt 0 ]; then
    echo "Le nombre est positif."
elif [ "$number" -lt 0 ]; then
    echo "Le nombre est négatif."
else
    echo "Le nombre est zéro."
Fi
## 5. 
echo 'Malgré le prix élevé de 100$, il a dit' 
echo '"Bonjour !" au vendeur:' 
echo'"Bonjour est-ce que ce clavier fonctionne bien ?''' 
echo '"Evidemment! On peut tout écrire avec, que ce soit des pipe | ou bien des backslash |\ !''' echo '"Même des tildes ~ ?'' 
echo ""Evidemment!"''
## 6. 
fg %1
## 7. 
Couche 2 :
Switch : Gère les adresses MAC, relie les appareils sur un même réseau. Pont : Relie des segments de réseau. Couche 3 :
Routeur : Gère les adresses IP, relie différents réseaux. Passerelle : Relie des réseaux de types différents.
## 8.
cd: cd
cp: Copy-Item
mkdir : mkdir
ls : Get-ChildItem
## 9. 
Payload : C'est les données utiles dans une trame Ethernet
## 10. 
CIDR : remplace les classes IP :pour mieux gérer les adresses et éviter le gaspillage.

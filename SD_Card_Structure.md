# Structure de la carte SD
  - /ACTION
  ... 
  - /CONFIG  
  Contient le fichier Json mis à jour  
  - /DEFAULT  
  Les sons Moteur par défaut  
  - /ENGINE  
  Les sons Moteur  
  - /ENGINE/BEIER  
  Les sons Moteur au format Beier  
  - /FIXEDSOUND  
  Sons divers OBLIGATOIRE pour les Fonctions Spéciales  
  - /RANDOM  
  Contient les sons utilisés en plus de ambiant en mode aléatoire  
  - /USERSOUND  
  Liste des 16 sons attribués aux boutons  

## USERSOUND
Si aucun fichier spécifique n'est trouvé dans le répertoire /USERSOUND, le système les définira comme NOT USED.  
Un appuis sur le bouton 5 et 6, ici, ne fera rien .  
```
USER1 = /USERSOUND/1_SHORT.WAV  
USER2 = /USERSOUND/2_LONG.WAV  
USER3 = /USERSOUND/3_SEAGULL.WAV  
USER4 = /USERSOUND/4_RING.WAV  
USER5 = NOT USED  
USER6 = NOT USED  
```

## FOG 
Sons fixes autorisés même si FOG == false : GUN, MG, HORN , ALARM  
Autres sons fixes (lié a FOG) :  
Joués uniquement si FOG == true, sinon un son utilisateur est utilisé à la place.  
Ces boutons ont donc une double fonctionnalité suivant que le switch FOG soit actif ou non.  

## RANDOM
Lit les fichiers se trouvant dans le répertoire /RANDOM/X_NOM.wav attribue ces fichier aux sons RANDOM jusqu'à 8 sons disponibles.  
Compte le nombres de fichiers disponible pour adapter la fonction random aux nombres de sons 
"Nombre de sons aléatoires disponibles : 4"  
```
RANDOM_1 = /RANDOM/1_MOUETTE.WAV  
RANDOM_2 = /RANDOM/2_MOUETTE2.WAV  
RANDOM_3 = /RANDOM/3_MOUETTE3.WAV  
RANDOM_4 = /RANDOM/4_MOUETTE4.WAV  
RANDOM_5 = NOT USED  
RANDOM_6 = NOT USED  
RANDOM_7 = NOT USED  
RANDOM_8 = NOT USED  
```
 

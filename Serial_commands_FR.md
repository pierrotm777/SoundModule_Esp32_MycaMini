```
	- H Help
	Liste toutes les commandes disponibles
	- SW set Default settings
	Réinitialise la configuration avec les paramètres par défaut
	- S? Read Settings
	Affiche la configuration actuelle
	- W? Board Connections
	Liste les connexions matérielles à réaliser (câblage des sorties)
	- SI X X=1(PWM), X=2(CPPM), X=3(SBUS), X=4(IBUS), X=5(SUMD), X=6(JETI), X=7(SRXL), X=8(CRSF)
	Définit le type de signal d'entrée utilisé pour la radio
	- SX Y Z Y=0 to 16 Xany 0=OFF 1 to 16=Xany Channel / Z=1 to 4 Xany mode
	Configure l'entrée RCUL : Y=canal, Z=mode (1: 8 inters, 2: 16 inters, 3: 8 inters + prop., 4: angle + prop.)
	- SY Y Z Y=0 to 16 Xany 0=OFF 1 to 16=Xany Channel / Z=1 to 4 Xany mode
	Configure l'entrée RCUL5 (mêmes paramètres que SX)
																									 
	- F X X=0 to 3 Set Xany filter
	Définit le niveau de filtrage du signal Xany (0 à 3)
	- R set Ambient On/Off
	Active ou désactive le son d'ambiance
	- S1 X=Ch set Ambient Ch
	Attribue un canal pour activer/désactiver le son d’ambiance
	- S2 X=Ch set Fog Ch
	Attribue un canal pour activer/désactiver le mode brouillard
	- S3 X=Ch set Anchor Ch
	Attribue un canal pour piloter le son du treuil de l’ancre
	- S4 X=Ch set Ambients Random Ch
	Attribue un canal pour lancer aléatoirement des sons d’ambiance
	- S5 X=Ch set Motor Ch
	Attribue un canal pour démarrer/arrêter le son moteur
	- S6 X=Ch set Action1 Ch
	Attribue un canal pour une action utilisateur personnalisée
	- S7 X=Ch set Action2 Ch  >>> est devenu ESC 
	Attribue un canal pour activer ou désactiver la gestion d'un esc qui sera géré comme la variation du son moteur 
	- G Y=0 or 1 set Xany=0 Buttons=1
	Sélectionne le mode de contrôle : 0 = via écran, 1 = via émetteur (boutons)
	- X1 Y Y=0 to 2 Debug RCUL1 Mode (visible uniquement si DEBU_XANY est activé)
	Active les modes de debug RCUL1 (0: off, 1: log, 2: détails)
	- X5 Y Y=0 to 2 Debug RCUL5 Mode (visible uniquement si DEBU_XANY est activé)
	Active les modes de debug RCUL5 (0: off, 1: log, 2: détails)
	- U0 set Smoke On/Off
	Active ou désactive la production de fumée
	- U1 X=Ch set Engine Ch
	Attribue un canal pour contrôler le régime du son moteur
	- U2 X=0 or 1 set Engine Mode
	Sélectionne le type de modèle : 0 = bateau, 1 = avion
	- U3 X=name set Engine Name
	Définit le nom du moteur 
	- U4 X set Engine/Smoke STOP after X seconds
	Définit le délai d'arrêt du moteur et de la fumée après relâchement (ou manche au neutre)
	- U5 X=Ch set Smoke On/Off Ch
	Attribue un canal pour activer/désactiver la pompe à fumée
	- U6 X=10 to 50 set Minimum Smoke
	Définit le niveau minimum de fumée produit
	- U7 X=100 to 255 set Maximum Smoke
	Définit le niveau maximum de fumée produit
	- U8 X=1 to 10 set Engine Speed
	Définit la vitesse de variation du son moteur
	- U9  X=0 or 1 set ESC On Off
	Active la gestion d'un esc qui sera géré comme la variation du son moteur
	- U10 X set Anchor SoundD STOP after X seconds
	Définit la durée avant l’arrêt automatique du son de l’ancre
	- I I=XXXX X=N or P (Alarms Priorities)
	Définit les priorités des sons d'alarmes (expérimental)
	- V X X=Ch Set Volume Ch (Ch=100 if by XANY)
	Attribue un canal pour le réglage du volume général
	- M Check Min and Max Channel
	Lit et mémorise les valeurs min/max µs des voies du récepteur
	- P X Y X=0 to 13 (Sound) / Y=1 to 4 (Start/Idle/Stop, 4=PRINT SOUNDS)
	Teste les sons moteur (Y=1: start, 2: idle, 3: stop, 4: liste les sons)
	- A X X=NAME (Read NAME.wav file from root SDcard).
	Lit un fichier son placé à la racine de la carte SD
	- D Debug Mode On/Off
	Active ou désactive le mode de débogage global
	- L Y Y=100 to 255 ms (Check All leds at Y speed)
	Teste toutes les LED RGB à l’intervalle Y millisecondes
	- SV X X=1.0 External Voltage Scale
	Calibre l’échelle de tension externe pour une lecture précise en télémétrie

	- TEST X X=1 to 16 Play USERX.wav from SD root
	Joue un fichier sonore utilisateur (depuis / ou /USERSOUND/)
	- FS S B  S=SoundName B=Button (1-16). Ex: FS confirm 3
	Assigne une fonction Spéciales à un bouton
	- FS?  
	Liste les assignations actuelles des boutons
	- FS_RESET  
	Supprime toutes les assignations de Fonction Spéciales aux boutons
	- REPEAT B X=0/1  
	Active (1) ou désactive (0) le mode répétition pour un bouton
	- REPEAT?  
	Affiche l’état de répétition de tous les boutons
	- REPEAT_RESET  
	Réinitialise tous les boutons en mode non répétitif
```
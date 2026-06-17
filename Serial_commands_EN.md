```
	- H Help
	Liste toutes les commandes
	- SW set Default settings
	Sauvegarde des variables par défaut
	- S? Read Settings
	Lite l'éat courant
	- W? Board Connections
	Liste le cablâge à réaliser
	- SI X X=1(PWM), X=2(CPPM), X=3(SBUS), X=4(IBUS), X=5(SUMD), X=6(JETI), X=7(SRXL), X=8(CRSF)
	Définie le type de connexion en entrée
	- SX Y Z Y=0 to 16 Xany 0=OFF 1 to 16=Xany Channel / Z=1 to 4 Xany mode
	Définie RCUL
	- SY Y Z Y=0 to 16 Xany 0=OFF 1 to 16=Xany Channel / Z=1 to 4 Xany mode
	Définie RCUL5
	Définie le type de connexion Xany Y=voie, Z=1(8 inters), 2(16 inters), 3(8 + PROP), 4(ANGLE + PROP)
	- F X X=0 to 3 Set Xany filter
	Définie un filtrage Xany entre 0 et 3
	- R set Ambient On/Off
	Active le son ambiant
	- S1 X=Ch set Ambient Ch
	Définie un canal pour le son Ambiant
	- S2 X=Ch set Fog Ch
	Définie un canal pour le Brouillard
	- S3 X=Ch set Anchor Ch
	Définie un canal pour le guindeau de l'ancre
	- S4 X=Ch set Ambients Random Ch
	Définie un canal pour les sons Ambiants lancés au hasard
	- S5 X=Ch set Motor Ch
	Définie un canal pour le démarrer le moteur
	- S6 X=Ch set Action1 Ch
	Définie un canal pour ????
	- S7 X=Ch set Action2 Ch
	Définie un canal pour ????
	- G Y=0 or 1 set Xany=0 Buttons=1
	Définie le mode ECRAN ou EMETEUR
	- X1 Y Y=0 to 2 Debug RCUL1 Mode (visible uniquement si DEBU_XANY est activé)
	Debug type Xany2Spy pour RCUL
	- X5 Y Y=0 to 2 Debug RCUL5 Mode (visible uniquement si DEBU_XANY est activé)
	Debug type Xany2Spy pour RCUL5
	- U0 set Smoke On/Off
	Active la cuve de la fumée
	- U1 X=Ch set Engine Ch
	Définie le canal pour la variation du son du moteur
	- U2 X=0 or 1 set Engine Mode
	Définie le type de modèle, bateau ou avion
	- U3 X=name set Engine Name
	Définie le nom du moteur
	- U4 X set Engine/Smoke STOP after X seconds
	Définie le temps après lequel le moteur et la fumée stoppent lorque le manche est centré ou position basse selon le model
	- U5 X=Ch set Smoke On/Off Ch
	Définie le canal de la pompe de fumée
	- U6 X=10 to 50 set Minimum Smoke
	Définie un minimum pour la fumée
	- U7 X=100 to 255 set Maximum Smoke
	Définie un maximum pour la fumée
	- U8 X=1 to 10 set Engine Speed
	Définie la vitesse de variation du son moteur
	- U9  X=0 or 1 set ESC On Off
	Active la gestion d'un esc qui sera géré comme la varaition du son moteur
	- U10 X set Anchor SoundD STOP after X seconds
	Définie un delai après quoi le son de l'ancre stop
	- I I=XXXX X=N or P (Alarms Priorities)
	Définie les prioritées des sons d'alarmes (non testé)
	- V X X=Ch Set Volume Ch (Ch=100 if by XANY)
	Définie le volume par défaut
	- M Check Min and Max Channel
	Lecture et sauvegarde des min et max en µS du récepteur utilisé
	- P X Y X=0 to 13 (Sound) / Y=1 to 4 (Start/Idle/Stop, 4=PRINT SOUNDS)
	Tests sons moteurs
	- A X X=NAME (Read NAME.wav file from root SDcard).
	Lecture d'un son à la racine de la carte SD
	- D Debug Mode On/Off
	Debug principal
	- L Y Y=100 to 255 ms (Check All leds at Y speed)
	Test des leds RGB
	- SV X X=1.0 External Voltage Scale
	Valeur à modifier pour obtenir une tension de la batterie précise en télémétrie
	
	- TEST X X=1 to 16 Play USERX.wav from SD root
	Lit un son USERx ou un son sous **/USERSOUND/**
	- FS S B  S=SoundName B=Button (1-16). Ex: FS confirm 3
	- FS? List assigned fixed sounds
	- FS_RESET Clear all fixed sound bindings
	- REPEAT B X=0/1 Set repeat OFF/ON for button B (1-16)
	- REPEAT? Show repeat state for all buttons
	- REPEAT_RESET Clear all repeat states
```
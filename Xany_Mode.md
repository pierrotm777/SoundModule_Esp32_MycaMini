# Xany Serial Commands

## Help Xany Menu
H  
```
H           : Afficher cette aide courte
SW          : Restaurer les paramètres par défaut (Non-Volatile)
W?          : Affiche le câblage de la carte
S?          : Afficher la configuration courante
SI <prot>   : Protocol=0(PWM), 1(CPPM), 2(SBUS), 3(IBUS), 4(SUMD), 5(JETI), 6(SRXL), 7(SRXL2), 8(CRSF), 9(FBUS)
M           : Mesurer les valeurs min/max des voies
D           : Basculer le mode Debug

SX <ch> <payload> : RCUL1 Channel=0(OFF), 1 to 16 / Payload=0(SW:8), 1(SW:16), 2(SW:8 + PROP), 3(SW:16 + PROP), 4(ANGLE + PROP)
SY <ch> <payload> : RCUL5 Channel=0(OFF), 1 to 16 / Payload=0(SW:8), 1(SW:16), 2(SW:8 + PROP), 3(SW:16 + PROP), 4(ANGLE + PROP)
F <lvl>           : Régler le niveau de filtre XANY (0..3)
G <mode>          : Mode commandes : 0=XANY / 1=Boutons
V <ch>            : Canal de volume (100 = XANY, 1..16 = CH)

S0 <ch>     : Canal de référence moteur/fumée
S1 <ch>     : Canal ON/OFF moteur
S2 <ch>     : Canal ambiances
S3 <ch>     : Canal brouillard (fog)
S4 <ch>     : Canal ancre
S5 <ch>     : Canal aléatoire d’ambiance
S6 <ch>     : Canal Action1
S7 <ch>     : Canal Action2
S8 <ch>     : Canal Action3
S9 <ch>     : Canal Action4
S10 <ch>    : Canal Action5
S11 <ch>    : Canal fumée (sécurité ON/OFF)
S12 <ch>    : Canal ESC

U0 <mode>   : Mode moteur (0=Bateau / 1=Avion)
U1 <nom>    : Sélection de la banque son moteur
U2 <val>    : Facteur vitesse moteur (1..10)
U3 <sec>    : Arrêt moteur/fumée après N secondes (0=off)
U4 <val>    : Valeur minimale fumée (10..50)
U5 <val>    : Valeur maximale fumée (100..255)
U6          : Réservoir fumée toujours ON/OFF (sécurité)
U7          : Activer/Désactiver le contrôle ESC
U8 <sec>    : Arrêt son ancre après N secondes
U9 <0|1>    : Engine system mode
U10 <name>  : Engine Beier name

B           : Lire les valeurs et modes des boutons
O <XXXXXXXX>: Définir le masque du mode pulse (X=0/1)
T           : Démarrer/Arrêter la calibration des boutons

I  <NN>     : Priorités des alarmes (2 caractères N/P)
C0          : Basculer les sons d’ambiance aléatoires
C1 <0|1>    : Activer les sons d’ambiance 0/1
C2 <0|1>    : Mode clavier boutons 0/1
C3 <0|1>    : La fumée suit le moteur 0/1
C4 <0|1>    : Activer les alarmes 0/1
C5 <0|1>    : Activer les LED RGB 0/1
C?          : Afficher la configuration des options

MEM           : Afficher info mémoires

L <speed>   : Tester toutes les LED RGB à une période (100..255 ms)
P <n>       : ENGINE_SOUND : 1=Start, 2=Idle, 3=Stop, 4=List
A <name>    : Lire <name>.wav à la racine SD
TEST <id>   : Tester un son utilisateur 1..16

REPEAT <B R C>   : Répétition OFF/ON pour bouton B (1..16), R=0/1, C=compte (0=∞)
REPEAT?          : Afficher l’état de répétition pour tous les boutons
REPEAT_RESET     : Effacer tous les états de répétition
FS <Sound> <Btn> : Associer un son fixe à un bouton (1..16). Ex : FS confirm 3
FS?              : Lister les sons fixes affectés
FS_RESET?        : Effacer tous les liens de sons fixes
HOLD <B H>       : Mode Hold OFF/ON pour bouton B (1..16), H=0/1
HOLD?            : Afficher l’état Hold pour tous les boutons
HOLD_RESET       : Effacer tous les états Hold
ALL?             : Afficher toutes les affectations (fixe/utilisateur) + repeat/hold
VOL_AMB <0..100> : Volume des ambiances (0..100)
FH_TYPE <n>      : Variant du corne de brume (1 = SHORT_1/LONG_1…)
AL_TYPE <n>      : Variant d’alarme (1..2)

TM <type>   : TM=0(None), 1(Frsky Hub), 2(Frsky Sport), 3(IBUS), 4(CRSF), 5(HOTT), 6(JETIEX ), 7(RADIOLINK), 8(MLINK), 9(FBUS)
SV <fact>   : Facteur d’échelle tension externe (ex : 1.0 = valeur brute)

SAVE        : Sauvegarder tous les réglages (BIN + JSON)
LOAD [J]    : Charger les réglages (BIN ou JSON avec 'J')
Z           : Effacer toute l’EEPROM

DEBUG_STRUCT     : Debug des structures cibles (volume, moteur, LED, ...)
MEM         : Afficher info mémoires
```

S?  for Screen mode (type G 0)  
```
oO Settings Oo
SBUS [ Xany by Screen ] use Channels 6(1) and 7(2) | Filter:0 | SW:16(1) SW:8 + PROP(RCUL5)
S-PORT Telemetry in use.
SD Card   : Ready
ENG.LIST  : BF109, CAT-C32, DIESEL, DIESEL7, DSL-120, DSL-180, DSL-BIG, DSL-LTL, DSL-OLD, DSL-TUG, DSL-TURB, DSL-V12, MOTOR, PT-BOAT, SCAN-250, SCAN-V12, VAPEUR
Engine   1: Ready (Boat Mode) Name:MOTOR Use Ch:2 (Start by Xany)
Volume    : Use Xany (Limited Vol:0.10)
Ambient   : (Off) Use Xany
Amb. Rnd. : (Off) Use Xany
Fog       : (Off) Use Xany
Anchor    : (Off) Use Xany
Action    : (Off) Use Xany
Action2   : (Off) Use Xany
Smoke     : (Enabled)  (Off) Use Xany
Engine Spd: 4
ESC       : (Enabled)  (Off) Use Xany
Smoke Ach : 2
Smoke Min : 40
Smoke Max : 126
Priorities: 0000 (Alarms Sounds)
Mini Ch   : 1000
Maxi Ch   : 2000
Scale ExtV: 1.26
```

S?  for Handset mode (type G 1)
```
Sound Module 1.5.2 Powered By Rc-Navy libraries

oO Settings for PIERRE Oo
SBUS [ Xany by Screen ] use Channels 6(RCUL) and 7(RCUL5) | Filter:0 | SW:16(RCUL) SW:16 + PROP(RCUL5)
Telemetry : Frsky Sport in use
SD Card   : Ready
ENG.LIST  : BF109, C63AMG, CAT-C32, DIESEL, DIESEL7, DSL-120, DSL-180, DSL-BIG, DSL-LTL, DSL-OLD, DSL-TUG, DSL-TURB, DSL-V12, HAWK-TMP, MOTOR, PT-BOAT, RIVA, SCAN-250, SCAN-V12, VAPEUR
EngineSys : CLASSIC
Engine    : Ready (Boat Mode) Name:DSL-V12 Use Ch:2 (Start by Xany)
Volume    : Use Xany (Limited Vol:0.10)
Ambient   : (Off) Use Xany
Amb. Rnd. : (Off) Use Xany
Fog       : (Off) Use Xany
Anchor    : (Off) Use Xany
Action    : (Off) Use Xany
Action2   : (Off) Use Xany
Action3   : (Off) Use Xany
Action4   : (Off) Use Xany
Action5   : (Off) Use Xany
ESC       : (Off) Use Xany
Smoke     : (Enabled)  (Off) Use Xany
Engine Spd: 8
ESC       : (Enabled)  (Off) Use Xany
Priorities: NN (Alarms Sounds)
Mini Ch   : 1000
Maxi Ch   : 2000
Scale ExtV: 1.00
Temp CPU  : 62.40°C / 144.32°F
EspNow is : (On) 
External I2C is Ready:
Nano    is: (Off)
Smoke   is: (Off)
TmpTank is: (Off)
```

## Explanation of all XANY commands
The following commands appear in XANY mode (G 0)  
	- [Serial Commands FR](Serial_commands_FR.md)  
	- [Serial Commands EN](Serial_commands_EN.md)  
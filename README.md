# 2023_1D_S5_SystNum_Boutiche_Beugre
CompteRendu TP1 Système Numérique
Auteurs : Beugré Esther Boutiche Abdelrahmen
Réponses aux questions
1) Le rôle de cette carte est d’ajouter des capacités ou des au
microcontrôleur ici, NUCLEO-L476RG
2) Il peut gérer 16 entrées/sorties GPIO simultanément.
3) On y reviendra
4) 10 MHz est la fréquence maximale qu’on peut communiquer à la
MCP23S17
5) La liste des pins reliés au microcontrôleur et leurs rôles
• Pin 18 Vu_nRESET : il sert à faire une remise à 0
• Pin 11 Vu_nCS : il sert à faire un chip select
• Pin 12 Vu_SCK : il correspond à l’horloge d’entrée
• Pin 13 Vu_MOSI : Il est utilisé pour la réception de données
• Pin 14 Vu_MUSO : Il est utilisé pour la transmission de donnes

7) Tableau des associations des pins
Le microcontrôleur La MCP23S17
Pin 128             Vu_nRESET Pin 18
Pin 121             Vu_nCS Pin 11
Pin 101             Vu_SCK Pin 12
Pin 229             Vu_MOSI Pin 13
Pin 102             Vu_MUSO Pin 14

8) Définition : L’opcode est la partie d’une instruction en langage qui
spécifie l’opération à effectuer
Les pins A0, A1 et A2 servent à faire de l’adressage
9) Les pins INTA et INTB servent à interrompre les systèmes
10) La valeur de la sortie d’une pin pour allumer la led est : 0,6
11) Les résistances R501 à R516 servent à éviter de griller la led. Et la
différence de leurs valeurs est du au fait qu’elles sont elles mêmes
différentes. On a des leds de couleurs différente, rouges et oranges qui
éclaire de manière différente, et donc qui nécessite un appel de courant
différent
12)Chaque registre correspond a un bloc de pins, si on veut ecrire sur un pin particulier il faut ecrire sur son registre attribue, les IODIR contiennent toute les entree/sorties, les GPIO tous les GPIO.
13)En mettant tous les bits des registres GPIOA et GPIOB a 1, cela permet d'allumer toute les leds
14)En mettant tous les bits des registres GPIOA et GPIOB a 0, cela permet d'eteindre toute les leds
15)Pour allumer seulement la led D508 il faut mettre le 8e bit du registre GPIOB a 1 

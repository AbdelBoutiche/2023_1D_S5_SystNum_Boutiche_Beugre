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
16) Pour configurer l'ensemble des pins correctement,
La trame a envoyer pour configurer toute les GPIOA en sortie (mise a 0)  : OPCode :0100000 W/R:0 Address: 0000 0000 Data: 0000 0000
La trame a envoyer pour configurer toute les GPIOB en sortie (mise a 0)  : OPCode :0100000 W/R:0 Address: 0000 0001 Data: 0000 0000

La trame a envoyer pour allumer toute les leds:
Pour allumer toute les leds relies a GPIO A : OPCode :0100000 W/R:0 Address: 0001 0010 Data: 1111 1111
Pour allumer toute les leds relies a GPIO B : OPCode :0100000 W/R:0 Address: 0001 0011 Data: 1111 1111

La trame a envoyer pour eteindre toute les leds:
Pour eteindre toute les leds relies a GPIO A : OPCode :0100000 W/R:0 Address: 0001 0010 Data: 0000 0000
Pour eteindre toute les leds relies a GPIO B : OPCode :0100000 W/R:0 Address: 0001 0011 Data: 0000 0000 
On envoi au total 18 octets au composant





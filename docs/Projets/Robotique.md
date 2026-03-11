# La robotique

## Introduction

??? abstract  "Histoire de robots : ..."

    <center>
    <iframe frameborder="0" width="720" height="405"  src="https://www.dailymotion.com/embed/video/x2u6uxc" allowfullscreen="" allow="autoplay"></iframe>
    </center>

??? abstract  "Evolution technologique de l'unité de traitement : ..."

    Un système technique (automatisme, robot, objet connecté (IoT), système embarqué...) peut-être représenté par sa chaîne d'information et sa chaîne d'énergie tel que :

    <center><img src="https://ericecmorlaix.github.io/img/AnalyseSystemique-GlobaleFocusTraiter.svg" alt="Focus sur la chaine d'information"></center>

    Dans un projet de robotique, le composant à programmer est celui qui réalise la fonction **traiter**.

    C'est dans ce domaine que les solutions ont particulièrement évolué ces dernières années :  
    Les progrès en automatisme industriel et en robotique sont intimmement liés aux évolutions de l'informatique générale et à celle des ordinateurs en particulier. Ce sont des branches cousines qui suivent des évolutions parallèles avec souvent un décalage temporel inhérent aux besoins de développer des solutions fiables et robustes à coût réduit.

    | <img src="https://ericecmorlaix.github.io/img/Sequenceur_a_cames.jpg" width="80%"> | <img src="https://ericecmorlaix.github.io/img/sequenceur.png" width="85%"> | <img src="https://ericecmorlaix.github.io/img/Relais.jpg" width="60%">  | <img src="https://ericecmorlaix.github.io/img/lampe.jpg" width="60%">  |
    |:-:|:-:|:-:|:-:|
    | Séquenceur à cames  | Séquenceur pneumatique  |  Relais | Tubes à vide  |

    Les solutions mécaniques (cames), pneumatiques (séquenceur), électriques (relais), ont laissé la place à celles électroniques des tubes à vide, remplacés par des [transistors](https://fr.wikipedia.org/wiki/Transistor){target=_blank} à partir du milieu des années 1950 eux mêmes miniturisés dans des [circuits intégrés](https://fr.wikipedia.org/wiki/Circuit_int%C3%A9gr%C3%A9){target=_blank} (1958) et dans les [microprocesseurs](https://fr.wikipedia.org/wiki/Microprocesseur){target=_blank} (1969).

    <center><img src="https://ericecmorlaix.github.io/img/TI_TMS1000.jpg" width="55%"></center>

    Les premiers microcontrôleurs apparaisent dans les années 70, Texas Instrument, son inventeur, commercialise à partir de 1974 les [TMS1000](https://en.wikipedia.org/wiki/Texas_Instruments_TMS1000){target=_blank} mais c'est depuis la fin des années 90 qu'ils se sont développés de manière spectaculaire.

    <center><img src="https://ericecmorlaix.github.io/img/architecture_%C2%B5C_base.png" width="75%"></center>

    Un [microcontrôleur](https://fr.wikipedia.org/wiki/Microcontr%C3%B4leur){target=_blank} est en quelque sorte un ordinateur miniaturisé et simplifié généralement dédié à une application de traitement de l'information dans un système embarqué (clavier, souris, automobile, calculatrice, électroménagé, jeux, ...)  Il inclut, sur une même puce, à minima, un microprocesseur, de la mémoire ROM et RAM, une interface entrées/sorties (GPIO, General Purpose Input/Output) et selon le cas d'autres modules tels qu'un oscillateur, un convertisseur analogique numérique (CAN), un Timer, de la mémoire flash, EPROM ou EEPROM, des générateurs de signaux MLI (PWM), des controleurs de communication UART, SPI, I2C, radio, Bluetooth, Wifi...

    ??? tip ""Flasher" ? ..."

        <center><img src="https://ericecmorlaix.github.io/img/sourisLogitec_%C2%B5C.png" width="40%"></center>

        On observe sur le boitier de ce microcontrôleur la fenêtre qui permetait par insolation de rayons UV d'effacer l'EPROM, Ereasable Programmable Read Only Memory. Cette mémoire possède les mêmes propriétés que la ROM sauf que l'on peut l'effacer pour la reprogrammer. L'EPROM est accessible en lecture uniquement, et contient généralement le programme à exécuter.

        >C'est de là que viendrait le verbe **"flasher"** synonyme de téléverser un programme dans le microcontroleur.  
        >Aujourd'hui on continue donc à "flasher" mais de l'EEPROM : Electrically Ereasable Programmable Read Only Memory.

    ???+ abstract "Arduino : ..."

        Il était encore complexe et coûteux de mettre en œuvre un microcontrôleur au début des années 2000. L'arrivée de cartes à microcontrôleur telles que l'Arduino à partir de 2005 a grandement simplifié la chose. Cela ne nécessite alors que du matériel peu coûteux, environ 20€ pour la carte la plus populaire qu'est l'Arduino Uno R3 basée sur l'ATmega328. Un simple PC suffit pour le développement du programme en langage C.

        <center><img src="https://ericecmorlaix.github.io/img/Arduino_Uno-R3.jpg" width="45%"></center>

    ???+ abstract "Raspberry PI : ..."
    
        En 2012 l'ordinateur à carte unique Raspberry PI, un [Single Board Computer](https://en.wikipedia.org/wiki/Single-board_computer){target=_blank} low cost, avec son [GPIO](https://fr.wikipedia.org/wiki/General_Purpose_Input/Output){target=_blank} vient concurrencer les cartes à microcontrôleur pour des applications qui requièrent un interfaçage vers des appareils simples mais avec plus de capacité de calcul. Le langage de programmation privilégié sur cette plateforme est Python.

        > Le processeur du Raspberry PI est également monté sur une puce ([SoC](https://en.wikipedia.org/wiki/System_on_a_chip){target=_blank}) plus coûteux et énergivore qu'un simple microcontrôleur il intègre plus de fonctionnalités : [MCU vs SOC](https://www.geeksforgeeks.org/difference-between-mcu-and-soc/){target=_blank}.  

        <center><img src="https://ericecmorlaix.github.io/img/Raspberry_Pi_Model_B.jpg" width="45%"></center>

    ???+ abstract "MicrPython : ..."
    
        Depuis 2013, l'augmentation des capacités de certains microcontrôleur permet de les programmer également en [MicroPython](https://github.com/micropython){target=_blank} une version allégée de Python 3 créée par [Damien George](https://github.com/dpgeorge){target=_blank}

        C'est le cas des cartes BBC micro:bit V1 et V2, du Circuit Playground Express (CPX), des ESP8266 et ESP32.

        | <img src="https://ericecmorlaix.github.io/img/bbcmicrobit.gif" width="95%"> | <img src="https://ericecmorlaix.github.io/img/ESP8266.jpg" width="95%"> |  <img src="https://ericecmorlaix.github.io/img/CPX.gif" width="95%"> | <img src="https://ericecmorlaix.github.io/img/lolin32.jpg" width="95%">  |
        |:-:|:-:|:-:|:-:|
        | [BBC micro:bit](https://tech.microbit.org/hardware/)  | [Wemos ESP8266](https://wiki.wemos.cc/products:d1:d1_mini)  |  [Adafruit CPX](https://www.adafruit.com/product/3333) | [Wemos ESP32](https://wiki.wemos.cc/products:lolin32:lolin32)  |

    Les microcontrôleurs sont donc devenus des composants électronique incontournables, modifiant profondément la manière de concevoir les circuits électroniques des systèmes embarqués et des objets connectés.

        
    > *" Les objets qui sont dotés d'un microcontrôleur embarqué, éventuellement en réseau, deviennent enchantés de la même façon que les objets des mondes magiques : il suffit de leur donner des ordres. Comme dans les histoires de magie, il est impératif d'apprendre comment réalise les incantations pour que les objets enchantés se plient à votre volonté.*
    >
    > *Et c'est ici qu'entre en jeu le langage MicroPython "*
    >
    > Extrait du livre de Nicholas H. Tollervey, Programming with MicroPython.

    ???+ info "Autres cartes : ..." 

        | <img src="https://ericecmorlaix.github.io/img/Calliope.jpg" width="95%">   |  <img src="https://ericecmorlaix.github.io/img/M5.jpg" width="95%"> | <img src="https://ericecmorlaix.github.io/img/halocode.png" width="95%">  | <img src="https://ericecmorlaix.github.io/img/Tiny2040.jpg" width="80%">  | <img src="https://ericecmorlaix.github.io/img/PI_Pico_W.jpg" width="50%">  |
        |:-:|:-:|:-:|:-:|:-:|
        |[CALLIOPE](https://en.wikipedia.org/wiki/Calliope_mini)   | [m5stack](https://m5stack.com/)  | [HALOCODE](https://www.makeblock.com/steam-kits/halocode)| [Tiny 2040](https://www.raspberrypi.com/documentation/microcontrollers/rp2040.html) | [Raspberry Pi Pico](https://www.raspberrypi.com/documentation/microcontrollers/raspberry-pi-pico.html)  |

        ***
        >Sortie en novembre 2020, le Raspberry Pi 400  inclut un ordinateur complet dans un clavier. Cette idée n'est pas nouvelle, elle s'inspire des  machines des années 80 telles que le [BBC micro](https://fr.wikipedia.org/wiki/BBC_Micro){target=_blank} :

        ><center><img src="https://images.prismic.io/rpf-products/877421eb-1c8f-4698-853e-9bf664e9b061_400%20Desktop%20KIt%20Main.jpg" width="40%">
        ><figcaption><a href="https://www.01net.com/actualites/raspberry-pi-400-le-mini-ordinateur-se-glisse-enfin-dans-un-clavier-2000549.html" target="_blank">Le Nouveau Raspberry Pi 400 : un mini-ordinateur dans un clavier !</a></figcaption></center> 
    
      

## Applications sur BBC micro:bit

<center><img src="https://ericecmorlaix.github.io/img/bbcmicrobit.gif" width="70%"></center>

> **Prérequis** :  [Savoir programmer un BBC micro:bit](https://ericecmorlaix.github.io/adn-Tutoriel_lab_si/IOT/BBC_microbit/){target=_blank}

Le point de vue du programmeur en robotique concerne donc l'unité de traitement qui reçoit des informations électriques en **entrées** et en émet en **sortie** :

<center><img src="https://ericecmorlaix.github.io/img/traiter.svg" width="50%"></center>

??? abstract "Les broches"

    Il y a 25 connecteurs en cuivre sur la tranche du bas de la carte BBC micro:bit. Ce sont des Entrées/Sorties qui permettent au micro:bit d'interagir avec son environnement en s'y connectant physiquement.

    Le BBC micro:bit dispose de 19 broches qui peuvent être utiliser en tant que :

    - sortie pour faire fonctionner des **actionneurs** tels qu'une LED, un moteur ou encore un buzzer...
    - entrée logique pour faire fonctionner des **capteurs** tels qu'une fourche optique, un Interrupteur à Lame Souple, un contact de fin de course, un bouton poussoir...

    Chacunes est associées à un objet `pinN`, instance de la class `pin`, ou `N`correspond au numéro attribué à la broche de 0 à 16 ainsi que 19 et 20.

    <center><img src="https://microbit-micropython.readthedocs.io/en/v1.0.1/_images/pinout.png" alt="Broches" width=50%></center>

    !!! warning "Partage de broches"
        
        Si ces broches sont utilisées en tant qu'entrée/sortie externes alors leurs autres fonctionnalités internes potentielles ne seront pas disponibles simultannément.
        
        Par exemple les broches `pin3`, `pin4`, `pin6`, `pin7`, `pin9` et `pin10` sont également raccordées à la matrice de LEDs, il faudra donc [désactiver l'affichage](https://microbit-micropython.readthedocs.io/en/latest/display.html#microbit.display.off){target=_blank} afin de les libérer pour autre chose : `microbit.display.off()`.

    !!! tip "Raccordement"

        Pour pouvoir utiliser ces broches il faut les raccorder physiquement à d'autres composants électoniques par l'intermédiaire de fils à connecteur bannane ou à pince crocodile ou encore avec des straps sur une platine d'essais via un connecteur...

        <center><img src="https://ericecmorlaix.github.io/img/breadbit.png" width="50%"></center>
        <center><figcaption><a href="https://perso.crans.org/geneau/NewCligne/ressources/03_La_platine_essais.html" target="_blank">breadboard</a></figcaption></center>

### Sortie logique

???+ abstract "**Tout Ou Rien (TOR), digital output** : ..."

    Les niveaux électriques des broches du BBC micro:bit ne peuvent être mis qu'à $0\;\mathrm{V}$ ou à $3,3\;\mathrm{V}$. Ce qui correspond respectivement aux valeurs `0` ou `1` :

    - mettre la broche `N` au potentiel $0\;\mathrm{V}$ :
    ```python
    pinN.write_digital(0)
    ```
    - mettre la broche `N` au potentiel $3,3\;\mathrm{V}$ :
    ```python
    pinN.write_digital(1)
    ```

??? example "Application : `Hello World !` spécial robotique"

    ??? quote "`Hello world !` ? ..."
        Le premier programme que réalise tout apprenti informaticien est le fameux [Hello World!](https://fr.wikipedia.org/wiki/Hello_world)... Celà permet avec un programme minimal de prendre en main un langage et surtout de s'assurer du bon fonctionnement de l'environnement de développement choisi [IDE](https://fr.wikipedia.org/wiki/Environnement_de_d%C3%A9veloppement).

    **Raccorder** une LED sur la sortie `P0` tel que sur les circuit et schéma ci-dessous puis **programmer** un allumage alternatif à la fréquence de 1Hz.

    | <img src="https://ericecmorlaix.github.io/img/LED+R_BreadBooardDeBasePourBBCmicro_bit.png" width="80%"> | <img src="https://ericecmorlaix.github.io/img/LED+R_BreadBooardDeBasePourBBCmicro_bit_schema.png" width="60%"> |
    |:-:|:-:|
    | Circuit  | Schéma  |

    ??? tip "Gérer le temps : ..."

        La fonction `sleep(t)` met en pause l’exécution pendant t millisecondes.  
        Exemple : `sleep(1000)` suspend l’exécution pendant 1 seconde.

    ??? tip "Répéter indéfiniment : ..."

        Les instructions placées dans une boucle `while True :` seront répétées tant que le microcontrôleur restera sous tension.

    ??? question "Limiter le courant dans la LED"
        
        - Sachant que la sortie `P0` délivre au maximum une tension de $3,3\;\mathrm{V}$, **calculer** la résistance R1 minimale afin de limiter le courant dans la [LED](https://www.framboiseetcompagnie.fr/fiche-n4-les-bases-de-lelectronique-les-leds/){target=_blank} à $20\;\mathrm{mA}$ pour une tension de $2\;\mathrm{V}$ à ses bornes.
        
        ??? info "Réponse : ..."

            

        ***

        - La valeur réelle retenue pour la résistance R1 est ici de $220\;\mathrm{\Omega}$, en **déduire** l'intensité du courant dans la LED.
        
        ??? info "Réponse : ..."

            

            ??? warning "Courant et tension aux bornes d'une LED : ..."

                En fait, c'est un peu plus compliqué car la tension aux bornes d'une LED n'est pas fixe et égal à $2\;\mathrm{V}$ mais elle varie également en fonction du courant et du type de LED :

                [![](https://www.framboiseetcompagnie.fr/wp-content/uploads/2021/10/word-image-39.png)](https://www.framboiseetcompagnie.fr/fiche-n4-les-bases-de-lelectronique-les-leds/){target=_blank}

                



    ??? success "Solution de programme MicroPython"

        

### Sortie pseudo-analogique

???+ abstract "**Modulation de Largeur d'Impulsion (MLI), Pulse Width Modulation (PWM), analog output** : ..."

    Même si les broches du BBC micro:bit ne peuvent être mises qu'aux potentiels $0\;\mathrm{V}$ ou $3,3\;\mathrm{V}$, il est possible de faire croire au composant raccordé qu'il est alimenté sous une tension comprise entre $0\;\mathrm{V}$ et $3,3\;\mathrm{V}$.

    La technique s'appelle la **Modulation de Largeur d'Impulsion (MLI)**, Pulse Width Modulation (PWM) en Anglais.  
    Le principe consiste à générer un signal pseudo-périodique qui met à `1` la sortie sur une portion ($t_h$) de la période ($T$) du signal.

    <center><img src="https://ericecmorlaix.github.io/img/PWM0.png" width="40%"></center>

    On appelle rapport cyclique le ratio $\alpha = {t_h \over T}$. Ainsi le composant connecté à une sortie PWM aura l'impression d'être alimenter en moyenne sous une tension telle que $V_{MOY} = \alpha \times 3,3$ 

    <center><img src="https://ericecmorlaix.github.io/img/PWM.png" width="80%"></center>

    Ainsi, dans l'instruction suivante `valeur` est telle que $\alpha = {{valeur \times 100} \over 1023}$. Une valeur à `0` correspond à $\alpha = 0$% et à une tension de $0\;\mathrm{V}$ en sortie, une valeur à `511` correspond à $\alpha = 50$% et à une tension de $1,65\;\mathrm{V}$ en sortie et une valeur à `1023` correspond à $\alpha = 100$% et à une tension de $3,3\;\mathrm{V}$ en sortie.

    ```python
    pinN.write_analog(valeur)
    ```

    ??? tip "Régler la pseudo-période du signal PWM : ..."

        La durée de la pseudo-période est choisie suffisamment petite par rapport au temps de réaction de l'oeil humain dans le cas d'une LED ou, de l'inertie du composant électrique piloté par cette broche dans le cas d'un moteur par exemple.

        Il est possible de régler la pseudo-période du signal PWM,
        
        - soit en millisecondes (1ms minimum) :

        ```python
        set_analog_period(period)
        ```

        - soit en microseconde (254µs minimum) :

        ```python
        set_analog_period(period)
        ```

    !!! warning "Attention"
        Le BBC micro:bit ne peux gérer qu'un maximum de trois sorties en PWM simultannément.

??? example "Application : variation d'intensité"

    **Raccorder** une LED sur la sortie `P0` et **programmer** un allumage progressif en intensité sur 5 secondes à partir de l'initialisation de la carte ( = une rampe de démarrage). Puis la LED s'éteint instantannément après 6 secondes...

    ??? tip "Répéter X fois : ..."

        Les instructions placées dans une boucle `for valeur in range(256) :` seront répétées 256 fois et la variable de boucle `valeur` prendra successivement les valeurs de 0 à 255.

    !!! tip "Il faut appuyer sur le bouton `Reset` pour réinitialiser la carte."

    ??? success "Solution de programme MicroPython"

        

### Piloter des Moteurs

???+ abstract "Régler la vitesse et le sens : ..."
    La fréquence de rotation d'un moteur à courant continu dépendant de sa tension d'alimentation, une sortie pseudo-analogique permet de régler sa vitesse par Modulation de Largeur d'Impulsion (MLI).

    ```python
    pin0.write_analog(vitesse) # avec vitesse allant de 0 à 1023
    ```

    Une sortie logique permet de commander son sens de rotation qui dépend de la polarité de son alimentation.

    ```python
    pin8.write_digital(sens) # sens = 0 => avance, sens = 1 => recule
    ```

    ??? tip "Pont en H : ..."

        <center><img src="https://arduino.blaisepascal.fr/wp-content/uploads/2017/05/Pont_H_schema1.png" width="23%" ><img src="https://arduino.blaisepascal.fr/wp-content/uploads/2017/05/Pont_H_schema2.png" width="23%" ><img src="https://arduino.blaisepascal.fr/wp-content/uploads/2017/05/Pont_H_schema3.png" width="23%" ></center>

        Le circuit électrique nommé "pont en H" permet d'inverser la polarité de l'alimentation d'un moteur tel que représenté ci-dessus.

        Le [Bit:Bot](https://4tronix.co.uk/blog/?p=2317){target=_blank} et le [Robot:Bit MK3](https://4tronix.co.uk/blog/?p=1832){target=_blank} dispose comme la carte [Motor:Bit](https://ericecmorlaix.github.io/adn-Tutoriel_lab_si/IOT/BBC_microbit/MotorBit/){target=_blank} d'un circuit intégrer (TB6612) à double pont en H permettant d'alimenter notamment deux Moteurs à Courant Continu (MCC). 


??? example "Application : piloter un moteur"

    **Enficher** une carte BBC micro:bit dans un [Bit:Bot](https://4tronix.co.uk/blog/?p=2317){target=_blank}, un [Robot:Bit MK3](https://4tronix.co.uk/blog/?p=1832){target=_blank} ou une carte [Motor:Bit](https://ericecmorlaix.github.io/adn-Tutoriel_lab_si/IOT/BBC_microbit/MotorBit/){target=_blank} afin de **programmer** une séquence de rotation du moteur gauche pour une durée de 2 secondes vers l'avant puis 2 seconde vers l'arrière à une vistesse "moyenne".

    ??? tip "Fonction : ..."

        Une fonction permet de regrouper des instructions pour les rappeler eensuite à loisir dans un programme avec éventuellement des paramètres variables :

        ```Python
        from microbit import *

        def avance(vitesse, duree) :
            pin0.write_analog(vitesse)
            pin8.write_digital(0)
            sleep(duree)

        avance(23, 1000)    
        avance(223,1000)
        avance(423, 1000)
        avance(623, 1000)
        avance(823, 1000)
        avance(1023, 1000)
        avance(0, 1)
        ```

        **Expérimenter** ce code puis **compléter** le d'une fonction `recule(vitesse, duree)`    

    ??? success "Solution de programme MicroPython"

        ```Python
        from microbit import *

        
        ```
    !!! tip "On observe qu'en reculant, `pin0.write_analog(0)` produit la plus grande vitesse"
       

??? example "Application : piloter deux moteurs"

    **Rechercher** dans la documentation du [Bit:Bot](https://4tronix.co.uk/blog/?p=2317){target=_blank}, du [Robot:Bit MK3](https://4tronix.co.uk/blog/?p=1832){target=_blank} ou de la carte [Motor:Bit](https://ericecmorlaix.github.io/adn-Tutoriel_lab_si/IOT/BBC_microbit/MotorBit/){target=_blank} les n° de broches permettant de piloter le moteur de droite afin de **compléter** votre programme pour faire avancer puis reculer le robot alternativement pour une durée de 2 secondes à vitesse "moyenne".

    ??? success "Solution de programme MicroPython"

        ```Python
        from microbit import *

        
        ```

??? example "Application : tourner"

    **Ajouter** de nouvelles fonctions ou **modifier** les précédentes pour que votre robot puisse aussi tourner à droite comme à gauche selon un programme.

    ??? success "Solution de programme MicroPython"

        ```Python
        from microbit import *

        
        ```
??? question "Que fait le programme ci-dessous ? L'expliquer en complétant les commentaires ..."

    ```Python
    from microbit import *

    # ...
    def piloter(gaughe,droite) :
        # ...
        pin8.write_digital(0)
        pin12.write_digital(0)
        # ...
        if gauche < 0 :
            pin8.write_digital(1)
            gauche = 1023 + gauche
        # ...
        if droite < 0 :
            pin12.write_digital(1)
            droite = 1023 + droite
        # ...
        pin0.write_analog(gauche)
        pin1.write_analog(droite)
        
    while True:
        # ... 
        pilote(800,800)
        sleep(1000)
        # ...
        pilote(0,0)
        sleep(1000)
        # ...
        pilote(-800,-800)
        sleep(1000)
        # ... 
        pilote(0,0)
        sleep(1000)
        # ...
        pilote(400,800)
        sleep(1000)
        # ...
        pilote(0,0)
        sleep(1000)
        # ...
        pilote(800,0)
        sleep(1000)
    ```


### Entrée logique

???+ abstract "**Tout Ou Rien (TOR), digital input** : ..."

    On peut connaitre l’état d’une entrée logique avec la méthode `read_digital()` qui retourne un entier égal à `0` si le niveau de tension sur l'entrée est bas ou `1` si le niveau de tension sur l'entrée est haut.

    ```python
    pinN.read_digital()
    ```


???+ example "Application : ..."

    **Raccorder** une LED sur la sortie P0 et **programmer** l'intensité de son allumage par paliers progressifs de sorte que quatres impulsions successives sur l'entrée A conduisent à l'éclairage maximal. Tandis qu'une impulsion sur le bouton B provoque l'extinction totale de la LED.

    ??? tip "Boutons poussoirs A et B : ..."

        Les boutons poussoirs repérés A et B sur la carte BBC micro:bit sont raccordés respectivement aux broches 5 et 11.

    ??? tip "Variables : ... "

        Les variables permettent de mémoriser et de faire évoluer des valeurs (ou des états) au cours d'un programme.
        
        L'instruction suivante permet d'initialiser une variable, c'est à dire, la déclarer, lui affecter une valeur initiale et donc un type (int, str, float, bool, ...):

        ```Python
        niveau = 0 # => type = integer
        ```
        L'instruction `niveau += pas` est équivalente à l'instruction `niveau = niveau + pas` ce qui permet d'incrémenter (d'augmenter) la variable de la valeur d'un pas.

    ??? tip "Structures conditionnelles : ..."

        ```
        if condition_1 :
            instruction_1
        elif condition_2 :
            instruction_2
        else :
            instruction_3
        ```

        Les instructions 1, 2 ou 3 ne seront exécutées que selon l'état vrai (True) ou faux (False) des conditions 1 ou 2.

        ??? abstract "Les opérateurs de comparaison permettent de faire des tests conditionnels : ..."
            
            | Symbole | Opération |
            |---------|-----------|
            | ==      | égal      |
            | !=      | différent |
            | <       | inférieur |
            | >       | supérieur |
            | <=      | inférieur ou égal |
            | >=      | supérieur ou égal |

        ??? abstract "Les opérateurs booléens `and`, `or`, `not`, permettent de combiner des conditions : ..." 

    

    ??? success "Solution de programme MicroPython"

        

### Entrée analogique

???+ abstract "**Tout Ou Rien (TOR), digital input** : ..."

    Le microcontroleur du BBC micro:bit contient un Convertisseur Analogique Numérique (CAN), Analogue to Digital Converter (ADC) en Anglais, dont la résolution est de 10bits. Il convertit proportionnelement un niveau de tension variant de 0 à 3,3V en une valeur entière comprise entre 0 et 1023. La plus petite variation de tension que l'on peut mesurer est donc égale au $quantum = {3,3 \over 1023} = 3,2 mV$

    <center><img src="https://ericecmorlaix.github.io/img/CAN.svg" width="50%"></center>

    Le BBC micro:bit possède 6 broches sur lesquels on peut lire une valeur d'entrée analogique.

    Elles sont représentés par les instances `pin0`, `pin1`, `pin2`, `pin3`, `pin4`, `pin10`.

    La méthode `read_analog()` renvoie une valeur entière correspondante au niveau de tension mesuré :

    ```Python
    pinN.read_analog()
    ```

???+ example "Application : ..."

    **Raccorder**  une LED sur la sortie P0 et un potentiomètre sur l'entrée P1 et **programmer** le niveau d'intensité lumineuse de la LED selon le réglage de la position du potentiomètre...

    ??? success "Solution de programme MicroPython"

        

### Interface Homme Machine

Une [IHM](https://fr.wikipedia.org/wiki/Interactions_homme-machine){target=_blank} permet à l'utilisateur d'interagir avec un système.

#### Carte BBC micro:bit

Ainsi, la carte BBC, peut, par exemple, recevoir des consignes via les boutons poussoirs A et B et communiquer des informations en les affichant sur la matrice de 25 LEDs...

??? example "Application : diriger un robot roulant"

    **Enficher** une carte BBC micro:bit dans un [Bit:Bot](https://4tronix.co.uk/blog/?p=2317){target=_blank} ou un [Robot:Bit MK3](https://4tronix.co.uk/blog/?p=1832){target=_blank} afin de **programmer** le robot pour qu'il avance en tournant à gauche si l'on appuie sur le bouton A, qu'il avance en tournant à droite si l'on appuie sur le bouton B, qu'il avance tout droit si l'on appuie à la fois sur les boutons A et B.

    ??? tip "Logique booléenne ..."        

#### Manette

Les extensions [Joystick_bit](https://www.elecfreaks.com/learn-en/microbitExtensionModule/joystick_bit_v1.html?highlight=python%20programming){target=_blank} comme [Bit:Commander](https://4tronix.co.uk/blog/?p=1734){target=_blank} permettent de recevoir une carte BBC micro:bit pour étendre ses fonctionnalitées d'IHM.

??? question "Que fait le programme ci-dessous ? L'expliquer en complétant les commentaires ..."

    ```Python
    # ...
    from microbit import *
    import music
    import neopixel

    # ...
    leds_colorees = neopixel.NeoPixel(pin13, 6)

    # ... 
    rouge = (64,0,0)
    vert = (0,64,0)
    bleu = (0,0,64)
    noir = (0,0,0)

    # ... 
    def allumer_toutes(couleur):
        for led in range(0, len(leds_colorees)):
            leds_colorees[led] = couleur
        leds_colorees.show()

    # ...  
    def balayer(couleur, duree):
        for led in range(0, len(leds_colorees)):
            leds_colorees[led] = couleur
            leds_colorees.show()
            sleep(duree)

    # ...
    def lire_joystick():
        return pin1.read_analog(), pin2.read_analog(), pin8.read_digital()

    # ...
    def lire_pad():
        # rouge, bleu, vert, jaune
        broches_pad = [pin12,pin15,pin14,pin16]
        return [broche.read_digital() for broche in broches_pad]

    # ...
    def lire_potentiometre():    
        return pin0.read_analog()

    # ...
    def play_tune():
        music.play(music.BADDY)
        pin0.read_digital()

    # ...    
    allumer_toutes(rouge)

    # ...
    play_tune()

    # ...
    balayer(bleu,250)

    # ...
    while True:
        x,y,j = lire_joystick()
        boutons = lire_pad()
        potentiel = lire_potentiometre()
        print(x,y, j, boutons, potentiel) # Où peut-on visualiser cet affichage ?
        sleep(20)
    ```

### Communication avec BBC micro:bit

Lorsqu'elle est programmée en MicroPython, la carte BBC micro:bit permet d'établir une communication filaire avec, par exemple, un PC via un moniteur série (application Putty) ou une console REPL (éditeur Mu).

Mais il est également possible d'établir une communication sans fil entre deux cartes BBC micro:bit avec le module `radio` de MicroPython.

## Projet de robot

??? question "Que font les deux programmes ci-dessous ? L'expliquer en complétant les commentaires ..."

    ```Python
    # Bit:Commander # ...

    # ...
    from microbit import *
    import radio

    # ...
    canal = 10
    radio.config(channel=canal)
    radio.on()

    # ...
    while True:
        av = pin12.read_digital()
        ar = pin14.read_digital()
        dx = pin1.read_analog()    
        if  av and dx < 150:
            # ...
            display.show(Image.ARROW_NW)
            radio.send("NO")
        elif av and dx>850:
            # ...
            display.show(Image.ARROW_NE)
            radio.send("NE")
        elif ar and dx<150:
            # ... 
            display.show(Image.ARROW_SW)
            radio.send("SO")
        elif ar and dx>850:
            # ... 
            display.show(Image.ARROW_SE)
            radio.send("SE")
        elif ar:
            # ...
            display.show(Image.ARROW_S)
            radio.send("S")
        elif av:
            # ...
            display.show(Image.ARROW_N)
            radio.send("N")
        sleep(20)
    ```

    ```Python
    # Bit:Bot ou Robo:Bit MK3 # ...

    # ...
    from microbit import *
    import radio

    # ...
    canal = 10
    radio.config(channel=canal)
    radio.on()

    # ...
    def piloter(gauche,droite):
        pin8.write_digital(0)
        pin12.write_digital(0)
        if gauche<0:
            pin8.write_digital(1)
            gauche = 1023 + gauche
        if droite<0:
            droite = 1023 + droite
            pin12.write_digital(1)
        pin0.write_analog(gauche)
        pin1.write_analog(droite)

    # ...
    while True:
        # ...
        message = radio.receive()
        
        # ...
        if message is not None :
            if message == "N" :
                piloter(800,800)
            elif message == "S" :
                piloter(-800,-800)
            elif message  == "NE" :
                piloter(800,200)
            elif message == "NO" :
                piloter(200,800)
            elif message == "SE" :
                piloter(-800,-200)
            elif message == "SO" :
                piloter(-200,-800)
        # ...
        else:
            piloter(0,0)
        sleep(20)
    ```



## Ressources :

- [Quelques bases d'électronique associées aux microcontroleurs](https://www.framboiseetcompagnie.fr/category/electronique/){target=_blank}



<!-- 

https://nsirennes.fr/os-archi/bbc-microbit/



CARTE JOYSTICK:BIT

Joystick:bit v2.0 de ELECTROFREAKS
pin2 : pin2.read_analog() détecte le bouton pressé
buttons = {2: "A", 517: "B", 686: "C", 769: "D", 853: "E", 820: "F", 1021 : "aucun"}
pin0 et pin1 donnent la position du joystick :
pin0.read_analog() sur X : 3~1021 et Xcentre = 529
pin1.read_analog() sur Y : 3~1021 et Ycentre = 506
/!\ Ces valeurs sont approximatives car elles varient d’une carte Joystick:bit à l’autre !

Tester la Joystick:bit

Les coordonnées du joystick
1
2
3
4
5
6
7
8
9
10
11
from microbit import *
import radio
#######################################
# TEST : JOYSTICK:BIT
while True:
    press = pin2.read_analog()
    print("bouton : "+ str(press))
    X = pin0.read_analog()
    Y = pin1.read_analog()
    print("joystick : "+str(X)+" , "+str(Y))
    sleep(100)
Emetteur radio (carte Joystick:bit)

from microbit import *
import radio
 
#######################################
# JOYSTICK:BIT
def button_press():
    press = pin2.read_analog()
    if press > 938:  # le plus fréquent car aucun bouton : press=1021
        return ""
    elif press < 256:
        return "A"
    elif press < 597:
        return "B"
    elif press < 725:
        return "C"
    elif press < 793:
        return "D"
    elif press < 836:
        return "F"
    else:
        return "E"
 
def joystick_push():
    # Par défaut : x = 529 (3~1021)   y = 506 (3~1022)
    # map (1~1023) to (-1022~1022)
    x = 2 * pin0.read_analog() - 1024
    y = 2 * pin1.read_analog() - 1024
    if -100 < x < 100:
        x = 0
    if -100 < y < 100:
        y = 0
    return x, y
 
 
radio.config(channel=7, group=0, queue=1, power=7)
radio.on()
while True:
    X, Y = joystick_push()       
    message = str(X) + "|" + str(Y) + "|" + button_press()
    radio.send(message)      # ex : "-700|400|"
Récepteur radio (carte motor:bit)

from microbit import *
import radio
 
###################################
# MOTOR:BIT   M1=gauche   M2=droite
 
def drive(vitesseX, vitesseY): # vitesse : -1023 ~ 1023
    if vitesseX < 0:
        vitesseX = - vitesseX
        pin8.write_digital(0)  # direction M1
    else:
        pin8.write_digital(1)  # direction M1
 
    if vitesseY < 0:
        vitesseY = - vitesseY
        pin12.write_digital(1)  # direction M2
    else:
        pin12.write_digital(0)  # direction M2
 
    if vitesseX > 900:
        vitesseX = 900
    if vitesseY > 900:
        vitesseY = 900
    pin1.write_analog(vitesseX) # vitesse M1
    pin2.write_analog(vitesseY) # vitesse M2
 
 
radio.config(channel=7, group=0, queue=1, power=7)
radio.on()
ancien_bouton = ""
while True:
    msg_recu = radio.receive()
    if msg_recu is not None:
        [joystickX, joystickY, bouton] = msg_recu.split("|")
         
        # moteur
        joystickX = int(joystickX)
        joystickY = int(joystickY)
        drive(joystickY + joystickX//3 , joystickY - joystickX//3)
         
        # bouton
        # /!\ redondances car un appui bref de btn A donne "A" "A" "A" "A"
        if bouton != ancien_bouton:
            # faire qqch
        ancien_bouton = bouton -->
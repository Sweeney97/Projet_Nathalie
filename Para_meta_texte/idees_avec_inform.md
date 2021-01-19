## Idées pour l'histoire en lien avec Inform

La commande examine me permet de produire un texte sur le player. Il serait intéressant d’intercepter des commandes examine me selon ou le joueur se trouve, avec différentes description. Ou encore, de créer des routines qui appelle différentes descriptions selon un système de points .

Il est possible de programmer différentes fin de jeu à l’aide d’un système de valeur (DeathMessage)
voir page 90 IBG

il pourrait y avoir des séquences où il faudrait trouver un certain élément dans le décors qui n’apparaîtrait qu’au bout de 3 ou 4 descriptions (espèce de description finale qui révèle l’objet, la personne). Ou au retour du joueur (has been visited)

Il est possible de changer la variable player.description =

Le IBG recommande d’utiliser des facades avec has enterable qui téléportent  le joueur vers la pièce en question, pour les commerces dans la rue.

Dans le game play, faire en sorte que certaine cinématique doivent amener le joueur à trouver leur correspondance dans l’univers de jeu (les quartiers) afin de déclencher la suite (trouver des lieux préçis font se dialoguer cinématique et jeu, et force le joueur à explorer)

un ordi dans le jeu permet de voir le code squelette du jeu, (c'est a dire sans le texte destiné au joueur )

La vie du joueur dépend d'un drapeau, d'un seul signal.

Il serait possible d'utiliser à mon avantage les mines. Les mines seraient dans les terres brûlées, et abandonnées.
Les mines seraient réputées par la population locale pour être hantées, magiques.
Elles seraient visitées lors de rituels par la shaman.
L'inspecteur pourraient s'y rendre, perdre la shaman et sa lumière (elle «s'évanouit») et être pris dans l'obscurité «qui avale».
Après un nombre prédéfinis de tour (5 à 20 tours), le joueurs seraient avalés par les ténèbres (voir Ruins, DM4).
Ainsi, la routine AfterLife() serait appelée.
C'est une possibilité, qui ferait comprendre à l'inspecteur que le corps n'est qu'une enveloppe, et qu'il serait possible que Nathalie soit une possédée, comme les crois les sauvage des terres brûlées.

Il pourrait être intéressant d'utiliser les fonctionnalités random + switch, qui permettent plusieurs utilisations. De même, utiliser des Daemon et des timer serait cool.
J'aimerais, dans la même lancée, créer au moins un PNJ intéressant, pas nécessairement Nathalie.

Je pourrais utiliser la fonction Score + silent pour qu'à la fin, le joueur puisse voir combien de pièce ou d'objet lui manque.

Durant la séquence à l'ordinateur, il est possible de changer la phrase montrée à l'écran pour inviter le joueur à taper. Par exemple:
TERMINAL:
ou quelque chose dans le genre.

Il serait intéressant, si possible, d'utiliser le temps: chaque tour vaudrait soit 15, 30, ou 60m.
Ainsi, il faudrait par exemple attendre à 23h dans la ruelle de tel quartier pour épingler tel rendez-vous.

Pour l'automobile, ça serait soit un objet avec l'attribut vehicle, ou bien, un super-objet connecté à plein d'autres (les endroits principaux).
Ça serait plus simple pour moi de coder la deuxième option.

Finalement, je pourrais jouer avec Concealed: cet attribut sert pour les développeur, puisqu'une porte concealed ne peut pas être utilisée, et un objet concealed pert son attribut après avoir été saisi.
Et si, dans le monde des morts, sous forme d'esprit, le joueur pouvait saisir les portes concealed pour les utiliser ensuite, ça serait une utilisation originale de l'attribut. 

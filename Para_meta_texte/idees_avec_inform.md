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
À ce moment, l'inspecteur serait un esprit ou une âme, il vivrait une expérience post-mortem.
L'object ame aurait l'attribut light, ainsi, une fois mort, il serait possible de «voir» les mines.
Finalement, une fois mort, le joueur devrait trouver une porte ayant la propriété concealed, il devrait la prendre (littéralement) et entrer dans le monde des esprits.
Une fois dans le monde des esprit, il pourrait rencontrer Nathalie,  qui tente de fuir son corps (c'est-à-dire qu'elle veut mourir, ayant abandonné tout espoir).
L'inspecteur promet de la retrouver et de l'aider lui demande de rester.
Nathalie lui explique qu'elle est parfois posséder.
À son réveil l'inspecteur ne sait pas s'il a tout halluciné, puisqu'il y a devant lui le repas et la boisson de la veille, et les cendres du feu de la veillée.
Ainsi il pense pouvoir avoir été empoisonné.
L'armée débarque, il doit se cacher (le général le suit de son propre chef, le même présent lors de la scène du bar, ).
Peut-être le joueur pourrait revenir après la scène pour acheter des potions au village?
Les potions permettrait de le guérir lorsqu'il est blessé.

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

Oublier l'utilisation du temps (trop complexe et brouillon). Il fera nuit tout le jeu, excluant dans les terre brûlées.

L'inspecteur pourrait être blessé parfois (lors de certaine rencontre par exemple, suivant un daemon aléatoire).
Lorsqu'il est blessé, un timer serait enclenché, permettant environ une dizaine de tours (ou plus, à déterminer) avant la mort de l'inspecteur.
Aller au dortoir du poste de police guérirait l'inspecteur.

Pour ne pas abandonner ma veille intention sur la moralité.
Lors de quelques que points clefs il est possible de faire les actions en bien ou en mal.
Par exemple, arrêter un personnage (intercepte par un before) ou le tuer (dans la routine life).
Chaque action bonne donne un credit au dossier (global variable?), chaque mauvaise action donne un soupçon au dossier.

Il est impossible de se promener entre les quartiers.
Chaque endroit sera un arc narratif isolé.
La carte de crédit se mérite, pour aller au supermarché.
Autrement, affilié avec les criminel, ce sera au bar pour acheter, ou a la planque (àvoir).


Cela changerait la fin selon l'affiliation.
Aussi, il y aurait un policier et un criminels aléatoires (avec un daemon).
Un policier dans le quartier de la planque.
Un criminel dans le quartier principal.
Tomber sur l'un ou sur l'autre change l'issue selon l'affiliation.
Affilié avec les criminels - guérison dans la planque.
Affilié avec les policiers - guérison dans le dortoir
Blessé en territoire «ennemi» - il faut un objet pour se guérir!
Le badge sera l'élément qui sert de flag pour savoir dans quel camp est le joueur (coder un before pour pas que le joueur le donne/drop).
Sans badge, l'inspecteur est un criminel.
Se rendre en voiture pourrait se faire avec une volée ou donne par le poste selon si le joueur est criminel ou non.
La carte de crédit s'obtient à la fin du parcours du premier quartier, comme récompense d'avoir gardé son badge.
Si le joueur a tué/intimidé un seul perso, il n'aura pas de carte de crédit.

J'aimerais coder aussi trois autres PNJ:
un marchant ambulant(commun)
Un évènement dans le quartier principal (à voir)
un renégat (rare)
Nathalie (hyper rare)


oublier la voiture/moto comme objet interactif.
En faire un objet dans le jeu seulement descriptif.

Il sera impossible de rentrer dans la bibliothèque.
Elle ne sera présente que dans l'histoire.

Le quartier finale, c'est à ce moment que le joueur devient Nathalie.

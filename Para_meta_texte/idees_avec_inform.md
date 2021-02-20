## Idées pour l'histoire en lien avec Inform

Ce qu'il reste a faire:

Remplir la cuisine d'anne-marie
Remplir la maison
Remplir le caffe
Remplir le parc (statue voir livre histoire)
Remplir l'hypermarché

Apres avoir parle a mauriac, move voiture to stationnement (enlever scenery ou concelead)
Dire bye a anne marie
Mettre un sub pour le babillard
Les odeurs, les sons (before)

Faire un chat qui se promène dans le premier quartier? le ramener à son proprio ferait monter le score. Je peux prendre le même code que pour le vendeur ambulant et confiner le vendeur aux quartiers 2 et 3.

Si les string pour les cut-scene sont trop grosses pour Frotz-z5, je peux toujours faire un e-book ou un html à côté pour que le joueur puisse le lire. (Exemple, dans le jeu: lisez le chapitre trois du livre). Dans tous les cas je peux faire une stand-alone file pour l'histoire.

L'énigme du croco, il faut lire entre les lignes, littéralement (solution dans le code source, en commentaire).

Coder un objet cutscene par partie:
exemple: introduction partie un, partie deux, etc.

Quand vient le temps à la fin du premier quartier de choisir le camp, si trop de meurtre/mauvais actes ont été commis, il serait impossible de rester dans la police.

peut-être les criminels demandent-ils l'inspecteur de détruire une pièce à conviction dans les mines (à voir)

Idée d'objet: un défibrillateur pour mettre hors jeu le drone-garde à l'entrée du pont (vue sur l'eau, vue sur la cité.)

Les indigènes sont inoffensif, si le joueur les attaques, il devient automatiquement empoisonné. Mais s'il leur parle simplement, il pourrait même avoir des indices sur les statuettes.

La moto est trouvable dans la cours à scrap. Mais elle n'a pas d'essence. Sans essence, le joueur à faim? (encore).
Ou avec la police le joueur doit trouver l'essence dans le quartier, contre avec les criminel l'essence est fournie.
Il y a une piece avant la cours à scrap (à gauche) où le joueur peut déposer des objets. Cela afin de chercher des statuettes et des objets dans la cours à scrap.

Répartir les goodies dans les trois quartier

Me mettre dans le jeu (un appartement au complet avec moi dedans, 5 étages, chacun étant un de mes lieux de vie, et où j'epxlique la création de nathalie. Cela dans le dernier quartier.

Objet rêve colonne

un rêve, à l'arrivée des terres brûlées, ou l'inspecteur doit marcher sur un sol invisible (un chemin tracé invisible), s'il va dans la mauvaise direction, il tombe et retourne sur la colonne.
Il pourrait voir un visage géant (du croco?) avec qui il parle. Mettre un chemin caché?
Faire un rêve méta sur le hangar

Flaguer le joueur s'il vient du hangar *vers* les cinématique, pour pas que le hangar soit accessible depuis les cinématiques.

Fusionner les Daemon du criminel et du policier en un seul Daemon ennemis dont la description change selon le badge

###### Moyen de transport
avec la police:
- voiture (sabotée)
- moto

avec les criminels:
- Voiture (chauffeur)
- Moto (essence fournie par la planque?)



Ensuite une moto de la scrap?
Faux choux de la voiture de police qui crash (maison abandonnée)


L'enfant prodige habite en bordure de la ligne verte, ver le dernier quartier, genre de lieu abandonné.

Mettre le hangar sous une rue/poste


### Score
- Prier a l'autel
- Nourrir les canard au parc
- Découvrir le hangar
- L'entrée derrière l'armoire dans la maison
- Converser avec le vieil homme
- Découvrir l'appartement spécial
- Découvrir une statuette rare
- Ramener l'animal

### Objets

###### Magasin
- Pain (pour la faim, nourrir les canards)
- Essence (mettre le feu, faire fonctionner la moto de la scrap)
- Alcool (Trompe-faim, feu, sans-abris, nettoie la plaie)
- Tissu (cocktail molotov, étouffer, bandage)
- Bombe fumée (crocodile, enemis)
- Corde (intrus)

###### Autre objets
- Drone (désactive les daemons ennemis, à voir)
- Pistol laser (joker pour n'importe quelle rencontre incluant le droïde)
- Potion des terre brûlée (cure anything)


Les cut scene pourrait être accessible depuis le hangar!

Personnifier la faim dans le hangar

Éléments aléatoire possible:

- Un homme blessé (nécessite une trousse ou une potion)
À réserver pour le dernier quartier,
Quand tous les autres daemon sont stoppés

Faire des lieux caché (pour le score)
Score objet maison lieu cache perso rares
L'autel trou clôture stationnement


La bibliothécaire c'est l'oracle?


Faire l'entrée secrète de l'infirmerie?
(En parlant plus d'une fois avec l'infirmière)

La maison est loin.

Après l'épisode du cybercafe, le joueur est flagué:
Il ne peut plus entrer dans les appartements ou dans l'usine.
Seul reste l'oracle, l'hypermarché (et le poste?)
Pour s'en aller du quartier, il doit retourner à sa voiture

Finalement, coder la bibliothèque
(Chaque livre = un objet à examiner)
Une seule pièce

L'ordinateur est un lieu!
Avec autant de dossier-objet à examiner
Pour aller a l'ordi il faut s'adresse au commis, une routine YesOrNo est invoquée
Si oui : MovePlayerTo(Ordi)
Print_ret "vous vous installer à un poste de travail"
StartDaemon: nombre de tours comptés pour le joueur!!!
(Genre 3-4)
Afin qu'il ne puisse pas lire tous les fichiers (rejouabilité haha)
Quand le code hit default: scène avec l'enfant prodige
If self hast visited: {
Interaction avec le commis}

Else (Vous n'avec aucune instant à perdre avec cette information en main)

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

Le quartier finale, c'est à ce moment que le joueur devient Nathalie.

### Notes sur Inform tirées du Beginner's guide

What if devrait être la phrase clef dans le développement d’une IF

Les descriptions d’une IF doivent être le plus possibles voulues/appelées par le joueur.

Tout dans une histoire prend la forme d’objet pour la machine, sentiment, lieux, objets, etc.
Les objets ont des attributs (wtih) et des propriétés (has). Ce qui les différencie : les attributs on un nom (ex : description) et les attribue non (ex : lumière).

Les attributs sont valeur booléenne, c’est-à-dire binaire. Ils répondent à des questions.



Dans un lieu donné, la machine ne présente que ce qui est illuminé, généralement le lieu en soi. Tout ce qui est sans lumière n’apparaît pas.

Le nom interne doit être unique
Le nom externe, non

Propriété :
description, noms (dico), capacité, connexions, each_turn []



Les relation d’objet fonctionnent en parenté : parents-enfants. Chaque objet n’a qu’un seul parent (conteneur) et peu avoir plusieurs enfants (contenu). Chaque objet n’a qu’un seul parent, c’est-à-dire son conteneur le plus près : exemple, l’oiseau dans le nid a pour parent le nid, et non la forêt, qui est le parent du nid. Même si, en vrai, il est inclut dans deux conteneurs.

Une pièce est simplement un objet sans parents, qui peut avoir plusieurs enfants, dont le joueur notamment.

l’accent circonflexe à l’intérieur d’un texte (entre guillemet anglais) demande à la machine de sauter une ligne.

DOSI : Double guillement = Output, Simple guillement = Input

Écrier les if sur deux lignes aide à la division logique

if (gâteau on table)
eat_cake
(sous-entendu logique : Then)

before [; Listen: print "It sound scared and in need of assistance.^";
return true;
],
Tellement utilisé qu’il y a un raccourci :
before [; le_verbe: print_ret "Blah blah blah."; ],

 Before permet d’intercepter (si j’ai bien compris) la commande, return true d’indiquer à la machine que nous avons programmer une action complète et qu’elle n’a rien à ajouter.

Cette suite est primordiale pour préprogrammer des réponses!

La valeur cant_go renvoit vers un message lorsqu’une direction non programmée est appliquée (par exemple afin d’indiquer au joueur où aller)

On peut aussi connecter des description (print) à des direction

pour écrire un routine qui relocalise le joueur, il faut utilisier PlayerTo(location_were_you_want_to_go)
Afin de lui masquer où il se trouve téléporté : (location,1) ajouter la valeur 1


noun is a library variable that
always contains the internal ID of the object which is the target of the current
action.
Répétition de l’information : noun holds the internal ID of the object which is the focus of the
action, and second holds the internal ID of the secondary object (if there is one)
Exemple : put bird in nest = noun, bird; nest, second

Self est une variable similaire à noun, mieux adaptée au descriptions, qui concerne l’objet dans lequel le joueur se trouve : self is a variable which, within an object, always refers to that object.

À mettre dans le initialise routine :
lookmode = 2;
Cela fait en sorte que les descriptions sont toujours affichées, même pour des endroits déjà visités, pratique pour les versions test

There’s a library variable self which always contains the internal ID of the
current object, and is really convenient when using a Class . By using this
variable in our print_ret statement, we ensure that the message contains the
name of the appropriate object.



Pour enlever une caractéristique issue de l’héritage (dans les classes), il faut utiliser le tilde

ex.  has ~light

found_in permet d’insérer dans plusieurs lieux des objets à interraction réduite (décors, peronnages sans interractions, etc.)

|| = or



Il est possible d’intercepter des action pour les rediriger vers d’autres actions, par exemple :

[; before : Kill : <Talk noun>; return true;],
Ou en raccourci : [; before : Kill : <<Talk noun>>;],





Il est possible de dupliquer un objet avec found_in dans la section « with », c’est à dire que le même objet ne sera plus enfant d’un autre, mais sera dupliqué dans tous les internal_id suivant found_in
Pour dupliquer un objet partout :
found_in [; return true; ],
dans cet exemple il n’y a pas de valeur associée, c’est toujours vrai

la caractéristique initial permet de personnaliser la monstration d’un objet par l’interpréteur. Au lieu de dire : vous pouvez voir un fusil.

Si la caractéristique initial est définie ainsi :

Fusils  pistolet_silencieux "pistolet muni d’un silencieux" the_cave
with initial "Oh! Un pistolet muni d’un silencieux! Ce fusil semble parfait pour un assassinat furtif."

Cela apparaîtra ainsi : Oh! Un pistolet muni d’un silencieux! Ce fusil semble parfait pour un assassinat furtif.


La caractéristique initial peut aussi être une embed routine

les accolades { } servent à encapsuler plusieurs conscéquences d’une condition (if)


score = 10
[est]
If (score == 10)
[est égal a]

dans une série de valeurs (1 : telle chose arrive, 2 : telle chose, etc.) default signifie la valeur autre que celle listée



Un attribut vient toujours en duo : un nom et une ou des valeurs. Une propriété est la valeur en soi, et peut soit exister, soit n’exister pas.

Dans une routine, default signifie tout le reste. Ex : exmanine, return false, default, print_return « blablabla ».


lookmode = 2
ça veut dire, pour tester, que toutes les descriptions sont toujours affichées

STEF standalone routine return true, embed routine return false


Il faudrait que je puisse déterminer quand les return true return false sont prédéterminer par le système!



À la fin de L’IGB se trouve la théorie, vraiment pratique, à relire (somme last lousy points).

Une expression est une valeur ou plusieurs valeurs combinées grâce aux opérateurs.

Un opérateur est logique, arithmétique, mathématique, booélien, etc.

Un statement est une instruction pour l’interprétateur.Ex : if (expression) statement_bloc else statement_bloc; print_ret, etc.

Un directive est une instruction pour le compilateur. Ex : Class class_id, attribute, etc.

Un object est une collection de variables qui ensemble représentent les capacités et le statu actuel d’une composante spécifique du monde modélisé.

Pour cacher une description, il faut soit utiliser scenery ou concealed ou bien enlever la lumière

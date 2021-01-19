# DM4 Notes de lectures

### Introduction

« "Inform is an easel, not a painting". Though I am no longer so sure that the two can be divided. » While revising this book, I have been ruefully reminded of Coleridge's notebooks, that vaulted miscellany of staircases and hidden doors, connections found and lost, plans abandoned and made again. Slipping away from my attempts to index and organise it, this book, too, remains for me a maze of twisty little passages, all different, a kind of interactive fiction itself. » p.3

### Chapitre un

& and, | or, ~ note
&& || ~~ shortcut evaluator, par exemple si A && B, mais que A est faux, B n'est pas vérifié (voir page 20)

Conditions are expression like any other, except their value are always either true or false

Flag are always true or false

Quan une routine s'appelle elle-même, cela s'appelle recursion

Un code block c'est quand il y a plusieurs statements avec les { }

!-- Les routine à l'intérieur des  [ ] ont des variables privées, au contraire des code blocks. De plus, l'exécution peut sauter dans un block code d'un à l'autre, au contraire des routines.
If... else... are like railway signals for two possible tracks, where Switch is like a railway turntable.

While (condition) [do] statement
do statement until (condition)
Pour des exemples plus complexes voir page 25

@00 to @31, printing variable, voire page 30

Here is one way to imagine how an Inform routine works: you feed some values into it, it then goes away and works on them, possibly printing some text out or doing other interesting things, and it then returns with a single value which it gives back to you.

In some ways, code blocks are like routines, and at first it may seem inconsistent to write routines between [ and ] brackets and code blocks between braces { and }. However, code blocks cannot have private variables of their own and do not return values; and it is possible for execution to break out of code blocks again, or to jump from block to block, which cannot happen with routines.


if (condition) [then do] statement else [do] statement [instead]

Global variable est une permanent value qui peut être utilisée par toutes les routines
Array is an indexed collection of variables, organised into a sequence



Les lettres peuvent être utilisé pour générer des nombres, donc je pourrais créer un mot caché qui n'apparaîtrait que dans le code.


objects are little bundles of routines and variables tied up together.

objectloop (variable-name) statement

runs Though the statement once for each object in the game, putting each object in turn into the variable
voire page 53

Dans un object, with spécifie les variables, routines et arrays

Quand une variable s'attache à un objet, elle s'appelle ensuite dans le code objet.variable.

Exemple, si j'ai l'objet Arbre with magieverte, pour appeler la variable magieverte: arbre.magieverte

embedded routine has no name, since it is referred to as a property
embedded routine return false

Object have attribute, declared with has, attribute are either false or true
(Properties aren't true or false)

self means the object receiving the message and sender means the object which send it

pour emprunter une propriété d'une autre classe, voire le super-opérateur :: page 64

les objets ont des variables appelés propriétés

 “object”: a bundle of variables and routines encoding the relevant rules of the game

 And although you almost never need to know or care, routines as in §1 are internally considered as a kind of object, of class Routine

 Every Inform source program is a list of constructions, made using commands called “directives”. These are quite different from the statements inside routines, because directives create something at compilation time, whereas statements are only instructions for the interpreter to follow later, when the story file is being played.
 The directive written [, meaning “construct a routine containing the following statements, up to the next ]”
 The four directives to do with objects, Attribute, Class, Object and Property, will be the subject of §3. The two directives to do with laying out grammar, Verb and Extend, are intimately tied up with the needs of adventure games using the Inform library

### Chapitre deux

Il y a un commentaire intéressant, page 78, à propos de la création d'un jeu: soit écrire en premier le transcript idéal (genre de lecteur idéal transposé au joueur) ou bien en construisant les objets un à un.

<Examine self> cause the action to be triggered automatically
Exemple, si elle est rattachée a un before listen couplée avec un return true.
Alors l'action pourrait être exprimée ainsi Listen: <<Examine self>>.

The current action is always stored in the four variables: actor, action, noun, second

Pour lever l'ambiguïté, dans le code source, pour faire référence à une action, on utilise ##.
Exemple: if (action == ## Look)

La variable Keep silent affecte les actions: si elle est vraie, the actions print nothing in the event of success.

 To create new action, first you need to create a routine (sub)
 Then you need to create grammar, the simplest way is to create a verb linked to that action, see p.92

Dans la résolution des Before, il y a un ordre (ex.:react_before, room, noun) v. p. 93-4

### Chapitre trois

Pour cacher un objet, on peut soit: utiliser concealed, scenery, ou enlever la lumière

found_in permet d'indiquer plusieurs locations

l'attribu absent permet d'overide un objet déplacé par found_in voir page 109

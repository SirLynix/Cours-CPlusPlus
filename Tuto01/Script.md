**Gag intro**
___

Bienvenue dans l'épisode 1 du tutoriel d'apprentissage du langage C++.
Dans la vidéo précédente, nous avons vu ce qu'était le C++ et à quoi il pouvait servir, ainsi que les outils à utiliser. Je vous conseille de la regarder si vous n'avez pas ce qu'il faut (et de lire la description contenant les liens).

Aujourd'hui nous allons enfin nous attaquer à la pratique, faire de vrais programmes, pour les bonhommes, qui en jettent un max, on va faire ... 

___
**Vue code**

** Apparition du code HelloWorld1.cpp, numéro de lignes cachées**

*(voix douce)* Un programme qui dit bonjour.

**zoom résultat**

*(voix fluette)* Bonjour !

___
**Vue caméra**

*(regard confus)* Bon, il faut bien commencer quelque part.

___
**Vue code**

Ce que vous avez sous les yeux s'appelle un "Hello world", il s'agit d'un programme minimal souvent utilisé dans les cours de programmation comme point de départ, et nous n'allons pas faire exception.

Ainsi donc ce code, qui est du C++, sert souvent de première expérience aux débutants, et nous allons le décortiquer pour tâcher de comprendre ce qu'il fait.

Bon, tout d'abord en programmation on raisonne beaucoup en terme de ligne, et il vaut mieux les afficher. *affichage des numéro de ligne* Le compilateur va lire notre programme de la première à la dernière ligne, donc de haut en bas, et de gauche à droite.

Voyons donc la première ligne, celle-ci commence par un croisillon (souvent confondu avec le dièse), souvent appelé hash (depuis l'avènement de Twitter). 

___
**Vue caméra**

Ce caractère est important, il indique que la ligne concerne le préprocesseur, que nous verrons plus en détail dans une vidéo à venir. Pour l'instant comprenez que ce n'est pas du code C++ classique.

___
**Vue code**

Après ce caractère nous avons l'instruction include, indiquant que nous souhaitons .. inclure, importer si vous préférez, un fichier définissant des instructions supplémentaires.

___
**Vue caméra**

En C++ les includes sont très courants et sont actuellement le seul moyen de dire au compilateur que nous souhaitons utiliser des fonctionnalités autres que celles de base, très limitées. Afficher du texte en fait partie.

___
**Vue code**

Ensuite nous avons une ligne vide, qui en C++ est simplement ignorée par le compilateur.
Juste après, nous avons une ligne assez mystérieuse. Un nom de type suivi d'un autre nom suivi de parenthèses vides. Vous avez devant les yeux une déclaration de fonction.

___
**Vue caméra**

Une fonction, tirant son nom des mathématiques, est l'endroit où s'exécute votre code. En C++, et dans les langages bas-niveau en général, votre programme ne peut s'exécuter qu'à l'intérieur de fonctions.
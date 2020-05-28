**Gag intro**
___
**Vue caméra**

Bienvenue dans l'épisode 1 du tutoriel d'apprentissage du langage C++.
Dans la vidéo précédente, nous avons vu ce qu'était le C++ et à quoi il pouvait servir, ainsi que les outils à utiliser. Je vous conseille de la regarder si vous n'avez pas ce qu'il faut (et de lire la description contenant les liens).

Aujourd'hui nous allons enfin nous attaquer à la pratique, faire de vrais programmes, pour les bonhommes, qui en jettent un max, on va faire ... 

___
**Vue code**

*Apparition du code HelloWorld1.cpp, numéro de lignes cachées*

*(voix douce)* Un programme qui dit bonjour.

*zoom résultat*

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

Ce caractère au début est important, il indique que la ligne concerne le préprocesseur, que nous verrons plus en détail dans une vidéo à venir. Pour l'instant comprenez que ce n'est pas du code C++ classique.

___
**Vue code**

Après ce caractère nous avons l'instruction include, indiquant que nous souhaitons .. inclure, importer si vous préférez, une bibliothèque définissant des fonctionnalités supplémentaires.

En C++ les includes sont très courants et sont actuellement le seul moyen de dire au compilateur que nous souhaitons utiliser des fonctionnalités autres que celles de base. Afficher du texte en fait partie.

___
**Vue caméra**

Dans la quasi-totalité des langages, vous ne pouvez rien faire sans utiliser des bibliothèques. Il s'agit d'un ensemble de fonctionnalités que nous pouvons utiliser pour donner plus de capacités à nos programmes.

Et rien que le fait d'écrire du texte dans une console nécessite une bibliothèque, c'est dire à quel point de base on est limités.

___
**Vue code**

Ensuite nous avons une ligne vide, qui en C++ est simplement ignorée par le compilateur. Et juste après, nous avons une ligne intriguante: 
un nom de type suivi d'un identificateur suivi de parenthèses vides. 

Aucun doute, vous avez devant les yeux une déclaration de fonction.

___
**Vue caméra**

Une fonction, c'est une boite, une boite qui prend des paramètres (ou non) en entrée et qui ressort des valeurs (ou non) en sortie.
Ici par exemple notre fonction ne prend aucun paramètre en entrée et sort un entier, nous verrons ça plus en détail par la suite.

En C++, et dans les langages bas-niveau en général, votre programme ne peut s'exécuter qu'à l'intérieur de fonctions. On aura l'occasion d'en reparler des fonctions, pour l'instant retenez surtout que tout programme commence dans la fonction main.

___
**Vue code**

Ensuite, nous avons ce qu'on appelle un bloc. Un bloc commence par une accolade ouvrante et se termine par une accolade fermante. Cette notion va être importante pour la suite.

Dans ce cas-ci, le bloc sert à définir le contenu de la fonction main, l'ensemble du code qu'elle contient.

Petite remarque à ce propos, le C++ fait partie des langages où les espacement et retours à la ligne ont assez peu d'importance, de fait 

```cpp
int main() {

}
```

et


```cpp
int main()
{
    
}
```

sont strictement équivalents et n'ont qu'un intérêt esthétique. J'utilise la deuxième forme ici par habitude et préférence personnelle, mais sentez-vous libre d'opter pour la première si vous la préférez.

Bien, il ne nous reste plus que deux lignes à comprendre, les plus importantes car elles représentent le comportement de notre programme.

```cpp
std::cout << "Bonjour !\n";
```

___
**Vue caméra**

Vous vous souvenez quand je vous ai dit que les lignes se lisaient de gauche à droite ? Hé ben pour le coup, celle-ci s'explique plus facilement de droite à gauche.

___
**Vue code**

```cpp
"Bonjour !\n"
```

On commence par définir du texte, ou chaîne de caractère, celui-ci est délimité par des guillemets.
La seule petite surprise qui nous attend se trouve à la fin, avec un anti-slash + n.

(\ = alt gr + 8 sur un clavier azerty français classique)

___
**Vue caméra**

Dans une chaine de caractère, l'anti-slash sert à indiquer un caractère spécial, selon ce qui le suit. Dans ce cas particulier \n indique une nouvelle ligne, et donc que les prochains caractères doivent s'écrire à la ligne suivante.

Vous tomberez d'ailleurs parfois sur \r\n, c'est un reliquat de l'époque où on avait besoin de dire aux imprimantes qu'il fallait revenir au début de la ligne puis passer la ligne suivante.

___
**Vue code**

```cpp
std::cout << "Bonjour !\n";
```

Ensuite, à gauche, avons `std::cout`.

Il s'agit d'une représentation du flux de sortie `cout`, c'est-à-dire l'endroit par lequel nous pouvons afficher quelque chose sur la console de notre programme. Nous verrons ça plus en détail après.

Mais au fait, si le flux s'appelle `cout`, qu'est-ce que `std::` signifie ?

___
**Vue caméra**

Vous vous rappelez quand je vous ai parlé des bibliothèques ? Ici nous utilisons la bibliothèque standard, et celle-ci utilise l'espace de nom `std`. On aura l'occasion d'en reparler des espaces de noms.

___
**Vue code**

```cpp
std::cout << "Bonjour !\n";
```

Ainsi donc `std::cout` signifie dans ce cas "le machin `cout` faisant partie de `std`", et le machin dans ce cas précis est un flux de sortie, sur lequel nous effectuons une opération : écrire dedans. Cela se fait ici avec l'opérateur `<<`.

___
**Vue caméra**

Fonction, bloc, flux de sortie, espace de nom, opérateur, ... ?

Étant donné qu'il s'agit du premier cours de C++, je suis obligé d'introduire plein de notions et nous aurons largement l'occasion de rentrer dans les détails plus tard, ne vous inquiétez pas. C'est normal si vous ne comprenez pas tout du premier coup, ça viendra avec le temps.

___
**Vue code**

```cpp
std::cout << "Bonjour\n" << "YouTube!";
```

L'opérateur << nous permet donc d'écrire notamment les chaines de caractères que nous voulons, de gauche à droite. On se servira de ça dans la prochaine vidéo.

___
**Vue caméra**

Voilà, nous sommes au bout de ce premier code en C++, assez simple à première vue mais tout de suite plus complexe lorsque vous cherchez à comprendre ce qu'il s'y passe exactement. Et comprenez bien que la vidéo aurait fait plusieurs heures si j'avais dû vous expliquer en détail tout ce qu'il se passe ici.

___
**Vue code**

Amusez-vous donc à changer le texte, à enchaîner les flux, voire pourquoi pas à afficher des nombres, que nous aborderons dans le deuxième chapitre de ce tutoriel.

```cpp
std::cout << "Il est " << 13 << "h" << 46 << "\n";
```

Notez cependant que vous allez très vite tomber sur une limitation.

```cpp
std::cout << "Bonjour à tous !\n";
```

Si vous êtes sous Windows, il y a de fortes chances pour que vos accents apparaissent de façon bizarre.

___
**Vue caméra**

C'est dû à l'encodage de votre chaîne de caractère et au fait que la console de Windows est une très vieille dame. Si le sujet vous intéresse plus en profondeur, j'y ai consacré un article d'une vingtaine de pages sur mon devblog, dont le lien est en description.

Mais pour dire les choses simplement, il n'y a pas de solution miracle. C'est pourquoi je vous conseillerais d'abandonner l'idée d'afficher des accents à ce stade.

Voilà, nous sommes au bout de ce premier tutoriel sur le C++. Je sais que les choses doivent paraitre un peu floues mais ne vous inquiétez pas, ça va venir.

Le C++ est un langage plutôt complexe à apprendre et il faut y aller petit à petit, et pratiquer, beaucoup pratiquer.

Dans le prochain chapitre nous apprendrons ce que sont les types et les variables, et nous allons rendre notre petit programme un peu plus interactif !

___
**Conclusion**

Merci d'avoir regardé ce premier épisode d'apprentissage du langage C++, je sais qu'il n'est pas parfait mais j'espère bien améliorer ça au fil des épisodes.
N'hésitez pas à me dire ce que vous en avez pensé, mettre un commentaire, un poce bleu, la cloche et même la vache qui va avec.

On se retrouve vite !
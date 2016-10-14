# stdout (la sortie standard)

## Lesson Content

Maintenant que nous somme familiers avec la plupart des commandes et leur sorties, nous allons maintenant voir les flux d'entrées/sorties. Exécutons cette commande, et nous observerons son fonctionnement.

<pre>$ echo Hello World > toto.txt</pre>

Que c'est-il passé ? Observez le répertoire dans lequel vous avez exécuté la commande, vous devriez voir un fichier toto.txt, et à l'intérieur vous verrez la phrase 'Hello World'. Plusieurs choses se sont passé, nous allons donc décomposer la commande.

tout d'abord la première partie :  

<pre>$ echo Hello World</pre>

Nous savons que cela affiche 'Hello World' à l'écran, mais comment ? Les processus utilisent les flux d'entrée/sortie pour recevoir des entrées et renvoyer des sorties. Par défaut, echo  utilise l'entrée standard (stdin), c'est à dire le clavier, et affiche dans la sortie standard (stdout) c'et à dire l'écran. C'est pour ça que quand on écrit echo Hello World dans la console, on a Hello World affiché à l'écran. Cependant, les redirections permettent de changer cela, afin d'avoir plus de flexibilité.

regardons la deuxième partie de la commande :

<pre> > </pre>

le > permet de spécifier ou va aller la sortie. On peut ainsi envoyer la sortie de echo Hello World dans un fichier au lieu de l'écran. Si le fichier n'existe pas, il sera automatiquement créé. S'il existe, le fichier sera écrasé (selon le shell utilisé, on peut changer ce comportement par défaut).

Et voila, vous savez comment fonctionnent les redirections de sortie !

Disons que je ne veut pas  écraser toto.txt, on peut utiliser un autre opérateur de redirection : >>

<pre>$ echo Hello World >> toto.txt</pre>

Cela va ajouter Helo world à la fin de toto.txt, ou créer toto.txt s'il n'existe pas, comme avec > !


## Exercices

essayez ces commandes:

<pre>
$ ls -l /var/log > sortie.txt
$ echo Hello World > rm
$ > fichier.txt
</pre>

## Quiz Question

Quel opérateur de redirection permet d'ajouter la sortie à la fin d'un fichier ?

## Quiz Answer

>>

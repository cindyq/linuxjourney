# stdin (Standard In)

## Lesson Content

Dans le cours précédent,  nous avons appris que nous pouvons utiliser différents flux de sortie, par exemple un fichier ou l'écran. Et bien, il existe également une entrée standard (stdin), que nous pouvons rediriger également. Nous savons que stdin prend son entrée depuis le clavier, mais nous pouvons utiliser des fichiers, la sortie d'autres commandes, ou le terminal lui-même ; voyons un exemple :

Utilisons le toto.txt du cours précédent, qui contient Hello World.

<pre>$ cat <b>&lt;</b> toto.txt <b>&gt;</b> banana.txt </pre>

Comme pour <b>&gt;</b> avec la redirection de stdout, on utilise <b>&lt;</b> pour rediriger stdin.

Normalement, dans cat, on lui envoie un fichier, qui devient stdin. Dans ce cas, c'est toto.txt qui devient notre entrée standard. La sortie de `cat toto.txt` qui est Hello World est redirigée vers banana.txt.

## Exercise

essayez ces commandes :
<pre>
$ echo <b>&lt;</b> toto.txt <b>&gt;</b> banana.txt
$ ls <b>&lt;</b> toto.txt <b>&gt;</b> banana.txt
$ pwd <b>&lt;</b> toto.txt <b>&gt;</b> banana.txt
</pre>

## Quiz Question

Quel opérateur de redirection utilise-t-on pour rediriger stdin ?

## Quiz Answer

<

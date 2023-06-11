# stdin (Standard In)

## Lesson Content

Dans notre leçon précédente, nous avons appris que nous avions différents flux stdout que nous pouvions utiliser, tels qu'un fichier ou l'écran. Eh bien, il existe également différents flux d'entrée standard (stdin) que nous pouvons également utiliser. Nous savons que nous avons stdin à partir de périphériques tels que le clavier, mais nous pouvons également utiliser des fichiers, la sortie d'autres processus et le terminal. Voyons un exemple.

Utilisons le fichier peanuts.txt de la leçon précédente pour cet exemple, souvenez-vous qu'il contenait le texte "Hello World".

<pre>$ cat <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt </pre>

Tout comme nous avions <b>&gt;</b> pour la redirection de stdout, nous pouvons utiliser <b>&lt;</b> pour la redirection de stdin.

Normalement, dans la commande cat, vous lui envoyez un fichier et ce fichier devient stdin, dans ce cas, nous avons redirigé peanuts.txt pour qu'il soit notre stdin. Ensuite, la sortie de cat peanuts.txt, qui serait "Hello World", est redirigée vers un autre fichier appelé banana.txt.

## Exercise

Essayez quelques commandes :

<pre>
$ echo <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ ls <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ pwd <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
</pre>

## Quiz Question

Quel redirigeur utilisez-vous pour rediriger stdin ?

## Quiz Answer

<

# stderr (Standard Error)

## Lesson Content

Essayons quelque chose d'un peu différent : essayons d'afficher un répertoire qui n'existe pas, et de rediriger la sortie vers toto.txt encore une fois.

<pre>$ ls /repertoire/inexistant/ > toto.txt </pre>

Ce que vous devriez voir est :

<pre>ls: /fake/directory: No such file or directory</pre>

Là, vous pensez probablement, ce message aurait du être envoyé dans le fichier ? En fait, il y a un troisième flux d'entrées/sorties, la sortie erreur (stderr). Par défaut, stderr envoie sa sortie sur l'écran également, mais c'est un flux différent de stdout. Il faudra donc le rediriger également.

Malheureusement, l'opérateur de redirection n'est pas aussi simple que <b>&lt;</b> ou <b>&gt;</b> mais il y ressemble fortement. Nous allons devoir utiliser des descripteurs de fichier. Un descripteur de fichier est un nombre positif utilisé pour accéder à un fichier ou un flux. Nous verrons cela plus en  détail plus tard, sachez pour l'instant que les descripteurs de fichier de stdin, stdout et stderr sont 0, 1, et 2 respectivement.

donc pour rediriger stderr vers un fichier, nous pouvons faire :

<pre>$ ls /fake/directory 2> toto.txt</pre>

Maintenant, vous devriez voir le message d'erreur dans toto.txt.

Et si je veux voir stderr et stdout dans toto.txt ? On peut également utiliser les descripteurs :

<pre>$ ls /repertoire/inexistant > toto.txt 2>&1</pre>

Cela envoie le résultat de ls /repertoire/inexistant vers toto.txt, et redirige stderr vers stdout via 2>&1. L'ordre est important, 2>&1 renvoie stderr vers ce que pointe stdout. Dans ce cas, stdout pointe vers un fichier, donc 2>&1 envoie stderr vers ce fichier. Si vous ouvrez toto.txt file, vous devriez voir stderr et stdout. Dans notre cas, il n'y a que stderr.

Il y a un raccourci pour rediriger stdout et stderr vers un fichier :

<pre>$ ls /repertoire/inexistant &> toto.txt</pre>

Et Maintenant, si on ne veut pas voir les messages d'erreur du tout ? Il suffit simplement de rediriger la sortie vers un fichier spécial appelé /dev/null qui va supprimer tout ce qui lui est envoyé.

<pre>$ ls /repertoire/inexistant 2> /dev/null</pre>

## Exercise

Que fait cette commande ?

<pre>$ ls /repertoire/inexistant >> /dev/null 2>&1</pre>

## Quiz Question

Quel est l'opérateur de redirection pour stderr ?

## Quiz Answer

2>

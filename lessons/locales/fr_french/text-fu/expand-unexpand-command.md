# expand and unexpand

## Lesson Content

Dans le cours sur cut, nous avions sample.txt qui contenait un TAB. Normalement, TAB est affiché corerctement, mais dans certains textes, elles ne s'affichent pas comme on le voudrait. On utiliser expand pour remplacer les TAB par des espaces.

<pre>$ expand sample.txt</pre>

Cela va afficher la sortie, avec les tab remplacées par un groupe d'espaces. Pour le sauvegarder dans un fichier, on utilise une redirection.

<pre>$ expand sample.txt > result.txt</pre>

au contraire, on peut convertir un groupe d'espaces en tab avec unexpand :

<pre>$ unexpand -a result.txt</pre>

## Exercise

que se passe-t-il si on utilise expand sans paramètre ?

## Quiz Question

Quelle commande utilise-t-on pour convertir des TAB en espaces ?

## Quiz Answer

expand

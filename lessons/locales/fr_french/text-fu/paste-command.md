# paste

## Lesson Content

la commande paste ressemble à cat, elle fusionne des lignes dans un fichier. Créons un nouveau fichier sample2.txt avec ce contenu :

<pre>
The
quick
brown
fox
</pre>

combinons tout cela sur une ligne:

<pre>$ paste -s sample2.txt</pre>

le délimiteur par défaut est TAB, donc on a tout sur une ligne, séparé par des TAB.

changeons le délimiteur pour rendre cela un peu plus lisible :

<pre>$ paste -d ' ' -s sample2.txt</pre>

Maintenant tout est sur une ligne, séparé par des espaces.

## Exercise

Essayons de 'paste' plusieurs fichiers ensemble. Que se passe-t-il ?

## Quiz Question

quel flag doit-on utiliser avec paste pour tout mettre sur une ligne ?

## Quiz Answer

-s

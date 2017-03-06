# head

## Lesson Content

Disons que nous avons un très long fichier, par exemple cat /var/log/syslog. vous devriez voir des pages de texte défiler. Et si vous vouliez simplement voir les 10 premières lignes ? C'est à ça que sert la commande head. Par défaut, elle affiche les 10 premières lignes d'un fichier.

<pre>$ head /var/log/syslog</pre>

On peut bien sur choisir le nombre de lignes à afficher :

<pre>$ head -n 15 /var/log/syslog</pre>

-n sert à choisir le nombre de lignes.

## Exercise

que fait cette commande ?

<pre>$ head -c 15 /var/log/syslog</pre>

## Quiz Question

quel flag utiliser pour choisir le nombre de lignes à afficher ?

## Quiz Answer

-n

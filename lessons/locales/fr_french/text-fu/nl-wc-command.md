# wc et nl

## Lesson Content
La commande wc (word count) affiche le nombre de mots dans un fichier.

<pre>$ wc /etc/passwd
 96     265    5925 /etc/passwd
</pre>

Elle affiche le nombre de lignes, de mots et d'octets, respectivement.

POur ne voir q'une seule de ces valeurs, il faut utiliser -l, -w ou -c respectivement.

<pre>$ wc -l /etc/passwd
96</pre>

On peut également utiliser nl pour compter le nombre de lignes :

<pre>
file1.txt
i
like
turtles
</pre>

<pre>$ nl file1.txt
1. i
2. like
3. turtles
</pre>

## Exercise

Comment avoir le nombre total de lignes en utilisant nl sans chercher dans toute la sortie ? Aide : il faut utiliser une commande vue précédemment.

## Quiz Question

Quelle commande utiliser pour voir uniquement le nombre de mots d'un fichier ?
## Quiz Answer

wc -w

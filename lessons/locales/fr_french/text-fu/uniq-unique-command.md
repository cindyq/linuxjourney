# uniq (Unique)

## Lesson Content

La commande uniq est utile pour analyser du texte.

Disons que l'on a un texte plein de doublons :

<pre>
reading.txt
book
book
paper
paper
article
article
magazine
</pre>

On peut utiliser uniq pour supprimer ces doublons :

<pre>$ uniq reading.txt
book
paper
article
magazine</pre>

On peut également compter le nombre d'occurrences dans un texte :

<pre>$ uniq -c reading.txt
2 book
2 paper
2 article
1 magazine</pre>

Ou ne sortir que les mots uniques :

<pre>$ uniq -u reading.txt
magazine</pre>

ou seulement ceux qui sont dupliqués :

<pre>$ uniq -d reading.txt
book
paper
article
</pre>

<b>Note</b> : uniq ne voit que les lignes dulpiqèes qui se suivent.

Par exemple, avec ce fichier:

<pre>
reading.txt
book
paper
book
paper
article
magazine
article
</pre>

<pre>$ uniq reading.txt
reading.txt
book
paper
book
paper
article
magazine
article</pre>

uniq renvoie toutes les valeurs, sauf la toute première.

POur contourner cette limite, on peut utiliser sort :

<pre>
$ sort reading.txt | uniq
article
book
magazine
paper</pre>

## Exercise

Que se passe-t-il si on utilise uniq -uc ?

## Quiz Question

Quelle commande utiliser pour enlever les doublons d'un fichier ?

## Quiz Answer

uniq

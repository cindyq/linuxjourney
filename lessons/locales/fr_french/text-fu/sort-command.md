# sort

## Lesson Content

La commande sort permet de trier facilement des lignes :

<pre>
file1.txt
dog
cow
cat
elephant
bird

$ sort file1.txt
bird
cat
cow
dog
elephant
</pre>

on peut également trier dans l'ordre inverse :

<pre>$ sort -r file1.txt
elephant
dog
cow
cat
bird
</pre>

Et également par des valeurs numériques :

<pre>$ sort -n file1.txt
bird
cat
cow
elephant
dog
</pre>

## Exercise

sort est très utile pour être combiné à d'autres commandes. Essayez celle-ci :

<pre>$ ls /etc | sort -rn</pre>

## Quiz Question

Quel flag utiliser pour trier dans l'ordre inverse ?

## Quiz Answer

-r

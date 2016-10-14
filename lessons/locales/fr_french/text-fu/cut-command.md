# cut

## Lesson Content

Nous allons apprendre quelques commandes très utiles pour éditer du texte. Avant de commencer, créons un fichier dans lequel nous allons travailler. Copiez-collez cette commande, puis ajouter un tab entre lazy et dog (appuyer sur Ctrl-v + TAB).

<pre>$ echo 'The quick brown; fox jumps over the lazy  dog' > sample.txt</pre>

Nous allons tout d'abord voir la commande cut. Elle permet d'extraire une portion d'un texte.

Pour extraire une liste de caractères :

<pre>$ cut -c 5 sample.txt</pre>

va renvoyer le  5ème caractère de chaque ligne du fichier. Dans notre cas, c'est 'q'. Notez que les espaces comptent comme un caractère.

Pour extraire le contenu d'un champ, nous allons faire une petite modification:

<pre>$ cut -f 2 sample.txt</pre>

The -f (field flag) pour le texte text selon un délimiteur, par défaut TAB, donc tout ce qui est séparé par une TAB est un champ. Vous devriez voir 'dog'.

vous pouvez combiner -f avec -d pour choisir votre séparateur :
<pre>$ cut -f 1 -d ";" sample.txt</pre>

Cela va choisir ';' comme délimiteur, ce qui va donc afficher 'The quick brown'

## Exercise

Que font ces commandes ? Pourquoi ?

<pre>$ cut -c 5-10 sample.txt
$ cut -c 5- sample.txt
$ cut -c -5 sample.txt
</pre>

## Quiz Question

Quelle commande utiliser pour avoir le premier caractère de chaque ligne ?

## Quiz Answer

cut -c 1

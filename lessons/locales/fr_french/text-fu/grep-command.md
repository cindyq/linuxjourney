# grep

## Lesson Content

La commande grep est probablement la commande de texte que vous utiliserez le plus. Elle permet de chercher dans un fichier pour un certain motif. Par exemple, vous voulez savoir si un fichier existe dans un certain répertoire, ou chercher si une phrase est dans ce fichier ? Vous allez utiliser grep !

Par exemple avec sample.txt 

<pre>$ grep fox sample.txt</pre>

Nous avons trouvé fox dans le fichier avec grep !

On peut utiliser -i pour ne pas prendre la casse en considération :

<pre>$ grep -i motif fichier</pre>

Pour être vraiment flexible, on l'utilise avec une autre commande :

<pre>$ env | grep -i User</pre>

Come vous le voyez, il y a plein d'options. On peut même utiliser des expressions régulières :

<pre>$ ls /somedir | grep '.txt$'</pre>

renvoie les fichiers txt dans somedir.

## Exercise

Vous avez peut-être entendu parler de egrep et fgrep , qui sont des appels dépréciés, remplacés par grep -E et grep -F. Lisez la page man de grep pour en savoir plus.

## Quiz Question

Quel commande utiliser pour chercher un motif dans un fichiers ?

## Quiz Answer

grep

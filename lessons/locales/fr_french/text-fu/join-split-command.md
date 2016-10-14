# join et split

## Lesson Content

la commande join permet de fusionner plusieurs fichiers, selon un champ commun.
Disons que l'ai 2 fichiers que je veux fusionner :
<pre>file1.txt
1 John
2 Jane
3 Mary

file2.txt
1 Doe
2 Doe
3 Sue

$ join file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

Vous voyez ? Par défaut, ils sont fusionné selon le premier champ, qui doit être identique dans les 2 fichiers. Si ils ne le sont pas, vous pouvez les trier, et ils seront fusionnés selon 1, 2, 3...

Comment fusionner ces 2 fichiers ?

<pre>file1.txt
John 1
Jane 2
Mary 3

file2.txt
1 Doe
2 Doe
3 Sue
</pre>

Nous devons spécifier les champs,  ici on veut le champ 2 sur file1.txt et le champ 1 sur file2.txt, ce qui nous donne :

<pre>
$ join -1 2 -2 1 file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

-1 se réfère à  to file1.txt and -2 se réfère à file2.txt.
On peut également séparer un fichier en plusieurs avec la commande split.

<pre>$ split somefile</pre>

Cela va séparer le fichier en plusieurs fichiers. Par défaut, la découpe se fait toute les 1000 lignes.

## Exercise

essayez de fusionner 2 fichier qui n'ont pas le même nombre de lignes. que se passe-t-il ?

## Quiz Question

Quelle commande utiliser pour fusionner cat , dog et cow ?

## Quiz Answer

join cat dog cow

# pipe et tee

## Lesson Content

Faisons maintenant un peu de plomberie. Essayons cette commande :

<pre>$ ls -la /etc</pre>

Vous devriez obtenir une liste très longue, assez difficile à lire. Au lieu de l'envoyer dans un fichier, ce serait bien de pouvoir voir la sortie avec une autre commande, comme less ! Et bien, c'est possible !

<pre>$ ls -la /etc | less </pre>

le pipe (ou tuyau) |, représenté par une barre verticale, nous permet de rediriger le stdout d'une commande vers le stdin d'une autre commande. dans ce cas, on prend stdout de ls -la /etc et on le  <i>pipe</i> vers la commande less. La commande pipe est très utile, et nous l'utiliserons très souvent.

Et si je veux rediriger ma sortie vers 2 flux différents ? C'est possible grâce à tee :

<pre>$ ls | tee toto.txt</pre>

La sortie de ls est affichée à l'écran, et si l'on ouvre toto.txt, on aura la même information.

## Exercise

essayez cette commande :
<pre>$ ls | tee toto.txt titi.txt</pre>

## Quiz Question

Quel caractère représente le pipe ?

## Quiz Answer

|

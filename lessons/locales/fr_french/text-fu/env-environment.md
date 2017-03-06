# env (Environnement)

## Lesson Content

essayez cette commande :

<pre>$ echo $HOME</pre>

vous devriez voir le chemin de votre dossier personnel, le mien ressemble à /home/pete.

Et cette commande ?

<pre>$ echo $USER </pre>

Vous voyez votre nom d'utilisateur !
Mais d'ou veient cette information ? de vos vaariables d'environnement. vous pouvez les voir en tapant :

<pre>$ env </pre>

Cela va renvoyer beaucoup d'informations sur les variables d'environnement que vous avez définies. Ces variabls contiennent des informations précieuses, que les processus vont pouvoir utiliser.

Voici un exemple :

<pre>
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
PWD=/home/user
USER=pete
</pre>


Une des variabls les plus importantes est le PATH. Vous pouvez y accéder en mettant un $ devant :

<pre>
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
</pre>

Cela renvoie une liste de chemins, séparés par 2 points, dans lesquels le système va chercher quand on exécute une commande. Disons que vous téléchargez un exécutable,  et l'installez dans un répertoire quelconque ; quand vous voulez exécuter la commande, vous tapez $ coolcommand et vous avez un magnifique  command not found. C'et ridicule, vous voyez le fichier binaire dans votre répertoire, et il existe bien ! Ce qui se passe , est que votre variable $PATH ne contient pas ce répertoire, et donc ne cherche pas dedans.

Disons que vous avez plein de binaires dans ce répertoire que vous voulez exécuter, vous pouvez modifier PATH pour inclure ce répertoire, et exécuter facilement les commandes.


## Exercise

qu'affiche cette commande ? Pourquoi ?
<pre>$ echo $HOME</pre>

## Quiz Question

Comment afficher toutes les variables d'environnement ?

## Quiz Answer

env

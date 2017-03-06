# tail

## Lesson Content

Comme head, tail affiche les 10 dernières lignes d'un fichier.

<pre>$ tail /var/log/syslog</pre>

ON peut également choisir le nombre de lignes :

<pre>$ tail -n 10 /var/log/syslog</pre>

Une option intéressante est le flag -f (follow), qui va suivre le fichier à mesure qu'il grossit.

<pre>$ tail -f /var/log/syslog</pre>

le ficher syslog va grossir à mesure que vous interagissez avec le système, et tail va permettre de voir les changements.

## Exercise

regardez le manuel de tail, et observer les autres flags.

<pre>$ man tail</pre>

## Quiz Question

quel est le flag utilisé pour suivre un fichier avec tail ?

## Quiz Answer

-f

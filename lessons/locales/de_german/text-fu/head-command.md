# head

## Inhalte der Lektion

Nehmen wir an, wir haben eine sehr lange Datei. Auf deinem System gibt es unzählige davon, analysiere mal /var/log/syslog mit cat. Seiten um Seiten von Text wo das Auge hinreicht! Was wenn du nur die ersten paar Linien der Datei sehen möchtest? Das können wir natürlich tun, und zwar mit dem head Befehl. Standardmässig zeigt dieser Befehl die ersten 10 Linien einer Datei.

<pre>$ head /var/log/syslog</pre>

Du kannst die Zahl natürlich ändern, zum Beispiel auf die ersten 15 Linien:

<pre>$ head -n 15 /var/log/syslog</pre>

Das -n Flag setzt die Anzahl Linien. 

## Übung

Was tut der folgende Command und wieso? 

<pre>$ head -c 15 /var/log/syslog</pre>

## Quizfrage

Welches Flag benutzt du um die Anzahl auszugebende Linien anzupassen?

## Quizantwort

-n

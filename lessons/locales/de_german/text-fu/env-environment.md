# env (Environment)

## Inhalt der Lektion

Gib den folgenden Befehl ein:

<pre>$ echo $HOME</pre>

Du solltest den Dateipfad zu deinem Startverzeichnis erhalten. Meiner sieht so aus /home/pete.

Und dieser Befehl?

<pre>$ echo $USER </pre>

Du erhälst deinen Benutzernamen!

Woher kommt diese Information? Sie kommt aus den Umgebungs-Variablen. Du kannst diese folgendermaßen aufrufen:

<pre>$ env </pre>

Dies gibt sehr viele Informationen über die aktuellen Umgebungs-Variablen aus. Das sind Variablen, die die Prozesse des Computers verwenden können.

Hier ist ein kurzes Beispiel:

<pre>
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
PWD=/home/user
USER=pete
</pre>


Eine wichtige Variabel ist die PATH-Variabel. Du erhälst diese Variablen, indem Du ein $-Zeichen vor den Namen der Variabel setzt:

<pre>
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
</pre>

Dies gibt eine Liste, abgegrenzt durch einen Doppelpunkt, mit Dateipfaden zurück, die dein System durchsucht, wenn es Befehle ausführt. Du lädst zum Beispiel eine Datei manuell herunter und installierst ein Programm aus dem Internet. Du verschiebst es in einen nichtstandardmäßigen Ordner und möchtest einen Befehl ausführen. Du schreibst $coolerbefehl und dir wird gesagt, dass der Befehl nicht gefunden wurde. Also schaust Du in den entsprechenden Ordner und siehst, dass er aber existiert. Hierbei überprüft die $PATH-Variabel nicht den entsprechenden Ordner und Du erhälst einen Fehler.

Nun kannst Du einfach die PATH-Variabel anpassen, um diesen Ordner einzubinden.


## Übung

Was gibt der folgende Befehl aus?

<pre>$ echo $HOME</pre>

## Quizfrage

Wie erhälst Du eine Liste mit allen Umgebungs-Variablen?

## Quiz Antwort

env

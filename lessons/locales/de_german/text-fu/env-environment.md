# env (Environment)

## Inhalt der Lektion

Führe den folgenden Command aus:

<pre>$ echo $HOME</pre>

Du solltest nun den Pfad zu deinem Home- Verzeichnis sehen, meiner ist /home/pete. 

Was ist mit diesem Command?

<pre>$ echo $USER </pre>

Du siehst deinen Benutzernamen, nicht war?

Woher kommen diese Informationen? Sie kommen von deinen Umgebungsvariablen (environment variables). Mit

<pre>$ env </pre>

kannst du alle gesetzten Umgebungsvariablen ansehen. Darin sind wertvolle Informationen gespeichert, die die Shell und andere Prozesse benützten können um korrekt zu funktionieren.

Hier ein kleines Beispiel:

<pre>
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
PWD=/home/user
USER=pete
</pre>

Eine sehr wichtige Variable ist die PATH Variable. Du kannst auf sie zugreifen indem du ein $ vor den Variablennamen setzt:

<pre>
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
</pre>

In PATH ist eine Liste von Pfäden gespeichert, separiert mit einem Doppelpunkt. In diesen Pfäden sucht das System wenn du einen Befehl/Command ausführen möchtest. Sagen wir, du möchtest manuell ein Softwarepaket herunterladen und installierst es in ein nicht-standard Verzeichnis. Nun möchtest du ein Befehl ausführen, der dir dieses Softwarepaket zur Verfügung stellt. Du schreibst also $ software-command, tippst Enter und die Shell antwortet mit "Command not found". Was hat da nicht geklappt? Nun, die Shell schaut nur in Pfaden die in der PATH-Variable stehen nach, ob es eine ausführbare Datei gibt (binary).

Du kannst nun einfach die PATH-Variable anpassen und den Pfad zu deinem Binary hinzufügen und schon kannst du $ software-command ausführen.

## Übung

Was wird auf den Bildschirm geschrieben?

<pre>$ echo $HOME</pre>

## Quizfrage

Wie kannst du deine gesetzten Umgebungsvariablen ansehen?

## Quizantwort 

env

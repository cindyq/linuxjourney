# tail

## Inhalt der Lektion

Ähnlich wie beim Befehl head, lässt dich tail die letzten 10 Zeilen einer Datei sehen.

<pre>$ tail /var/log/syslog</pre>

Wie bei head, kannst Du die Anzahl der Zeilen verändern, die Du sehen möchtest.

<pre>$ tail -n 10 /var/log/syslog</pre>

Ein weiteres Attribut is -f (follow), welches die Datei verfolgt, wie sie wächst. Probiere es aus und sieh, was passiert.

<pre>$ tail -f /var/log/syslog</pre>

Deine Datei syslog verändert sich ständig, wenn Du mit deinem Computer arbeitest. Mit dem Attribut -f siehst Du alles, was zur Datei hinzugefügt wird.

## Übung

Schau dir die Anleitung des Befehls tail an und probiere ein paar Befehle, die wir hier nicht gezeigt haben.

<pre>$ man tail</pre>

## Quizfrage

Mit welchem Attribut kannst Du die Datei beobachten, wie sie wächst?

## Quiz Antwort

-f

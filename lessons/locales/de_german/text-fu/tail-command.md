# tail

## Inhalte der Lektion

Ähnlich zum head Befehl zeigt dir der tail (Schwanz) Befehl die letzten 10 Linien einer Datei an.

<pre>$ tail /var/log/syslog</pre>

Auch hier dient das -n Flag zur Bestimmung der Anzahl Linien.

<pre>$ tail -n 10 /var/log/syslog</pre>

Eine grossartige Option ist das -f (follow) Flag. Mit diesem kannst du der Datei folgen, wenn sie wächst. Probiere es aus!

<pre>$ tail -f /var/log/syslog</pre> 

Deine syslog Datei wird dauernd verändert während du mit dem System interagierst. tail -f hält dich auf dem Laufenden, du siehst immer gleich was zur Datei hinzugefügt wird.

## Übung

Schau dir die man Seite von tail an und lese ein bisschen über die anderen Befehle, die wir nicht benutzt haben.

<pre>$ man tail</pre>

## Quizfrage

Mit welchem Flag kannst du das Fileende verfolgen?

## Quizantwort

-f

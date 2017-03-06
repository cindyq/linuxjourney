# head

## Inhalt der Lektion

Sagen wir mal, wir haben eine sehr lange Datei. Hierfür können wir zum Beispiel Logdaten des Systems verwenden. Öffne mit cat die Datei /var/log/syslog. Du wirst ein sehr langes Dokument sehen. Nun möchtest Du nur die ersten paar Zeilen der Datei sehen. Das können wir mit dem Befehl head machen, wobei Du standardmäßig 10 Zeilen sehen wirst.

<pre>$ head /var/log/syslog</pre>

Du kannst aber auch die Anzahl der Zeilen anpassen.

<pre>$ head -n 15 /var/log/syslog</pre>

Das Attribut -n steht für Anzahl an Linien (number of lines).

## Übung

Was macht der folgende Befehl und warum?

<pre>$ head -c 15 /var/log/syslog</pre>

## Quizfrage

Welches Attribut würdest Du verwenden, um die Anzahl der Zeilen festzulegen, die Du mit dem Befehl head ausgeben möchtest.

## Quiz Antwort

-n

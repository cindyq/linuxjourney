# paste

## Inhalt der Lektion

Der Befehl paste ähnelt dem Befehl cat. Erstellen wir eine neue Datei mit folgendem Inhalt:

<pre>
sample2.txt
The
quick
brown
fox
</pre>

Nun verbinden wir all diese Zeilen in eine Zeile:

<pre>$ paste -s sample2.txt</pre>

Das standardmäßige Abtrennungszeichen ist TAB.

Nun ändern wir dieses Abtrennungszeichen mit -d (delimiter), damit die Ausgabe etwas lesbarer wird:

<pre>$ paste -d ' ' -s sample2.txt</pre>

Jetzt sollte alles in einer Zeile und durch Leerzeichen abgetrennt sein.

## Übung

Try to paste multiple files together, what happens?

## Quizfrage

Welches Attribut verwendest Du, um alles in eine Zeile zu schieben?

## Quiz Antwort

-s

# cut

## Inhalt der Lektion

Lerne wir ein paar nützliche Befehle, die du brauchen kannst um Text zu verarbeiten. Bevor wir starten müssen wir eine Datei erzeugen, mit der wir arbeiten können. Kopiere dazu den folgenden Befehl in deine Shell (einfügen in die Shell kannst du mit Ctrl + Shift + V), und achte dabei darauf, dass zwischen lazy und dog ein TAB Zeichen steht (Ctrl + V gedrückt halten, TAB drücken).

<pre>$ echo 'The quick brown; fox jumps over the lazy  dog' > sample.txt</pre>

Zuerst lernen wir den cut Befehl. Er schneidet Teile aus einer Textdatei.

Um Inhalte ab einer bestimmten Anzahl Zeichen zu extrahieren:

<pre>$ cut -c 5 sample.txt</pre>

Dieser Command gibt den fünften Buchstaben in jeder Linie der Datei aus. In diesem Fall ist es "q", der Abstand zählt auch als Buchstabe.

Möchten wir nicht die Buchstaben zählen, sondern die Felder, brauchen wir eine kleine Anpassung:

<pre>$ cut -f 2 sample.txt</pre>

Das -f oder field Flag schneidet Text aus basierend auf Feldern. Was ist ein Feld? Ein Feld wird standardmässig durch TABs limitiert, es ist also alles, das von einem TAB separiert wird ein Field. Der Output sollte das Wort dog sein.

Das field Flag kannst du mit einem delimiter (delimiter = Separator) flag ergänzen, um einen anderen Separator zu verwenden.

<pre>$ cut -f 1 -d ";" sample.txt</pre>

Jetzt wird nicht mehr TAB als delimiter verwendet, sondern das Semikolon ";". Und da wir das erste Feld ausschneiden sollte "The quick brown" als Output erscheinen.

## Übung

Was tut der folgende Befehl? Weshalb?

<pre>$ cut -c 5-10 sample.txt
$ cut -c 5- sample.txt
$ cut -c -5 sample.txt
</pre>

## Quizfrage

Welchen Command würdest du benutzten um den ersten Buchstaben von jeder Linie einer Datei auszugeben?

## Quizantwort

cut -c 1

# join and split

## Inhalte der Lektion

Der join Befehl erlaubt dir, mehrere Dateien bei einem gängigen Feld zu vereinen.

Sagen wir du hast 2 Dateien, du du zusammen kombinieren möchtest:
<pre>file1.txt
1 John
2 Jane
3 Mary

file2.txt
1 Doe
2 Doe
3 Sue

$ join file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

Hast du gesehen, wie es die Dateien verbunden hat? Die Dateien werden über das erste Feld miteinander verbunden. Du kannst den Befehl auch anpassen, um nicht über das erste Feld zu verbinden. Dann musst du aber eine Nummerierung verwenden.

Wie würden die folgenden Linien zusammengesetzt werden?

<pre>file1.txt
John 1
Jane 2
Mary 3

file2.txt
1 Doe
2 Doe
3 Sue
</pre>

Um diese Dateien zu verienen musst du bestimmen, welche Felder du zusammennehmen möchtest. In diesem Fall möchten wir Feld 2 von file1.txt und Feld 1 von file2.txt auf der gleichen Linie, also würde der Befehl folgendermassen aussehen:

<pre>
$ join -1 2 -2 1 file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

-1 zeigt auf file1.txt und -2 auf file2.txt. Du kannst eine Datei auch wieder in zwei unterschiedliche Dateien splitten:
<pre>$ split somefile</pre>

Dies splittet die Datei somefile in verschiedene Dateien, standardmässig bis sie ein Limit von 1000 Linien erreichen. Die Dateien werden, falls nicht anders angegeben, x** benannt.

## Übung

Verbinde zwei Dateien mit einer unterschiedlichen Anzahl Linien in jeder Datei. Was passiert?

## Quizfrage

Welchen Befehl würder du benutzen um Dateien zu verbinden die cat, dog und cow heissen?

## Quizantwort

join cat dog cow

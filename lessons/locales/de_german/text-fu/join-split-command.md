# join und split

## Inhalt der Lektion

Der Befehl join lässt uns mehrere Dateien zusammenfassen:

Gehen wir davon aus, wir haben zwei Datein, die wir zusammenfügen wollen:

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

Hast Du gesehen, wie die Dateien zusammengefügt worden sind. Sie werden mit dem ersten Abschnitt der Zeile zusammengefasst, so dass diese identisch sein müssen.

Wie würdest Du folgende Datein zusammenfügen?

<pre>file1.txt
John 1
Jane 2
Mary 3

file2.txt
1 Doe
2 Doe
3 Sue
</pre>

Um diese Dateien zusammenzufügen, musst Du festlegen, welche Abschnitte Du verwendest. In diesem Fall wollen wir Abschnitt 2 aus file1.txt und Abschnitt 1 aus file2.txt. Also sieht der Befehl wie folgt aus:

<pre>
$ join -1 2 -2 1 file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

-1 gehört zu file1.txt und -2 gehört zu file2.txt. Ziemlich geschickt. Du kannst aber auch eine Datei aufspalten:

<pre>$ split somefile</pre>

Das wird die Datei in unterschiedliche Dateien aufspalten, wobei dies standarmäßig nach 1000 Zeilen passiert. Normalerweise werden die Datein x** genannt.

## Übung

Füge zwei Dateien mit unterschiedlich vielen Zeilen zusammen. Was passiert?

## Quizfrage

Welchen Befehl würdest Du verwenden, um die Dateien mit den Namen cat dog und cow zusammenzufügen?

## Quiz Antwort

join cat dog cow

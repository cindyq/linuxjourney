# wc und nl

## Lesson Content

Der Befehl wc (word count) zählt die Anzahl der Zeichen in einer Datei.

<pre>$ wc /etc/passwd
 96     265    5925 /etc/passwd
</pre>

Es gibt jeweils die Anzahl der Zeilen, Wörter und Bytes zurück.

Um nur die Anzahl der einzelnen Inhalte zu sehen, kannst Du -l. -w oder -c verwenden.

<pre>$ wc -l /etc/passwd
96</pre>

Ein anderer Befehl, mit dem Du die Anzahl der Zeilen herausfindest, lautet nc (number lines).

<pre>
file1.txt
i
like
turtles
</pre>

<pre>$ nl file1.txt
1. i
2. like
3. turtles
</pre>

## Übung

Wie erhälst die Anzahl der Linien mit dem Befehl nl ohne die ganze Ausgabe durchzuschauen? Hinweis: Verwende einen anderen Befehl, den wir in diesem Kapitel gelernt haben.

## Quizfrage

Welchen Befehl verwendest Du, um die Anzahl an Wörtern aus einer Datei zu erhalten?

## Quiz Antwort

wc -w

# wc and nl

## Inhalte der Lektion

Der wc (word count) Befehl zeigt die totale Anzahl Wörter in einer Datei an.

<pre>$ wc /etc/passwd
 96     265    5925 /etc/passwd
</pre>

Er zeigt die Anzahl Linien, Anzahl Wörter und die Anzahl Bytes (von links nach rechts) der Datei.

Um nur die Anzahl Elemente eines bestimmten Feldes zu zeigen, benutze das -l, -w oder -c Flag.

<pre>$ wc -l /etc/passwd
96</pre>

Ein weiterer Command um die Anzahl Linien einer Datei zu prüfen ist nl (number lines).

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

Wie würdest du die totale Anzahl Linien mit dem nl Command kriegen, ohne den gesamten Output zu durchsuchen? Tipp: Benutze einen weiteren Command welchen du in diesem Kurs kennengelernt hast.

## Quizfrage

Welchen Befehl würdest du benutzen umd die totale Anzahl Wörter in einer Datei zu kriegen?

## Quizantwort

wc -w

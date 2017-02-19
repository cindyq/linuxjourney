# cut

## Inhalt der Lektion

Wir werden einige nützliche Befehle kennen lernen, um mit Texten zu arbeiten. Bevor wir starten, erstellen wir eine Datei, mit der wir arbeiten werden. Kopiere den folgendend Befehl und füge ihn ein. Wenn Du ihn hinzugefügt hast, füge ein TAB zwischen lazy und dog ein (drücke Strg-V + TAB)

<pre>$ echo 'The quick brown; fox jumps over the lazy  dog' > sample.txt</pre>

Der ersten Befehl, den wir kennenlernen werden, ist cut. Damit erhält man das Zeichen an einer bestimmten Stelle in einer Datei.

So erhält man einen Teil einer Liste mit Zeichen:

<pre>$ cut -c 5 sample.txt</pre>

Dies gibt das 5. Zeichen von jeder Zeile in der Datei aus. In diesem Fall ist es "q", da Leerzeichen auch als Zeichen gezählt werden.

Um den Inhalt eines Textabschnittes zu erhalten, müssen wir den Befehl etwas anpassen.

<pre>$ cut -f 2 sample.txt</pre>

Der Parameter -f oder field nimmt einen Abschnitt einer Datei, welcher normalerweise mit eiem TAB abgetrennt ist. Hier solltest Du "dog" als Ausgabe erhalten.

Du kannst den Textabschnitts-Parameter mit dem Trenn-Parameter (delimiter) kombinieren, um den Inhalt durch ein anderes Zeichen zu trennen:

<pre>$ cut -f 1 -d ";" sample.txt</pre>

Dies ändert das Trennzeichen von einem TAB zu ";" und so sollte der erste Abschnitt "The quick brown" sein.

## Übung

Was machen folgende Befehle? Warum?

<pre>$ cut -c 5-10 sample.txt
$ cut -c 5- sample.txt
$ cut -c -5 sample.txt
</pre>

## Quizfrage

Welchen Befehl würdest Du verwenden, um das erste Zeichen von jeder Zeile aus einer Datei zu erhalten?

## Quiz Antwort

cut -c 1

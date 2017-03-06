# grep

## Inhalt der Lektion

Der Befehl grep ist der bekannteste Textverarbeitungs-Befehl. Er gibt unsdie Möglichkeit, Dateien nach Zeichen in einem bestimmten Muster zu durchsuchen. Du möchtest zum Beispiel wissen, ob eine Datei in einem bestimmten Ordner vorhanden ist oder ob eine Zeichenkette in einer Datei vorkommt. Du würdest dich nicht durch jede einzelne Zeile durchkämpfen, Du verwendest grep!

Verwenden wir wieder die sample.txt Datei:

<pre>$ grep fox sample.txt</pre>

Du solltest herausfinden, dass grep in der sample.txt den Begriff fox gefunden hat.

Du kannst mit grep auch Muster finden, indem Du das -i (insensitive) Attribut verwendest:

<pre>$ grep -i somepattern somefile</pre>

Um noch flexibler mit grep zu arbeiten, kannst Du es mit anderen Befehl verknüpfen, indem Du ein | zwischen die beiden Befehle schreibst.

<pre>$ env | grep -i User</pre>

Wie Du sehen kannst, ist grep sehr vielseitig. Du kannst sogar normale Ausdrücke in deinem Muster verwende:

<pre>$ ls /somedir | grep '.txt$'</pre>

Dies sollte alle Dateien in /somedir zurückgeben, die mit .txt enden.

## Übung

Vielleicht hast Du schon von egrep oder fgrep gehört. Das sind veraltete Varianten von grep, die durch grep -E und grep -F abgelöst worden sind. Lies die Anleitung zu grep, um mehr darüber zu erfahren.

## Quizfrage

Welchen Befehl benutzt Du, um bestimmte Muster zu finden.

## Quiz Antwort

grep

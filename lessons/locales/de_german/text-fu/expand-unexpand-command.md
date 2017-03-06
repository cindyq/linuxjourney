# expand und unexpand

## Inhalt der Lektion

In dem Artikel über den cut Befehl, haben wir eine Datei mit dem Namen sample.txt erstellt, die einen TAB enthielt. Normalerweise sehen TABs anders aus, aber in manchen Dateien wird das nicht ganz deutlich. TABs in einer Text-Datei können anders als Leerzeichen wirken. Um TABs zu Leerzeichen zu ändern, verwendet man den Ausdehnungs-Befehl.

<pre>$ expand sample.txt</pre>

Der sich oberhalb befindende Befehl gibt den Inhalt der Datei aus, wobei alle TABs zu (mehreren) Leerzeichen umgewandelt worden sind. Um die Ausgabe zu speichern, gib folgendes ein:

<pre>$ expand sample.txt > result.txt</pre>

Im Gegensatz zum Ausdehnen, gibt es auch noch das Zusammendrücken, mit dem man mehrere Leerzeichen zu einem TABs abändern kann:

<pre>$ unexpand -a result.txt</pre>

## Übung

Was passiert, wenn Du nur expand, ohne Dateinamen eingibst?

## Quizfrage

Welcher Befehl wird genutzt, um TABs zu Leerzeichen umzuwandeln?

## Quiz Antwort

expand

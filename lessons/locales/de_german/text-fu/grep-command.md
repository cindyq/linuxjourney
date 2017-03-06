# grep

## Inhalte der Lektion

Der am meisten verwendete Textmanipulierbefehl ist zweifelsohne grep. Mit ihm kannst du Dateien nach Buchstabenmustern durchsuchen. Was wenn du zum Beispiel wissen möchtest, ob eine Datei in einem Verzeichnis existiert oder ob ein Text in einer Datei vorkommt? Du musst ganz sicher nicht die ganzen Outputs analysieren, du benutzt einfach grep!

Benutzen wir unser sample.txt als Beispiel:

<pre>$ grep fox sample.txt</pre>

Du solltest sehen, das grep das Wort fox in sample.txt gefunden hat.

Mit dem -i Flag kannst du die Gross-/Kleinschreibung ignorieren (case insensitive -i):

<pre>$ grep -i somepattern somefile</pre>

Um noch flexibler mit grep zu werden kannst du ihn mit anderen Commands verwenden mit dem Pipe Zeichen.

<pre>$ env | grep -i User</pre>

grep ist also sehr vielseitig. Du kannst sogar reguläre Ausdrücke in deinem Muster verwenden (Regex):

<pre>$ ls /somedir | grep '.txt$'</pre>

Das sollte alle Dateien die auf .txt enden ausgeben.

## übung

Vielleicht hast du schon von egrep oder fgrep gehört. Diese Befehle sind mittlerweile überholt und sind seit je her ersetzt worden durch grep -E und grep -F. In der manpage über grep erfährst du mehr dazu.

## Quizfrage

Welchen Command benurzr du um ein bestimmtes Muster zu finden?

## Quizantwort

grep

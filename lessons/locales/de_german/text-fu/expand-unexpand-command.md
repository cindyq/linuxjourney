# expand and unexpand

## Inhalte der Lektion

In der Lektion über den cut Befehl hatten wir unsere sample.txt Datei, welche einen TAB beinhaltete. Normalerweise erkennt man ein TAB Zeichen sofort, aber einige Textdateien zeigen es nicht gut genug. TABS sind vielleicht auch nicht die bevorzugte Art, Abstände in einer Datei zu realisieren. Um Tabs zu Abständen zu ändern, benutze

<pre>$ expand sample.txt</pre>.

Der obrige Befehl gibt den Text mit jedem TAB ersetzt durch eine Gruppe von Abständen aus. Um die Ausgabe in eine Datei umzuleiten, benutze die stdout- Umleitung:

<pre>$ expand sample.txt > result.txt</pre>

Das Gegenteil von expand ist unexpand, wobei wir jede Leerzeichengruppe in einen Tab zurückwandeln können.

<pre>$ unexpand -a result.txt</pre>

## Übung

Was passiert wenn du nur expand in der Shell ausführst, ohne irgendwelchen Dateiinput?

## Quizfrage

Mit welchem Command kann man TABs in Leerzeichen verwandeln?

## Quizantwort

expand

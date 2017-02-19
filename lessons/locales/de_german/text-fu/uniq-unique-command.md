# uniq (Unique)

## Inhalt der Lektion

Der Befehl uniq steht für einmalig (unique) und lässt uns einen Text analysieren.

Gehen wir davon aus, das wir eine Datei mit vielen doppelten Einträgen haben.

<pre>
reading.txt
book
book
paper
paper
article
article
magazine
</pre>

Um die Duplikate zu entfernen, kannst Du den Befehl uniq verwenden.

<pre>$ uniq reading.txt
book
paper
article
magazine</pre>

Nun möchten wir herausfinden, wie oft dies auftritt:

<pre>$ uniq -c reading.txt
2 book
2 paper
2 article
1 magazine</pre>

Nun möchten wir nur Wörter, die nur einmal vorkommen, erhalten.

<pre>$ uniq -u reading.txt
magazine</pre>

Oder auch nur welche, die mehrmals vorkommen.

<pre>$ uniq -d reading.txt
book
paper
article
</pre>

<b>Hinweis</b> : Der Befehl uniq entdeckt keine Duplikate, die nicht direkt hintereinander folgen. Zum Beispiel:

Gehen wir davon aus, dass wir eine Datei mit Duplikaten haben, die nicht direkt hintereinander folgen:

<pre>
reading.txt
book
paper
book
paper
article
magazine
article
</pre>

<pre>$ uniq reading.txt
reading.txt
book
paper
book
paper
article
magazine
article</pre>

Das Ergebnis wird nach wie vor alle Einträge beinhalten.

Um dies zu überwinden, können wir die Einträge zuerst sortieren:

<pre>
$ sort reading.txt | uniq
article
book
magazine
paper</pre>

## Übung

Welches Ergebnis erhälst Du, wenn Du uniq -uc ausprobierst?

## Quizfrage

Welchen Befehl verwendst Du, um Duplikate aus einer Datei zu entfernen?

## Quiz Antwort

uniq

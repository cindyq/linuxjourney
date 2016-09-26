# uniq (Unique)

## Inhalte der Lektion

Der uniq (unique = einzigartig) Befehl ist ein weiteres praktisches Tool um Text zu parsen.

Sagen wir, du hast eine Datei mit sehr vielen Duplikaten:

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

Um nun die Duplikate zu ersetzen, kannst du den uniq Befehl verwenden:

<pre>$ uniq reading.txt
book
paper
article
magazine</pre>

Zählen wir die Anzahl Linien einer Datei:

<pre>$ uniq -c reading.txt
2 book
2 paper
2 article
1 magazine</pre>

Extrahiere alle unique (einzigartigen) Werte:

<pre>$ uniq -u reading.txt
magazine</pre>

Extrahiere alle Duplikate:

<pre>$ uniq -d reading.txt
book
paper
article
</pre>

<b>Bemerkung</b>: uniq erkennt nur Duplikate, wenn sie nebeneinander sind. Beispiel:

Nehmen wir an, du hast ein Datei mit Duplikaten, welche nicht nebeneinander sind:

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

Das Resultat von uniq ist ernüchternd, es enthält alle Einträge der Datei.

Um dieses Defizit von uniq auszulösche können wir den Befehl mit sort kombinieren:

<pre>
$ sort reading.txt | uniq
article
book
magazine
paper</pre>

## Übung

Welches Resultat würdest du mit uniq -uc kriegen?

## Quizfrage

Mit welchem Command entfernst du Duplikate in einer Datei?

## Quizantwort

uniq

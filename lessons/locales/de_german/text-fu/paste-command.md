# paste

## Inhalt der Lektion

Der paste Befehlt ist ähnlich zum cat Befehl, er verbindet (merges) Linien zusammen in einer Datei. Erstelle eine neue Datei mit folgendem Inhalt:

<pre>
sample2.txt
The
quick
brown
fox
</pre>

Kombiniere nun alle diese Linien in eine: 

<pre>$ paste -s sample2.txt</pre>

Auch hier ist der standardmässige delimiter TAB. Das Resultat ist also eine Linie mit durch TABs separierten Wörtern.

Ändere nun den delimiter (-d) zu etwas besser lesbarem:

<pre>$ paste -d ' ' -s sample2.txt</pre>

Jetzt sollte alles auf einer Linie, separiert mit einem Leerzeichen, stehen.

## Übung

Versuche mehrere Dateien zusammenzufügen, was passiert?

## Quizfrage

Welches flag benutzt du, damit alle Inhalte auf einer Linie landen?

## Quizantwort

-s

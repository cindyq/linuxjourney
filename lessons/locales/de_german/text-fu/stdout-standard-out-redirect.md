# stdout (Standard Ausgabe)

## Lesson Content

Jetzt kennen wir viele Befehle und kommen somit weiter zu dem Thema I/O (input/output) Ströme. Probiere einfach mal folgenden Befehl aus.

<pre>$ echo Hello World > peanuts.txt</pre>

Was ist passiert? Schaue in dem Ordner nach, wo Du diesen Befehl ausgeführt hast und Du solltest eine Datei mit dem Namen peanuts.txt finden. Wenn Du in die Datei hineinschaust, enthält diese den Text Hello World. Durch diesen Befehl sind viele Dinge passiert.

Schauen wir uns zuerst den ersten Teil an:

<pre>$ echo Hello World</pre>

Wir wissen, dass das Hello World ausgibt. Aber wie funktioniert das? Prozesse verwenden I/O Ströme um Eingaben zu machen und Ausgaben zu erhalten. Normalerweise nimmt der Befehl die Eingabe (Standard Eingabe stdin) und gibt den Ausgabe (Standard Ausgabe oder stdout) zurück. Wenn Du also echo Hello World eingibst, bekommst Du Hello World zurück. Also geben uns I/O Ströme die Möglichkeit das Verhalten von Eingaben und Ausgaben zu kontrollieren.

Kommen wir zum nächsten Teil des Befehls:

<pre> > </pre>

Das Zeichen > gibt uns die Möglichkeit zu verändern, wo die Ausgabe hingeht. Damit können wir die Ausgabe in eine Datei schreiben, anstelle sie auf dem Bildschirm auszugeben. Wenn die Datei noch nicht existiert, wird sie für uns erstellt. Sollte sie aber schon existieren, wird sie überschrieben (dies kannst Du mit einem Attribut verhindern).

gehen wir davon aus, dass ich die Datei peanuts.txt nicht überschreiben möchte. Zum Glück gibt es eine Möglichkeit dies zu verhindern, >>:

<pre>$ echo Hello World >> peanuts.txt</pre>

Dieser Befehl wird Hello World an das Ende der Datei peanuts.txt anhängen. Wenn die Datei noch nicht existiert, wird sie erstellt und der Befehl handelt ganz normal wie >.


## Übung

Probiere ein paar Befehle aus:

<pre>
$ ls -l /var/log > myoutput.txt
$ echo Hello World > rm
$ > somefile.txt
</pre>

## Quizfrage

Welches Zeichen verwendest Du, um die Ausgabe an eine Datei anzuhängen?

## Quiz Antwort

>>
